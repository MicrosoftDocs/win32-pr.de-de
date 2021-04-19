---
description: Wilogutl.exe unterstützt die Analyse von Protokolldateien von einer Windows Installer-Installation und zeigt vorgeschlagene Lösungen für Fehler an, die in einer Protokolldatei gefunden werden.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81c3c82299a08fd947fbbecc7afd8a373252b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357128"
---
# <a name="wilogutlexe"></a><span data-ttu-id="c700c-103">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="c700c-103">Wilogutl.exe</span></span>

<span data-ttu-id="c700c-104">Wilogutl.exe unterstützt die Analyse von Protokolldateien von einer Windows Installer-Installation und zeigt vorgeschlagene Lösungen für Fehler an, die in einer Protokolldatei gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c700c-104">Wilogutl.exe assists the analysis of log files from a Windows Installer installation, and it displays suggested solutions to errors that are found in a log file.</span></span>

<span data-ttu-id="c700c-105">Nicht kritische Fehler werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c700c-105">Non-critical errors are not displayed.</span></span> <span data-ttu-id="c700c-106">Wilogutl.exe können im stillen Modus oder mit einer Benutzeroberfläche (UI) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c700c-106">Wilogutl.exe can be run in quiet mode or with a user interface (UI).</span></span> <span data-ttu-id="c700c-107">Das Tool generiert Berichte als Textdateien sowohl in der Benutzeroberfläche als auch in den stillen Modi.</span><span class="sxs-lookup"><span data-stu-id="c700c-107">The tool generates reports as text files in both the UI and quiet modes.</span></span> <span data-ttu-id="c700c-108">Dies funktioniert am besten mit ausführlichen Windows Installer Protokolldateien, funktioniert aber auch mit nicht ausführlichen Protokollen.</span><span class="sxs-lookup"><span data-stu-id="c700c-108">It works best with verbose Windows Installer log files, but also works with non-verbose logs.</span></span> <span data-ttu-id="c700c-109">Weitere Informationen finden Sie unter [Protokollierung](logging.md).</span><span class="sxs-lookup"><span data-stu-id="c700c-109">For more information, see [Logging](logging.md).</span></span>

<span data-ttu-id="c700c-110">Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c700c-110">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c700c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c700c-111">Syntax</span></span>

<span data-ttu-id="c700c-112">\**wilogutl.exe\*\*\*\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span><span class="sxs-lookup"><span data-stu-id="c700c-112">**wilogutl.exe** *\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span></span>

<span data-ttu-id="c700c-113">Sie können die folgenden Befehlszeilen verwenden, um im stillen Modus auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c700c-113">You can use the following command lines to run in quiet mode.</span></span>

<span data-ttu-id="c700c-114">**Wilogutl/q/l** *c: \\ mymsilog. log* **/o** *c \\ OutputDir \\*</span><span class="sxs-lookup"><span data-stu-id="c700c-114">**wilogutl /q /l** *c:\\mymsilog.log* **/o** *c\\outputdir\\*</span></span>

<span data-ttu-id="c700c-115">**Wilogutl/q/l** *c: \\ mymsilog. log*</span><span class="sxs-lookup"><span data-stu-id="c700c-115">**wilogutl /q /l** *c:\\mymsilog.log*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="c700c-116">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="c700c-116">Command-Line Options</span></span>

<span data-ttu-id="c700c-117">Wilogutl.exe verwendet die folgenden Befehlszeilenoptionen ohne Beachtung der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="c700c-117">Wilogutl.exe uses the following case insensitive command-line options.</span></span> <span data-ttu-id="c700c-118">Ein Bindestrich-Trennzeichen kann anstelle eines Schrägstrichs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c700c-118">A dash delimiter can be used in place of a slash.</span></span>



