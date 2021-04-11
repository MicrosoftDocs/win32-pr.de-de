---
description: Zum Erfassen von Ablauf Verfolgungs Informationen für die VSS-Infrastruktur können Sie das vsstrace-Tool, das Logman-Tool oder das tracelog-Tool verwenden.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Verwenden von Ablauf Verfolgungs Tools mit VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214620"
---
# <a name="using-tracing-tools-with-vss"></a><span data-ttu-id="c4f56-103">Verwenden von Ablauf Verfolgungs Tools mit VSS</span><span class="sxs-lookup"><span data-stu-id="c4f56-103">Using Tracing Tools with VSS</span></span>

<span data-ttu-id="c4f56-104">Zum Erfassen von Ablauf Verfolgungs Informationen für die VSS-Infrastruktur können Sie das vsstrace-Tool, das Logman-Tool oder das tracelog-Tool verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-104">To collect tracing information for the VSS infrastructure, you can use the VssTrace tool, the Logman tool, or the Tracelog tool.</span></span> <span data-ttu-id="c4f56-105">Vsstrace ist im Microsoft Windows Software Development Kit (SDK) verfügbar und kann verwendet werden, um VSS-Anwendungen unter Windows 7 und höheren Versionen des Windows-Betriebssystems nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="c4f56-105">VssTrace is available in the Microsoft Windows Software Development Kit (SDK) and can be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="c4f56-106">Logman ist ein Ablauf Verfolgungs Controller für Ablauf Verfolgungs Ereignisse und Leistungsindikatoren. Sie kann auch verwendet werden, um VSS-Anwendungen unter Windows 7 und höheren Versionen des Windows-Betriebssystems nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="c4f56-106">Logman is a trace controller for trace events and performance counters; it can also be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="c4f56-107">TraceLog ist im Windows-Treiberkit (WDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="c4f56-107">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="c4f56-108">Informationen zur Verwendung von Ablauf Verfolgungs Tools mit der [automatisierten System Wiederherstellung (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md)finden Sie unter [Verwenden von Ablauf Verfolgungs Tools mit ASR-Anwendungen](using-tracing-tools-with-vss-asr-applications.md)</span><span class="sxs-lookup"><span data-stu-id="c4f56-108">To use tracing tools with [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), see [Using Tracing Tools with ASR Applications](using-tracing-tools-with-vss-asr-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="c4f56-109">Vsstrace, logman und tracelog erfordern alle Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="c4f56-109">VssTrace, Logman, and Tracelog all require administrator privilege.</span></span>

 

<span data-ttu-id="c4f56-110">Weitere Informationen zu den einzelnen Tools finden Sie in den folgenden Abschnitten:</span><span class="sxs-lookup"><span data-stu-id="c4f56-110">For information about each tool, see the following sections:</span></span>

