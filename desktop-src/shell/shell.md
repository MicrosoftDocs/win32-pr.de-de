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
ms.openlocfilehash: d31adcbf5a12d699750029c15a308ef73f4d8c03
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467227"
---
# <a name="shell-object"></a>Shellobjekt

Stellt die Objekte in der Shell dar. Methoden werden bereitgestellt, um die Shell zu steuern und Befehle in der Shell auszuführen. Es gibt auch Methoden, um andere Shell-bezogene Objekte zu erhalten.

## <a name="members"></a>Member

Das **Shell-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Shell-Objekt** verfügt über diese Methoden.




| Methode | BESCHREIBUNG | 
|--------|-------------|
| <a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a> | Fügt der Liste der zuletzt verwendeten Dateien (MRU) eine Datei hinzu.<br /> | 
| <a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a> | Erstellt ein Dialogfeld, in dem der Benutzer einen Ordner auswählen und dann das Ordnerobjekt des ausgewählten <a href="folder.md"><strong>Ordners zurückgibt.</strong></a><br /> | 
| <a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a> | Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und beenden kann.<br /> | 
| <a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a> | Kaskadiert alle Fenster auf dem Desktop. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen <strong>von Cascade Windows.</strong><br /> | 
| <a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a> | Führt die angegebene Systemsteuerung (*.cpl) aus. Wenn die Anwendung bereits geöffnet ist, wird die ausgeführte Instanz aktiviert. <br /><blockquote><p>[!Note]<br />Ab Windows Vista sind die Systemsteuerung Shell-Elemente und können nicht mit dieser Funktion geöffnet werden. Um diese anwendungen Systemsteuerung öffnen, übergeben Sie den kanonischen Namen an control.exe. Beispiel:</p><pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre></blockquote><br /> | 
| <a href="shell-ejectpc.md"><strong>EjectPC</strong></a> | Wirft den Computer aus seiner Andockstation. Dies entspricht dem Klicken auf das <strong>Startmenü</strong> und dem Auswählen von <strong>Eject PC</strong>, wenn Ihr Computer diesen Befehl unterstützt.<br /> | 
| <a href="shell-explore.md"><strong>Erkunden</strong></a> | Öffnet einen angegebenen Ordner in einem Windows Explorer-Fenster.<br /> | 
| <a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a> | Ruft den Wert für eine angegebene Internet Explorer ab.<br /> | 
| <a href="shell-filerun.md"><strong>FileRun</strong></a> | Zeigt dem <strong>Benutzer das</strong> Dialogfeld Ausführen an. Diese Methode hat die gleiche Wirkung wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen <strong>von Ausführen.</strong><br /> | 
| <a href="shell-findcomputer.md"><strong>FindComputer</strong></a> | Zeigt das <strong>Dialogfeld Suchergebnisse: Computer</strong> an. Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.<br /> | 
| <a href="shell-findfiles.md"><strong>FindFiles</strong></a> | Zeigt das <strong>Dialogfeld Suchen: Alle Dateien</strong> an. Dies entspricht dem Klicken auf das <strong>Startmenü</strong> und dem anschließenden Auswählen von Suchen <strong>(oder</strong> der entsprechenden Option unter Systemen vor Windows XP).<br /> | 
| <a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a> | Zeigt das <strong>Dialogfeld Drucker suchen</strong> an.<br /> | 
| <a href="/windows/desktop/shell/shell-getsetting"><strong>Getsetting</strong></a> | Ruft eine globale Shelleinstellung ab.<br /> | 
| <a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a> | Ruft Systeminformationen ab.<br /> | 
| <a href="shell-help.md"><strong>Hilfe</strong></a> | Zeigt die Windows Hilfe- und Supportcenter. Diese Methode hat die gleiche Wirkung wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen <strong>von Hilfe und Support.</strong><br /> | 
| <a href="/windows/desktop/shell/shell-isrestricted"><strong>Isrestricted</strong></a> | Ruft die Einschränkungseinstellung einer Gruppe aus der Registrierung ab.<br /> | 
| <a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a> | Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.<br /> | 
| <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> | Minimiert alle Fenster auf dem Desktop. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die <strong></strong> Taskleiste und das Auswählen von Alle <strong>Windows</strong> auf älteren Systemen minimieren oder auf das Symbol Desktop anzeigen im Schnellstart-Bereich der Taskleiste in Windows 2000 oder Windows XP.<br /> | 
| <a href="shell-namespace.md"><strong>Namespace</strong></a> | Erstellt ein <a href="folder.md"><strong>Folder-Objekt für</strong></a> den angegebenen Ordner und gibt es zurück.<br /> | 
| <a href="shell-open.md"><strong>Öffnen</strong></a> | Öffnet den angegebenen Ordner.<br /> | 
| <a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a> | Aktualisiert den Inhalt des <strong>Startmenüs.</strong> Wird nur mit Systemen vor Windows XP verwendet.<br /> | 
| <a href="shell-searchcommand.md"><strong>SearchCommand</strong></a> | Zeigt den Bereich Apps-Suche an.<br /> | 
| <a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a> | Startet einen benannten Dienst.<br /> | 
| <a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a> | Beendet einen benannten Dienst.<br /> | 
| <a href="shell-settime.md"><strong>Settime</strong></a> | Zeigt das <strong>Dialogfeld Datums- und Uhrzeiteigenschaften</strong> an. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen <strong>von Datum/Uhrzeit anpassen.</strong><br /> | 
| <a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a> | Führt einen angegebenen Vorgang für eine angegebene Datei aus.<br /> | 
| <a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a> | Zeigt eine Browserleiste an.<br /> | 
| <a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a> | Zeigt das <strong>Dialogfeld Herunterfahren Windows</strong> an. Dies ist identisch mit dem Klicken auf das <strong>Startmenü</strong> und dem Auswählen <strong>von Herunterfahren.</strong><br /> | 
| <a href="shell-suspend.md"><strong>Angehalten</strong></a> | Td | 
| <a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a> | Kacheln aller Fenster auf dem Desktop horizontal. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Windows horizontal</strong>.<br /> | 
| <a href="shell-tilevertically.md"><strong>TileVertically</strong></a> | Kacheln aller Fenster auf dem Desktop vertikal. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Windows Vertikal.</strong><br /> | 
| <a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a> | Zeigt den Desktop an oder blendet den Desktop aus.<br /> | 
| <a href="shell-trayproperties.md"><strong>TrayProperties</strong></a> | Zeigt das <strong>Dialogfeld Taskleiste und Eigenschaften des Startmenüs</strong> an. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Eigenschaften.</strong><br /> | 
| <a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a> | Stellt alle Desktopfenster in dem Zustand wieder her, in dem sie sich vor dem letzten <a href="shell-minimizeall.md"><strong>MinimizeAll-Befehl</strong></a> befanden. Diese Methode hat den gleichen Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Rückgängig minimieren Alle Windows</strong> auf älteren Systemen oder ein zweites Klicken auf das Symbol Desktop <strong>anzeigen</strong> im Schnellstart Bereich der Taskleiste in Windows 2000 oder Windows XP.<br /> | 
| <a href="shell-windows.md"><strong>Windows</strong></a> | Erstellt ein <a href="shellwindows.md"><strong>ShellWindows-Objekt</strong></a> und gibt es zurück. Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.<br /> | 
| <a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a> | Zeigt das Dialogfeld <strong>Windows-Sicherheit</strong> an.<br /> | 
| <a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a> | Zeigt die geöffneten Fenster in einem 3D-Stapel an, den Sie durchlaufen können.<br /> | 




 

### <a name="properties"></a>Eigenschaften

Das **Shell-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp          | BESCHREIBUNG                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Application**](shell-application.md)<br/> | Schreibgeschützt<br/> | Enthält das Application-Objekt des Objekts.<br/>                        |
| [**Parent**](shell-parent.md)<br/>           | Schreibgeschützt<br/> | Ruft ein -Objekt ab, das das übergeordnete Element des aktuellen -Objekts darstellt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 