| <span data-ttu-id="c700c-119">Option</span><span class="sxs-lookup"><span data-stu-id="c700c-119">Option</span></span> | <span data-ttu-id="c700c-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c700c-120">Description</span></span>                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c700c-121">none</span><span class="sxs-lookup"><span data-stu-id="c700c-121">none</span></span>   | <span data-ttu-id="c700c-122">Wird im Benutzeroberflächen Modus ausgeführt – ohne Befehlszeilenoptionen.</span><span class="sxs-lookup"><span data-stu-id="c700c-122">Runs in UI mode—without command-line options.</span></span>                                                                                                                                                   |
| <span data-ttu-id="c700c-123">/q</span><span class="sxs-lookup"><span data-stu-id="c700c-123">/q</span></span>     | <span data-ttu-id="c700c-124">Gibt den stillen Modus an.</span><span class="sxs-lookup"><span data-stu-id="c700c-124">Specifies the quiet mode.</span></span> <span data-ttu-id="c700c-125">Wilogutl.exe generiert Berichtsdateien und zeigt keine Benutzeroberfläche an.</span><span class="sxs-lookup"><span data-stu-id="c700c-125">Wilogutl.exe generates report files and does not display a user interface.</span></span>                                                                                            |
| <span data-ttu-id="c700c-126">/l</span><span class="sxs-lookup"><span data-stu-id="c700c-126">/l</span></span>     | <span data-ttu-id="c700c-127">Gibt den Namen der Protokolldatei an, die analysiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c700c-127">Specifies the name of the log file to be analyzed.</span></span> <span data-ttu-id="c700c-128">Diese Option ist erforderlich, wenn Sie den stillen Modus verwenden.</span><span class="sxs-lookup"><span data-stu-id="c700c-128">This option is required when using the quiet mode.</span></span>                                                                                           |
| <span data-ttu-id="c700c-129">/o</span><span class="sxs-lookup"><span data-stu-id="c700c-129">/o</span></span>     | <span data-ttu-id="c700c-130">Gibt das Ausgabeverzeichnis für Berichtsdateien an.</span><span class="sxs-lookup"><span data-stu-id="c700c-130">Specifies the output directory for report files.</span></span> <span data-ttu-id="c700c-131">Dieser Ausgabepfad wird nur verwendet, wenn er im stillen Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c700c-131">This output path is used only when running in quiet mode.</span></span> <span data-ttu-id="c700c-132">Wenn die Option nicht vorhanden ist, werden die Berichte in das Verzeichnis "C: \\ wilogresults" eingefügt.</span><span class="sxs-lookup"><span data-stu-id="c700c-132">If the option is not present, the reports are put in the C:\\WiLogResults directory.</span></span> |



 

