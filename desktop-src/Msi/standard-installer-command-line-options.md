---
<span data-ttu-id="037e6-101">Beschreibung: das ausführbare Programm zum Interpretieren von Paketen und zum Installieren von Produkten ist Msiexec.exe. Beachten Sie, dass msiexec bei der Rückgabe auch eine Fehlerstufe festlegt, die System Fehler Codes entspricht.</span><span class="sxs-lookup"><span data-stu-id="037e6-101">description: The executable program that interprets packages and installs products is Msiexec.exe.Note  Msiexec also sets an error level on return that corresponds to System Error Codes.</span></span> <span data-ttu-id="037e6-102">In der folgenden Tabelle sind die standardmäßigen Befehlszeilenoptionen für dieses Programm aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="037e6-102">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="037e6-103">Befehlszeilenoptionen Unterscheidung nach Groß-/Kleinschreibung. Windows Installer 2,0: die in diesem Thema identifizierten Befehlszeilenoptionen sind ab Windows Installer 3,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="037e6-103">Command-line options are case insensitive.Windows Installer 2.0:  The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="037e6-104">Die Windows Installer Command-Line Optionen sind in Windows Installer&\# 160; 3.0 und früheren Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="037e6-104">The Windows Installer Command-Line Options are available with Windows Installer&\#160;3.0 and earlier versions.</span></span>
<span data-ttu-id="037e6-105">ms. assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e Title: Standard-Installer Command-Line Optionen ms. Topic: article ms. Date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="037e6-105">ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e title: Standard Installer Command-Line Options ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="standard-installer-command-line-options"></a><span data-ttu-id="037e6-106">Standard Installations Command-Line Optionen</span><span class="sxs-lookup"><span data-stu-id="037e6-106">Standard Installer Command-Line Options</span></span>

<span data-ttu-id="037e6-107">Das ausführbare Programm, das Pakete interpretiert und Produkte installiert, ist Msiexec.exe.</span><span class="sxs-lookup"><span data-stu-id="037e6-107">The executable program that interprets packages and installs products is Msiexec.exe.</span></span>

> [!Note]  
> <span data-ttu-id="037e6-108">Msiexec legt außerdem eine Fehlerstufe für die Rückgabe fest, die [System Fehler Codes](../debug/system-error-codes.md)entspricht.</span><span class="sxs-lookup"><span data-stu-id="037e6-108">Msiexec also sets an error level on return that corresponds to [System Error Codes](../debug/system-error-codes.md).</span></span>

 

<span data-ttu-id="037e6-109">In der folgenden Tabelle sind die standardmäßigen Befehlszeilenoptionen für dieses Programm aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="037e6-109">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="037e6-110">Befehlszeilenoptionen Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="037e6-110">Command-line options are case insensitive.</span></span>

