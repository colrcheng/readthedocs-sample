Incremental Build Process
===========================

Incremental Build process deals with assembly informational version of Dynamic link library.This process came into picture to make user understand the difference between latest dll deployed with same version number

AssemblyInfo.cs provides two attributes to set two different types of versions -  Assembly Version and Assembly File Version. Lets a have look how to set these two versions and its use


**How to use Assembly Version and Assembly File Version**

.NET framework provides opportunity to set two different types of version numbers to each assembly.
 
1.	Assembly Version 
 
This is the version number used by framework during build and at runtime to locate, link and load the assemblies. When you add reference to any assembly in your project, it is this version number which gets embedded. At runtime, CLR looks for assembly with this version number to load. But remember this version is used along with name, public key token and culture information only if the assemblies are strong-named signed. If assemblies are not strong-named signed, only file names are used for loading.
 
2. Assembly File Version

This is the version number given to file as in file system. It is displayed by Windows Explorer. Its never used by .NET framework or runtime for referencing.
 
Attributes in AssemblyInfo.cs
// Version information for an assembly consists of the following four values:
//
//      Major Version
//      Minor Version 
//      Build Number
//      Revision
//
[assembly: AssemblyVersion("1.0.0.0")]
[assembly: AssemblyFileVersion("1.0.0.0")] 
 
Providing a (*) in place of absolute number makes compiler increase the number by one every time you build.
 
Suppose you are building a framework assembly for your project which is used by lot of developers while building the application assemblies. If you release new version of assembly very frequently, say once every day, and if assemblies are strong named, Developers will have to change the reference every time you release new assembly. This can be quite cumbersome and may lead to wrong references also. A better option in such closed group and volatile scenarios would be to fix he 'Assembly Version' and change only the 'Assembly File Version'. Use the assembly file version number to communicate the latest release of assembly. In this case, developers will not have to change the references and they can simply overwrite the assembly in reference path. In central/final release builds it makes more sense to change the 'Assembly Version' and most keep the 'Assembly File Version' same as assembly version.
Properties

3. Incremental Build Template

Build Template: NugetterMultipkgBuildVersionedTemplate20
	
	.. image:: _static/build-template.png


Below field items contribute to incremental build process

- Basic	:	Build number format
- NuGetter(B) -Package	 :	Build Number prefix 
- Force  create version
- Perform checkin of the Assemblyinfo Files
- Use version seed file
- Version seed file path
- NuGetter(B) -Package -> Version or Version Seed file path

4.	Files to modified for Incremental build process


- BuildMultiplePackage.xml : 	 Update version as 6.0.1.B where B depicts incremental Assembly Informational version

- Packages.config :		Changes Dll version with Assembly Informational version

- Nuspec :		Change dependencies version number with Assembly informational version

- .csProj :	Changes Dll version in hintpath with respect to packages path

5.	Output

Check the respective DLL in Proget 

	.. image:: _static/build-output.png


Where 1007 depicts Assembly informartion version

