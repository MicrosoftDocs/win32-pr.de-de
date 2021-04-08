---
title: Die accchecker-Konsole
description: Die accchecker-Konsole (AccCheckConsole.exe) ist ein Befehlszeilen Tool zum Überprüfen der Barrierefreiheits Implementierung der Benutzeroberfläche Ihrer Anwendung.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- Accchecker-Konsole
- Accchecker-Befehlszeilen Tool
- Befehlszeile, Zugriffs Prüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef010b2079d364c43bf2a6e47b0e3b0f24bb37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855556"
---
# <a name="the-accchecker-console"></a><span data-ttu-id="7fc49-106">Die accchecker-Konsole</span><span class="sxs-lookup"><span data-stu-id="7fc49-106">The AccChecker Console</span></span>

<span data-ttu-id="7fc49-107">Die accchecker-Konsole (AccCheckConsole.exe) ist ein Befehlszeilen Tool zum Überprüfen der Barrierefreiheits Implementierung der Benutzeroberfläche Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7fc49-107">AccChecker Console (AccCheckConsole.exe) is a command-line tool for verifying the accessibility implementation of your application's UI.</span></span> <span data-ttu-id="7fc49-108">Die Befehlszeile akzeptiert eine Vielzahl von Eingaben (z. b. HWND, Fenstertitel und Überprüfungs Routine) und liefert einen Exitcode, der der Anzahl der Fehlerprotokolle entspricht.</span><span class="sxs-lookup"><span data-stu-id="7fc49-108">The command-line accepts a variety of inputs (such as HWND, window title, and verification routine) and supplies an exit code that corresponds to the error log count.</span></span>

