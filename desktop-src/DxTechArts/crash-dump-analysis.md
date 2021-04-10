---
title: Absturz Abbild Analyse
description: Dieser technische Artikel enthält Informationen zum Schreiben und Verwenden eines minidumpdiensts.
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7558e47d08cb0183b8d9cefa5f22f0750fd1c598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039243"
---
# <a name="crash-dump-analysis"></a><span data-ttu-id="7872b-103">Absturz Abbild Analyse</span><span class="sxs-lookup"><span data-stu-id="7872b-103">Crash Dump Analysis</span></span>

<span data-ttu-id="7872b-104">Vor der Freigabe können nicht alle Fehler gefunden werden. Dies bedeutet, dass nicht alle Fehler, die Ausnahmen auslösen, vor der Freigabe gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="7872b-104">Not all bugs can be found prior to release, which means not all bugs that throw exceptions can be found before release.</span></span> <span data-ttu-id="7872b-105">Glücklicherweise hat Microsoft in das Platform SDK eine Funktion integriert, um Entwicklern bei der Erfassung von Informationen zu Ausnahmen zu helfen, die von Benutzern erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="7872b-105">Fortunately, Microsoft has included in the Platform SDK a function to help developers collect information on exceptions that are discovered by users.</span></span> <span data-ttu-id="7872b-106">Die [**minidumpschreitedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) -Funktion schreibt die erforderlichen Absturz Abbild Informationen in eine Datei, ohne den gesamten Prozessbereich zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7872b-106">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function writes the necessary crash dump information to a file without saving the whole process space.</span></span> <span data-ttu-id="7872b-107">Diese Datei mit Absturz Abbild Informationen wird als Minidump bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7872b-107">This crash dump information file is called a minidump.</span></span> <span data-ttu-id="7872b-108">Dieser technische Artikel enthält Informationen zum Schreiben und Verwenden eines minidumpdiensts.</span><span class="sxs-lookup"><span data-stu-id="7872b-108">This technical article provides info about how to write and use a minidump.</span></span>