<span data-ttu-id="c700c-133">Wenn Sie den Benutzeroberflächen Modus ausführen, werden in Wilogutl.exe die folgenden Dialogfelder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c700c-133">When run in UI mode, Wilogutl.exe displays the following dialog boxes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c700c-134">Name</span><span class="sxs-lookup"><span data-stu-id="c700c-134">Name</span></span></th>
<th><span data-ttu-id="c700c-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c700c-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c700c-136">Windows Installer Verbose Log Analyzer</span><span class="sxs-lookup"><span data-stu-id="c700c-136">Windows Installer Verbose Log Analyzer</span></span></td>
<td><span data-ttu-id="c700c-137">Im Dialogfeld Windows Installer Verbose Log Analyzer können Benutzer eine Protokolldatei für die Analyse auswählen:</span><span class="sxs-lookup"><span data-stu-id="c700c-137">The Windows Installer Verbose Log Analyzer dialog box enables users to select a log file for analysis:</span></span>
<ul>
<li><span data-ttu-id="c700c-138">Die Schaltfläche <strong>Öffnen</strong> öffnet die Datei im Editor.</span><span class="sxs-lookup"><span data-stu-id="c700c-138">The <strong>Open</strong> button opens the file in Notepad.</span></span> <span data-ttu-id="c700c-139">Der Vorschaubereich kann verwendet werden, um zu überprüfen, ob die richtige Protokolldatei ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="c700c-139">The preview area can be used to verify that the correct log file has been selected.</span></span></li>
<li><span data-ttu-id="c700c-140">Mit der Schaltfläche <strong>analysieren</strong> wird die Protokolldatei Analyse gestartet, und das Dialogfeld ausführliche Protokolldatei Ansicht wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c700c-140">The <strong>Analyze</strong> button begins log file analysis and displays the Detailed Log File View dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c700c-141">Ausführliche Protokolldatei Ansicht</span><span class="sxs-lookup"><span data-stu-id="c700c-141">Detailed Log File View</span></span></td>
<td><span data-ttu-id="c700c-142">Im Dialogfeld ausführliche Protokolldatei Ansicht werden protokollierte Fehlerinformationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c700c-142">The Detailed Log File View dialog box displays logged error information.</span></span> <span data-ttu-id="c700c-143">Verwenden Sie die Schaltflächen <strong>zurück</strong> und <strong>weiter</strong> , um durch mehrere Fehler zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="c700c-143">Use the <strong>Back</strong> and <strong>Next</strong> buttons to navigate through multiple errors.</span></span> <span data-ttu-id="c700c-144">Aktivieren Sie das Kontrollkästchen <strong>ignorierte Debugfehler anzeigen</strong> , um nicht kritische Fehler anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c700c-144">To display non-critical errors select the <strong>Show Ignored Debug Errors</strong> check box.</span></span> <span data-ttu-id="c700c-145">Die Installer-Version auf dem Computer, der zum Ausführen der protokollierten Installation verwendet wird, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c700c-145">The installer version on the computer used to run the logged installation is displayed.</span></span> <span data-ttu-id="c700c-146">Wenn die protokollierte Installation mit erweiterten Berechtigungen ausgeführt wurde, ist das Kontrollkästchen <strong>Installation mit erhöhten</strong> rechten aktiviert, und Informationen finden Sie in den Textfeldern Details zu den <strong>Client seitigen</strong> Berechtigungen und <strong>Details zur Server seitigen Berechtigung</strong> .</span><span class="sxs-lookup"><span data-stu-id="c700c-146">If the logged installation was run with elevated permissions, the <strong>Elevated install</strong> check box is selected and information is provided in the <strong>Client Side Privilege Details</strong> and <strong>Server Side Privilege Details</strong> text boxes.</span></span> <span data-ttu-id="c700c-147">Das Dialogfeld ausführliche Protokolldatei Ansicht enthält die folgenden Schaltflächen:</span><span class="sxs-lookup"><span data-stu-id="c700c-147">The Detailed Log File View dialog box contains the following buttons:</span></span><br/>
<ul>
<li><span data-ttu-id="c700c-148"><strong>Zustände</strong> - Zeigt das Dialogfeld Funktions-und Komponenten Zustände an.</span><span class="sxs-lookup"><span data-stu-id="c700c-148"><strong>States</strong> - Show the Feature and Component States dialog box.</span></span></li>
<li><span data-ttu-id="c700c-149"><strong>Eigenschaften</strong> - Zeigen Sie das Dialogfeld Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="c700c-149"><strong>Properties</strong> - Show the Properties dialog box.</span></span></li>
<li><span data-ttu-id="c700c-150"><strong>Richtlinien</strong> - Zeigen Sie das Dialogfeld Richtlinien an.</span><span class="sxs-lookup"><span data-stu-id="c700c-150"><strong>Policies</strong> - Show the Policies dialog box.</span></span></li>
<li><span data-ttu-id="c700c-151"><strong>HTML-Protokoll</strong> - mit Anmerkungen Protokoll als mit Anmerkungen versehene HTML-Datei anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c700c-151"><strong>HTML Annotated Log</strong> - Show log as annotated HTML file.</span></span></li>
<li><span data-ttu-id="c700c-152"><strong>Ergebnisse speichern</strong> - Speichert Berichtsdateien im angegebenen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="c700c-152"><strong>Save Results</strong> - Save report files to specified directory.</span></span></li>
<li><span data-ttu-id="c700c-153"><strong>Hilfe zu</strong> - Fehlermeldungen Hilfe zur Installationsprogramm Fehlermeldung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c700c-153"><strong>Error Message Help</strong> - Show installer error message help.</span></span></li>
<li><span data-ttu-id="c700c-154"><strong>Hilfe</strong> - Anzeigen der Hilfe für Windows Installer Setup Log Analyzer.</span><span class="sxs-lookup"><span data-stu-id="c700c-154"><strong>Help</strong> - Show help for Windows Installer Setup Log Analyzer.</span></span></li>
<li><span data-ttu-id="c700c-155">Vorgehens <strong>Weise beim Lesen einer Protokolldatei</strong> - Zeigen Sie das Hilfedokument für die Protokolldatei an.</span><span class="sxs-lookup"><span data-stu-id="c700c-155"><strong>How to Read a Log File</strong> - Show the log file help document.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c700c-156">Funktions-und Komponenten Zustände</span><span class="sxs-lookup"><span data-stu-id="c700c-156">Feature and Component States</span></span></td>
<td><span data-ttu-id="c700c-157">Im Dialogfeld <strong>Funktions-und Komponenten Zustände</strong> werden die Status der Features und Komponenten angezeigt:</span><span class="sxs-lookup"><span data-stu-id="c700c-157">The <strong>Feature and Component States</strong> dialog box displays the states of features and components:</span></span>
<ul>
<li><span data-ttu-id="c700c-158">In der Spalte <strong>Feature</strong> wird der Name der Funktion im Installationspaket angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c700c-158">The <strong>Feature</strong> column shows the name for the feature in the installation package.</span></span></li>
<li><span data-ttu-id="c700c-159">In der Spalte <strong>Komponente</strong> wird der Name der Komponente im Installationspaket angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c700c-159">The <strong>Component</strong> column shows the name of the component in the installation package.</span></span></li>
<li><span data-ttu-id="c700c-160">In der Spalte <strong>installiert</strong> wird der Zustand oder der Zustand der Komponente am Ende der Installation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c700c-160">The <strong>Installed</strong> column shows the feature or component's state at the end of the installation.</span></span></li>
<li><span data-ttu-id="c700c-161">In der Spalte <strong>Anforderung</strong> wird die Auswahl des Benutzers während der Installation für den Funktions-oder Komponenten Zustand angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c700c-161">The <strong>Request</strong> column shows the user's selection during the installation for the feature or component's state.</span></span></li>
<li><span data-ttu-id="c700c-162">In der Spalte <strong>Aktion</strong> wird die Aktion angezeigt, die vom Installationsprogramm für das Feature oder die Komponente ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c700c-162">The <strong>Action</strong> column shows the action taken by the installer for the feature or component.</span></span></li>
</ul>
<span data-ttu-id="c700c-163">Weitere Informationen finden Sie unter <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> und <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c700c-163">For more information, see <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> and <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c700c-164">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c700c-164">Properties</span></span></td>
<td><span data-ttu-id="c700c-165">Im Dialogfeld Eigenschaften werden Windows Installer <a href="properties.md">Eigenschaften</a> und deren Werte am Ende der Installation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c700c-165">The Properties dialog box shows Windows Installer <a href="properties.md">Properties</a> and their values at the end of the installation.</span></span> <span data-ttu-id="c700c-166">Sie können die Eigenschaften nach Name oder Wert sortieren:</span><span class="sxs-lookup"><span data-stu-id="c700c-166">You can sort the properties by name or by value:</span></span>
<ul>
<li><span data-ttu-id="c700c-167">Auf der Registerkarte <strong>Client</strong> werden Eigenschaften und Werte während des Client seitigen Teils der Installation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c700c-167">The <strong>Client</strong> tab shows properties and values during the client side portion of the installation.</span></span></li>
<li><span data-ttu-id="c700c-168">Die Registerkarte <strong>Server</strong> zeigt Eigenschaften und Werte während des Server Teils der Installation an.</span><span class="sxs-lookup"><span data-stu-id="c700c-168">The <strong>Server</strong> tab shows properties and values during the server portion of the installation.</span></span></li>
<li><span data-ttu-id="c700c-169">Die <strong>Registerkarte</strong> "neu" zeigt die Eigenschaften und Werte aller <a href="concurrent-installations.md">gleichzeitigen Installationen</a>an.</span><span class="sxs-lookup"><span data-stu-id="c700c-169">The <strong>Nested</strong> tab shows the properties and values of any <a href="concurrent-installations.md">Concurrent Installations</a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c700c-170">Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c700c-170">Policies</span></span></td>
<td><span data-ttu-id="c700c-171">Im Dialogfeld Richtlinien wird die <a href="system-policy.md">System Richtlinie</a> angezeigt, die nach der Installation festgelegt wurde:</span><span class="sxs-lookup"><span data-stu-id="c700c-171">The Policies dialog box displays the <a href="system-policy.md">System Policy</a> set after the installation:</span></span>
<ul>
<li><span data-ttu-id="c700c-172">Der für die Richtlinie festgelegte Wert 0 (null) bedeutet, dass die Richtlinie nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c700c-172">A value of 0 (zero) set for the policy means the policy is not enabled.</span></span></li>
<li><span data-ttu-id="c700c-173">Der Wert 1 (eins) bedeutet, dass die Richtlinie aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c700c-173">A value of 1 (one) means the policy is enabled.</span></span></li>
<li><span data-ttu-id="c700c-174">Der Wert?</span><span class="sxs-lookup"><span data-stu-id="c700c-174">A value of ?</span></span> <span data-ttu-id="c700c-175">(Fragezeichen) bedeutet, dass der Richtlinien Wert nicht im Protokoll aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="c700c-175">(question mark) means the policy value is not recorded in the log.</span></span></li>
</ul>
<span data-ttu-id="c700c-176">Wenn Sie einen Richtlinien Wert benötigen, der nicht im Protokoll angezeigt wird, verwenden Sie Regedit.exe, um die Registrierungsschlüssel auf dem Computer zu überprüfen, der die Installation nicht bestanden hat.</span><span class="sxs-lookup"><span data-stu-id="c700c-176">If you need a policy value that is not in the log, try using Regedit.exe to check the registry keys on the computer failing the installation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="report-files"></a><span data-ttu-id="c700c-177">Berichtsdateien</span><span class="sxs-lookup"><span data-stu-id="c700c-177">Report Files</span></span>