-   [<span data-ttu-id="7fc49-109">Befehlszeilen Syntax</span><span class="sxs-lookup"><span data-stu-id="7fc49-109">Command-line Syntax</span></span>](#command-line-syntax)
-   [<span data-ttu-id="7fc49-110">Befehlszeilen-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="7fc49-110">Command-line Error Codes</span></span>](#command-line-error-codes)
-   [<span data-ttu-id="7fc49-111">Befehlszeilen Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fc49-111">Command-line Examples</span></span>](#command-line-examples)
-   [<span data-ttu-id="7fc49-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7fc49-112">Related topics</span></span>](#related-topics)

![Befehlszeilen Tool der accchecker-Konsole](images/accchecker-console.png)

## <a name="command-line-syntax"></a><span data-ttu-id="7fc49-114">Befehlszeilensyntax</span><span class="sxs-lookup"><span data-stu-id="7fc49-114">Command-line Syntax</span></span>

<span data-ttu-id="7fc49-115">Die accchecker-Konsole weist die folgende Befehlszeilen Syntax auf.</span><span class="sxs-lookup"><span data-stu-id="7fc49-115">AccChecker Console has the following command-line syntax.</span></span>

<span data-ttu-id="7fc49-116">**Acccheckconsole \[ \] -Optionen (-HWND <hwnd> \| -Process <name> ) \[<dlls>\]**</span><span class="sxs-lookup"><span data-stu-id="7fc49-116">**AccCheckConsole \[options\] (-hwnd <hwnd> \| -process <name>) \[<dlls>\]**</span></span>

<span data-ttu-id="7fc49-117">Die Befehlszeilenoptionen lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="7fc49-117">The command-line options are as follows.</span></span>



| <span data-ttu-id="7fc49-118">Optionen</span><span class="sxs-lookup"><span data-stu-id="7fc49-118">Options</span></span>                                                                                                                                                         | <span data-ttu-id="7fc49-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fc49-119">Description</span></span>                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc49-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-HWND <hwnd></span><span class="sxs-lookup"><span data-stu-id="7fc49-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd <hwnd></span></span><br/>                                                                     | <span data-ttu-id="7fc49-121">Überprüft das Fenster, das über das angegebene Handle (HWND) verfügt.</span><span class="sxs-lookup"><span data-stu-id="7fc49-121">Validates the window that has the specified handle (HWND).</span></span> <span data-ttu-id="7fc49-122">Das Handle kann in einem Hexadezimal-oder Dezimaltrennzeichen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7fc49-122">The handle can be specified in hexidecimal or decimal.</span></span><br/> |
| <span data-ttu-id="7fc49-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-Fenster <title></span><span class="sxs-lookup"><span data-stu-id="7fc49-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-window <title></span></span><br/>                                                            | <span data-ttu-id="7fc49-124">Überprüft das Fenster, das über den angegebenen Titel verfügt.</span><span class="sxs-lookup"><span data-stu-id="7fc49-124">Validates the window that has the specified title.</span></span><br/>                                                                |
| <span data-ttu-id="7fc49-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -Prozess <name></span><span class="sxs-lookup"><span data-stu-id="7fc49-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -process <name></span></span><br/>                       | <span data-ttu-id="7fc49-126">Überprüft das Hauptfenster des Prozesses, der über den angegebenen Namen verfügt.</span><span class="sxs-lookup"><span data-stu-id="7fc49-126">Validates the main window of the process that has the specified name.</span></span><br/>                                             |
| <span data-ttu-id="7fc49-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -Liste</span><span class="sxs-lookup"><span data-stu-id="7fc49-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list</span></span><br/>                                       | <span data-ttu-id="7fc49-128">Listet alle verfügbaren Überprüfungs Routinen auf.</span><span class="sxs-lookup"><span data-stu-id="7fc49-128">Lists all of the available verification routines.</span></span><br/>                                                                 |
| <span data-ttu-id="7fc49-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -Aktivieren <name></span><span class="sxs-lookup"><span data-stu-id="7fc49-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -enable <name></span></span><br/>                          | <span data-ttu-id="7fc49-130">Führt die angegebene Überprüfungs Routine aus.</span><span class="sxs-lookup"><span data-stu-id="7fc49-130">Runs the specified verification routine.</span></span> <span data-ttu-id="7fc49-131">Diese Option kann mehrmals angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7fc49-131">This option can be specified more than once.</span></span><br/>                             |
| <span data-ttu-id="7fc49-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -Deaktivieren <name></span><span class="sxs-lookup"><span data-stu-id="7fc49-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -disable <name></span></span><br/> | <span data-ttu-id="7fc49-133">Führt alle außer der angegebenen Überprüfungs Routine aus.</span><span class="sxs-lookup"><span data-stu-id="7fc49-133">Runs all but the specified verification routine.</span></span> <span data-ttu-id="7fc49-134">Diese Option kann mehrmals angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7fc49-134">This option can be specified more than once.</span></span><br/>                     |
| <span data-ttu-id="7fc49-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -Log (Info \| Warnung \| Err)</span><span class="sxs-lookup"><span data-stu-id="7fc49-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info\|warn\|err)</span></span><br/>                          | <span data-ttu-id="7fc49-136">Die niedrigste Ereignis Bewertung, die protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="7fc49-136">The lowest event rating that will be logged.</span></span><br/>                                                                      |
| <span data-ttu-id="7fc49-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -Logfile <file></span><span class="sxs-lookup"><span data-stu-id="7fc49-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file></span></span><br/>                       | <span data-ttu-id="7fc49-138">Schreibt die Ausgabe in die angegebene Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="7fc49-138">Write the output to the specified log file.</span></span> <span data-ttu-id="7fc49-139">Diese Option kann mehrmals angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7fc49-139">This option can be specified more than once.</span></span><br/>                          |
| <span data-ttu-id="7fc49-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-unterdrücken <file></span><span class="sxs-lookup"><span data-stu-id="7fc49-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suppress <file></span></span><br/>                                                         | <span data-ttu-id="7fc49-141">Verwenden Sie die angegebene XML-Datei, um Fehler zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="7fc49-141">Use the specified XML file to suppress errors.</span></span> <br/>                                                                   |
| <span data-ttu-id="7fc49-142"><span id="-quiet"></span><span id="-QUIET"></span>-Quiet</span><span class="sxs-lookup"><span data-stu-id="7fc49-142"><span id="-quiet"></span><span id="-QUIET"></span>-quiet</span></span><br/>                                                                                             | <span data-ttu-id="7fc49-143">Schreiben Sie die Protokollierungs Ausgabe nicht in stdout.</span><span class="sxs-lookup"><span data-stu-id="7fc49-143">Do not write logging output to stdout.</span></span><br/>                                                                            |
| <span data-ttu-id="7fc49-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-Hilfe</span><span class="sxs-lookup"><span data-stu-id="7fc49-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help</span></span> <br/>                           | <span data-ttu-id="7fc49-145">Zeigt eine schnelle Hilfe an.</span><span class="sxs-lookup"><span data-stu-id="7fc49-145">Displays quick help.</span></span> <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a><span data-ttu-id="7fc49-146">Befehlszeilen-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="7fc49-146">Command-line Error Codes</span></span>

<span data-ttu-id="7fc49-147">Die folgenden Fehlercodes werden von der acccheckconsole bei Verwendung von "Echo% ERRORLEVEL%" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7fc49-147">Following are error codes returned from AccCheckConsole when using "echo %errorlevel%"</span></span>



| <span data-ttu-id="7fc49-148">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="7fc49-148">Error code</span></span>                       | <span data-ttu-id="7fc49-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fc49-149">Description</span></span>                                 |
|----------------------------------|---------------------------------------------|
| <span data-ttu-id="7fc49-150"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="7fc49-150"><span id="0"></span>0</span></span><br/> | <span data-ttu-id="7fc49-151">Keine Fehler und keine Warnungen.</span><span class="sxs-lookup"><span data-stu-id="7fc49-151">No errors and no warnings.</span></span><br/>       |
| <span data-ttu-id="7fc49-152"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="7fc49-152"><span id="1"></span>1</span></span><br/> | <span data-ttu-id="7fc49-153">Die Verwendung der-Anweisung wurde angefordert.</span><span class="sxs-lookup"><span data-stu-id="7fc49-153">Usages statement was requested.</span></span> <br/> |
| <span data-ttu-id="7fc49-154"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="7fc49-154"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="7fc49-155">Fehler und keine Warnungen.</span><span class="sxs-lookup"><span data-stu-id="7fc49-155">Errors and no warnings.</span></span><br/>          |
| <span data-ttu-id="7fc49-156"><span id="3"></span>€</span><span class="sxs-lookup"><span data-stu-id="7fc49-156"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="7fc49-157">Fehler und Warnungen.</span><span class="sxs-lookup"><span data-stu-id="7fc49-157">Errors and warnings.</span></span><br/>             |
| <span data-ttu-id="7fc49-158"><span id="4"></span>4</span><span class="sxs-lookup"><span data-stu-id="7fc49-158"><span id="4"></span>4</span></span><br/> | <span data-ttu-id="7fc49-159">Warnungen, aber keine Fehler.</span><span class="sxs-lookup"><span data-stu-id="7fc49-159">Warnings but no errors.</span></span><br/>          |
| <span data-ttu-id="7fc49-160"><span id="5"></span>5@@</span><span class="sxs-lookup"><span data-stu-id="7fc49-160"><span id="5"></span>5</span></span><br/> | <span data-ttu-id="7fc49-161">Ungültige Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="7fc49-161">Invalid command line.</span></span> <br/>           |



 

## <a name="command-line-examples"></a><span data-ttu-id="7fc49-162">Befehlszeilen Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fc49-162">Command-line Examples</span></span>

<span data-ttu-id="7fc49-163">Im folgenden finden Sie einige Beispiele für die Befehlszeile für die Zugriffs Steuerung.</span><span class="sxs-lookup"><span data-stu-id="7fc49-163">Following are several AccChecker Console command-line examples.</span></span>

-   <span data-ttu-id="7fc49-164">Führt alle Überprüfungen in einem Fenster mit einem angegebenen Namen aus.</span><span class="sxs-lookup"><span data-stu-id="7fc49-164">Run all verifications on a window with a specified name.</span></span>

    <span data-ttu-id="7fc49-165">**Acccheckconsole-Window "unbenannt-Notepad"**</span><span class="sxs-lookup"><span data-stu-id="7fc49-165">**AccCheckConsole -window "Untitled - Notepad"**</span></span>

-   <span data-ttu-id="7fc49-166">Führen Sie eine Teilmenge der Überprüfungen für ein HWND aus, und geben Sie eine Unterdrückungs Datei an.</span><span class="sxs-lookup"><span data-stu-id="7fc49-166">Run a subset of the verifications against an HWND, specifying a suppression file.</span></span>

    <span data-ttu-id="7fc49-167">**Acccheckconsole-HWND 0x00382f-enable checktabp-enable checkname-SUPsuppress.xml**</span><span class="sxs-lookup"><span data-stu-id="7fc49-167">**AccCheckConsole -hwnd 0x00382f00 -enable CheckTabbing -enable CheckName -suppress suppress.xml**</span></span>

-   <span data-ttu-id="7fc49-168">Führt alle Überprüfungen aus einer neuen Überprüfungs-dll aus.</span><span class="sxs-lookup"><span data-stu-id="7fc49-168">Run all verifications from a new verification DLL.</span></span>

    <span data-ttu-id="7fc49-169">**Acccheckconsole-Window "unbenannt-Notepad" VerificationRoutine1.dll**</span><span class="sxs-lookup"><span data-stu-id="7fc49-169">**AccCheckConsole -window "Untitled - Notepad" VerificationRoutine1.dll**</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fc49-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7fc49-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fc49-171">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="7fc49-171">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





