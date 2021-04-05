---
title: Verwenden von Bits aus .NET mithilfe von Verweis-DLLs
description: In den folgenden Beispielen wird gezeigt, wie die Bits-com-Schnittstelle aus einem .NET-Programm aufgerufen wird.
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c359bafe4f1937d49a6ec21896af32606a2ae894
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "103719583"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a><span data-ttu-id="f1209-103">Aufrufen von Bits aus .net und c# mithilfe von Verweis-DLLs</span><span class="sxs-lookup"><span data-stu-id="f1209-103">Calling into BITS from .NET and C# using Reference DLLs</span></span>

<span data-ttu-id="f1209-104">Eine Möglichkeit, die Bits-com-Klassen aus einem .NET-Programm aufzurufen, besteht darin, eine Verweis-dll-Datei zu erstellen, die mit den Bits [IDL](/windows/desktop/Midl/midl-start-page) (Interface Definition Language)-Dateien im Windows SDK beginnt, mithilfe der Tools " [Mittel l](/windows/desktop/Midl/using-the-midl-compiler-2) " und " [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) "</span><span class="sxs-lookup"><span data-stu-id="f1209-104">One way to call into the BITS COM classes from a .NET program is to create a reference DLL file starting with the BITS [IDL](/windows/desktop/Midl/midl-start-page) (Interface Definition Language) files in the Windows SDK, using the [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) and [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) tools.</span></span> <span data-ttu-id="f1209-105">Die Verweis-dll ist ein Satz von Klassen-Wrappern für die Bits-com-Klassen. Anschließend können Sie die Wrapper Klassen direkt aus .NET verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1209-105">The reference DLL is a set of class wrappers for the BITS COM classes; you can then use the wrapper classes directly from .NET.</span></span>