<span data-ttu-id="c700c-178">Wenn Sie im Dialog **Feld ausführliche Protokolldatei Ansicht** eine Analyse im stillen Modus durchführen oder auf die Schaltfläche **Ergebnisse speichern** klicken, generiert das Windows Installer Setup Analyzer-Tool drei Textdateien und eine mit Anmerkungen versehene Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="c700c-178">When performing a quiet mode analysis or clicking the **Save Results** button on the **Detailed Log File View** dialog, the Windows Installer Setup Analyzer tool generates three text files and an HTML annotated log file.</span></span>

<span data-ttu-id="c700c-179">In der folgenden Tabelle sind die Namen und Inhalte der Berichtsdateien aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c700c-179">The following table identifies the names and contents in the report files.</span></span>



| <span data-ttu-id="c700c-180">Name</span><span class="sxs-lookup"><span data-stu-id="c700c-180">Name</span></span>                      | <span data-ttu-id="c700c-181">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c700c-181">Description</span></span>                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c700c-182">Protokoll Dateiname- \_summary.txt</span><span class="sxs-lookup"><span data-stu-id="c700c-182">logfilename\_summary.txt</span></span>  | <span data-ttu-id="c700c-183">Fasst die Protokolldatei zusammen.</span><span class="sxs-lookup"><span data-stu-id="c700c-183">Summarizes the log file.</span></span> <span data-ttu-id="c700c-184">Listet die Informationen auf, die im Dialogfeld ausführliche Protokolldatei Ansicht und der erste Fehler angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c700c-184">Lists the information displayed by the Detailed Log File View dialog box and the first error.</span></span>         |
| <span data-ttu-id="c700c-185">Protokoll Dateiname- \_errors.txt</span><span class="sxs-lookup"><span data-stu-id="c700c-185">logfilename\_errors.txt</span></span>   | <span data-ttu-id="c700c-186">Gibt die Anzahl von Fehlern, die Fehler und die empfohlenen Lösungen an.</span><span class="sxs-lookup"><span data-stu-id="c700c-186">Identifies the number of errors, the errors, and recommended solutions.</span></span> <span data-ttu-id="c700c-187">In dieser Datei werden sowohl kritische als auch nicht kritische Fehler aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c700c-187">This file lists both critical and non-critical errors.</span></span> |
| <span data-ttu-id="c700c-188">Protokoll Dateiname- \_policies.txt</span><span class="sxs-lookup"><span data-stu-id="c700c-188">logfilename\_policies.txt</span></span> | <span data-ttu-id="c700c-189">Identifiziert die Richtlinien Namen und Werte, die am Ende der Installation wie im Dialogfeld Richtlinien festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c700c-189">Identifies the policy names and values set at the end of the installation as in the Policies dialog box.</span></span>                       |
| <span data-ttu-id="c700c-190">Details \_logfilename.htm</span><span class="sxs-lookup"><span data-stu-id="c700c-190">details\_logfilename.htm</span></span>  | <span data-ttu-id="c700c-191">Ein HTML-Protokoll mit Anmerkungen und einer Legende für die Farbcodierung.</span><span class="sxs-lookup"><span data-stu-id="c700c-191">An HTML annotated log with a legend for the color coding.</span></span>                                                                      |



 