-   [<span data-ttu-id="c4f56-111">Verwenden von vsstrace</span><span class="sxs-lookup"><span data-stu-id="c4f56-111">Using VssTrace</span></span>](#using-vsstrace)
    -   [<span data-ttu-id="c4f56-112">Optionen für vsstrace Command-Line</span><span class="sxs-lookup"><span data-stu-id="c4f56-112">VssTrace Command-Line Options</span></span>](#vsstrace-command-line-options)
-   [<span data-ttu-id="c4f56-113">Verwenden von logman</span><span class="sxs-lookup"><span data-stu-id="c4f56-113">Using Logman</span></span>](#using-logman)
-   [<span data-ttu-id="c4f56-114">Verwenden von tracelog</span><span class="sxs-lookup"><span data-stu-id="c4f56-114">Using Tracelog</span></span>](#using-tracelog)

## <a name="using-vsstrace"></a><span data-ttu-id="c4f56-115">Verwenden von vsstrace</span><span class="sxs-lookup"><span data-stu-id="c4f56-115">Using VssTrace</span></span>

<span data-ttu-id="c4f56-116">Verwenden Sie die folgende Syntax, um das vsstrace-Tool über die Befehlszeile auszuführen:</span><span class="sxs-lookup"><span data-stu-id="c4f56-116">To run the VssTrace tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="c4f56-117">**vsstrace** *-Befehlszeilenoptionen*</span><span class="sxs-lookup"><span data-stu-id="c4f56-117">**vsstrace** *command-line-options*</span></span>

<span data-ttu-id="c4f56-118">Verwenden Sie die folgende Syntax, um eine präzise Befehlszeilen Hilfe für das vsstrace-Tool anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="c4f56-118">To display concise command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="c4f56-119">**vsstrace-Hilfe**</span><span class="sxs-lookup"><span data-stu-id="c4f56-119">**vsstrace -help**</span></span>

<span data-ttu-id="c4f56-120">Verwenden Sie die folgende Syntax, um eine ausführliche Befehlszeilen Hilfe für das vsstrace-Tool anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="c4f56-120">To display detailed command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="c4f56-121">**vsstrace-Hilfe**</span><span class="sxs-lookup"><span data-stu-id="c4f56-121">**vsstrace -help all**</span></span>

### <a name="vsstrace-command-line-options"></a><span data-ttu-id="c4f56-122">Optionen für vsstrace Command-Line</span><span class="sxs-lookup"><span data-stu-id="c4f56-122">VssTrace Command-Line Options</span></span>

<span data-ttu-id="c4f56-123">Das vsstrace-Tool verwendet die folgenden Befehlszeilenoptionen:</span><span class="sxs-lookup"><span data-stu-id="c4f56-123">The VssTrace tool uses the following command-line options:</span></span>

<dl> <dt>

<span data-ttu-id="c4f56-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f-** *Flags*</span><span class="sxs-lookup"><span data-stu-id="c4f56-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f** *Flags*</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-125">Aktivieren Sie die Module, deren Flags von der *Flags* -Bitmaske angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-125">Enable the modules whose flags are specified by the *Flags* bitmask.</span></span> <span data-ttu-id="c4f56-126">Jedes Flag entspricht einem VSS-Modul.</span><span class="sxs-lookup"><span data-stu-id="c4f56-126">Each flag corresponds to a VSS module.</span></span> <span data-ttu-id="c4f56-127">Wenn *Flags* 0 (null) ist, werden keine Module aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c4f56-127">If *Flags* is zero, no modules are enabled.</span></span> <span data-ttu-id="c4f56-128">Beachten Sie, dass die meisten Module standardmäßig aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="c4f56-128">Note that most modules are enabled by default.</span></span> <span data-ttu-id="c4f56-129">Diese Option kann mit der **+** Option _Module_ kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-129">This option can be combined with the **+**_Module_ option.</span></span> <span data-ttu-id="c4f56-130">Beispielsweise deaktiviert **vsstrace-f 0 + Writer + coord** die Ablauf Verfolgung aller Module, die standardmäßig aktiviert sind, und ermöglicht die Ablauf Verfolgung von VSS-Writern und des VSS-Diensts.</span><span class="sxs-lookup"><span data-stu-id="c4f56-130">For example, **vsstrace -f 0 +WRITER +COORD** disables tracing of all of the modules that are enabled by default and enables tracing of VSS writers and the VSS service.</span></span> <span data-ttu-id="c4f56-131">Alternativ ermöglicht **vsstrace + f 0xFFFF-coord** die Ablauf Verfolgung aller Module mit Ausnahme des VSS-Diensts.</span><span class="sxs-lookup"><span data-stu-id="c4f56-131">Alternatively, **vsstrace +f 0xffff -COORD** enables tracing of all modules except the VSS service.</span></span>

> [!Note]  
> <span data-ttu-id="c4f56-132">Wenn Sie die Option **-f** in Verbindung mit der **+** Option _Module_ verwenden, muss die **-f** vor der **+** _Modul_ Option angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-132">If you use the **-f** option together with the **+**_Module_ option, the **-f** must appear before the **+**_Module_ option.</span></span>

 

<span data-ttu-id="c4f56-133">In der folgenden Tabelle sind der Modulname und das Flag für die einzelnen verfügbaren Module aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c4f56-133">The following table lists the module name and flag for each available module.</span></span>

| <span data-ttu-id="c4f56-134">Modul</span><span class="sxs-lookup"><span data-stu-id="c4f56-134">Module</span></span> | <span data-ttu-id="c4f56-135">Flag</span><span class="sxs-lookup"><span data-stu-id="c4f56-135">Flag</span></span>       | <span data-ttu-id="c4f56-136">Standardmäßig aktiviert</span><span class="sxs-lookup"><span data-stu-id="c4f56-136">Enabled by default</span></span> | <span data-ttu-id="c4f56-137">Verfolgte Elemente</span><span class="sxs-lookup"><span data-stu-id="c4f56-137">Items traced</span></span>                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f56-138">EXCEPT</span><span class="sxs-lookup"><span data-stu-id="c4f56-138">EXCEPT</span></span> | <span data-ttu-id="c4f56-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c4f56-139">0x00000001</span></span> | <span data-ttu-id="c4f56-140">Ja</span><span class="sxs-lookup"><span data-stu-id="c4f56-140">Yes</span></span>                | <span data-ttu-id="c4f56-141">C++-Ausnahmebehandlung.</span><span class="sxs-lookup"><span data-stu-id="c4f56-141">C++ exception handling.</span></span>                                                                                                                       |
| <span data-ttu-id="c4f56-142">Koord</span><span class="sxs-lookup"><span data-stu-id="c4f56-142">COORD</span></span>  | <span data-ttu-id="c4f56-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c4f56-143">0x00000002</span></span> | <span data-ttu-id="c4f56-144">Ja</span><span class="sxs-lookup"><span data-stu-id="c4f56-144">Yes</span></span>                | <span data-ttu-id="c4f56-145">Der VSS-Dienst, der auch als VSS Coordinator bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="c4f56-145">The VSS service, which is also called the VSS coordinator.</span></span>                                                                                    |
| <span data-ttu-id="c4f56-146">Austausch Vorgänge</span><span class="sxs-lookup"><span data-stu-id="c4f56-146">SWPRV</span></span>  | <span data-ttu-id="c4f56-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c4f56-147">0x00000004</span></span> | <span data-ttu-id="c4f56-148">Ja</span><span class="sxs-lookup"><span data-stu-id="c4f56-148">Yes</span></span>                | <span data-ttu-id="c4f56-149">Der VSS-System Schatten Kopie-Anbieter Dienst.</span><span class="sxs-lookup"><span data-stu-id="c4f56-149">The VSS System Shadow Copy Provider service.</span></span>                                                                                                  |
| <span data-ttu-id="c4f56-150">Bucomp</span><span class="sxs-lookup"><span data-stu-id="c4f56-150">BUCOMP</span></span> | <span data-ttu-id="c4f56-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c4f56-151">0x00000008</span></span> | <span data-ttu-id="c4f56-152">Ja</span><span class="sxs-lookup"><span data-stu-id="c4f56-152">Yes</span></span>                | <span data-ttu-id="c4f56-153">Die VSS-Anforderer und die Verarbeitung der Sicherungs Metadaten.</span><span class="sxs-lookup"><span data-stu-id="c4f56-153">The VSS requester and backup metadata processing.</span></span>                                                                                             |
| <span data-ttu-id="c4f56-154">WRITER</span><span class="sxs-lookup"><span data-stu-id="c4f56-154">WRITER</span></span> | <span data-ttu-id="c4f56-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4f56-155">0x00000010</span></span> | <span data-ttu-id="c4f56-156">Ja</span><span class="sxs-lookup"><span data-stu-id="c4f56-156">Yes</span></span>                | <span data-ttu-id="c4f56-157">VSS Writer Vorgänge und VSS-gehosteten Writer-Implementierungen, wie z. b. der Windows-Registrierungs Schreiber.</span><span class="sxs-lookup"><span data-stu-id="c4f56-157">VSS writer operations and VSS hosted writer implementations, such as the Windows Registry writer.</span></span>                                             |
| <span data-ttu-id="c4f56-158">Vssapi</span><span class="sxs-lookup"><span data-stu-id="c4f56-158">VSSAPI</span></span> | <span data-ttu-id="c4f56-159">0x00000020</span><span class="sxs-lookup"><span data-stu-id="c4f56-159">0x00000020</span></span> | <span data-ttu-id="c4f56-160">Ja</span><span class="sxs-lookup"><span data-stu-id="c4f56-160">Yes</span></span>                | <span data-ttu-id="c4f56-161">Verschiedene Funktionen der VSS-API, die von VSSAPI.DLL exportiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-161">Miscellaneous functions of the VSS API exported by VSSAPI.DLL.</span></span>                                                                                |
| <span data-ttu-id="c4f56-162">Hwdiag</span><span class="sxs-lookup"><span data-stu-id="c4f56-162">HWDIAG</span></span> | <span data-ttu-id="c4f56-163">0x00000040</span><span class="sxs-lookup"><span data-stu-id="c4f56-163">0x00000040</span></span> | <span data-ttu-id="c4f56-164">Ja</span><span class="sxs-lookup"><span data-stu-id="c4f56-164">Yes</span></span>                | <span data-ttu-id="c4f56-165">VSS-Hardware Anbieter Infrastruktur und-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="c4f56-165">VSS hardware provider infrastructure and operations.</span></span>                                                                                          |
| <span data-ttu-id="c4f56-166">ADMIN</span><span class="sxs-lookup"><span data-stu-id="c4f56-166">ADMIN</span></span>  | <span data-ttu-id="c4f56-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="c4f56-167">0x00000080</span></span> | <span data-ttu-id="c4f56-168">Ja</span><span class="sxs-lookup"><span data-stu-id="c4f56-168">Yes</span></span>                | <span data-ttu-id="c4f56-169">VSS-Befehlszeilen Dienstprogramme, z. b. VSSADMIN.EXE und DISKSHADOW.EXE.</span><span class="sxs-lookup"><span data-stu-id="c4f56-169">VSS command line utilities such as VSSADMIN.EXE and DISKSHADOW.EXE.</span></span>                                                                           |
| <span data-ttu-id="c4f56-170">Vssui</span><span class="sxs-lookup"><span data-stu-id="c4f56-170">VSSUI</span></span>  | <span data-ttu-id="c4f56-171">0x00000100</span><span class="sxs-lookup"><span data-stu-id="c4f56-171">0x00000100</span></span> | <span data-ttu-id="c4f56-172">Ja</span><span class="sxs-lookup"><span data-stu-id="c4f56-172">Yes</span></span>                | <span data-ttu-id="c4f56-173">Die Schattenkopien für freigegebene Ordner Konfigurations Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="c4f56-173">The Shadow Copies for Shared Folders configuration user interface (UI).</span></span> <span data-ttu-id="c4f56-174">Die Benutzeroberfläche ist nur unter Windows Server-Betriebssystemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c4f56-174">The UI is available only on Windows Server operating systems.</span></span>         |
| <span data-ttu-id="c4f56-175">TEST</span><span class="sxs-lookup"><span data-stu-id="c4f56-175">TEST</span></span>   | <span data-ttu-id="c4f56-176">0x00000200</span><span class="sxs-lookup"><span data-stu-id="c4f56-176">0x00000200</span></span> | <span data-ttu-id="c4f56-177">Ja</span><span class="sxs-lookup"><span data-stu-id="c4f56-177">Yes</span></span>                | <span data-ttu-id="c4f56-178">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="c4f56-178">Not applicable.</span></span> <span data-ttu-id="c4f56-179">(Dieses Ablauf Verfolgungs Modul ist reserviert.)</span><span class="sxs-lookup"><span data-stu-id="c4f56-179">(This tracing module is reserved.)</span></span>                                                                                            |
| <span data-ttu-id="c4f56-180">IOCTL</span><span class="sxs-lookup"><span data-stu-id="c4f56-180">IOCTL</span></span>  | <span data-ttu-id="c4f56-181">0x00000400</span><span class="sxs-lookup"><span data-stu-id="c4f56-181">0x00000400</span></span> | <span data-ttu-id="c4f56-182">Ja</span><span class="sxs-lookup"><span data-stu-id="c4f56-182">Yes</span></span>                | <span data-ttu-id="c4f56-183">Details zu FSCTL-und ioctl-Vorgängen, die der VSS-Dienst durch Aufrufen der [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="c4f56-183">Details of FSCTL and IOCTL operations that the VSS service has initiated by calling the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span> |
| <span data-ttu-id="c4f56-184">Genen</span><span class="sxs-lookup"><span data-stu-id="c4f56-184">GEN</span></span>    | <span data-ttu-id="c4f56-185">0x00000800</span><span class="sxs-lookup"><span data-stu-id="c4f56-185">0x00000800</span></span> | <span data-ttu-id="c4f56-186">Ja</span><span class="sxs-lookup"><span data-stu-id="c4f56-186">Yes</span></span>                | <span data-ttu-id="c4f56-187">Allgemeine VSS-Dienstprogramm Funktionen, z. b. Zuweisungen, Zeichen folgen Klassen sowie Registrierungs-und Volumevorgänge.</span><span class="sxs-lookup"><span data-stu-id="c4f56-187">General VSS utility functions, such as allocators, string classes, and registry and volume operations.</span></span>                                        |
| <span data-ttu-id="c4f56-188">Wrxml</span><span class="sxs-lookup"><span data-stu-id="c4f56-188">WRXML</span></span>  | <span data-ttu-id="c4f56-189">0x00001000</span><span class="sxs-lookup"><span data-stu-id="c4f56-189">0x00001000</span></span> | <span data-ttu-id="c4f56-190">Nein</span><span class="sxs-lookup"><span data-stu-id="c4f56-190">No</span></span>                 | <span data-ttu-id="c4f56-191">XML-Verarbeitung für Writer-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="c4f56-191">XML processing for writer metadata.</span></span> <span data-ttu-id="c4f56-192">Dieses Modul weist ein sehr hohes Maß an Rauschen auf.</span><span class="sxs-lookup"><span data-stu-id="c4f56-192">This module has a very high level of noise.</span></span>                                                               |
| <span data-ttu-id="c4f56-193">Vssxml</span><span class="sxs-lookup"><span data-stu-id="c4f56-193">VSSXML</span></span> | <span data-ttu-id="c4f56-194">0x00002000</span><span class="sxs-lookup"><span data-stu-id="c4f56-194">0x00002000</span></span> | <span data-ttu-id="c4f56-195">Nein</span><span class="sxs-lookup"><span data-stu-id="c4f56-195">No</span></span>                 | <span data-ttu-id="c4f56-196">Basisklassen für die XML-Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="c4f56-196">XML processing base classes.</span></span> <span data-ttu-id="c4f56-197">Dieses Modul weist ein sehr hohes Maß an Rauschen auf.</span><span class="sxs-lookup"><span data-stu-id="c4f56-197">This module has a very high level of noise.</span></span>                                                                      |



 

</dd> <dt>

<span data-ttu-id="c4f56-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Mond_</span><span class="sxs-lookup"><span data-stu-id="c4f56-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-199">Aktivieren Sie das Modul, das durch das *Modul* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4f56-199">Enable the module specified by *Module*.</span></span> <span data-ttu-id="c4f56-200">Mehrere Module können gleichzeitig aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-200">More than one module can be enabled at a time.</span></span> <span data-ttu-id="c4f56-201">Um die verfügbaren Module aufzulisten, geben Sie **vsstrace – Help modules** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="c4f56-201">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="c4f56-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Mond_</span><span class="sxs-lookup"><span data-stu-id="c4f56-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-203">Deaktivieren Sie das Modul, das durch das *Modul* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4f56-203">Disable the module specified by *Module*.</span></span> <span data-ttu-id="c4f56-204">Um die verfügbaren Module aufzulisten, geben Sie **vsstrace – Help modules** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="c4f56-204">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="c4f56-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+ PID** *-ProcessID*</span><span class="sxs-lookup"><span data-stu-id="c4f56-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-206">Aktivieren Sie den durch *ProcessID* angegebenen Prozess.</span><span class="sxs-lookup"><span data-stu-id="c4f56-206">Enable the process specified by *ProcessId*.</span></span> <span data-ttu-id="c4f56-207">Um alle Prozesse zu aktivieren, verwenden Sie " \* " für den Wert von *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="c4f56-207">To enable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="c4f56-208">Es kann jeweils mehr als eine **PID** -Option angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-208">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="c4f56-209">Die Reihenfolge der Optionen bestimmt, welche Prozesse aktiviert oder deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-209">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="c4f56-210">Um z. b. nur den Prozess zu aktivieren, dessen Prozess-ID 0xe8c ist, verwenden Sie **vsstrace-PID \* + PID 0xe8c**.</span><span class="sxs-lookup"><span data-stu-id="c4f56-210">For example, to enable only the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="c4f56-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-PID** *ProcessID*</span><span class="sxs-lookup"><span data-stu-id="c4f56-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-212">Deaktivieren Sie den durch *ProcessID* angegebenen Prozess.</span><span class="sxs-lookup"><span data-stu-id="c4f56-212">Disable the process specified by *ProcessId*.</span></span> <span data-ttu-id="c4f56-213">Um alle Prozesse zu deaktivieren, verwenden Sie " \* " für den Wert von *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="c4f56-213">To disable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="c4f56-214">Es kann jeweils mehr als eine **PID** -Option angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-214">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="c4f56-215">Die Reihenfolge der Optionen bestimmt, welche Prozesse aktiviert oder deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-215">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="c4f56-216">Um z. b. alle Prozesse außer dem Prozess zu deaktivieren, dessen Prozess-ID 0xe8c ist, verwenden Sie **vsstrace-PID \* + PID 0xe8c**.</span><span class="sxs-lookup"><span data-stu-id="c4f56-216">For example, to disable all processes except the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="c4f56-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+ TID** *ThreadId*</span><span class="sxs-lookup"><span data-stu-id="c4f56-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-218">Aktivieren Sie den von *ThreadId* angegebenen Thread.</span><span class="sxs-lookup"><span data-stu-id="c4f56-218">Enable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="c4f56-219">Um alle Threads zu aktivieren, verwenden Sie " \* " für den Wert von *ThreadId*.</span><span class="sxs-lookup"><span data-stu-id="c4f56-219">To enable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="c4f56-220">Es kann jeweils mehr als eine **TID** -Option angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-220">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="c4f56-221">Die Reihenfolge der Optionen bestimmt, welche Threads aktiviert oder deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-221">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="c4f56-222">Um z. b. nur den Thread zu aktivieren, dessen Prozess-ID 0x31a ist, verwenden Sie **vsstrace-TID \* + TID 0x31a**.</span><span class="sxs-lookup"><span data-stu-id="c4f56-222">For example, to enable only the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="c4f56-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-TID** *ThreadId*</span><span class="sxs-lookup"><span data-stu-id="c4f56-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-224">Deaktivieren Sie den von *ThreadId* angegebenen Thread.</span><span class="sxs-lookup"><span data-stu-id="c4f56-224">Disable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="c4f56-225">Um alle Threads zu deaktivieren, verwenden Sie " \* " für den Wert von *ThreadId*.</span><span class="sxs-lookup"><span data-stu-id="c4f56-225">To disable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="c4f56-226">Es kann jeweils mehr als eine **TID** -Option angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-226">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="c4f56-227">Die Reihenfolge der Optionen bestimmt, welche Threads aktiviert oder deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-227">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="c4f56-228">Wenn Sie z. b. alle Threads außer dem Thread, dessen Prozess-ID 0x31a ist, deaktivieren möchten, verwenden Sie **vsstrace-TID \* + TID 0x31a**.</span><span class="sxs-lookup"><span data-stu-id="c4f56-228">For example, to disable all threads except the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="c4f56-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l-** *Ebene*</span><span class="sxs-lookup"><span data-stu-id="c4f56-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *Level*</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-230">Verwenden Sie die nach *Ebene* angegebene Ablauf Verfolgungs Ebene.</span><span class="sxs-lookup"><span data-stu-id="c4f56-230">Use the tracing level specified by *Level*.</span></span> <span data-ttu-id="c4f56-231">Je höher die Ebene, desto ausführlicher wird die Ausgabe der Ablauf Verfolgung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4f56-231">The higher the level, the more verbose the trace output.</span></span> <span data-ttu-id="c4f56-232">Jede Ebene enthält alle niedrigeren Ebenen.</span><span class="sxs-lookup"><span data-stu-id="c4f56-232">Each level includes all of the lower levels.</span></span> <span data-ttu-id="c4f56-233">Der Standardwert ist 170.</span><span class="sxs-lookup"><span data-stu-id="c4f56-233">The default level is 170.</span></span> <span data-ttu-id="c4f56-234">Die folgenden Ebenen sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c4f56-234">The following levels are available.</span></span>



| <span data-ttu-id="c4f56-235">Ebene</span><span class="sxs-lookup"><span data-stu-id="c4f56-235">Level</span></span> | <span data-ttu-id="c4f56-236">In der Ausgabe der Ablauf Verfolgung enthaltene Informationen</span><span class="sxs-lookup"><span data-stu-id="c4f56-236">Information included in the trace output</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="c4f56-237">000</span><span class="sxs-lookup"><span data-stu-id="c4f56-237">000</span></span>   | <span data-ttu-id="c4f56-238">Keine</span><span class="sxs-lookup"><span data-stu-id="c4f56-238">None</span></span>                                     |
| <span data-ttu-id="c4f56-239">020</span><span class="sxs-lookup"><span data-stu-id="c4f56-239">020</span></span>   | <span data-ttu-id="c4f56-240">Schwerwiegende Fehler</span><span class="sxs-lookup"><span data-stu-id="c4f56-240">Fatal errors</span></span>                             |
| <span data-ttu-id="c4f56-241">030</span><span class="sxs-lookup"><span data-stu-id="c4f56-241">030</span></span>   | <span data-ttu-id="c4f56-242">Ausnahmefehler</span><span class="sxs-lookup"><span data-stu-id="c4f56-242">Unhandled exceptions</span></span>                     |
| <span data-ttu-id="c4f56-243">040</span><span class="sxs-lookup"><span data-stu-id="c4f56-243">040</span></span>   | <span data-ttu-id="c4f56-244">Errors</span><span class="sxs-lookup"><span data-stu-id="c4f56-244">Errors</span></span>                                   |
| <span data-ttu-id="c4f56-245">050</span><span class="sxs-lookup"><span data-stu-id="c4f56-245">050</span></span>   | <span data-ttu-id="c4f56-246">Assertionen</span><span class="sxs-lookup"><span data-stu-id="c4f56-246">Assertions</span></span>                               |
| <span data-ttu-id="c4f56-247">060</span><span class="sxs-lookup"><span data-stu-id="c4f56-247">060</span></span>   | <span data-ttu-id="c4f56-248">Warnungen</span><span class="sxs-lookup"><span data-stu-id="c4f56-248">Warnings</span></span>                                 |
| <span data-ttu-id="c4f56-249">080</span><span class="sxs-lookup"><span data-stu-id="c4f56-249">080</span></span>   | <span data-ttu-id="c4f56-250">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="c4f56-250">Exception handling</span></span>                       |
| <span data-ttu-id="c4f56-251">100</span><span class="sxs-lookup"><span data-stu-id="c4f56-251">100</span></span>   | <span data-ttu-id="c4f56-252">Ereignisprotokoll Aktivität</span><span class="sxs-lookup"><span data-stu-id="c4f56-252">Event Log activity</span></span>                       |
| <span data-ttu-id="c4f56-253">120</span><span class="sxs-lookup"><span data-stu-id="c4f56-253">120</span></span>   | <span data-ttu-id="c4f56-254">Allgemeine Informationen</span><span class="sxs-lookup"><span data-stu-id="c4f56-254">General information</span></span>                      |
| <span data-ttu-id="c4f56-255">140</span><span class="sxs-lookup"><span data-stu-id="c4f56-255">140</span></span>   | <span data-ttu-id="c4f56-256">Codeflow</span><span class="sxs-lookup"><span data-stu-id="c4f56-256">Code flow</span></span>                                |
| <span data-ttu-id="c4f56-257">160</span><span class="sxs-lookup"><span data-stu-id="c4f56-257">160</span></span>   | <span data-ttu-id="c4f56-258">Funktion eingeben und beenden</span><span class="sxs-lookup"><span data-stu-id="c4f56-258">Function enter and exit</span></span>                  |
| <span data-ttu-id="c4f56-259">170</span><span class="sxs-lookup"><span data-stu-id="c4f56-259">170</span></span>   | <span data-ttu-id="c4f56-260">Funktions Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="c4f56-260">Function return values</span></span>                   |
| <span data-ttu-id="c4f56-261">180</span><span class="sxs-lookup"><span data-stu-id="c4f56-261">180</span></span>   | <span data-ttu-id="c4f56-262">Funktionsparameter (Terse)</span><span class="sxs-lookup"><span data-stu-id="c4f56-262">Function parameters (terse)</span></span>              |
| <span data-ttu-id="c4f56-263">190</span><span class="sxs-lookup"><span data-stu-id="c4f56-263">190</span></span>   | <span data-ttu-id="c4f56-264">Funktionsparameter (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="c4f56-264">Function parameters (verbose)</span></span>            |
| <span data-ttu-id="c4f56-265">200</span><span class="sxs-lookup"><span data-stu-id="c4f56-265">200</span></span>   | <span data-ttu-id="c4f56-266">Ausführliche Informationsebene 1</span><span class="sxs-lookup"><span data-stu-id="c4f56-266">Verbose information level 1</span></span>              |
| <span data-ttu-id="c4f56-267">210</span><span class="sxs-lookup"><span data-stu-id="c4f56-267">210</span></span>   | <span data-ttu-id="c4f56-268">Ausführliche Informationsebene 2</span><span class="sxs-lookup"><span data-stu-id="c4f56-268">Verbose information level 2</span></span>              |
| <span data-ttu-id="c4f56-269">220</span><span class="sxs-lookup"><span data-stu-id="c4f56-269">220</span></span>   | <span data-ttu-id="c4f56-270">Ausführliche Informationen Ebene 3</span><span class="sxs-lookup"><span data-stu-id="c4f56-270">Verbose information level 3</span></span>              |
| <span data-ttu-id="c4f56-271">230</span><span class="sxs-lookup"><span data-stu-id="c4f56-271">230</span></span>   | <span data-ttu-id="c4f56-272">Schnelle Codeebene 1</span><span class="sxs-lookup"><span data-stu-id="c4f56-272">Fast Code Level 1</span></span>                        |
| <span data-ttu-id="c4f56-273">240</span><span class="sxs-lookup"><span data-stu-id="c4f56-273">240</span></span>   | <span data-ttu-id="c4f56-274">Schnelle Codeebene 2</span><span class="sxs-lookup"><span data-stu-id="c4f56-274">Fast Code Level 2</span></span>                        |
| <span data-ttu-id="c4f56-275">250</span><span class="sxs-lookup"><span data-stu-id="c4f56-275">250</span></span>   | <span data-ttu-id="c4f56-276">Schnelle Codeebene 3</span><span class="sxs-lookup"><span data-stu-id="c4f56-276">Fast Code Level 3</span></span>                        |
| <span data-ttu-id="c4f56-277">255</span><span class="sxs-lookup"><span data-stu-id="c4f56-277">255</span></span>   | <span data-ttu-id="c4f56-278">Alle</span><span class="sxs-lookup"><span data-stu-id="c4f56-278">All</span></span>                                      |



 

</dd> <dt>

<span data-ttu-id="c4f56-279"><span id="_indent"></span><span id="_INDENT"></span>**+ Einzug**</span><span class="sxs-lookup"><span data-stu-id="c4f56-279"><span id="_indent"></span><span id="_INDENT"></span>**+indent**</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-280">Einzug der formatierten Ablauf Verfolgungs Ausgabe an jeder Funktions-und unter Funktions Grenze.</span><span class="sxs-lookup"><span data-stu-id="c4f56-280">Indent the formatted trace output at each function and subfunction boundary.</span></span>

</dd> <dt>

<span data-ttu-id="c4f56-281"><span id="-indent"></span><span id="-INDENT"></span>**Einzug**</span><span class="sxs-lookup"><span data-stu-id="c4f56-281"><span id="-indent"></span><span id="-INDENT"></span>**-indent**</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-282">Die formatierte Ablauf Verfolgungs Ausgabe nicht einziehen.</span><span class="sxs-lookup"><span data-stu-id="c4f56-282">Do not indent the formatted trace output.</span></span>

</dd> <dt>

<span data-ttu-id="c4f56-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-ETL** *etlfile*</span><span class="sxs-lookup"><span data-stu-id="c4f56-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-etl** *EtlFile*</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-284">Konvertieren Sie die von *etlfile* angegebene logman-Ausgabedatei in ein lesbares Textformat.</span><span class="sxs-lookup"><span data-stu-id="c4f56-284">Convert the Logman output file specified by *EtlFile* into a readable text format.</span></span>

</dd> <dt>

<span data-ttu-id="c4f56-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*</span><span class="sxs-lookup"><span data-stu-id="c4f56-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-286">Speichern Sie die Ablauf Verfolgungs Informationen in der Ausgabedatei, die von *OutputFile* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4f56-286">Save the tracing information to the output file specified by *OutputFile*.</span></span> <span data-ttu-id="c4f56-287">Um die optimale Leistung zu erzielen, sollte sich die Ausgabedatei auf einem Volume befinden, das nicht Teil der Schatten Kopie ist.</span><span class="sxs-lookup"><span data-stu-id="c4f56-287">For best performance, the output file should be located on a volume that is not part of the shadow copy.</span></span>

</dd> <dt>

<span data-ttu-id="c4f56-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-Help** *helpop tion*</span><span class="sxs-lookup"><span data-stu-id="c4f56-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-help** *HelpOption*</span></span>
</dt> <dd>

<span data-ttu-id="c4f56-289">Zeigt die Befehlszeilen Hilfe an, wie von *helpoption* angegeben.</span><span class="sxs-lookup"><span data-stu-id="c4f56-289">Display the command-line help as specified by *HelpOption*.</span></span> <span data-ttu-id="c4f56-290">Gültige *helpoption* -Werte sind **Module**, **Levels** und **all**.</span><span class="sxs-lookup"><span data-stu-id="c4f56-290">The valid *HelpOption* values are **modules**, **levels**, and **all**.</span></span> <span data-ttu-id="c4f56-291">Die Angabe von **Modulen** bewirkt, dass die Module aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-291">Specifying **modules** causes the modules to be listed.</span></span> <span data-ttu-id="c4f56-292">Das Angeben von **Ebenen** bewirkt, dass die verfügbaren Ebenen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-292">Specifying **levels** causes the available levels to be listed.</span></span> <span data-ttu-id="c4f56-293">Das Angeben von **all** bewirkt, dass ausführliche Hilfe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4f56-293">Specifying **all** causes detailed help to be displayed.</span></span> <span data-ttu-id="c4f56-294">Wenn keine Optionen verwendet werden, wird eine kurze Hilfe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4f56-294">If no options are used, concise help is displayed.</span></span>

</dd> </dl>

## <a name="using-logman"></a><span data-ttu-id="c4f56-295">Verwenden von logman</span><span class="sxs-lookup"><span data-stu-id="c4f56-295">Using Logman</span></span>

<span data-ttu-id="c4f56-296">Im folgenden Verfahren wird beschrieben, wie Sie Logman mit der VSS-Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4f56-296">The following procedure describes how to use Logman with your VSS application.</span></span>

<span data-ttu-id="c4f56-297">**So verwenden Sie Logman mit der VSS-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="c4f56-297">**To use Logman with your VSS application**</span></span>

1.  <span data-ttu-id="c4f56-298">Verwenden Sie den folgenden Befehl zum Starten der Ablauf Verfolgung:</span><span class="sxs-lookup"><span data-stu-id="c4f56-298">Use the following command to start tracing:</span></span>

    <span data-ttu-id="c4f56-299">**logman Start VSS-o** *x: \\ \* \* \* VSS. ETL-ETS-p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170*\*</span><span class="sxs-lookup"><span data-stu-id="c4f56-299">**logman start vss -o** *x:\\*\*\*vss.etl -ets -p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="c4f56-300">Ersetzen Sie "x: \\ " durch den Pfad zu dem Verzeichnis, in dem die Ablauf Verfolgungs Protokolldatei gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4f56-300">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

2.  <span data-ttu-id="c4f56-301">Verwenden Sie den folgenden Befehl, um die Ablauf Verfolgung anzuhalten:</span><span class="sxs-lookup"><span data-stu-id="c4f56-301">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="c4f56-302">**logman stoppt VSS-ETS**</span><span class="sxs-lookup"><span data-stu-id="c4f56-302">**logman stop vss -ets**</span></span>

<span data-ttu-id="c4f56-303">Die Ablauf Verfolgungs Protokolldatei ist *x \\ :* VSS. ETL.</span><span class="sxs-lookup"><span data-stu-id="c4f56-303">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="c4f56-304">Weitere Informationen zum Logman-Tool finden Sie unter [logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="c4f56-304">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="c4f56-305">Verwenden von tracelog</span><span class="sxs-lookup"><span data-stu-id="c4f56-305">Using Tracelog</span></span>

<span data-ttu-id="c4f56-306">Im folgenden Verfahren wird die Verwendung von tracelog beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c4f56-306">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="c4f56-307">**So verwenden Sie tracelog**</span><span class="sxs-lookup"><span data-stu-id="c4f56-307">**To use Tracelog**</span></span>

1.  <span data-ttu-id="c4f56-308">Erstellen Sie eine Textdatei mit dem Namen "VSS. CTL", die nur den folgenden Text enthält:</span><span class="sxs-lookup"><span data-stu-id="c4f56-308">Create a text file named vss.ctl that contains only the following text:</span></span>

    <span data-ttu-id="c4f56-309">**9138500e-3648-4edb-aa4c-859e9f7b7c38 VSS**</span><span class="sxs-lookup"><span data-stu-id="c4f56-309">**9138500e-3648-4edb-aa4c-859e9f7b7c38 vss**</span></span>

2.  <span data-ttu-id="c4f56-310">Verwenden Sie den folgenden Befehl zum Starten der Ablauf Verfolgung:</span><span class="sxs-lookup"><span data-stu-id="c4f56-310">Use the following command to start tracing:</span></span>

    <span data-ttu-id="c4f56-311">**tracelog-Start VSS-f** *x: \\ \* \* \* VSS. ETL-GUID VSS. CTL-Flag 0xFF-Level 0xaa*\*</span><span class="sxs-lookup"><span data-stu-id="c4f56-311">**tracelog -start vss -f** *x:\\*\*\*vss.etl -guid vss.ctl -flag 0xff -level 0xaa*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="c4f56-312">Ersetzen Sie "x: \\ " durch den Pfad zu dem Verzeichnis, in dem die Ablauf Verfolgungs Protokolldatei gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4f56-312">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

3.  <span data-ttu-id="c4f56-313">Verwenden Sie den folgenden Befehl, um die Ablauf Verfolgung anzuhalten:</span><span class="sxs-lookup"><span data-stu-id="c4f56-313">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="c4f56-314">**tracelog-VSS Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="c4f56-314">**tracelog -stop vss**</span></span>

<span data-ttu-id="c4f56-315">Die Ablauf Verfolgungs Protokolldatei ist *x \\ :* VSS. ETL.</span><span class="sxs-lookup"><span data-stu-id="c4f56-315">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="c4f56-316">Weitere Informationen zum tracelog-Tool finden Sie unter [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span><span class="sxs-lookup"><span data-stu-id="c4f56-316">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
