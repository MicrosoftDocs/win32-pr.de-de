---
description: Stellt die Objekte in der Shell dar. Methoden werden bereitgestellt, um die Shell zu steuern und Befehle in der Shell auszuführen. Es gibt auch Methoden, um andere Shell-bezogene Objekte zu erhalten.
title: 'Shellobjekt (Shldisp.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 75fc151e-5b9e-476b-b4e5-b848917357a8
ms.openlocfilehash: 55f8062b71e553ec5ceefa413b45f439874744b8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841761"
---
# <a name="shell-object"></a>Shellobjekt

Stellt die Objekte in der Shell dar. Methoden werden bereitgestellt, um die Shell zu steuern und Befehle in der Shell auszuführen. Es gibt auch Methoden, um andere Shell-bezogene Objekte zu erhalten.

## <a name="members"></a>Member

Das **Shell-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Shell-Objekt** verfügt über diese Methoden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Methode</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></td>
<td style="text-align: left;">Fügt der Liste der zuletzt verwendeten Dateien (MRU) eine Datei hinzu.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">Erstellt ein Dialogfeld, in dem der Benutzer einen Ordner auswählen und dann das Ordnerobjekt des ausgewählten <a href="folder.md"><strong>Ordners zurückgibt.</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></td>
<td style="text-align: left;">Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und beenden kann.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">Kaskadiert alle Fenster auf dem Desktop. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Cascade Windows</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Führt die angegebene Systemsteuerung (*.cpl)-Anwendung aus. Wenn die Anwendung bereits geöffnet ist, wird die ausgeführte Instanz aktiviert. <br/>
<blockquote>
<p>[!Note]<br />
Ab Windows Vista sind die meisten Systemsteuerung Anwendungen Shell-Elemente und können nicht mit dieser Funktion geöffnet werden. Um diese Systemsteuerung Anwendungen zu öffnen, übergeben Sie den kanonischen Namen an control.exe. Zum Beispiel:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">Wirft den Computer von seiner Andockstation aus. Dies entspricht dem Klicken auf das <strong>Startmenü</strong> und der Auswahl von <strong>PC auswerfen,</strong>wenn Ihr Computer diesen Befehl unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-explore.md"><strong>Erkunden</strong></a></td>
<td style="text-align: left;">Öffnet einen angegebenen Ordner in einem Windows-Explorer Fenster.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></td>
<td style="text-align: left;">Ruft den Wert für eine angegebene Internet Explorer Richtlinie ab.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Ausführen</strong> für den Benutzer an. Diese Methode hat die gleiche Auswirkung wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen <strong>von Ausführen.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Suchergebnisse: Computer</strong> an. Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Suchen: Alle Dateien</strong> an. Dies entspricht dem Klicken auf das <strong>Startmenü</strong> und der anschließenden Auswahl von <strong>Suchen</strong> (oder der entsprechenden Entsprechung unter Systemen vor Windows XP).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Drucker suchen</strong> an.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsetting"><strong>Getsetting</strong></a></td>
<td style="text-align: left;">Ruft eine globale Shelleinstellung ab.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></td>
<td style="text-align: left;">Ruft Systeminformationen ab.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-help.md"><strong>Hilfe</strong></a></td>
<td style="text-align: left;">Zeigt die Windows-Hilfe- und Supportcenter. Diese Methode hat die gleiche Wirkung wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen <strong>von Hilfe und Support.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isrestricted"><strong>Isrestricted</strong></a></td>
<td style="text-align: left;">Ruft die Einschränkungseinstellung einer Gruppe aus der Registrierung ab.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></td>
<td style="text-align: left;">Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">Minimiert alle Fenster auf dem Desktop. Diese Methode hat die gleiche Wirkung wie das Klicken <strong></strong> mit der rechten Maustaste auf die Taskleiste und das Auswählen von Alle Fenster auf älteren Systemen minimieren oder auf das Symbol <strong>Desktop</strong> anzeigen im Schnellstart-Bereich der Taskleiste in Windows 2000 oder Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-namespace.md"><strong>Namespace</strong></a></td>
<td style="text-align: left;">Erstellt ein <a href="folder.md"><strong>Folder-Objekt für</strong></a> den angegebenen Ordner und gibt es zurück.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-open.md"><strong>Öffnen</strong></a></td>
<td style="text-align: left;">Öffnet den angegebenen Ordner.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Aktualisiert den Inhalt des <strong>Startmenüs.</strong> Wird nur mit Systemen vor Windows XP verwendet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></td>
<td style="text-align: left;">Zeigt den Bereich Apps-Suche an.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></td>
<td style="text-align: left;">Startet einen benannten Dienst.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></td>
<td style="text-align: left;">Beendet einen benannten Dienst.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-settime.md"><strong>Settime</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Datums- und Uhrzeiteigenschaften</strong> an. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Uhr im Taskleistenstatusbereich und das Auswählen <strong>von Datum/Uhrzeit anpassen.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></td>
<td style="text-align: left;">Führt einen angegebenen Vorgang für eine angegebene Datei aus.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></td>
<td style="text-align: left;">Zeigt eine Browserleiste an.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Windows herunterfahren</strong> an. Dies entspricht dem Klicken auf das <strong>Menü Start</strong> und der Auswahl von <strong>Herunterfahren.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-suspend.md"><strong>Auszusetzen</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Kachelt alle Fenster auf dem Desktop horizontal. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Fenster horizontal kacheln.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Kacheln aller Fenster auf dem Desktop vertikal. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen <strong>von Vertikales Kachelfenster.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></td>
<td style="text-align: left;">Zeigt den Desktop an oder blendet den Desktop aus.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></td>
<td style="text-align: left;">Zeigt das <strong>Dialogfeld Taskleiste und Eigenschaften des Startmenüs</strong> an. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Eigenschaften.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Stellt alle Desktopfenster in dem Zustand wieder wieder auf, den sie vor dem letzten <a href="shell-minimizeall.md"><strong>MinimizeAll-Befehl hatten.</strong></a> Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Alle</strong> Fenster auf älteren Systemen minimieren oder ein zweites Klicken auf das Symbol <strong>Desktop</strong> anzeigen im Schnellstart-Bereich der Taskleiste in Windows 2000 oder Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Erstellt ein <a href="shellwindows.md"><strong>ShellWindows-Objekt und gibt es</strong></a> zurück. Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></td>
<td style="text-align: left;">Zeigt das <strong>Windows-Sicherheit</strong> An.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></td>
<td style="text-align: left;">Zeigt Ihre geöffneten Fenster in einem 3D-Stapel an, den Sie durchblättern können.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Eigenschaften

Das **Shell-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp          | BESCHREIBUNG                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Application**](shell-application.md)<br/> | Schreibgeschützt<br/> | Enthält das Application-Objekt des -Objekts.<br/>                        |
| [**Parent**](shell-parent.md)<br/>           | Schreibgeschützt<br/> | Ruft ein -Objekt ab, das das übergeordnete Element des aktuellen -Objekts darstellt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 
