---
description: Stellt die-Objekte in der Shell dar. Es werden Methoden bereitgestellt, um die Shell zu steuern und um Befehle in der Shell auszuführen. Es gibt auch Methoden zum Abrufen anderer shellbezogener Objekte.
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
ms.openlocfilehash: 3e891278d98ca2eb51fca11054cba01947e03c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867744"
---
# <a name="shell-object"></a>Shellobjekt

Stellt die-Objekte in der Shell dar. Es werden Methoden bereitgestellt, um die Shell zu steuern und um Befehle in der Shell auszuführen. Es gibt auch Methoden zum Abrufen anderer shellbezogener Objekte.

## <a name="members"></a>Member

Das **Shellobjekt** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Shellobjekt** verfügt über diese Methoden.



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
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-addtorecent"><strong>Addtor</strong></a></td>
<td style="text-align: left;">Fügt der Liste der zuletzt verwendeten (MRU) eine Datei hinzu.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-browseforfolder.md"><strong>Browsorforfolder</strong></a></td>
<td style="text-align: left;">Erstellt ein Dialogfeld, das dem Benutzer ermöglicht, einen Ordner auszuwählen, und gibt dann das <a href="folder.md"><strong>Ordner</strong></a> Objekt des ausgewählten Ordners zurück.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>Canstartstopservice</strong></a></td>
<td style="text-align: left;">Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und Abbrechen kann.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-cascadewindows.md"><strong>Cascade-Fenster</strong></a></td>
<td style="text-align: left;">Alle Fenster auf dem Desktop werden kaskadiert. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und <strong>kaskadierte Fenster</strong>auswählen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Führt die angegebene System Steuerungsanwendung (*. cpl) aus. Wenn die Anwendung bereits geöffnet ist, wird die laufende Instanz aktiviert. <br/>
<blockquote>
<p>[!Note]<br />
Ab Windows Vista sind die meisten System Steuerungsanwendungen shellelemente und können nicht mit dieser Funktion geöffnet werden. Wenn Sie diese System Steuerungsanwendungen öffnen möchten, übergeben Sie den kanonischen Namen an control.exe. Beispiel:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-ejectpc.md"><strong>Ejectpc</strong></a></td>
<td style="text-align: left;">Der Computer wird von seiner Docking Station eingelesen. Dies ist das gleiche wie beim Klicken auf das <strong>Startmenü</strong> und beim Auswählen von <strong>ausgelösten PCs</strong>, wenn Ihr Computer diesen Befehl unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-explore.md"><strong>Erkunden</strong></a></td>
<td style="text-align: left;">Öffnet einen angegebenen Ordner in einem Windows-Explorer-Fenster.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-explorerpolicy.md"><strong>Explorerpolicy</strong></a></td>
<td style="text-align: left;">Ruft den Wert für eine angegebene Internet Explorer-Richtlinie ab.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-filerun.md"><strong>Filerun</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld " <strong>Ausführen</strong> " für den Benutzer an. Diese Methode hat denselben Effekt wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen von <strong>Ausführen</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-findcomputer.md"><strong>Findcomputer</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Suchergebnisse: Computer</strong> an. Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-findfiles.md"><strong>"Findfiles</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>suchen: alle Dateien</strong> an. Dies ist das gleiche wie beim Klicken auf das <strong>Startmenü</strong> und anschließendes Auswählen von <strong>Suchen</strong> (oder der entsprechenden Entsprechung unter Systeme vor Windows XP).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-findprinter"><strong>Findprinter</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Drucker suchen</strong> an.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></td>
<td style="text-align: left;">Ruft eine globale shelleinstellung ab.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>Getsysteminformation</strong></a></td>
<td style="text-align: left;">Ruft Systeminformationen ab.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-help.md"><strong>Hilfe</strong></a></td>
<td style="text-align: left;">Zeigt das Windows-Hilfe-und Support Center an. Diese Methode hat denselben Effekt wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen von <strong>Hilfe und Support</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></td>
<td style="text-align: left;">Ruft die Einschränkungs Einstellung einer Gruppe aus der Registrierung ab.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>Isservicerunning</strong></a></td>
<td style="text-align: left;">Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-minimizeall.md"><strong>Minimizeall</strong></a></td>
<td style="text-align: left;">Minimiert alle Fenster auf dem Desktop. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von "alle Fenster auf älteren Systemen <strong>minimieren</strong> " oder das Klicken auf das Symbol " <strong>Desktop anzeigen</strong> " im Bereich "Schnellstart" der Taskleiste in Windows 2000 oder Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-namespace.md"><strong>Namespace</strong></a></td>
<td style="text-align: left;">Erstellt ein <a href="folder.md"><strong>Ordner</strong></a> Objekt für den angegebenen Ordner und gibt dieses zurück.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-open.md"><strong>Eren</strong></a></td>
<td style="text-align: left;">Öffnet den angegebenen Ordner.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-refreshmenu.md"><strong>Aktuerfrischendes Menü</strong></a></td>
<td style="text-align: left;">Aktualisiert den Inhalt des <strong>Start</strong> Menüs. Wird nur mit Systemen vor Windows XP verwendet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-searchcommand.md"><strong>Searchcommand</strong></a></td>
<td style="text-align: left;">Zeigt den Bereich apps-Suche an.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestart"><strong>Servicestart</strong></a></td>
<td style="text-align: left;">Startet einen benannten Dienst.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestop"><strong>Servicestop</strong></a></td>
<td style="text-align: left;">Beendet einen benannten Dienst.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Datums-und Uhrzeit Eigenschaften</strong> an. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen von <strong>Datum/Uhrzeit anpassen</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></td>
<td style="text-align: left;">Führt einen angegebenen Vorgang für eine angegebene Datei aus.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>Showbrowserbar</strong></a></td>
<td style="text-align: left;">Zeigt eine Browserleiste an.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-shutdownwindows.md"><strong>Shutdownwindows</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Windows herunter</strong> fahren an. Dies ist das gleiche wie beim Klicken auf das <strong>Startmenü</strong> und beim Auswählen von " <strong>herunter</strong>fahren".<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-suspend.md"><strong>Angehalten</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-tilehorizontally.md"><strong>Tilehorizontisch</strong></a></td>
<td style="text-align: left;">Kachelt alle Fenster auf dem Desktop horizontal. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und <strong>Fenster horizontal</strong>nebeneinander auswählen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-tilevertically.md"><strong>Tilevertikal</strong></a></td>
<td style="text-align: left;">Kachelt alle Fenster auf dem Desktop vertikal. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und nebeneinander <strong>Fenster</strong>nebeneinander auswählen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></td>
<td style="text-align: left;">Zeigt den Desktop an oder blendet ihn aus.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-trayproperties.md"><strong>Trayproperties</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Eigenschaften von Taskleiste und Startmenü</strong> an. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und <strong>Eigenschaften</strong>auswählen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-undominimizeall.md"><strong>Undominimizeall</strong></a></td>
<td style="text-align: left;">Stellt alle Desktop Fenster in dem Zustand wieder her, in dem Sie vor dem letzten <a href="shell-minimizeall.md"><strong>minimizeall</strong></a> -Befehl standen. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von "alle Fenster auf älteren Systemen <strong>minimieren</strong> " oder ein zweites klicken auf das Symbol " <strong>Desktop anzeigen</strong> " im Bereich "Schnellstart" der Taskleiste in Windows 2000 oder Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Erstellt ein <a href="shellwindows.md"><strong>shellwindows</strong></a> -Objekt und gibt es zurück. Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Windows-Sicherheit</strong> an.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windowswitcher.md"><strong>Windowswitcher</strong></a></td>
<td style="text-align: left;">Zeigt die geöffneten Fenster in einem 3D-Stapel an, den Sie durchlaufen können.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Eigenschaften

Das **Shellobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp          | BESCHREIBUNG                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Application**](shell-application.md)<br/> | Schreibgeschützt<br/> | Enthält das Anwendungs Objekt des-Objekts.<br/>                        |
| [**Parent**](shell-parent.md)<br/>           | Schreibgeschützt<br/> | Ruft ein-Objekt ab, das das übergeordnete Element des aktuellen-Objekts darstellt.<br/> |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 