<span data-ttu-id="037e6-111">**Windows Installer 2,0:** Die Befehlszeilenoptionen, die in diesem Thema identifiziert werden, sind ab Windows Installer 3,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="037e6-111">**Windows Installer 2.0:** The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="037e6-112">Die Windows Installer [Befehlszeilenoptionen](command-line-options.md) sind in Windows Installer 3,0 und früheren Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="037e6-112">The Windows Installer [Command-Line Options](command-line-options.md) are available with Windows Installer 3.0 and earlier versions.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="037e6-113">Option</span><span class="sxs-lookup"><span data-stu-id="037e6-113">Option</span></span></th>
<th><span data-ttu-id="037e6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="037e6-114">Parameters</span></span></th>
<th><span data-ttu-id="037e6-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="037e6-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="037e6-116"><strong>/help</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-116"><strong>/help</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="037e6-117">Hilfe und Quick Reference-Option.</span><span class="sxs-lookup"><span data-stu-id="037e6-117">Help and quick reference option.</span></span> <span data-ttu-id="037e6-118">Zeigt die korrekte Verwendung des Setup-Befehls einschließlich einer Liste aller Switches und des Verhaltens an.</span><span class="sxs-lookup"><span data-stu-id="037e6-118">Displays the correct usage of the setup command including a list of all switches and behavior.</span></span> <span data-ttu-id="037e6-119">Die Beschreibung der Verwendung kann in der Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="037e6-119">The description of usage can be displayed in the user interface.</span></span> <span data-ttu-id="037e6-120">Die falsche Verwendung einer beliebigen Option ruft diese Hilfe Option auf.</span><span class="sxs-lookup"><span data-stu-id="037e6-120">Incorrect use of any option invokes this help option.</span></span><br/> <span data-ttu-id="037e6-121">Beispiel: <strong>msiexec/Help</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-121">Example: <strong>msiexec /help</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="037e6-122">Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/?</strong>.</span><span class="sxs-lookup"><span data-stu-id="037e6-122">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/?</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="037e6-123"><strong>/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-123"><strong>/quiet</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="037e6-124">Option zur stillen Anzeige.</span><span class="sxs-lookup"><span data-stu-id="037e6-124">Quiet display option.</span></span> <span data-ttu-id="037e6-125">Das Installationsprogramm führt eine Installation aus, ohne eine Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="037e6-125">The installer runs an installation without displaying a user interface.</span></span> <span data-ttu-id="037e6-126">Dem Benutzer werden keine Eingabe Aufforderungen, Meldungen oder Dialogfelder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="037e6-126">No prompts, messages, or dialog boxes are displayed to the user.</span></span> <span data-ttu-id="037e6-127">Der Benutzer kann die Installation nicht abbrechen.</span><span class="sxs-lookup"><span data-stu-id="037e6-127">The user cannot cancel the installation.</span></span> <span data-ttu-id="037e6-128">Verwenden Sie die <strong>/norestart</strong> -oder <strong>/forcerestart</strong> -Standard Befehlszeilenoptionen, um Neustarts zu steuern.</span><span class="sxs-lookup"><span data-stu-id="037e6-128">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="037e6-129">Wenn keine Neustart Optionen angegeben werden, wird der Computer vom Installer bei Bedarf neu gestartet, ohne dass dem Benutzer eine Eingabeaufforderung oder eine Warnung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="037e6-129">If no reboot options are specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span><br/> <span data-ttu-id="037e6-130">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="037e6-130">Examples:</span></span> <br/> <span data-ttu-id="037e6-131"><strong>msiexec/Package Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-131"><strong>msiexec /package Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="037e6-132"><strong>Msiexec/Uninstall Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-132"><strong>Msiexec /uninstall Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="037e6-133"><strong>Msiexec/Update msipatch. msp/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-133"><strong>Msiexec /update msipatch.msp /quiet</strong></span></span><br/> <span data-ttu-id="037e6-134"><strong>Msiexec/Uninstall msipatch. msp/Package Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-134"><strong>Msiexec /uninstall msipatch.msp /package Application.msi / quiet</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="037e6-135">Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/QN</strong>.</span><span class="sxs-lookup"><span data-stu-id="037e6-135">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qn</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="037e6-136"><strong>/passive</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-136"><strong>/passive</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="037e6-137">Passive Anzeigeoption.</span><span class="sxs-lookup"><span data-stu-id="037e6-137">Passive display option.</span></span> <span data-ttu-id="037e6-138">Das Installationsprogramm zeigt dem Benutzer eine Statusanzeige an, die anzeigt, dass eine Installation ausgeführt wird, dem Benutzer jedoch keine Eingabe Aufforderungen oder Fehlermeldungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="037e6-138">The installer displays a progress bar to the user that indicates that an installation is in progress but no prompts or error messages are displayed to the user.</span></span> <span data-ttu-id="037e6-139">Der Benutzer kann die Installation nicht abbrechen.</span><span class="sxs-lookup"><span data-stu-id="037e6-139">The user cannot cancel the installation.</span></span> <span data-ttu-id="037e6-140">Verwenden Sie die <strong>/norestart</strong> -oder <strong>/forcerestart</strong> -Standard Befehlszeilenoptionen, um Neustarts zu steuern.</span><span class="sxs-lookup"><span data-stu-id="037e6-140">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="037e6-141">Wenn keine Neustart Option angegeben ist, wird der Computer vom Installer bei Bedarf neu gestartet, ohne dass dem Benutzer eine Eingabeaufforderung oder eine Warnung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="037e6-141">If no reboot option is specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span> <br/> <span data-ttu-id="037e6-142">Beispiel: <strong>msiexec/Package Application.msi/passive</strong> </span><span class="sxs-lookup"><span data-stu-id="037e6-142">Example: <strong>msiexec /package Application.msi /passive</strong> </span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="037e6-143">Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/qb!-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>= S wird in der Befehlszeile festgelegt.</span><span class="sxs-lookup"><span data-stu-id="037e6-143">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qb!-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>=S set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="037e6-144"><strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-144"><strong>/norestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="037e6-145">Option nie neu starten.</span><span class="sxs-lookup"><span data-stu-id="037e6-145">Never restart option.</span></span> <span data-ttu-id="037e6-146">Das Installationsprogramm startet den Computer nach der Installation nie neu.</span><span class="sxs-lookup"><span data-stu-id="037e6-146">The installer never restarts the computer after the installation.</span></span><br/> <span data-ttu-id="037e6-147">Beispiel: msiexec/Package Application.msi <strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-147">Example: msiexec /package Application.msi <strong>/norestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="037e6-148">In der entsprechenden Windows Installer Befehlszeile ist <a href="reboot.md"><strong>Reboot</strong></a>= reallyunterdrückung in der Befehlszeile festgelegt.</span><span class="sxs-lookup"><span data-stu-id="037e6-148">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="037e6-149"><strong>/forcerestart</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-149"><strong>/forcerestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="037e6-150">Option "immer neu starten".</span><span class="sxs-lookup"><span data-stu-id="037e6-150">Always restart option.</span></span> <span data-ttu-id="037e6-151">Das Installationsprogramm startet den Computer nach jeder Installation immer neu.</span><span class="sxs-lookup"><span data-stu-id="037e6-151">The installer always restarts the computer after every installation.</span></span><br/> <span data-ttu-id="037e6-152">Beispiel: msiexec/Package Application.msi <strong>/forcerestart</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-152">Example: msiexec /package Application.msi <strong>/forcerestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="037e6-153">In der entsprechenden Windows Installer Befehlszeile ist <a href="reboot.md"><strong>Reboot</strong></a>= Force in der Befehlszeile festgelegt.</span><span class="sxs-lookup"><span data-stu-id="037e6-153">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=Force set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="037e6-154"><strong>/promptrestart</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-154"><strong>/promptrestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="037e6-155">Eingabeaufforderung vor Neustarts.</span><span class="sxs-lookup"><span data-stu-id="037e6-155">Prompt before restarting option.</span></span> <span data-ttu-id="037e6-156">Zeigt eine Meldung an, dass ein Neustart erforderlich ist, um die Installation abzuschließen, und fragt den Benutzer, ob das System jetzt neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="037e6-156">Displays a message that a restart is required to complete the installation and asks the user whether to restart the system now.</span></span> <span data-ttu-id="037e6-157">Diese Option kann nicht in Verbindung mit der <strong>/quiet</strong> -Option verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="037e6-157">This option cannot be used together with the <strong>/quiet</strong> option.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="037e6-158">In der entsprechenden Windows Installer Befehlszeile ist <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; in der Befehlszeile festgelegt.</span><span class="sxs-lookup"><span data-stu-id="037e6-158">The equivalent Windows Installer command line has <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a> = &quot;&quot; set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="037e6-159"><strong>/uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-159"><strong>/uninstall</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="037e6-160">Option zum Deinstallieren von Produkten.</span><span class="sxs-lookup"><span data-stu-id="037e6-160">Uninstall product option.</span></span> <span data-ttu-id="037e6-161">Deinstalliert ein Produkt.</span><span class="sxs-lookup"><span data-stu-id="037e6-161">Uninstalls a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="037e6-162">Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/x</strong>.</span><span class="sxs-lookup"><span data-stu-id="037e6-162">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/x</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="037e6-163"><strong>/uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-163"><strong>/uninstall</strong></span></span></td>
<td><span data-ttu-id="037e6-164"><em>/Package <Package.msi | ProductCode> /Uninstall <Update1.msp | PatchGUID1> [; Update2. msp | PatchGUID2]</em></span><span class="sxs-lookup"><span data-stu-id="037e6-164"><em>/package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1>[;Update2.msp | PatchGUID2]</em></span></span></td>
<td><span data-ttu-id="037e6-165">Option zum Deinstallieren von Updates.</span><span class="sxs-lookup"><span data-stu-id="037e6-165">Uninstall update option.</span></span> <span data-ttu-id="037e6-166">Deinstalliert einen Update Patch.</span><span class="sxs-lookup"><span data-stu-id="037e6-166">Uninstalls an update patch.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="037e6-167">Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/I</strong> mit <a href="msipatchremove.md"><strong>msipatchremove</strong></a>= Update1. msp | PatchGUID1[; Update2. msp | PatchGUID2] in der Befehlszeile festgelegt.</span><span class="sxs-lookup"><span data-stu-id="037e6-167">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong> with <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>=Update1.msp | PatchGUID1[;Update2.msp | PatchGUID2] set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="037e6-168"><strong>/Log</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-168"><strong>/log</strong></span></span></td>
<td><em><logfile></em></td>
<td><span data-ttu-id="037e6-169">Log-Option.</span><span class="sxs-lookup"><span data-stu-id="037e6-169">Log option.</span></span> <span data-ttu-id="037e6-170">Schreibt Protokollierungs Informationen in eine Protokolldatei unter dem angegebenen vorhandenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="037e6-170">Writes logging information into a log file at the specified existing path.</span></span> <span data-ttu-id="037e6-171">Der Pfad zum Speicherort der Protokolldatei muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="037e6-171">The path to the log file location must already exist.</span></span> <span data-ttu-id="037e6-172">Das Installationsprogramm erstellt nicht die Verzeichnisstruktur für die Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="037e6-172">The installer does not create the directory structure for the logfile.</span></span><br/> <span data-ttu-id="037e6-173">Die folgenden Informationen werden in das Protokoll eingegeben:</span><span class="sxs-lookup"><span data-stu-id="037e6-173">The following information is entered into the log:</span></span><br/>
<ul>
<li><span data-ttu-id="037e6-174">Statusmeldungen</span><span class="sxs-lookup"><span data-stu-id="037e6-174">Status messages</span></span></li>
<li><span data-ttu-id="037e6-175">Nicht schwerwiegende Warnungen</span><span class="sxs-lookup"><span data-stu-id="037e6-175">Nonfatal warnings</span></span></li>
<li><span data-ttu-id="037e6-176">Alle Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="037e6-176">All error messages</span></span></li>
<li><span data-ttu-id="037e6-177">Starten von Aktionen</span><span class="sxs-lookup"><span data-stu-id="037e6-177">Start up of actions</span></span></li>
<li><span data-ttu-id="037e6-178">Aktions spezifische Datensätze</span><span class="sxs-lookup"><span data-stu-id="037e6-178">Action-specific records</span></span></li>
<li><span data-ttu-id="037e6-179">Benutzer Anforderungen</span><span class="sxs-lookup"><span data-stu-id="037e6-179">User requests</span></span></li>
<li><span data-ttu-id="037e6-180">Anfängliche Benutzeroberflächen Parameter</span><span class="sxs-lookup"><span data-stu-id="037e6-180">Initial UI parameters</span></span></li>
<li><span data-ttu-id="037e6-181">Nicht genügend Arbeitsspeicher oder schwerwiegende Beendigungs Informationen</span><span class="sxs-lookup"><span data-stu-id="037e6-181">Out-of-memory or fatal exit information</span></span></li>
<li><span data-ttu-id="037e6-182">Nicht genügend Speicherplatz Nachrichten</span><span class="sxs-lookup"><span data-stu-id="037e6-182">Out-of-disk-space messages</span></span></li>
<li><span data-ttu-id="037e6-183">Terminal Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="037e6-183">Terminal properties</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="037e6-184">Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/L \*</strong>.</span><span class="sxs-lookup"><span data-stu-id="037e6-184">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/L\*</strong>.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="037e6-185">Weitere Informationen zu allen Methoden, die zum Festlegen des Protokollierungs Modus verfügbar sind, finden Sie unter <a href="normal-logging.md">normale Protokollierung</a> im Abschnitt <a href="windows-installer-logging.md">Windows Installer Protokollierung</a> .</span><span class="sxs-lookup"><span data-stu-id="037e6-185">For more information about all the methods that are available for setting the logging mode, see <a href="normal-logging.md">Normal Logging</a> in the <a href="windows-installer-logging.md">Windows Installer Logging</a> section.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="037e6-186"><strong>/Package</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-186"><strong>/package</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="037e6-187">Option zum Installieren von Produkten.</span><span class="sxs-lookup"><span data-stu-id="037e6-187">Install product option.</span></span> <span data-ttu-id="037e6-188">Installiert oder konfiguriert ein Produkt.</span><span class="sxs-lookup"><span data-stu-id="037e6-188">Installs or configures a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="037e6-189">Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/I</strong>.</span><span class="sxs-lookup"><span data-stu-id="037e6-189">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="037e6-190"><strong>/Update</strong></span><span class="sxs-lookup"><span data-stu-id="037e6-190"><strong>/update</strong></span></span></td>
<td><span data-ttu-id="037e6-191"><em><Update1.msp>[; Update2. msp]</em></span><span class="sxs-lookup"><span data-stu-id="037e6-191"><em><Update1.msp>[;Update2.msp]</em></span></span></td>
<td><span data-ttu-id="037e6-192">Option zum Installieren von Patches.</span><span class="sxs-lookup"><span data-stu-id="037e6-192">Install patches option.</span></span> <span data-ttu-id="037e6-193">Installiert ein oder mehrere Patches.</span><span class="sxs-lookup"><span data-stu-id="037e6-193">Installs one or multiple patches.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="037e6-194">Die entsprechende Windows Installer Befehlszeile enthält <a href="patch.md"><strong>Patch</strong></a> = [msipatch. msp] <; PatchGuid2> in der Befehlszeile festgelegt.</span><span class="sxs-lookup"><span data-stu-id="037e6-194">The equivalent Windows Installer command line has <a href="patch.md"><strong>PATCH</strong></a> = [msipatch.msp]<;PatchGuid2> set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
