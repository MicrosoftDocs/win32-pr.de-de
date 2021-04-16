---
title: Nachrichten Compiler (MC.exe)
description: Wird verwendet, um Instrumentierungs Manifeste und Nachrichtentext Dateien zu kompilieren.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- Message Compiler-Ereignisprotokoll (MC.exe)
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 5eb852dcbb13800705db0a0f19d912de899f9b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524240"
---
# <a name="message-compiler-mcexe"></a><span data-ttu-id="eb97a-104">Nachrichten Compiler (MC.exe)</span><span class="sxs-lookup"><span data-stu-id="eb97a-104">Message Compiler (MC.exe)</span></span>

<span data-ttu-id="eb97a-105">Wird verwendet, um Instrumentierungs Manifeste und Nachrichtentext Dateien zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="eb97a-105">Used to compile instrumentation manifests and message text files.</span></span> <span data-ttu-id="eb97a-106">Der Compiler generiert die Nachrichten Ressourcen Dateien, mit denen Ihre Anwendung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="eb97a-106">The compiler generates the message resource files to which your application links.</span></span>

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [<span data-ttu-id="eb97a-107">Argumente, die sowohl für Meldungs Textdateien als auch für Manifest-Dateien</span><span class="sxs-lookup"><span data-stu-id="eb97a-107">Arguments common to both message text files and manifest files</span></span>](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [<span data-ttu-id="eb97a-108">Spezifische Argumente für Manifest-Dateien</span><span class="sxs-lookup"><span data-stu-id="eb97a-108">Arguments specific to manifest files</span></span>](#arguments-specific-to-manifest-files)
-   [<span data-ttu-id="eb97a-109">Argumente, die zum Erstellen von Code verwendet werden, den Ihr Anbieter zum Protokollieren von Ereignissen verwendet</span><span class="sxs-lookup"><span data-stu-id="eb97a-109">Arguments specific to generating code that your provider would use to log events</span></span>](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [<span data-ttu-id="eb97a-110">Spezifische Argumente für Meldungs Textdateien</span><span class="sxs-lookup"><span data-stu-id="eb97a-110">Arguments specific to message text files</span></span>](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a><span data-ttu-id="eb97a-111">Argumente, die sowohl für Meldungs Textdateien als auch für Manifest-Dateien</span><span class="sxs-lookup"><span data-stu-id="eb97a-111">Arguments common to both message text files and manifest files</span></span>

<dl> <dt>

<span data-ttu-id="eb97a-112"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="eb97a-112"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-113">Zeigt die Verwendungs Informationen für den Nachrichten Compiler an.</span><span class="sxs-lookup"><span data-stu-id="eb97a-113">Displays the usage information for the Message Compiler.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-114"><span id="-c"></span><span id="-C"></span>**-c**</span><span class="sxs-lookup"><span data-stu-id="eb97a-114"><span id="-c"></span><span id="-C"></span>**-c**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-115">Verwenden Sie dieses Argument, damit der Compiler das Customer-Bit (Bit 28) in allen Nachrichten-IDs festlegen muss.</span><span class="sxs-lookup"><span data-stu-id="eb97a-115">Use this argument to have the compiler set the customer bit (bit 28) in all message IDs.</span></span> <span data-ttu-id="eb97a-116">Weitere Informationen zum Kunden Bit finden Sie unter Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="eb97a-116">For information on the customer bit, see winerror.h.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-117"><span id="-cp"></span><span id="-CP"></span>**-CP-** *Codierung*</span><span class="sxs-lookup"><span data-stu-id="eb97a-117"><span id="-cp"></span><span id="-CP"></span>**-cp** *encoding*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-118">Verwenden Sie dieses Argument, um die Zeichencodierung anzugeben, die für alle generierten Textdateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eb97a-118">Use this argument to specify the character encoding used for all generated text files.</span></span> <span data-ttu-id="eb97a-119">Gültige Namen sind "ANSI" (Standard), "UTF-8" und "UTF-16".</span><span class="sxs-lookup"><span data-stu-id="eb97a-119">Valid names include "ansi" (default), "utf-8", and "utf-16".</span></span> <span data-ttu-id="eb97a-120">Die Unicode-Codierungen fügen eine Byte Reihenfolge-Markierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="eb97a-120">The Unicode encodings will add a byte order mark.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e-** *Erweiterung*</span><span class="sxs-lookup"><span data-stu-id="eb97a-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e** *extension*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-122">Verwenden Sie dieses Argument, um die Erweiterung anzugeben, die für die Header Datei verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb97a-122">Use this argument to specify the extension to use for the header file.</span></span> <span data-ttu-id="eb97a-123">Sie können bis zu drei Zeichen ohne den Zeitraum angeben.</span><span class="sxs-lookup"><span data-stu-id="eb97a-123">You can specify up to a three characters extension, not including the period.</span></span> <span data-ttu-id="eb97a-124">Der Standardwert ist. h.</span><span class="sxs-lookup"><span data-stu-id="eb97a-124">The default is .h.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *Pfad*</span><span class="sxs-lookup"><span data-stu-id="eb97a-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *path*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-126">Verwenden Sie dieses Argument, um den Ordner anzugeben, in dem der Compiler die generierte Header Datei platzieren soll.</span><span class="sxs-lookup"><span data-stu-id="eb97a-126">Use this argument to specify the folder into which you want the compiler to place the generated header file.</span></span> <span data-ttu-id="eb97a-127">Der Standardwert ist das aktuelle Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="eb97a-127">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *Länge*</span><span class="sxs-lookup"><span data-stu-id="eb97a-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *length*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-129">Verwenden Sie dieses Argument, damit der Compiler eine Warnung generiert, wenn eine beliebige Nachricht die *Länge* von Zeichen überschreitet.</span><span class="sxs-lookup"><span data-stu-id="eb97a-129">Use this argument to have the compiler generate a warning if the any message exceeds *length* characters.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r-** *Pfad*</span><span class="sxs-lookup"><span data-stu-id="eb97a-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r** *path*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-131">Verwenden Sie dieses Argument, um den Ordner anzugeben, in dem der Compiler das generierte ressourcencompilerskript (RC-Datei) und die generierten. bin-Dateien (binäre Ressourcen) platzieren soll, die das ressourcencompilerskript enthält.</span><span class="sxs-lookup"><span data-stu-id="eb97a-131">Use this argument to specify the folder into which you want the compiler to place the generated resource compiler script (.rc file) and the generated .bin files (binary resources) that the resource compiler script includes.</span></span> <span data-ttu-id="eb97a-132">Der Standardwert ist das aktuelle Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="eb97a-132">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z-** *Name*</span><span class="sxs-lookup"><span data-stu-id="eb97a-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *name*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-134">Verwenden Sie dieses Argument, um den Standardbasis Namen zu überschreiben, den der Compiler für die generierten Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb97a-134">Use this argument to override the default base name that the compiler uses for the files that it generates.</span></span> <span data-ttu-id="eb97a-135">Standardmäßig wird der Basisname der Datei *Namen* -Eingabedatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb97a-135">The default is to use the base name of the *filename* input file.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-136"><span id="filename"></span><span id="FILENAME"></span>*Einfügen*</span><span class="sxs-lookup"><span data-stu-id="eb97a-136"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-137">Die Datei oder Meldungs Textdatei des Instrumentierungs Manifests.</span><span class="sxs-lookup"><span data-stu-id="eb97a-137">The instrumentation manifest file or message text file.</span></span> <span data-ttu-id="eb97a-138">Die Datei muss im aktuellen Verzeichnis vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="eb97a-138">The file must exist in the current directory.</span></span> <span data-ttu-id="eb97a-139">Sie können eine Manifest-Datei, eine Meldungs Textdatei oder beides angeben.</span><span class="sxs-lookup"><span data-stu-id="eb97a-139">You can specify a manifest file, message text file, or both.</span></span> <span data-ttu-id="eb97a-140">Der Dateiname muss die Erweiterung enthalten.</span><span class="sxs-lookup"><span data-stu-id="eb97a-140">The file name must include the extension.</span></span> <span data-ttu-id="eb97a-141">Die Konvention besteht in der Verwendung einer. man-Erweiterung für Manifest-Dateien und der Erweiterung ". MC" für Meldungs Textdateien.</span><span class="sxs-lookup"><span data-stu-id="eb97a-141">The convention is to use a .man extension for manifest files and a .mc extension for message text files.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a><span data-ttu-id="eb97a-142">Spezifische Argumente für Manifest-Dateien</span><span class="sxs-lookup"><span data-stu-id="eb97a-142">Arguments specific to manifest files</span></span>

<dl> <dt>

<span data-ttu-id="eb97a-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s-** *Pfad*</span><span class="sxs-lookup"><span data-stu-id="eb97a-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s** *path*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-144">Verwenden Sie dieses Argument, um eine Baseline Ihrer Instrumentierung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="eb97a-144">Use this argument to create a baseline of your instrumentation.</span></span> <span data-ttu-id="eb97a-145">Geben Sie den Pfad zum Ordner an, in dem sich die grundlegenden Manifest-Dateien befinden.</span><span class="sxs-lookup"><span data-stu-id="eb97a-145">Specify the path to the folder that contains your baseline manifest files.</span></span> <span data-ttu-id="eb97a-146">Bei nachfolgenden Releases verwenden Sie das Argument **-t** , um das neue Manifest anhand der Baseline auf Kompatibilitätsprobleme zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="eb97a-146">For subsequent releases, you would then use the **-t** argument to check the new manifest against the baseline for compatibility issues.</span></span>

<span data-ttu-id="eb97a-147">**Vor MC-Version 1.12.7051:** Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="eb97a-147">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *Pfad*</span><span class="sxs-lookup"><span data-stu-id="eb97a-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *path*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-149">Verwenden Sie dieses Argument, wenn Sie eine neue Version des Manifests erstellen und es auf die Anwendungs Kompatibilität mit der Baseline überprüfen möchten, die Sie mit dem **-s-** Argument erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="eb97a-149">Use this argument when you create a new version of your manifest and want to check it for application compatibility against the baseline that you created using the **-s** argument.</span></span> <span data-ttu-id="eb97a-150">Der Pfad muss auf den Ordner verweisen, der enthält. BIN-Dateien, die der baselinevorgang erstellt hat (siehe Schalter **-s** ).</span><span class="sxs-lookup"><span data-stu-id="eb97a-150">The path must point to the folder that contains the .BIN files that the baseline operation created (see the **-s** switch).</span></span>

<span data-ttu-id="eb97a-151">**Vor MC-Version 1.12.7051:** Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="eb97a-151">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *Pfad*</span><span class="sxs-lookup"><span data-stu-id="eb97a-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *path*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-153">Der Compiler ignoriert dieses Argument und überprüft das Manifest automatisch.</span><span class="sxs-lookup"><span data-stu-id="eb97a-153">The compiler ignores this argument and automatically validates the manifest.</span></span>

<span data-ttu-id="eb97a-154">**Vor MC-Version 1.12.7051:** Verwenden Sie dieses Argument, um den Ordner anzugeben, der die Schema Datei "eventman. xsd" enthält, die der Compiler verwendet, um das Manifest zu validieren.</span><span class="sxs-lookup"><span data-stu-id="eb97a-154">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Eventman.xsd schema file, which the compiler uses to validate your manifest.</span></span> <span data-ttu-id="eb97a-155">Der Windows SDK schließt die Schema Datei "eventman. xsd" in den \\ includeordner ein.</span><span class="sxs-lookup"><span data-stu-id="eb97a-155">The Windows SDK includes the Eventman.xsd schema file in the \\Include folder.</span></span> <span data-ttu-id="eb97a-156">Wenn Sie dieses Argument nicht angeben, überprüft der Compiler das Manifest nicht.</span><span class="sxs-lookup"><span data-stu-id="eb97a-156">If you do not specify this argument, the compiler does not validate your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *Pfad*</span><span class="sxs-lookup"><span data-stu-id="eb97a-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *path*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-158">Der Compiler ignoriert dieses Argument.</span><span class="sxs-lookup"><span data-stu-id="eb97a-158">The compiler ignores this argument.</span></span>

<span data-ttu-id="eb97a-159">**Vor MC-Version 1.12.7051:** Verwenden Sie dieses Argument, um den Ordner anzugeben, der die Winmeta.xml Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="eb97a-159">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Winmeta.xml file.</span></span> <span data-ttu-id="eb97a-160">Die Winmeta.xml-Datei enthält die erkannten Eingabe-und Ausgabetypen sowie die vordefinierten Kanäle, Ebenen und OpCodes.</span><span class="sxs-lookup"><span data-stu-id="eb97a-160">The Winmeta.xml file contains the recognized input and output types as well as the predefined channels, levels, and opcodes.</span></span> <span data-ttu-id="eb97a-161">Die Windows SDK enthält die Winmeta.xml Datei im \\ Ordner include.</span><span class="sxs-lookup"><span data-stu-id="eb97a-161">The Windows SDK includes the Winmeta.xml file in the \\Include folder.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a><span data-ttu-id="eb97a-162">Argumente, die zum Erstellen von Code verwendet werden, den Ihr Anbieter zum Protokollieren von Ereignissen verwendet</span><span class="sxs-lookup"><span data-stu-id="eb97a-162">Arguments specific to generating code that your provider would use to log events</span></span>

<span data-ttu-id="eb97a-163">Sie können die folgenden compilerargumente verwenden, um Kernel Modus-oder Benutzermoduscode zu generieren, den Sie zum Protokollieren von Ereignissen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="eb97a-163">You can use the following compiler arguments to generate kernel-mode or user-mode code that you can use to log events.</span></span> <span data-ttu-id="eb97a-164">Sie können auch anfordern, dass der Compiler Code generiert, um das Schreiben von Ereignissen auf Computern vor Windows Vista zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="eb97a-164">You can also request that the compiler generate code to support writing events on computers prior to Windows Vista.</span></span> <span data-ttu-id="eb97a-165">Wenn die Anwendung in c# geschrieben ist, kann der Compiler eine c#-Klasse generieren, die Sie zum Protokollieren von Ereignissen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="eb97a-165">If your application is written C#, the compiler can generate a C# class that you can use to log events.</span></span> <span data-ttu-id="eb97a-166">Diese Argumente sind ab der MC-Version 1.12.7051 verfügbar, die mit der Windows 7-Version des Windows SDK ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="eb97a-166">These arguments are available beginning with MC version 1.12.7051 that ships with the Windows 7 version of the Window SDK.</span></span>

<dl> <dt>

<span data-ttu-id="eb97a-167"><span id="-co"></span><span id="-CO"></span>**-Co**</span><span class="sxs-lookup"><span data-stu-id="eb97a-167"><span id="-co"></span><span id="-CO"></span>**-co**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-168">Verwenden Sie dieses Argument, damit der Protokollierungs Dienst die benutzerdefinierte Funktion für jedes Ereignis aufruft, das Sie protokollieren (die Funktion wird aufgerufen, nachdem das Ereignis protokolliert wurde).</span><span class="sxs-lookup"><span data-stu-id="eb97a-168">Use this argument to have the logging service call your user-defined function for each event that you log (the function is called after the event has been logged).</span></span> <span data-ttu-id="eb97a-169">Die benutzerdefinierte Funktion muss über die folgende Signatur verfügen.</span><span class="sxs-lookup"><span data-stu-id="eb97a-169">Your user-defined function must have the following signature.</span></span>


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



<span data-ttu-id="eb97a-170">Sie müssen auch die folgende-Direktive in Ihren Code einschließen.</span><span class="sxs-lookup"><span data-stu-id="eb97a-170">You must also include the following directive in your code.</span></span>

`#define MCGEN_CALLOUT pFnUserFunction`

<span data-ttu-id="eb97a-171">Sie sollten Ihre Implementierung so kurz wie möglich halten, um Protokollierungs Probleme zu vermeiden. der Dienst protokolliert Ihre Ereignisse nicht mehr, bis die Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eb97a-171">You should keep your implementation as short as possible to prevent logging issues; the service will not log anymore of your events until the function returns.</span></span>

<span data-ttu-id="eb97a-172">Sie können dieses Argument mit dem **-km-** oder **-um-** Argument verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb97a-172">You can use this argument with the **-km** or **-um** argument.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-CS-** *Namespace*</span><span class="sxs-lookup"><span data-stu-id="eb97a-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-174">Verwenden Sie dieses Argument, damit der Compiler eine c#-Klasse generiert, die auf der .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) -Klasse basiert.</span><span class="sxs-lookup"><span data-stu-id="eb97a-174">Use this argument to have the compiler generate a C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-CSS-** *Namespace*</span><span class="sxs-lookup"><span data-stu-id="eb97a-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-css** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-176">Verwenden Sie dieses Argument, damit der Compiler eine statische c#-Klasse generiert, die auf der .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) -Klasse basiert.</span><span class="sxs-lookup"><span data-stu-id="eb97a-176">Use this argument to have the compiler generate a static C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-177"><span id="-km"></span><span id="-KM"></span>**-km**</span><span class="sxs-lookup"><span data-stu-id="eb97a-177"><span id="-km"></span><span id="-KM"></span>**-km**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-178">Verwenden Sie dieses Argument, damit der Compiler den Kernelmoduscode generiert, mit dem die im Manifest definierten Ereignisse protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="eb97a-178">Use this argument to have the compiler generate the kernel-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-179"><span id="-mof"></span><span id="-MOF"></span>**-MOF**</span><span class="sxs-lookup"><span data-stu-id="eb97a-179"><span id="-mof"></span><span id="-MOF"></span>**-mof**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-180">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="eb97a-180">DEPRECATED.</span></span> <span data-ttu-id="eb97a-181">Verwenden Sie dieses Argument, damit der Compiler Code generiert, den Sie zum Protokollieren von Ereignissen auf Computern vor Windows Vista verwenden können.</span><span class="sxs-lookup"><span data-stu-id="eb97a-181">Use this argument to have the compiler generate code that you can use to log events on computers prior to Windows Vista.</span></span> <span data-ttu-id="eb97a-182">Mit dieser Option wird auch eine MOF-Datei erstellt, die die MOF-Klassen für jedes im Manifest definierte Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="eb97a-182">This option also creates a MOF file that contains the MOF classes for each event defined in the manifest.</span></span> <span data-ttu-id="eb97a-183">Um die Klassen in der MOF-Datei zu registrieren, damit Consumer die Ereignisse decodieren können, verwenden Sie den MOF-Compiler (Mofcomp.exe).</span><span class="sxs-lookup"><span data-stu-id="eb97a-183">To register the classes in the MOF file so that consumers can decode the events, use the MOF compiler (Mofcomp.exe).</span></span> <span data-ttu-id="eb97a-184">Ausführliche Informationen zur Verwendung des MOF-Compilers finden Sie unter [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="eb97a-184">For details on using the MOF compiler, see [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

<span data-ttu-id="eb97a-185">Wenn Sie diesen Switch verwenden möchten, müssen Sie die folgenden Einschränkungen einhalten:</span><span class="sxs-lookup"><span data-stu-id="eb97a-185">To use this switch, you must adhere to the following restrictions:</span></span>

-   <span data-ttu-id="eb97a-186">Jede Ereignis Definition muss die Attribute "Task" und "Opcode" enthalten.</span><span class="sxs-lookup"><span data-stu-id="eb97a-186">Every event definition must include the task and opcode attributes</span></span>
-   <span data-ttu-id="eb97a-187">Jeder Task muss das eventguid-Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="eb97a-187">Every task must include the eventGuid attribute</span></span>
-   <span data-ttu-id="eb97a-188">Die Vorlagen Daten, auf die das Ereignis verweist, dürfen Folgendes nicht enthalten:</span><span class="sxs-lookup"><span data-stu-id="eb97a-188">The template data that the event references cannot contain:</span></span>
    -   <span data-ttu-id="eb97a-189">Datenelemente, die die Eingabetypen Win: binary oder Win: SYSTEMTIME angeben</span><span class="sxs-lookup"><span data-stu-id="eb97a-189">Data items that specify the win:Binary or win:SYSTEMTIME input types</span></span>
    -   <span data-ttu-id="eb97a-190">Strukturen</span><span class="sxs-lookup"><span data-stu-id="eb97a-190">Structures</span></span>
    -   <span data-ttu-id="eb97a-191">Arrays mit variabler Größenanpassung; Sie können jedoch Arrays mit fester Länge angeben.</span><span class="sxs-lookup"><span data-stu-id="eb97a-191">Variable sized arrays; however, you can specify fixed length arrays</span></span>
    -   <span data-ttu-id="eb97a-192">Zeichen folgen-Datentypen können das length-Attribut nicht angeben</span><span class="sxs-lookup"><span data-stu-id="eb97a-192">String data types cannot specify the length attribute</span></span>

<span data-ttu-id="eb97a-193">Sie müssen dieses Argument mit dem **-um-**, **-CS**-, **-CSS**-oder **-km** -Argument verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb97a-193">You must use this argument with the **-um**, **-cs**, **-css**, or **-km** argument</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p-** *Präfix*</span><span class="sxs-lookup"><span data-stu-id="eb97a-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-195">Verwenden Sie dieses Argument, um das Standard Präfix zu überschreiben, das der Compiler für die Protokollierungs Makronamen und Methodennamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb97a-195">Use this argument to override the default prefix that the compiler uses for the logging macro names and method names.</span></span> <span data-ttu-id="eb97a-196">Das Standard Präfix ist "EventWrite".</span><span class="sxs-lookup"><span data-stu-id="eb97a-196">The default prefix is "EventWrite".</span></span> <span data-ttu-id="eb97a-197">Die Zeichenfolge beachtet die Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="eb97a-197">The string is case-sensitive.</span></span>

<span data-ttu-id="eb97a-198">Sie können dieses Argument mit dem **-um-**, **-CS**-, **-CSS**-oder **-km** -Argument verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb97a-198">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P-** *Präfix*</span><span class="sxs-lookup"><span data-stu-id="eb97a-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-200">Verwenden Sie dieses Argument, um Zeichen vom Anfang des symbolischen Namens zu entfernen, den Sie für das Ereignis angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="eb97a-200">Use this argument to remove characters from the beginning of the symbolic name that you specified for the event.</span></span> <span data-ttu-id="eb97a-201">Bei dem Vergleich wird Groß- und Kleinschreibung nicht unterschieden.</span><span class="sxs-lookup"><span data-stu-id="eb97a-201">The comparison is case-insensitive.</span></span> <span data-ttu-id="eb97a-202">Der Compiler verwendet den symbolischen Namen, um die Namen der Protokollierungs Makros und Methodennamen zu bilden.</span><span class="sxs-lookup"><span data-stu-id="eb97a-202">The compiler uses the symbolic name to form the logging macro names and method names.</span></span>

<span data-ttu-id="eb97a-203">Der Standardname für ein Protokollierungs Makro ist EventWrite *Symbolname*, wobei *Symbolname* der symbolische Name ist, den Sie für das Ereignis angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="eb97a-203">The default name for a logging macro is EventWrite *SymbolName*, where *SymbolName* is the symbolic name that you specified for the event.</span></span> <span data-ttu-id="eb97a-204">Wenn Sie z. b. das Symbol Attribut des Ereignisses auf printerconnection festlegen, wäre der Makro Name EventWrite teprinterconnection.</span><span class="sxs-lookup"><span data-stu-id="eb97a-204">For example, if you set the symbol attribute of the event to PrinterConnection, the macro name would be EventWritePrinterConnection.</span></span> <span data-ttu-id="eb97a-205">Wenn Sie den Drucker aus dem Namen entfernen möchten, verwenden Sie den **-P-** **Drucker**, der "EventWrite Connection" ergibt.</span><span class="sxs-lookup"><span data-stu-id="eb97a-205">To remove Printer from the name, use **-P** **Printer**, which results in EventWriteConnection.</span></span>

<span data-ttu-id="eb97a-206">Sie können dieses Argument mit dem **-um-**, **-CS**-, **-CSS**-oder **-km** -Argument verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb97a-206">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-207"><span id="-um"></span><span id="-UM"></span>**-um**</span><span class="sxs-lookup"><span data-stu-id="eb97a-207"><span id="-um"></span><span id="-UM"></span>**-um**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-208">Verwenden Sie dieses Argument, damit der Compiler den Benutzermoduscode generiert, mit dem die im Manifest definierten Ereignisse protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="eb97a-208">Use this argument to have the compiler generate the user-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> </dl>

<span data-ttu-id="eb97a-209">Damit der Compiler Protokollierungs Code generieren kann, müssen Sie das **-um**-, **-CS**-, **-CSS**-oder **-km** -Argument angeben. Diese Argumente schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="eb97a-209">To have the compiler generate logging code, you must specify the **-um**, **-cs**, **-css**, or **-km** argument; these arguments are mutually exclusive.</span></span>

<span data-ttu-id="eb97a-210">Um anzugeben, wo die vom Compiler generierten h-, CS-und MOF-Dateien abgelegt werden sollen, verwenden Sie das Argument **-h** .</span><span class="sxs-lookup"><span data-stu-id="eb97a-210">To specify where to place the .h, .cs, and .mof files that the compiler generates, use the **-h** argument.</span></span> <span data-ttu-id="eb97a-211">Wenn Sie das **-h-** Argument nicht angeben, werden die Dateien in den aktuellen Ordner eingefügt.</span><span class="sxs-lookup"><span data-stu-id="eb97a-211">If you do not specify the **-h** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="eb97a-212">Verwenden Sie das Argument **-r** , um anzugeben, wo die RC-Datei und Binärdateien (die die Metadatenressourcen enthalten), die der Compiler generiert, platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb97a-212">To specify where to place the .rc file and binary files (that contain the metadata resources) that the compiler generates, use the **-r** argument.</span></span> <span data-ttu-id="eb97a-213">Wenn Sie das Argument **-r** nicht angeben, werden die Dateien in den aktuellen Ordner eingefügt.</span><span class="sxs-lookup"><span data-stu-id="eb97a-213">If you do not specify the **-r** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="eb97a-214">Der Compiler verwendet den Basis Namen der Eingabedatei als Basis Namen für die generierten Dateien.</span><span class="sxs-lookup"><span data-stu-id="eb97a-214">The compiler uses the base name of the input file as the base name of the files that it generates.</span></span> <span data-ttu-id="eb97a-215">Um einen Basisnamen anzugeben, verwenden Sie das **-z-** Argument.</span><span class="sxs-lookup"><span data-stu-id="eb97a-215">To specify a base name, use the **-z** argument.</span></span>

### <a name="arguments-specific-to-message-text-files"></a><span data-ttu-id="eb97a-216">Spezifische Argumente für Meldungs Textdateien</span><span class="sxs-lookup"><span data-stu-id="eb97a-216">Arguments specific to message text files</span></span>

<dl> <dt>

<span data-ttu-id="eb97a-217"><span id="-a"></span><span id="-A"></span>**-a**</span><span class="sxs-lookup"><span data-stu-id="eb97a-217"><span id="-a"></span><span id="-A"></span>**-a**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-218">Verwenden Sie dieses Argument, um anzugeben, dass die Datei *Namen* -Eingabedatei Inhalt in der System Standard-Windows-ANSI-Codepage (CP_ACP) enthält.</span><span class="sxs-lookup"><span data-stu-id="eb97a-218">Use this argument to specify that the *filename* input file contains content in the system-default Windows ANSI code page (CP_ACP).</span></span> <span data-ttu-id="eb97a-219">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="eb97a-219">This is the default.</span></span> <span data-ttu-id="eb97a-220">Verwenden Sie **-u** für Unicode.</span><span class="sxs-lookup"><span data-stu-id="eb97a-220">Use **-u** for Unicode.</span></span> <span data-ttu-id="eb97a-221">Wenn die Eingabedatei eine BOM enthält, wird dieses Argument ignoriert.</span><span class="sxs-lookup"><span data-stu-id="eb97a-221">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-222"><span id="-A"></span><span id="-a"></span>**-A**</span><span class="sxs-lookup"><span data-stu-id="eb97a-222"><span id="-A"></span><span id="-a"></span>**-A**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-223">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="eb97a-223">DEPRECATED.</span></span> <span data-ttu-id="eb97a-224">Verwenden Sie dieses Argument, um anzugeben, dass die Nachrichten in der Datei Output. bin ANSI lauten sollen.</span><span class="sxs-lookup"><span data-stu-id="eb97a-224">Use this argument to specify that the messages in the output .bin file should be ANSI.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-225"><span id="-b"></span><span id="-B"></span>**-b**</span><span class="sxs-lookup"><span data-stu-id="eb97a-225"><span id="-b"></span><span id="-B"></span>**-b**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-226">Verwenden Sie dieses Argument, damit der Compiler den Basis Namen der Datei *Namen-Eingabedatei* für die. bin-Dateinamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb97a-226">Use this argument to have the compiler use the base name of the *filename* input file for the .bin file names.</span></span> <span data-ttu-id="eb97a-227">Der Standardwert ist die Verwendung von "msg".</span><span class="sxs-lookup"><span data-stu-id="eb97a-227">The default is to use "MSG".</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-228"><span id="-d"></span><span id="-D"></span>**-d**</span><span class="sxs-lookup"><span data-stu-id="eb97a-228"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-229">Verwenden Sie dieses Argument, um Dezimalwerte für den Schweregrad und die Anlagen Konstanten in der Header Datei anstelle von hexadezimalen Werten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb97a-229">Use this argument to use decimal values for the Severity and Facility constants in the header file instead of hexadecimal values.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-230"><span id="-n"></span><span id="-N"></span>**-n**</span><span class="sxs-lookup"><span data-stu-id="eb97a-230"><span id="-n"></span><span id="-N"></span>**-n**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-231">Verwenden Sie dieses Argument, um anzugeben, dass Nachrichten unmittelbar nach dem Nachrichtentext beendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb97a-231">Use this argument to specify that messages terminate immediately after the message body.</span></span> <span data-ttu-id="eb97a-232">Der Standardwert ist das Beenden des Nachrichten Texts mit CR/LF.</span><span class="sxs-lookup"><span data-stu-id="eb97a-232">The default is to terminate the message body with a CR/LF.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-233"><span id="-o"></span><span id="-O"></span>**-o**</span><span class="sxs-lookup"><span data-stu-id="eb97a-233"><span id="-o"></span><span id="-O"></span>**-o**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-234">Verwenden Sie dieses Argument, damit der Compiler eine OLE2-Header Datei mithilfe von **HRESULT** -Definitionen anstelle von Statuscodes generiert.</span><span class="sxs-lookup"><span data-stu-id="eb97a-234">Use this argument to have the compiler generate an OLE2 header file using **HRESULT** definitions instead of status codes.</span></span> <span data-ttu-id="eb97a-235">Die Verwendung von Statuscodes ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="eb97a-235">Using status codes is the default.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-236"><span id="-u"></span><span id="-U"></span>**-u**</span><span class="sxs-lookup"><span data-stu-id="eb97a-236"><span id="-u"></span><span id="-U"></span>**-u**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-237">Verwenden Sie dieses Argument, um anzugeben, dass die Eingabedatei des *Datei namens* UTF-16LE-Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="eb97a-237">Use this argument to specify that the *filename* input file contains UTF-16LE content.</span></span> <span data-ttu-id="eb97a-238">Der Standardwert ist ANSI-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="eb97a-238">The default is ANSI content.</span></span> <span data-ttu-id="eb97a-239">Wenn die Eingabedatei eine BOM enthält, wird dieses Argument ignoriert.</span><span class="sxs-lookup"><span data-stu-id="eb97a-239">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-240"><span id="-U"></span><span id="-u"></span>**-U**</span><span class="sxs-lookup"><span data-stu-id="eb97a-240"><span id="-U"></span><span id="-u"></span>**-U**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-241">Verwenden Sie dieses Argument, um anzugeben, dass die Nachrichten in der Datei Output. bin Unicode lauten sollen.</span><span class="sxs-lookup"><span data-stu-id="eb97a-241">Use this argument to specify that the messages in the output .bin file should be Unicode.</span></span> <span data-ttu-id="eb97a-242">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="eb97a-242">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-243"><span id="-v"></span><span id="-V"></span>**-v**</span><span class="sxs-lookup"><span data-stu-id="eb97a-243"><span id="-v"></span><span id="-V"></span>**-v**</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-244">Verwenden Sie dieses Argument, um die ausführliche Ausgabe zu generieren.</span><span class="sxs-lookup"><span data-stu-id="eb97a-244">Use this argument to generate verbose output.</span></span>

</dd> <dt>

<span data-ttu-id="eb97a-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x-** *Pfad*</span><span class="sxs-lookup"><span data-stu-id="eb97a-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *path*</span></span>
</dt> <dd>

<span data-ttu-id="eb97a-246">Verwenden Sie dieses Argument, um den Ordner anzugeben, in dem der Compiler die dbg-C-Includedatei platzieren soll.</span><span class="sxs-lookup"><span data-stu-id="eb97a-246">Use this argument to specify the folder into which you want the compiler to place the .dbg C include file.</span></span> <span data-ttu-id="eb97a-247">Die dbg-Datei ordnet den symbolischen Namen Nachrichten-IDs zu.</span><span class="sxs-lookup"><span data-stu-id="eb97a-247">The .dbg file maps message IDs to their symbolic names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb97a-248">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb97a-248">Remarks</span></span>

<span data-ttu-id="eb97a-249">Die Argumente " **-A** " und " **-MOF** " sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="eb97a-249">The **-A** and **-mof** arguments are deprecated and will be removed in the future.</span></span>

<span data-ttu-id="eb97a-250">Der Compiler akzeptiert als Eingabe eine Manifest-Datei (. man) oder eine Nachrichtentext Datei (. MC) und generiert die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="eb97a-250">The compiler accepts as input a manifest (.man) file or a message text (.mc) file and generates the following files:</span></span>

-   <span data-ttu-id="eb97a-251">*Dateiname*. h</span><span class="sxs-lookup"><span data-stu-id="eb97a-251">*filename*.h</span></span>

    <span data-ttu-id="eb97a-252">Eine C/C++-Header Datei, die die Ereignis Deskriptoren, die Anbieter-GUID und Symbolnamen enthält, auf die in der Anwendung verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="eb97a-252">A C/C++ header file that contains the event descriptors, provider GUID, and symbol names that you reference in your application.</span></span>

-   <span data-ttu-id="eb97a-253">*Dateiname* Temp. bin</span><span class="sxs-lookup"><span data-stu-id="eb97a-253">*filename* TEMP.bin</span></span>

    <span data-ttu-id="eb97a-254">Eine binäre Ressourcen Datei, die den Anbieter und die Ereignis Metadaten enthält.</span><span class="sxs-lookup"><span data-stu-id="eb97a-254">A binary resource file that contains the provider and event metadata.</span></span> <span data-ttu-id="eb97a-255">Dies ist die Vorlagen Ressource, die durch das Temp-Suffix des Basis namens der Datei gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="eb97a-255">This is the template resource, which is signified by the TEMP suffix of the base name of the file.</span></span>

-   <span data-ttu-id="eb97a-256">Msg00001. bin</span><span class="sxs-lookup"><span data-stu-id="eb97a-256">Msg00001.bin</span></span>

    <span data-ttu-id="eb97a-257">Eine binäre Ressourcen Datei für jede Sprache, die Sie angeben (z. b. wenn das Manifest Nachrichten Zeichenfolgen in "en-US" und "fr-FR" enthält), generiert der Compiler "Msg00001. bin" und "Msg00002. bin".</span><span class="sxs-lookup"><span data-stu-id="eb97a-257">A binary resource file for each language that you specify (for example, if your manifest contains message strings in en-US and fr-FR, the compiler would generate Msg00001.bin and Msg00002.bin).</span></span>

-   <span data-ttu-id="eb97a-258">*Dateiname*. RC</span><span class="sxs-lookup"><span data-stu-id="eb97a-258">*filename*.rc</span></span>

    <span data-ttu-id="eb97a-259">Ein ressourcencompilerskript, das die Anweisungen enthält, mit denen die einzelnen bin-Dateien als Ressource eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="eb97a-259">A resource compiler script that contains the statements to include each .bin file as a resource.</span></span>

<span data-ttu-id="eb97a-260">Bei Argumenten, die einen Pfad annehmen, kann der Pfad ein absoluter, relativer oder UNC-Pfad sein, und er kann Umgebungsvariablen enthalten.</span><span class="sxs-lookup"><span data-stu-id="eb97a-260">For arguments that take a path, the path can be an absolute, relative, or UNC path and it can contain environment variables.</span></span>

<span data-ttu-id="eb97a-261">**Vor MC-Version 1.12.7051:** Der Compiler lässt keine relativen Pfade oder Umgebungsvariablen zu.</span><span class="sxs-lookup"><span data-stu-id="eb97a-261">**Prior to MC version 1.12.7051:** The compiler does not allow relative paths or environment variables.</span></span>

<span data-ttu-id="eb97a-262">Der Windows SDK schließt den Compiler (mc.exe) in den \\ bin-Ordner ein.</span><span class="sxs-lookup"><span data-stu-id="eb97a-262">The Windows SDK includes the compiler (mc.exe) in the \\Bin folder.</span></span>

## <a name="examples"></a><span data-ttu-id="eb97a-263">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb97a-263">Examples</span></span>

<span data-ttu-id="eb97a-264">Im folgenden Beispiel wird ein Manifest mithilfe der compilerstandardwerte kompiliert.</span><span class="sxs-lookup"><span data-stu-id="eb97a-264">The following example compiles a manifest using the compiler defaults.</span></span>

``` syntax
mc spooler.man
```

<span data-ttu-id="eb97a-265">Im folgenden Beispiel wird das Manifest kompiliert und die Header-und Ressourcen Dateien in den angegebenen Ordnern platziert.</span><span class="sxs-lookup"><span data-stu-id="eb97a-265">The following example compiles the manifest and places the header and resource files in the specified folders.</span></span>

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a><span data-ttu-id="eb97a-266">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb97a-266">Requirements</span></span>

| <span data-ttu-id="eb97a-267">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb97a-267">Requirement</span></span> | <span data-ttu-id="eb97a-268">Wert</span><span class="sxs-lookup"><span data-stu-id="eb97a-268">Value</span></span> |
|--------------------------|-------------------------------------------------|
| <span data-ttu-id="eb97a-269">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb97a-269">Minimum supported client</span></span> | <span data-ttu-id="eb97a-270">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb97a-270">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="eb97a-271">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb97a-271">Minimum supported server</span></span> | <span data-ttu-id="eb97a-272">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb97a-272">Windows 2000 Server \[desktop apps only\]</span></span>       |