<span data-ttu-id="f1209-106">Eine Alternative zur Verwendung automatisch erstellter Verweis-DLLs ist die Verwendung eines .net-Bits-Wrappers von Drittanbietern von [GitHub](https://github.com/) und [nuget](https://www.nuget.org/).</span><span class="sxs-lookup"><span data-stu-id="f1209-106">An alternative to using automatically-created reference DLLs is to use a 3rd party .NET BITS wrapper from [GitHub](https://github.com/) and [NuGet](https://www.nuget.org/).</span></span> <span data-ttu-id="f1209-107">Diese Wrapper verfügen häufig über einen natürlicheren .net-Programmierstil, Sie können jedoch hinter den Änderungen und Aktualisierungen in den Bits-Schnittstellen liegen.</span><span class="sxs-lookup"><span data-stu-id="f1209-107">These wrappers often have a more natural .NET programming style but they might lag behind the changes and updates in the BITS interfaces.</span></span>

## <a name="creating-the-reference-dlls"></a><span data-ttu-id="f1209-108">Erstellen der Verweis-DLLs</span><span class="sxs-lookup"><span data-stu-id="f1209-108">Creating the reference DLLs</span></span>
### <a name="bits-idl-files"></a><span data-ttu-id="f1209-109">Bits-IDL-Dateien</span><span class="sxs-lookup"><span data-stu-id="f1209-109">BITS IDL files</span></span>

<span data-ttu-id="f1209-110">Sie beginnen mit dem Satz von Bits-IDL-Dateien.</span><span class="sxs-lookup"><span data-stu-id="f1209-110">You will start with the set of BITS IDL files.</span></span> <span data-ttu-id="f1209-111">Dies sind Dateien, die die Bits-com-Schnittstelle vollständig definieren.</span><span class="sxs-lookup"><span data-stu-id="f1209-111">These are files that fully define the BITS COM interface.</span></span> <span data-ttu-id="f1209-112">Die Dateien befinden sich im Verzeichnis " **Windows Kits** " und heißen Bits-*Version*. idl (z. b. bits10_2. idl), mit Ausnahme der Datei der Version 1,0, die nur Bits. idl ist.</span><span class="sxs-lookup"><span data-stu-id="f1209-112">The files are located in the **Windows Kits** directory and are named bits *version*.idl (for example, bits10_2.idl) except for the version 1.0 file which is just Bits.idl.</span></span> <span data-ttu-id="f1209-113">Wenn neue Versionen von Bits erstellt werden, werden auch neue Bits-IDL-Dateien erstellt.</span><span class="sxs-lookup"><span data-stu-id="f1209-113">As new versions of BITS are created, new BITS IDL files are also created.</span></span>

<span data-ttu-id="f1209-114">Möglicherweise möchten Sie auch eine Kopie der SDK Bits-IDL-Dateien ändern, um Bits-Funktionen zu verwenden, die nicht automatisch in .NET-Entsprechungen konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1209-114">You may also want to modify a copy of the SDK BITS IDL files to use BITS features that aren't automatically converted into .NET equivalents.</span></span> <span data-ttu-id="f1209-115">Mögliche Änderungen an der IDL-Datei werden später erläutert.</span><span class="sxs-lookup"><span data-stu-id="f1209-115">Possible IDL file changes are discussed later on.</span></span>

<span data-ttu-id="f1209-116">Die Bits-IDL-Dateien enthalten mehrere andere IDL-Dateien als Verweis.</span><span class="sxs-lookup"><span data-stu-id="f1209-116">The BITS IDL files include several other IDL files by reference.</span></span> <span data-ttu-id="f1209-117">Sie schachteln auch, sodass Sie bei Verwendung einer Version alle niedrigeren Versionen enthält.</span><span class="sxs-lookup"><span data-stu-id="f1209-117">They also nest, so that if you use one version, it includes all the lower versions.</span></span>

<span data-ttu-id="f1209-118">Für jede Version von Bits, die in Ihrem Programm als Ziel verwendet werden soll, benötigen Sie eine Verweis-dll für diese Version.</span><span class="sxs-lookup"><span data-stu-id="f1209-118">For each version of BITS that you want to target in your program you will need one reference DLL for that version.</span></span> <span data-ttu-id="f1209-119">Wenn Sie z. b. ein Programm schreiben möchten, das mit Bits 1,5 und up funktioniert, aber zusätzliche Funktionen aufweist, wenn Bits 10,2 vorhanden ist, müssen Sie sowohl die bits1_5. idl-als auch die bits10_2. IDL-Dateien konvertieren.</span><span class="sxs-lookup"><span data-stu-id="f1209-119">For example, if you want to write a program that works on BITS 1.5 and up but has additional features when BITS 10.2 is present, you need to convert both the bits1_5.idl and bits10_2.idl files.</span></span>


### <a name="midl-and-tlbimp-utilities"></a><span data-ttu-id="f1209-120">Mittel l-und Tlbimp-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="f1209-120">MIDL and TLBIMP utilities</span></span>

<span data-ttu-id="f1209-121">Das Hilfsprogramm " [Mittel l](/windows/desktop/Midl/using-the-midl-compiler-2) " (Microsoft Interface Definition Language) konvertiert die IDL-Dateien, die die Bits-com-Schnittstelle beschreiben, in eine TLB-Datei (Typbibliothek).</span><span class="sxs-lookup"><span data-stu-id="f1209-121">The [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) utility converts the IDL files that describe the BITS COM interface into a TLB (Type Library) file.</span></span> <span data-ttu-id="f1209-122">Das Tool "Mittel l" hängt vom CL-Hilfsprogramm (C-Präprozessor) ab, um die IDL-Sprachdatei ordnungsgemäß zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f1209-122">The MIDL tool depends on the CL utility (C preprocessor) to correctly read the IDL language file.</span></span> <span data-ttu-id="f1209-123">Das CL-Hilfsprogramm ist Teil von Visual Studio und wird installiert, wenn Sie C/C++-Funktionen in die Visual Studio-Installation einbinden.</span><span class="sxs-lookup"><span data-stu-id="f1209-123">The CL utility is part of Visual Studio and is installed when you include C/C++ features in the Visual Studio installation.</span></span>

<span data-ttu-id="f1209-124">Das Hilfsprogramm "Mittelwert" erstellt normalerweise einen Satz von c-und H-Dateien (c-Sprachcode und c-sprach Header).</span><span class="sxs-lookup"><span data-stu-id="f1209-124">The MIDL utility will normally create a set of C and H (C language code and C language header) files.</span></span> <span data-ttu-id="f1209-125">Sie können diese zusätzlichen Dateien unterdrücken, indem Sie die Ausgabe an das NUL:-Gerät senden.</span><span class="sxs-lookup"><span data-stu-id="f1209-125">You can suppress these extra files by sending the output to the NUL: device.</span></span> <span data-ttu-id="f1209-126">Wenn Sie z. b. den/dlldata NUL: Switch festlegen, wird das Erstellen einer dlldata. c-Datei unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="f1209-126">For example, setting the /dlldata NUL: switch will suppress creating a dlldata.c file.</span></span> <span data-ttu-id="f1209-127">Die folgenden Beispiel Befehle zeigen, welche Switches auf NUL festgelegt werden sollten:.</span><span class="sxs-lookup"><span data-stu-id="f1209-127">The sample commands below shows which switches should be set to NUL:.</span></span>

<span data-ttu-id="f1209-128">Das Hilfsprogramm [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (Typbibliotheks Import) liest in eine TLB-Datei und erstellt die entsprechende Verweis-dll-Datei.</span><span class="sxs-lookup"><span data-stu-id="f1209-128">The [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (Type Library Importer) utility reads in a TLB file and creates the corresponding reference DLL file.</span></span> 


### <a name="example-commands-for-midl-and-tlbimp"></a><span data-ttu-id="f1209-129">Beispiel Befehle für "Mittel l" und "Tlbimp"</span><span class="sxs-lookup"><span data-stu-id="f1209-129">Example commands for MIDL and TLBIMP</span></span>

<span data-ttu-id="f1209-130">Dies ist ein Beispiel für den kompletten Satz von Befehlen, um einen Satz von Verweis Dateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="f1209-130">This is an example of the complete set of commands to generate a set of reference files.</span></span> <span data-ttu-id="f1209-131">Möglicherweise müssen Sie die Befehle auf der Grundlage Ihrer Visual Studio-und Windows SDK Installation ändern und auf der Grundlage der Bits-Features und Betriebssystemversionen, auf die Sie abzielen.</span><span class="sxs-lookup"><span data-stu-id="f1209-131">You may need to modify the commands based on your Visual Studio and Windows SDK installation and based on the BITS features and OS versions you are targeting.</span></span> 

<span data-ttu-id="f1209-132">Im Beispiel wird ein Verzeichnis erstellt, in dem die dll-Referenzdateien abgelegt werden, und es wird eine Umgebungsvariable bitwort p erstellt, um auf dieses Verzeichnis zu verweisen</span><span class="sxs-lookup"><span data-stu-id="f1209-132">The example creates a directory to place the reference DLL files and creates an environment variable BITSTEMP to point to that directory.</span></span> 

<span data-ttu-id="f1209-133">Mit den Beispiel Befehlen führen Sie dann die vsdevcmd.bat Datei aus, die vom Visual Studio-Installer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f1209-133">The example commands then run the vsdevcmd.bat file that's created by the Visual Studio installer.</span></span> <span data-ttu-id="f1209-134">Mit dieser bat-Datei werden Ihre Pfade und einige Umgebungsvariablen so eingerichtet, dass die Befehle "Mittel l" und "Tlbimp" ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f1209-134">This BAT file will set up your paths and some environment variables so that the MIDL and TLBIMP commands will run.</span></span> <span data-ttu-id="f1209-135">Außerdem werden die Variablen WindowsSdkDir und windowssdklibversion so eingerichtet, dass Sie auf die neuesten Windows SDK Verzeichnisse zeigen.</span><span class="sxs-lookup"><span data-stu-id="f1209-135">It also sets up the WindowsSdkDir and WindowsSDKLibVersion variables to point to the most recent Windows SDK directories.</span></span>

```console
REM Create a working directory
REM You can select a different directory based on your needs.
SET BITSTEMP=C:\BITSTEMPDIR
MKDIR "%BITSTEMP%"

REM Run the VsDevCmd.bat file to locate the Windows
REM SDK directory and the tools directories
REM This will be different for different versions of
REM Visual Studio

CALL "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\vsdevcmd.bat"

REM Run the MIDL command on the desired BITS IDL file
REM This will generate a TLB file for the TLBIMP command
REM The IDL file will be different depending on which
REM set of BITS interfaces you need to use.
REM Run the MIDL command once per reference file
REM that you will need to explicitly use.
PUSHD .
CD /D "%WindowsSdkDir%Include\%WindowsSDKLibVersion%um"

MIDL  /I ..\shared /out "%BITSTEMP%" bits1_5.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits4_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits5_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_1.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_2.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:

REM Run the TLBIMP command on the resulting TLB file(s)
REM Try to keep a parallel set of names.
TLBIMP "%BITSTEMP%"\bits1_5.tlb /out: "%BITSTEMP%"\BITSReference1_5.dll
TLBIMP "%BITSTEMP%"\bits4_0.tlb /out: "%BITSTEMP%"\BITSReference4_0.dll
TLBIMP "%BITSTEMP%"\bits5_0.tlb /out: "%BITSTEMP%"\BITSReference5_0.dll
TLBIMP "%BITSTEMP%"\bits10_1.tlb /out: "%BITSTEMP%"\BITSReference10_1.dll
TLBIMP "%BITSTEMP%"\bits10_2.tlb /out: "%BITSTEMP%"\BITSReference10_2.dll
DEL "%BITSTEMP%"\bits*.tlb
POPD

```
<span data-ttu-id="f1209-136">Nachdem diese Befehle ausgeführt wurden, verfügen Sie über eine Reihe von Verweis-DLLs im Verzeichnis "bitstemp".</span><span class="sxs-lookup"><span data-stu-id="f1209-136">Once these commands are run you will have a set of reference DLLs in the BITSTEMP directory.</span></span>

### <a name="adding-the-reference-dlls-to-your-project"></a><span data-ttu-id="f1209-137">Hinzufügen der Verweis-DLLs zu Ihrem Projekt</span><span class="sxs-lookup"><span data-stu-id="f1209-137">Adding the reference DLLs to your project</span></span>

<span data-ttu-id="f1209-138">Öffnen Sie das c#-Projekt in Visual Studio, um eine Verweis-dll in einem c#-Projekt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1209-138">To use a reference DLL in a C# project, open your C# project in Visual Studio.</span></span> <span data-ttu-id="f1209-139">Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf Verweise, und klicken Sie dann auf Verweis hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f1209-139">In the Solution Explorer, right-click the References and click Add Reference.</span></span> <span data-ttu-id="f1209-140">Klicken Sie dann auf die Schaltfläche zum Durchsuchen und dann auf die Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="f1209-140">Then click the Browse button and then the Add button.</span></span> <span data-ttu-id="f1209-141">Navigieren Sie zu dem Verzeichnis mit den Verweis-DLLs, wählen Sie Sie aus, und klicken Sie auf hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f1209-141">Navigate to the directory with the reference DLLs, select them, and click Add.</span></span> <span data-ttu-id="f1209-142">Im Fenster "Verweis-Manager" werden die Verweis-DLLs geprüft.</span><span class="sxs-lookup"><span data-stu-id="f1209-142">In the Reference Manager window the reference DLLs will be checked.</span></span> <span data-ttu-id="f1209-143">Klicken Sie dann auf „OK“.</span><span class="sxs-lookup"><span data-stu-id="f1209-143">Then click OK.</span></span>

<span data-ttu-id="f1209-144">Die Bits-Verweis-DLLs werden nun dem Projekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f1209-144">The BITS reference DLLs are now added to your project.</span></span>

<span data-ttu-id="f1209-145">Die Informationen in den Verweis-dll-Dateien werden in das endgültige Programm eingebettet.</span><span class="sxs-lookup"><span data-stu-id="f1209-145">The information in the reference DLL files will be embedded into your final program.</span></span> <span data-ttu-id="f1209-146">Sie müssen die dll-Referenzdateien nicht an Ihr Programm senden. Sie müssen lediglich das versenden. Speichert.</span><span class="sxs-lookup"><span data-stu-id="f1209-146">You do not have to ship the reference DLL files with your program; you just need to ship the .EXE.</span></span> 

<span data-ttu-id="f1209-147">Sie können ändern, ob die Verweis-DLLs in die endgültige exe-Datei eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="f1209-147">You can change whether the reference DLLs are embedded into the final EXE.</span></span> <span data-ttu-id="f1209-148">Verwenden Sie die Eigenschaft [Interop-Typen einbetten](/dotnet/framework/interop/how-to-add-references-to-type-libraries) , um festzulegen, ob die Verweis-DLLs eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="f1209-148">Use the [Embed Interop Types](/dotnet/framework/interop/how-to-add-references-to-type-libraries) property to set whether or not the reference DLLs will be embedded.</span></span> <span data-ttu-id="f1209-149">Dies kann auf Verweis Basis erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f1209-149">This can be done on a per-reference basis.</span></span> <span data-ttu-id="f1209-150">Der Standardwert ist "true", um die DLLs einzubetten.</span><span class="sxs-lookup"><span data-stu-id="f1209-150">The default is True to embed the DLLs.</span></span>

## <a name="modifying-idl-files-for-more-complete-net-code"></a><span data-ttu-id="f1209-151">Ändern von IDL-Dateien für einen ausführlicheren .NET-Code</span><span class="sxs-lookup"><span data-stu-id="f1209-151">Modifying IDL files for more complete .NET code</span></span>

<span data-ttu-id="f1209-152">Die Bits-IDL-Dateien (Microsoft Interface Definition Language) können unverändert verwendet werden, um die backgroundcopymanager-dll-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f1209-152">The BITS IDL (Microsoft Interface Definition Language) files can be used unchanged to make the BackgroundCopyManager DLL file.</span></span> <span data-ttu-id="f1209-153">Allerdings fehlen in der resultierenden .net-Verweis-dll einige nicht übersetzbare Unions und verfügt über schwer zu verwendende Namen für einige Strukturen und enums.</span><span class="sxs-lookup"><span data-stu-id="f1209-153">However, the resulting .NET reference DLL will be missing some untranslatable unions and has hard-to-use names for some structures and enums.</span></span> <span data-ttu-id="f1209-154">In diesem Abschnitt werden einige der Änderungen beschrieben, die Sie vornehmen können, um die .net-dll zu vervollständigen und leichter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1209-154">This section will describe some of the changes that you can make to make the .NET DLL more complete and easier to use.</span></span>

### <a name="simpler-enum-names"></a><span data-ttu-id="f1209-155">Einfachere Enum-Namen</span><span class="sxs-lookup"><span data-stu-id="f1209-155">Simpler ENUM names</span></span>

<span data-ttu-id="f1209-156">Die Bits-IDL-Dateien definieren in der Regel Enumerationswerte wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f1209-156">The BITS IDL files typically define enum values like this:</span></span>
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
<span data-ttu-id="f1209-157">Der BG_AUTH_TARGET ist der Name der typedef. die tatsächliche Aufzählung wird nicht benannt.</span><span class="sxs-lookup"><span data-stu-id="f1209-157">The BG_AUTH_TARGET is the name of the typedef; the actual enum is not named.</span></span> <span data-ttu-id="f1209-158">Dies verursacht in der Regel keine Probleme mit C-Code, lässt sich jedoch nicht gut für die Verwendung mit einem .NET-Programm umsetzen.</span><span class="sxs-lookup"><span data-stu-id="f1209-158">This doesn’t typically cause problems with C code but doesn’t translate well for use with a .NET program.</span></span> <span data-ttu-id="f1209-159">Ein neuer Name wird automatisch erstellt, kann aber in etwa wie _MIDL___MIDL_itf_bits4_0_0005_0001_0001 aussehen, anstelle eines lesbaren Werts.</span><span class="sxs-lookup"><span data-stu-id="f1209-159">A new name will be automatically created, but it might look something like _MIDL___MIDL_itf_bits4_0_0005_0001_0001 instead of a human-readable value.</span></span> <span data-ttu-id="f1209-160">Sie können dieses Problem beheben, indem Sie die mittleren Dateien so aktualisieren, dass Sie einen Enumeration-Namen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f1209-160">You can fix this problem by updating the MIDL files to include an enum name.</span></span>

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

<span data-ttu-id="f1209-161">Der Enumeration-Name darf nicht mit dem Typedef-Namen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="f1209-161">The enum name is allowed to be the same as the typedef name.</span></span> <span data-ttu-id="f1209-162">Einige Programmierer verfügen über eine Benennungs Konvention, bei der Sie anders gehalten werden (z. b. durch Einfügen eines Unterstrichs vor dem Enumeration-Namen), aber dies verwechselt nur die .net-Übersetzungen.</span><span class="sxs-lookup"><span data-stu-id="f1209-162">Some programmers have a naming convention where they are kept different (for example, by putting an underscore before the enum name), but this will only confuse the .NET translations.</span></span> 

### <a name="string-types-in-unions"></a><span data-ttu-id="f1209-163">Zeichen folgen Typen in Unions</span><span class="sxs-lookup"><span data-stu-id="f1209-163">String types in unions</span></span>

<span data-ttu-id="f1209-164">Die Bits-IDL-Dateien übergeben Zeichen folgen mithilfe der LPWSTR-Konvention (Long-Zeiger auf breit Zeichen Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="f1209-164">The BITS IDL files pass strings using the LPWSTR (long pointer to wide-character string) convention.</span></span> <span data-ttu-id="f1209-165">Dies funktioniert zwar beim Übergeben von Funktionsparametern (wie z. b. die Job. getDisplayName ([out] LPWSTR \* PVal)-Methode), aber es funktioniert nicht, wenn die Zeichen folgen zu Unions gehören.</span><span class="sxs-lookup"><span data-stu-id="f1209-165">Although this works when passing function parameters (like the Job.GetDisplayName([out] LPWSTR \*pVal) method), it doesn’t work when the strings are part of unions.</span></span> <span data-ttu-id="f1209-166">Die bits5_0. IDL-Datei enthält z. b. die BITS_FILE_PROPERTY_VALUE Union:</span><span class="sxs-lookup"><span data-stu-id="f1209-166">For example, the bits5_0.idl file includes the BITS_FILE_PROPERTY_VALUE union:</span></span>

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

<span data-ttu-id="f1209-167">Das Feld "LPWSTR" ist nicht in der .NET-Version der Union enthalten.</span><span class="sxs-lookup"><span data-stu-id="f1209-167">The LPWSTR field won’t be included in the .NET version of the union.</span></span> <span data-ttu-id="f1209-168">Um dieses Problem zu beheben, ändern Sie "LPWSTR" in "WCHAR \*".</span><span class="sxs-lookup"><span data-stu-id="f1209-168">To fix this, change the LPWSTR to a WCHAR\*.</span></span> <span data-ttu-id="f1209-169">Das resultierende Feld (so genannte Zeichenfolge) wird als IntPtr übergeben.</span><span class="sxs-lookup"><span data-stu-id="f1209-169">The resulting field (called String) will be passed as a IntPtr.</span></span> <span data-ttu-id="f1209-170">Konvertieren Sie diese in eine Zeichenfolge mithilfe von System. Runtime. InteropServices. Marshal. ptrumstringauto (Value). Zeichenfolge); anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="f1209-170">Convert this into a string using the  System.Runtime.InteropServices.Marshal.PtrToStringAuto(value.String); method.</span></span>

### <a name="unions-in-structures"></a><span data-ttu-id="f1209-171">Unions in Strukturen</span><span class="sxs-lookup"><span data-stu-id="f1209-171">Unions in structures</span></span>

<span data-ttu-id="f1209-172">Manchmal sind Unions, die in Strukturen eingebettet sind, nicht in der Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="f1209-172">Sometimes unions that are embedded in structures won't be included in the structure at all.</span></span> <span data-ttu-id="f1209-173">Beispielsweise wird in der Bits1_5. idl die BG_AUTH_CREDENTIALS wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="f1209-173">For example, in the Bits1_5.idl the BG_AUTH_CREDENTIALS is defined as follows:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

<span data-ttu-id="f1209-174">Der BG_AUTH_CREDENTIALS_UNION wird wie folgt als Union definiert:</span><span class="sxs-lookup"><span data-stu-id="f1209-174">The BG_AUTH_CREDENTIALS_UNION is defined to be a union as follows:</span></span>
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
<span data-ttu-id="f1209-175">Das Feld Anmelde Informationen im BG_AUTH_CREDENTIALS wird nicht in die .net-Klassendefinition eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f1209-175">The Credentials field in the BG_AUTH_CREDENTIALS will not be included in the .NET class definition.</span></span>

<span data-ttu-id="f1209-176">Beachten Sie, dass die Union so definiert ist, dass Sie unabhängig von der BG_AUTH_SCHEME immer ein BG_BASIC_CREDENTIALS ist.</span><span class="sxs-lookup"><span data-stu-id="f1209-176">Note that the union is defined to always be a BG_BASIC_CREDENTIALS regardless of the BG_AUTH_SCHEME.</span></span> <span data-ttu-id="f1209-177">Da die Union nicht als Union verwendet wird, können wir einfach eine BG_BASIC_CREDENTIALS wie die folgende übergeben:</span><span class="sxs-lookup"><span data-stu-id="f1209-177">Because the union isn’t used as a union, we can just pass a BG_BASIC_CREDENTIALS like this:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a><span data-ttu-id="f1209-178">Verwenden von Bits aus C #</span><span class="sxs-lookup"><span data-stu-id="f1209-178">Using BITS from C#</span></span>

### <a name="recommended-using-statement"></a><span data-ttu-id="f1209-179">Empfohlene using-Anweisung</span><span class="sxs-lookup"><span data-stu-id="f1209-179">Recommended using statement</span></span>

<span data-ttu-id="f1209-180">Wenn Sie einige using-Anweisungen in c# einrichten, verringern Sie die Anzahl der Zeichen, die Sie eingeben müssen, um die verschiedenen Bits-Versionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1209-180">Setting up some using statements in C# will reduce the number of characters you need to type to use the different BITS versions.</span></span> <span data-ttu-id="f1209-181">Der Name "bizreference" stammt aus dem Namen der Verweis-dll.</span><span class="sxs-lookup"><span data-stu-id="f1209-181">The name "BITSReference" comes from the name of the reference DLL.</span></span>

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a><span data-ttu-id="f1209-182">Kurzes Beispiel: Herunterladen einer Datei</span><span class="sxs-lookup"><span data-stu-id="f1209-182">Quick Sample: download a file</span></span>

<span data-ttu-id="f1209-183">Im folgenden finden Sie einen kurzen, aber kompletten Ausschnitt von c#-Code zum Herunterladen einer Datei aus einer URL.</span><span class="sxs-lookup"><span data-stu-id="f1209-183">A short but complete snippet of C# code to download a file from a URL is given below.</span></span> 

```csharp
    var mgr = new BITS.BackgroundCopyManager1_5();
    BITS.GUID jobGuid;
    BITS.IBackgroundCopyJob job;
    mgr.CreateJob("Quick download", BITS.BG_JOB_TYPE.BG_JOB_TYPE_DOWNLOAD, out jobGuid, out job);
    job.AddFile("https://aka.ms/WinServ16/StndPDF", @"C:\Server2016.pdf");
    job.Resume();
    bool jobIsFinal = false;
    while (!jobIsFinal)
    {
        BITS.BG_JOB_STATE state;
        job.GetState(out state);
        switch (state)
        {
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ERROR:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_TRANSFERRED:
                job.Complete();
                break;

            case BITS.BG_JOB_STATE.BG_JOB_STATE_CANCELLED:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ACKNOWLEDGED:
                jobIsFinal = true;
                break;
            default:
                Task.Delay(500); // delay a little bit
                break;
        }
    }
    // Job is complete
```

<span data-ttu-id="f1209-184">In diesem Beispielcode wird ein Bits-Manager mit dem Namen "Mgr" erstellt.</span><span class="sxs-lookup"><span data-stu-id="f1209-184">In this sample code, a BITS manager named mgr is created.</span></span> <span data-ttu-id="f1209-185">Sie entspricht direkt der [ibackgroundcopymanager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f1209-185">It directly corresponds to the [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) interface.</span></span> 

<span data-ttu-id="f1209-186">Aus dem Manager wird ein neuer Auftrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="f1209-186">From the manager a new job is created.</span></span> <span data-ttu-id="f1209-187">Der Auftrag ist ein out-Parameter in der Methode "kreatejob".</span><span class="sxs-lookup"><span data-stu-id="f1209-187">The job is an out parameter on the CreateJob method.</span></span> <span data-ttu-id="f1209-188">Außerdem wird der Name des Auftrags (der nicht eindeutig sein muss) und der Downloadtyp, bei dem es sich um einen Download Auftrag handelt, übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f1209-188">Also passed in is the job name (which doesn't have to be unique) and the download type, which is a download job.</span></span> <span data-ttu-id="f1209-189">Außerdem wird eine Bits-GUID für den Auftrags Bezeichner ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f1209-189">A BITS GUID for the job identifier is also filled in.</span></span>

<span data-ttu-id="f1209-190">Nachdem der Auftrag erstellt wurde, fügen Sie dem Auftrag mit der AddFile-Methode eine neue Downloaddatei hinzu.</span><span class="sxs-lookup"><span data-stu-id="f1209-190">Once the job is created you add a new download file to the job with the AddFile method.</span></span> <span data-ttu-id="f1209-191">Sie müssen zwei Zeichen folgen übergeben, eine für die Remote Datei (URL oder Dateifreigabe) und eine für die lokale Datei.</span><span class="sxs-lookup"><span data-stu-id="f1209-191">You need to pass in two strings, one for the remote file (the URL or file share) and one for the local file.</span></span> 

<span data-ttu-id="f1209-192">Nachdem Sie die Datei hinzugefügt haben, können Sie den Auftrag fortsetzen, um ihn zu starten.</span><span class="sxs-lookup"><span data-stu-id="f1209-192">After adding the file, call Resume on the job to start it.</span></span> <span data-ttu-id="f1209-193">Dann wartet der Code, bis sich der Auftrag in einem abschließenden Zustand befindet (Fehler oder übertragen) und dann abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="f1209-193">Then the code waits until the job is in a final state (ERROR or TRANSFERRED) and is then completed.</span></span>

### <a name="bits-versions-casting-and-queryinterface"></a><span data-ttu-id="f1209-194">Bits-Versionen, Umwandlung und QueryInterface</span><span class="sxs-lookup"><span data-stu-id="f1209-194">BITS Versions, Casting and QueryInterface</span></span>

<span data-ttu-id="f1209-195">Sie werden feststellen, dass Sie häufig sowohl eine frühe Version eines Bits-Objekts als auch eine neuere Version in Ihrem Programm verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="f1209-195">You'll find that you often have to use both an early version of a BITS object and a more recent version in your program.</span></span>  

<span data-ttu-id="f1209-196">Wenn Sie z. b. ein Auftrags Objekt erstellen, erhalten Sie einen ibackgroundcopyjob (Teil der Bits-Version 1,0), auch wenn Sie ihn mit einem neueren Manager-Objekt erstellen und ein aktuelleres ibackgroundcopyjob-Objekt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f1209-196">For example, when you make a job object, you will get an IBackgroundCopyJob (part of BITS version 1.0) even when you're making it using a more recent manager object and a more recent IBackgroundCopyJob object is available.</span></span> <span data-ttu-id="f1209-197">Da die Methode "kreatejob" eine Schnittstelle für die aktuellste Version nicht akzeptiert, können Sie die aktuellste Version nicht direkt erstellen.</span><span class="sxs-lookup"><span data-stu-id="f1209-197">Because the CreateJob method doesn't accept an interface for the more recent version, you can't directly make the more recent version.</span></span>

<span data-ttu-id="f1209-198">Verwenden Sie eine .net-Umwandlung, um von einem älteren Typobjekt in ein neueres Typobjekt zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="f1209-198">Use a .NET cast to convert from an older type object to a newer type object.</span></span> <span data-ttu-id="f1209-199">Die Umwandlung ruft automatisch eine COM-QueryInterface-Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="f1209-199">The cast will automatically call a COM QueryInterface as appropriate.</span></span> 

<span data-ttu-id="f1209-200">In diesem Beispiel gibt es ein ibackgroundcopyjob-Objekt mit dem Namen "Job", und wir möchten es in ein IBackgroundCopyJob5-Objekt mit dem Namen "job5" konvertieren, damit wir die Methode "Bits 5,0 GetProperty" aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="f1209-200">In this example, there's a BITS IBackgroundCopyJob object named "job", and we want to convert it to an IBackgroundCopyJob5 object named "job5" so that we can call the BITS 5.0 GetProperty method.</span></span> <span data-ttu-id="f1209-201">Wir haben einfach wie folgt eine Umwandlung in den IBackgroundCopyJob5-Typ durch:</span><span class="sxs-lookup"><span data-stu-id="f1209-201">We just cast to the IBackgroundCopyJob5 type like this:</span></span>

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

<span data-ttu-id="f1209-202">Die job5-Variable wird von .NET mithilfe der korrekten QueryInterface initialisiert.</span><span class="sxs-lookup"><span data-stu-id="f1209-202">The job5 variable will be initialized by .NET by using the correct QueryInterface.</span></span> 

<span data-ttu-id="f1209-203">Wenn Ihr Code möglicherweise auf einem System ausgeführt wird, das eine bestimmte Version von Bits nicht unterstützt, können Sie die Umwandlung ausprobieren und die System. InvalidCastException-Ausnahme abfangen.</span><span class="sxs-lookup"><span data-stu-id="f1209-203">If your code might run on a system that doesn't support a particular version of BITS, you can try the cast and catch the System.InvalidCastException.</span></span> 

```csharp
BITS5.IBackgroundCopyJob5 job5 = null;
try
{
    job5 = (BITS5.IBackgroundCopyJob5)Job;
}
catch (System.InvalidCastException)
{
    ; // Must be running an earlier version of BITS
}
```

<span data-ttu-id="f1209-204">Ein häufiges Problem ist, wenn Sie versuchen, eine Umwandlung in die falsche Art von Objekt durchführen.</span><span class="sxs-lookup"><span data-stu-id="f1209-204">A common problem is when you try to cast into the wrong kind of object.</span></span> <span data-ttu-id="f1209-205">Das .NET-System kennt die wirkliche Beziehung zwischen den Bits-Schnittstellen nicht.</span><span class="sxs-lookup"><span data-stu-id="f1209-205">The .NET system doesn't know about the real relationship between the BITS interfaces.</span></span> <span data-ttu-id="f1209-206">Wenn Sie nach der falschen Art der Schnittstelle gefragt werden, versucht .net, Sie für Sie zu verwenden, und es tritt ein Fehler mit InvalidCastException und HRESULT 0x80004002 (E_NOINTERFACE) auf.</span><span class="sxs-lookup"><span data-stu-id="f1209-206">If you ask for the wrong kind of interface, .NET will try to make it for you and will fail with an InvalidCastException and HResult 0x80004002 (E_NOINTERFACE).</span></span>

### <a name="working-with-bits-versions-10_1-and-10_2"></a><span data-ttu-id="f1209-207">Arbeiten mit Bits-Versionen 10_1 und 10_2</span><span class="sxs-lookup"><span data-stu-id="f1209-207">Working with BITS Versions 10_1 and 10_2</span></span>

<span data-ttu-id="f1209-208">In einigen Versionen von Windows 10 können Sie kein Bits-ibackgroundcopymanager-Objekt direkt mithilfe der 10,1-oder 10,2-Schnittstellen erstellen.</span><span class="sxs-lookup"><span data-stu-id="f1209-208">On some versions of Windows 10 you can't directly create a BITS IBackgroundCopyManager object using the 10.1 or 10.2 interfaces.</span></span> <span data-ttu-id="f1209-209">Stattdessen müssen Sie mehrere Versionen der Referenzdateien der backgroundcopymanager-dll verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1209-209">Instead, you'll have to use multiple versions of the BackgroundCopyManager DLL reference files.</span></span> <span data-ttu-id="f1209-210">Beispielsweise können Sie die Version 1,5 verwenden, um ein ibackgroundcopymanager-Objekt zu erstellen, und dann die resultierenden Aufträge oder Datei Objekte mithilfe der Versionen 10,1 oder 10,2 umwandeln.</span><span class="sxs-lookup"><span data-stu-id="f1209-210">For example, you can use the 1.5 version to make an IBackgroundCopyManager object, and then cast the resulting job or file objects using the 10.1 or 10.2 versions.</span></span>