## <a name="return-values"></a><span data-ttu-id="c700c-192">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="c700c-192">Return Values</span></span>

<span data-ttu-id="c700c-193">Wenn für Vorgänge im stillen Modus ungültige Befehlszeilenargumente weitergegeben werden, führt Wilogutl.exe keine Aktion aus, und der Prozess gibt einen der Werte in der folgenden Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="c700c-193">If invalid command-line arguments are passed for quiet mode operations, Wilogutl.exe does nothing, and the process returns one of the values in the following table.</span></span>



| <span data-ttu-id="c700c-194">Wert</span><span class="sxs-lookup"><span data-stu-id="c700c-194">Value</span></span> | <span data-ttu-id="c700c-195">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c700c-195">Meaning</span></span>                                                                 |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="c700c-196">1</span><span class="sxs-lookup"><span data-stu-id="c700c-196">1</span></span>     | <span data-ttu-id="c700c-197">Es wurde ein ungültiges Ausgabeverzeichnis angegeben.</span><span class="sxs-lookup"><span data-stu-id="c700c-197">Bad output directory is specified.</span></span>                                      |
| <span data-ttu-id="c700c-198">2</span><span class="sxs-lookup"><span data-stu-id="c700c-198">2</span></span>     | <span data-ttu-id="c700c-199">Es wurde ein ungültiger Protokoll Dateiname angegeben.</span><span class="sxs-lookup"><span data-stu-id="c700c-199">Bad log file name is specified.</span></span>                                         |
| <span data-ttu-id="c700c-200">3</span><span class="sxs-lookup"><span data-stu-id="c700c-200">3</span></span>     | <span data-ttu-id="c700c-201">Der/q wurde erfolgreich, jedoch fehlt der erforderliche Switch/l für den Namen der Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="c700c-201">Passed /q, but is missing the required switch /l for the log file name.</span></span> |
| <span data-ttu-id="c700c-202">4</span><span class="sxs-lookup"><span data-stu-id="c700c-202">4</span></span>     | <span data-ttu-id="c700c-203">Der/l wurde erfolgreich ausgeführt, jedoch fehlt der erforderliche Switch/q für den stillen Modus.</span><span class="sxs-lookup"><span data-stu-id="c700c-203">Passed /l, but is missing the required switch /q for quiet mode.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c700c-204">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c700c-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c700c-205">Veröffentlichte Versionen, Tools und verteilbare Dateien</span><span class="sxs-lookup"><span data-stu-id="c700c-205">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> <dt>

[<span data-ttu-id="c700c-206">Entwicklungs Tools für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c700c-206">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> </dl>

 

 