-   [<span data-ttu-id="7872b-109">Schreiben eines Minidumps</span><span class="sxs-lookup"><span data-stu-id="7872b-109">Writing a Minidump</span></span>](#writing-a-minidump)
-   [<span data-ttu-id="7872b-110">Thread Sicherheit</span><span class="sxs-lookup"><span data-stu-id="7872b-110">Thread safety</span></span>](#thread-safety)
-   [<span data-ttu-id="7872b-111">Schreiben eines minidumpcodes mit Code</span><span class="sxs-lookup"><span data-stu-id="7872b-111">Writing a Minidump with Code</span></span>](#writing-a-minidump-with-code)
-   [<span data-ttu-id="7872b-112">Verwenden von Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="7872b-112">Using Dumpchk.exe</span></span>](#using-dumpchkexe)
-   [<span data-ttu-id="7872b-113">Analysieren eines minidumpdiensts</span><span class="sxs-lookup"><span data-stu-id="7872b-113">Analyzing a Minidump</span></span>](#analyzing-a-minidump)
    -   [<span data-ttu-id="7872b-114">Verwenden des öffentlichen Symbol Servers von Microsoft</span><span class="sxs-lookup"><span data-stu-id="7872b-114">Using the Microsoft Public Symbol Server</span></span>](#using-the-microsoft-public-symbol-server)
    -   [<span data-ttu-id="7872b-115">Debuggen eines Minidumps mit WinDbg</span><span class="sxs-lookup"><span data-stu-id="7872b-115">Debugging a Minidump with WinDbg</span></span>](#debugging-a-minidump-with-windbg)
    -   [<span data-ttu-id="7872b-116">Verwenden von Copy-Protection Tools mit Minidumps</span><span class="sxs-lookup"><span data-stu-id="7872b-116">Using Copy-Protection Tools with Minidumps</span></span>](#using-copy-protection-tools-with-minidumps)
-   [<span data-ttu-id="7872b-117">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7872b-117">Summary</span></span>](#summary)

## <a name="writing-a-minidump"></a><span data-ttu-id="7872b-118">Schreiben eines Minidumps</span><span class="sxs-lookup"><span data-stu-id="7872b-118">Writing a Minidump</span></span>

<span data-ttu-id="7872b-119">Die grundlegenden Optionen zum Schreiben eines Minidumps lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7872b-119">The basic options for writing a minidump are as follows:</span></span>

-   <span data-ttu-id="7872b-120">Sie unternehmen nichts.</span><span class="sxs-lookup"><span data-stu-id="7872b-120">Do nothing.</span></span> <span data-ttu-id="7872b-121">Windows generiert automatisch ein Minidump, wenn ein Programm eine nicht behandelte Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="7872b-121">Windows automatically generates a minidump whenever a program throws an unhandled exception.</span></span> <span data-ttu-id="7872b-122">Die automatische Generierung eines minidumpdiensts ist seit Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7872b-122">Automatic generation of a minidump is available since Windows XP.</span></span> <span data-ttu-id="7872b-123">Wenn der Benutzer dies zulässt, wird das Minidump über Windows-Fehlerberichterstattung (wer) an Microsoft gesendet und nicht an den Entwickler.</span><span class="sxs-lookup"><span data-stu-id="7872b-123">If the user allows it, the minidump will be sent to Microsoft, and not to the developer, through Windows Error Reporting (WER).</span></span> <span data-ttu-id="7872b-124">Entwickler können über das [Windows-Desktop Anwendungsprogramm](../appxpkg/windows-desktop-application-program.md)auf diese Minidumps zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7872b-124">Developers can gain access to these minidumps through the [Windows Desktop Application Program](../appxpkg/windows-desktop-application-program.md).</span></span>

    <span data-ttu-id="7872b-125">Die Verwendung von wer erfordert Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7872b-125">Use of WER requires:</span></span>

    -   <span data-ttu-id="7872b-126">Entwickler zum Signieren Ihrer Anwendungen mit Authenticode</span><span class="sxs-lookup"><span data-stu-id="7872b-126">Developers to sign their applications using Authenticode</span></span>
    -   <span data-ttu-id="7872b-127">Anwendungen verfügen über eine gültige VERSIONINFO-Ressource in jeder ausführbaren Datei und dll.</span><span class="sxs-lookup"><span data-stu-id="7872b-127">Applications have valid VERSIONINFO resource in every executable and DLL</span></span>

    <span data-ttu-id="7872b-128">Wenn Sie eine benutzerdefinierte Routine für nicht behandelte Ausnahmen implementieren, werden Sie nachdrücklich aufgefordert, die [**Report Fault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) -Funktion im Ausnahmehandler zu verwenden, um auch einen automatisierten Minidump an wer zu senden.</span><span class="sxs-lookup"><span data-stu-id="7872b-128">If you implement a custom routine for unhandled exceptions, you are strongly urged to use the [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) function in the exception handler to also send an automated minidump to WER.</span></span> <span data-ttu-id="7872b-129">Die Funktion **Report Fault** behandelt alle Probleme, die beim Herstellen einer Verbindung mit und dem Senden des Minidump an wer auftreten.</span><span class="sxs-lookup"><span data-stu-id="7872b-129">The **ReportFault** function handles all of the issues of connecting to and sending the minidump to WER.</span></span> <span data-ttu-id="7872b-130">Das Senden von Minidumps an wer verstößt gegen die Anforderungen von Spielen für Windows.</span><span class="sxs-lookup"><span data-stu-id="7872b-130">Not sending minidumps to WER violates the requirements of Games for Windows.</span></span>

    <span data-ttu-id="7872b-131">Weitere Informationen zur Funktionsweise von wer finden Sie unter [Funktionsweise von Windows-Fehlerberichterstattung](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span><span class="sxs-lookup"><span data-stu-id="7872b-131">For more information on how WER works, see [How Windows Error Reporting Works](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span></span> <span data-ttu-id="7872b-132">Eine Erläuterung der Registrierungsdetails finden Sie unter [Introducing Windows-Fehlerberichterstattung](https://msdn.microsoft.com/) in der MSDN- [ISV-Zone](https://msdn.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="7872b-132">For an explanation of registration details, see [Introducing Windows Error Reporting](https://msdn.microsoft.com/) on MSDN's [ISV Zone](https://msdn.microsoft.com/).</span></span>

-   <span data-ttu-id="7872b-133">Verwenden Sie ein Produkt aus dem Microsoft Visual Studio Team System.</span><span class="sxs-lookup"><span data-stu-id="7872b-133">Use a product from the Microsoft Visual Studio Team System.</span></span> <span data-ttu-id="7872b-134">Klicken Sie im Menü **Debuggen** auf **Dump speichern** unter, um eine Kopie eines dumpspeichers zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7872b-134">On the **Debug** menu, click **Save Dump As** to save a copy of a dump.</span></span> <span data-ttu-id="7872b-135">Die Verwendung eines lokal gespeicherten dumpdiensts ist nur eine Option für internes testen und Debuggen.</span><span class="sxs-lookup"><span data-stu-id="7872b-135">Use of a locally saved dump is only an option for in-house testing and debugging.</span></span>
-   <span data-ttu-id="7872b-136">Fügen Sie Ihrem Projekt Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="7872b-136">Add code to your project.</span></span> <span data-ttu-id="7872b-137">Fügen Sie die [**minidumpbeschreib tedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) -Funktion und den entsprechenden Code für die Ausnahmebehandlung hinzu, um ein Minidump direkt an den Entwickler zu speichern und zu senden.</span><span class="sxs-lookup"><span data-stu-id="7872b-137">Add the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function and the appropriate exception handling code to save and send a minidump directly to the developer.</span></span> <span data-ttu-id="7872b-138">In diesem Artikel wird veranschaulicht, wie diese Option implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="7872b-138">This article demonstrates how to implement this option.</span></span> <span data-ttu-id="7872b-139">Beachten Sie jedoch, dass **minidumpbeschreib tedump** derzeit nicht mit verwaltetem Code funktioniert und nur unter Windows XP, Windows Vista, Windows 7 verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7872b-139">However, note that **MiniDumpWriteDump** does not currently work with managed code and is only available on Windows XP, Windows Vista, Windows 7.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="7872b-140">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="7872b-140">Thread safety</span></span>

<span data-ttu-id="7872b-141">[**Minidumpschreitedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) ist Teil der DbgHelp-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="7872b-141">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) is part of the DBGHELP library.</span></span> <span data-ttu-id="7872b-142">Diese Bibliothek ist nicht Thread sicher, daher sollte jedes Programm, das **minidumpschreitedump** verwendet, alle Threads synchronisieren, bevor versucht wird, **minidumpschreitedump** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7872b-142">This library is not thread-safe, so any program that uses **MiniDumpWriteDump** should synchronize all threads before attempting to call **MiniDumpWriteDump**.</span></span>

## <a name="writing-a-minidump-with-code"></a><span data-ttu-id="7872b-143">Schreiben eines minidumpcodes mit Code</span><span class="sxs-lookup"><span data-stu-id="7872b-143">Writing a Minidump with Code</span></span>

<span data-ttu-id="7872b-144">Die tatsächliche Implementierung ist einfach.</span><span class="sxs-lookup"><span data-stu-id="7872b-144">The actual implementation is straightforward.</span></span> <span data-ttu-id="7872b-145">Im folgenden finden Sie ein einfaches Beispiel für die Verwendung von [**minidumpschreitedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span><span class="sxs-lookup"><span data-stu-id="7872b-145">The following is a simple example of how to use [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>


```C++
#include <dbghelp.h>
#include <shellapi.h>
#include <shlobj.h>

int GenerateDump(EXCEPTION_POINTERS* pExceptionPointers)
{
    BOOL bMiniDumpSuccessful;
    WCHAR szPath[MAX_PATH]; 
    WCHAR szFileName[MAX_PATH]; 
    WCHAR* szAppName = L"AppName";
    WCHAR* szVersion = L"v1.0";
    DWORD dwBufferSize = MAX_PATH;
    HANDLE hDumpFile;
    SYSTEMTIME stLocalTime;
    MINIDUMP_EXCEPTION_INFORMATION ExpParam;

    GetLocalTime( &stLocalTime );
    GetTempPath( dwBufferSize, szPath );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s", szPath, szAppName );
    CreateDirectory( szFileName, NULL );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s\\%s-%04d%02d%02d-%02d%02d%02d-%ld-%ld.dmp", 
               szPath, szAppName, szVersion, 
               stLocalTime.wYear, stLocalTime.wMonth, stLocalTime.wDay, 
               stLocalTime.wHour, stLocalTime.wMinute, stLocalTime.wSecond, 
               GetCurrentProcessId(), GetCurrentThreadId());
    hDumpFile = CreateFile(szFileName, GENERIC_READ|GENERIC_WRITE, 
                FILE_SHARE_WRITE|FILE_SHARE_READ, 0, CREATE_ALWAYS, 0, 0);

    ExpParam.ThreadId = GetCurrentThreadId();
    ExpParam.ExceptionPointers = pExceptionPointers;
    ExpParam.ClientPointers = TRUE;

    bMiniDumpSuccessful = MiniDumpWriteDump(GetCurrentProcess(), GetCurrentProcessId(), 
                    hDumpFile, MiniDumpWithDataSegs, &ExpParam, NULL, NULL);

    return EXCEPTION_EXECUTE_HANDLER;
}


void SomeFunction()
{
    __try
    {
        int *pBadPtr = NULL;
        *pBadPtr = 0;
    }
    __except(GenerateDump(GetExceptionInformation()))
    {
    }
}
```



<span data-ttu-id="7872b-146">Dieses Beispiel veranschaulicht die grundlegende Verwendung von [**minidumpbeschreib tedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) und die minimalen Informationen, die erforderlich sind, um es aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7872b-146">This example demonstrates the basic usage of [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) and the minimum information necessary to call it.</span></span> <span data-ttu-id="7872b-147">Der Name der Dumpdatei ist für den Entwickler. um Dateinamen Konflikte zu vermeiden, empfiehlt es sich jedoch, den Dateinamen aus dem Namen und der Versionsnummer der Anwendung, die Prozess-und Thread-IDs sowie das Datum und die Uhrzeit zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7872b-147">The name of the dump file is up to the developer; however, to avoid file name collisions, it is advisable to generate the file name from the application's name and version number, the process and thread IDs, and the date and time.</span></span> <span data-ttu-id="7872b-148">Dies trägt auch dazu bei, dass die Minidumps nach Anwendung und Version gruppiert bleiben.</span><span class="sxs-lookup"><span data-stu-id="7872b-148">This will also help to keep the minidumps grouped by application and version.</span></span> <span data-ttu-id="7872b-149">Der Entwickler kann entscheiden, wie viele Informationen zur Unterscheidung von Minidump-Dateinamen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7872b-149">It is up to the developer to decide how much information is used to differentiate minidump file names.</span></span>

<span data-ttu-id="7872b-150">Beachten Sie, dass der Pfadname im vorangehenden Beispiel durch Aufrufen der [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) -Funktion generiert wurde, um den Pfad des für temporäre Dateien vorgesehenen Verzeichnisses abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7872b-150">It should be noted that the path name in the preceding example was generated by calling the [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files.</span></span> <span data-ttu-id="7872b-151">Die Verwendung dieses Verzeichnisses funktioniert auch mit Benutzerkonten mit den geringsten Rechten. Außerdem wird verhindert, dass der Minidump Festplattenspeicher belegt, wenn er nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="7872b-151">Use of this directory works even with least-privileged user accounts, and it also prevents the minidump from taking up hard drive space after it is no longer needed.</span></span>

<span data-ttu-id="7872b-152">Wenn Sie das Produkt während des täglichen Buildvorgangs archivieren, achten Sie auch darauf, dass Sie Symbole für den Build einschließen, damit Sie ggf. eine alte Version des Produkts Debuggen können.</span><span class="sxs-lookup"><span data-stu-id="7872b-152">If you archive the product during your daily build process, also be sure to include symbols for the build so that you can debug an old version of the product, if necessary.</span></span> <span data-ttu-id="7872b-153">Außerdem müssen Sie Maßnahmen ergreifen, um bei der Erstellung von Symbolen vollständige Compileroptimierungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7872b-153">You also need to take steps to maintain full compiler optimizations while generating symbols.</span></span> <span data-ttu-id="7872b-154">Dies können Sie erreichen, indem Sie die Eigenschaften des Projekts in der Entwicklungsumgebung öffnen und für die Releasekonfiguration Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="7872b-154">This can be done by opening your project's properties in the development environment and, for the release configuration, doing the following:</span></span>

1.  <span data-ttu-id="7872b-155">Klicken Sie auf der linken Seite der Eigenschaften Seite des Projekts auf C/C++.</span><span class="sxs-lookup"><span data-stu-id="7872b-155">On the left side of the project's property page, click C/C++.</span></span> <span data-ttu-id="7872b-156">In der Standardeinstellung werden **Allgemeine** Einstellungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7872b-156">By default, this displays **General** settings.</span></span> <span data-ttu-id="7872b-157">Legen Sie auf der rechten Seite der Eigenschaften Seite des Projekts **Debug-Informations Format** auf **Programmdatenbank (/Zi)** fest.</span><span class="sxs-lookup"><span data-stu-id="7872b-157">On the right side of the project's property page, set **Debug Information Format** to **Program Database (/Zi)**.</span></span>
2.  <span data-ttu-id="7872b-158">Erweitern Sie auf der linken Seite der Eigenschaften Seite **Linker**, und klicken Sie dann auf **Debuggen**.</span><span class="sxs-lookup"><span data-stu-id="7872b-158">On the left side of the property page, expand **Linker**, and then click **Debugging**.</span></span> <span data-ttu-id="7872b-159">Legen Sie auf der rechten Seite der Eigenschaften Seite **Debuginformationen generieren** auf **Ja (/Debug)** fest.</span><span class="sxs-lookup"><span data-stu-id="7872b-159">On the right side of the property page, set **Generate Debug Info** to **Yes (/DEBUG)**.</span></span>
3.  <span data-ttu-id="7872b-160">Klicken Sie auf **Optimierung**, und legen Sie **Verweise** auf **nicht referenzierte Daten (/opt: Ref)** fest.</span><span class="sxs-lookup"><span data-stu-id="7872b-160">Click **Optimization**, and set **References** to E **liminate Unreferenced Data (/OPT:REF)**.</span></span>
4.  <span data-ttu-id="7872b-161">Legen Sie **COMDAT-Faltung aktivieren** fest, um **Redundante COMDATs (/opt: ICF) zu entfernen**.</span><span class="sxs-lookup"><span data-stu-id="7872b-161">Set **Enable COMDAT Folding** to **Remove Redundant COMDATs (/OPT:ICF)**.</span></span>

<span data-ttu-id="7872b-162">MSDN enthält ausführlichere Informationen zur [**Minidump- \_ Ausnahme \_ Informations**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) Struktur und der [**minidumpbeschreib tedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7872b-162">MSDN has more detailed information on the [**MINIDUMP\_EXCEPTION\_INFORMATION**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) structure and the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function.</span></span>

## <a name="using-dumpchkexe"></a><span data-ttu-id="7872b-163">Verwenden von Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="7872b-163">Using Dumpchk.exe</span></span>

<span data-ttu-id="7872b-164">Dumpchk.exe ist ein Befehlszeilenprogramm, das verwendet werden kann, um zu überprüfen, ob eine Dumpdatei ordnungsgemäß erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7872b-164">Dumpchk.exe is a command-line utility that can be used to verify that a dump file was created correctly.</span></span> <span data-ttu-id="7872b-165">Wenn Dumpchk.exe einen Fehler generiert, ist die Dumpdatei beschädigt und kann nicht analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="7872b-165">If Dumpchk.exe generates an error, then the dump file is corrupt and cannot be analyzed.</span></span> <span data-ttu-id="7872b-166">Weitere Informationen zur Verwendung von Dumpchk.exe finden [Sie unter Verwenden von Dumpchk.exe zum Überprüfen einer Speicher](https://support.microsoft.com/kb/315271/)Abbild Datei.</span><span class="sxs-lookup"><span data-stu-id="7872b-166">For information on using Dumpchk.exe, see [How to Use Dumpchk.exe to Check a Memory Dump File](https://support.microsoft.com/kb/315271/).</span></span>

<span data-ttu-id="7872b-167">Dumpchk.exe ist auf der Windows XP-Produkt-CD enthalten und kann auf System Drive \\ Program Files-Support Tools installiert werden, \\ \\ indem Setup.exe im Ordner "Support \\ Tools" \\ auf der Windows XP-Produkt-CD ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7872b-167">Dumpchk.exe is included on the Windows XP product CD and can be installed to System Drive\\Program Files\\Support Tools\\ by running Setup.exe in the Support\\Tools\\ folder on the Windows XP product CD.</span></span> <span data-ttu-id="7872b-168">Sie können auch die neueste Version von Dumpchk.exe herunterladen, indem Sie die Debugtools herunterladen und installieren, die in den [Windows-Debugtools](https://www.microsoft.com/whdc/devtools/debugging/) unter [Windows Hardware Developer Central](https://www.microsoft.com/whdc/)verfügbar</span><span class="sxs-lookup"><span data-stu-id="7872b-168">You can also get the latest version of Dumpchk.exe by download and installing the debugging tools available from [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

## <a name="analyzing-a-minidump"></a><span data-ttu-id="7872b-169">Analysieren eines minidumpdiensts</span><span class="sxs-lookup"><span data-stu-id="7872b-169">Analyzing a Minidump</span></span>

<span data-ttu-id="7872b-170">Das Öffnen eines Minidump für die Analyse ist so einfach wie das Erstellen eines Minidump.</span><span class="sxs-lookup"><span data-stu-id="7872b-170">Opening a minidump for analysis is as easy as creating one.</span></span>

<span data-ttu-id="7872b-171">**So analysieren Sie ein Minidump**</span><span class="sxs-lookup"><span data-stu-id="7872b-171">**To analyze a minidump**</span></span>

1.  <span data-ttu-id="7872b-172">Öffnen Sie Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7872b-172">Open Visual Studio.</span></span>
2.  <span data-ttu-id="7872b-173">Klicken Sie im Menü **Datei** auf **Projekt öffnen**.</span><span class="sxs-lookup"><span data-stu-id="7872b-173">On the **File** menu, click **Open Project**.</span></span>
3.  <span data-ttu-id="7872b-174">Legen Sie **Dateityp** auf **Dumpdateien** fest, navigieren Sie zu der Dumpdatei, wählen Sie Sie aus, und klicken Sie auf **Öffnen.**</span><span class="sxs-lookup"><span data-stu-id="7872b-174">Set **Files of type** to **Dump Files**, navigate to the dump file, select it, and click **Open.**</span></span>
4.  <span data-ttu-id="7872b-175">Führen Sie den Debugger aus.</span><span class="sxs-lookup"><span data-stu-id="7872b-175">Run the debugger.</span></span>

<span data-ttu-id="7872b-176">Der Debugger erstellt einen simulierten Prozess.</span><span class="sxs-lookup"><span data-stu-id="7872b-176">The debugger will create a simulated process.</span></span> <span data-ttu-id="7872b-177">Der simulierte Prozess wird bei der Anweisung angehalten, die den Absturz verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="7872b-177">The simulated process will be halted at the instruction that caused the crash.</span></span>

### <a name="using-the-microsoft-public-symbol-server"></a><span data-ttu-id="7872b-178">Verwenden des öffentlichen Symbol Servers von Microsoft</span><span class="sxs-lookup"><span data-stu-id="7872b-178">Using the Microsoft Public Symbol Server</span></span>

<span data-ttu-id="7872b-179">Um den Stapel für Abstürze auf Treiber-oder Systemebene zu erhalten, kann es erforderlich sein, Visual Studio so zu konfigurieren, dass er auf den öffentlichen Microsoft-Symbol Server verweist.</span><span class="sxs-lookup"><span data-stu-id="7872b-179">To get the stack for driver- or system-level crashes, it might be necessary to configure Visual Studio to point to the Microsoft public symbol server.</span></span>

<span data-ttu-id="7872b-180">**So legen Sie einen Pfad zum Microsoft-Symbol Server fest**</span><span class="sxs-lookup"><span data-stu-id="7872b-180">**To set a path to the Microsoft symbol server**</span></span>

1.  <span data-ttu-id="7872b-181">Klicken Sie im Menü **Debuggen** auf **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="7872b-181">On the **Debug** menu, click **Options**.</span></span>
2.  <span data-ttu-id="7872b-182">Öffnen Sie im Dialogfeld **Optionen** den Knoten **Debuggen** , und klicken Sie auf **Symbole**.</span><span class="sxs-lookup"><span data-stu-id="7872b-182">In the **Options** dialog box, open the **Debugging** node, and click **Symbols**.</span></span>
3.  <span data-ttu-id="7872b-183">Stellen Sie sicher, dass Sie **die obigen Speicherorte nur durchsuchen, wenn Symbole manuell geladen werden** nicht ausgewählt ist, es sei denn, Sie möchten Symbole beim Debuggen manuell laden</span><span class="sxs-lookup"><span data-stu-id="7872b-183">Make sure **Search the above locations only when symbols are loaded manually** is not selected, unless you want to load symbols manually when you debug.</span></span>
4.  <span data-ttu-id="7872b-184">Wenn Sie Symbole auf einem Remote Symbol Server verwenden, können Sie die Leistung verbessern, indem Sie ein lokales Verzeichnis angeben, in das Symbole kopiert werden können.</span><span class="sxs-lookup"><span data-stu-id="7872b-184">If you are using symbols on a remote symbol server, you can improve performance by specifying a local directory that symbols can be copied to.</span></span> <span data-ttu-id="7872b-185">Geben Sie hierzu einen Pfad für **das Zwischenspeichern von Symbolen von Symbol Server zu diesem Verzeichnis** ein.</span><span class="sxs-lookup"><span data-stu-id="7872b-185">To do this, enter a path for **Cache symbols from symbol server to this directory**.</span></span> <span data-ttu-id="7872b-186">Zum Herstellen einer Verbindung mit dem öffentlichen Symbol Server von Microsoft müssen Sie diese Einstellung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7872b-186">To connect to the Microsoft public symbol server, you need to enable this setting.</span></span> <span data-ttu-id="7872b-187">Beachten Sie Folgendes: Wenn Sie ein Programm auf einem Remote Computer Debuggen, verweist das Cache Verzeichnis auf ein Verzeichnis auf dem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="7872b-187">Note that if you are debugging a program on a remote computer, the cache directory refers to a directory on the remote computer.</span></span>
5.  <span data-ttu-id="7872b-188">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7872b-188">Click **OK**.</span></span>
6.  <span data-ttu-id="7872b-189">Da Sie den öffentlichen Microsoft-Symbol Server verwenden, wird das Dialogfeld Endbenutzer-Lizenzvertrag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7872b-189">Because you are using the Microsoft public symbol server, an End User License Agreement dialog box appears.</span></span> <span data-ttu-id="7872b-190">Klicken Sie auf **Ja** , um die Vereinbarung zu akzeptieren und Symbole in Ihren lokalen Cache herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="7872b-190">Click **Yes** to accept the agreement and download symbols to your local cache.</span></span>

### <a name="debugging-a-minidump-with-windbg"></a><span data-ttu-id="7872b-191">Debuggen eines Minidumps mit WinDbg</span><span class="sxs-lookup"><span data-stu-id="7872b-191">Debugging a Minidump with WinDbg</span></span>

<span data-ttu-id="7872b-192">Sie können auch WinDbg verwenden, einen Debugger, der Teil der Windows-Debuggingtools ist, um ein Minidump zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="7872b-192">You can also use WinDbg, a debugger that is part of the Windows Debugging Tools, to debug a minidump.</span></span> <span data-ttu-id="7872b-193">WinDbg ermöglicht das Debuggen, ohne Visual Studio verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="7872b-193">WinDbg allows you to debug without having to use Visual Studio.</span></span> <span data-ttu-id="7872b-194">Informationen zum Herunterladen der Windows-Debuggingtools finden Sie unter Windows- [Debugtools](https://www.microsoft.com/whdc/devtools/debugging/) unter [Windows Hardware](https://www.microsoft.com/whdc/)</span><span class="sxs-lookup"><span data-stu-id="7872b-194">To download Windows Debugging Tools, see [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

<span data-ttu-id="7872b-195">Nachdem Sie die Windows-Debuggingtools installiert haben, müssen Sie den Symbol Pfad in WinDbg eingeben.</span><span class="sxs-lookup"><span data-stu-id="7872b-195">After installing Windows Debugging Tools, you must enter the symbol path in WinDbg.</span></span>

<span data-ttu-id="7872b-196">**So geben Sie einen Symbol Pfad in WinDbg ein**</span><span class="sxs-lookup"><span data-stu-id="7872b-196">**To enter a symbol path in WinDbg**</span></span>

1.  <span data-ttu-id="7872b-197">Klicken Sie im Menü **Datei** auf **Symbol Pfad**.</span><span class="sxs-lookup"><span data-stu-id="7872b-197">On the **File** menu, click **Symbol Path**.</span></span>
2.  <span data-ttu-id="7872b-198">Geben Sie im Fenster **Symbol Suchpfad** Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="7872b-198">In the **Symbol Search Path** window, enter the following:</span></span>

    <span data-ttu-id="7872b-199">"SRV \* c: \\ Cache \* https://msdl.microsoft.com/download/symbols ;"</span><span class="sxs-lookup"><span data-stu-id="7872b-199">"srv\*c:\\cache\*https://msdl.microsoft.com/download/symbols;"</span></span>

### <a name="using-copy-protection-tools-with-minidumps"></a><span data-ttu-id="7872b-200">Verwenden von Copy-Protection Tools mit Minidumps</span><span class="sxs-lookup"><span data-stu-id="7872b-200">Using Copy-Protection Tools with Minidumps</span></span>

<span data-ttu-id="7872b-201">Entwickler müssen auch wissen, wie sich das Kopierschutz Schema auf das Minidump auswirken könnte.</span><span class="sxs-lookup"><span data-stu-id="7872b-201">Developers also need to be aware of how their copy-protection scheme might affect the minidump.</span></span> <span data-ttu-id="7872b-202">Die meisten Kopierschutz Schemas verfügen über eigene, abzurufbare Tools, und es ist für den Entwickler zu erfahren, wie diese Tools mit [**minidumpschreitedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7872b-202">Most copy-protection schemes have their own descramble tools, and it is up to the developer to learn how to use those tools with [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>

## <a name="summary"></a><span data-ttu-id="7872b-203">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7872b-203">Summary</span></span>

<span data-ttu-id="7872b-204">Die [**minidumpschreitedump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) -Funktion kann ein äußerst nützliches Tool zum Erfassen und lösen von Fehlern sein, nachdem das Produkt veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="7872b-204">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function can be an extremely useful tool in collecting and solving bugs after the product has been released.</span></span> <span data-ttu-id="7872b-205">Durch das Schreiben eines benutzerdefinierten Ausnahme Handlers, der **MiniDumpWriteDump** verwendet, kann der Entwickler die Informationssammlung anpassen und den Debugprozess verbessern.</span><span class="sxs-lookup"><span data-stu-id="7872b-205">Writing a custom exception handler that uses **MiniDumpWriteDump** allows the developer to customize the information collection and improve the debugging process.</span></span> <span data-ttu-id="7872b-206">Die-Funktion ist flexibel genug, um in jedem C++ basierten Projekt verwendet zu werden, und sollte als Teil des Stabilitäts Prozesses eines beliebigen Projekts betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="7872b-206">The function is flexible enough to be used in any C++-based project and should be considered part of any project's stability process.</span></span>

 

 