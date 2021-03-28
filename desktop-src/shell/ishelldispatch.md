---
description: Stellt ein Objekt in der Shell dar.
title: Ishelldispatch-Objekt (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.openlocfilehash: 20c6cc9f0b3a2e2fde8f56311564d63bc1cc9c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978073"
---
# <a name="ishelldispatch-object"></a>Ishelldispatch-Objekt

Stellt ein Objekt in der Shell dar. Es werden Methoden bereitgestellt, um die Shell zu steuern und um Befehle in der Shell auszuführen. Es gibt auch Methoden zum Abrufen anderer shellbezogener Objekte.

> [!Note]  
> **Ishelldispatch** wird implementiert und über das [**Shellobjekt**](shell.md) aufgerufen.

 

## <a name="members"></a>Member

Das **ishelldispatch** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **ishelldispatch** -Objekt verfügt über diese Methoden.



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
<td style="text-align: left;"><a href="ishelldispatch-browseforfolder.md"><strong>Browsorforfolder</strong></a></td>
<td style="text-align: left;">Erstellt ein Dialogfeld, das dem Benutzer ermöglicht, einen Ordner auszuwählen, und gibt dann das <a href="folder.md"><strong>Ordner</strong></a> Objekt des ausgewählten Ordners zurück.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-cascadewindows.md"><strong>Cascade-Fenster</strong></a></td>
<td style="text-align: left;">Alle Fenster auf dem Desktop werden kaskadiert. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und <strong>kaskadierte Fenster</strong>auswählen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Führt die angegebene System Steuerungsanwendung aus. Wenn die Anwendung bereits geöffnet ist, wird die laufende Instanz aktiviert. <br/>
<blockquote>
<p>[!Note]<br />
Ab Windows Vista sind die meisten System Steuerungsanwendungen shellelemente und können nicht mit dieser Funktion geöffnet werden. Wenn Sie diese System Steuerungsanwendungen öffnen möchten, übergeben Sie den kanonischen Namen an control.exe. Beispiel:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-ejectpc.md"><strong>Ejectpc</strong></a></td>
<td style="text-align: left;">Der Computer wird von seiner Docking Station eingelesen. Dies ist das gleiche wie beim Klicken auf das <strong>Startmenü</strong> und beim Auswählen von <strong>ausgelösten PCs</strong>, wenn Ihr Computer diesen Befehl unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-explore.md"><strong>Erkunden</strong></a></td>
<td style="text-align: left;">Öffnet einen angegebenen Ordner in einem Windows-Explorer-Fenster.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-filerun.md"><strong>Filerun</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld " <strong>Ausführen</strong> " für den Benutzer an.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-findcomputer.md"><strong>Findcomputer</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Suchergebnisse: Computer</strong> an. Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-findfiles.md"><strong>"Findfiles</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>suchen: alle Dateien</strong> an. Dies ist das gleiche wie beim Klicken auf das <strong>Startmenü</strong> und anschließendes Auswählen von <strong>Suchen</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-help.md"><strong>Hilfe</strong></a></td>
<td style="text-align: left;">Zeigt das Fenster Hilfe und Support an. Diese Methode hat denselben Effekt wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen von <strong>Hilfe und Support</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-minimizeall.md"><strong>Minimizeall</strong></a></td>
<td style="text-align: left;">Minimiert alle Fenster auf dem Desktop. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen der Option alle Fenster auf älteren Systemen <strong>minimieren</strong> oder klicken auf das Symbol <strong>Desktop anzeigen</strong> auf der Taskleiste.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-namespace.md"><strong>Namespace</strong></a></td>
<td style="text-align: left;">Erstellt ein <a href="folder.md"><strong>Ordner</strong></a> Objekt für den angegebenen Ordner und gibt dieses zurück.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-open.md"><strong>Eren</strong></a></td>
<td style="text-align: left;">Öffnet den angegebenen Ordner.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-refreshmenu.md"><strong>Aktuerfrischendes Menü</strong></a></td>
<td style="text-align: left;">Aktualisiert den Inhalt des <strong>Start</strong> Menüs. Wird nur mit Systemen vor Windows XP verwendet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Datum und Uhrzeit</strong> an. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen von <strong>Datum/Uhrzeit anpassen</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-shutdownwindows.md"><strong>Shutdownwindows</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Windows herunter</strong> fahren an. Dies ist das gleiche wie beim Klicken auf das <strong>Startmenü</strong> und beim Auswählen von " <strong>herunter</strong>fahren".<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-suspend.md"><strong>Angehalten</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-tilehorizontally.md"><strong>Tilehorizontisch</strong></a></td>
<td style="text-align: left;">Kachelt alle Fenster auf dem Desktop horizontal. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Gestapeltes Fenster anzeigen</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-tilevertically.md"><strong>Tilevertikal</strong></a></td>
<td style="text-align: left;">Kachelt alle Fenster auf dem Desktop vertikal. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und <strong>Fenster nebeneinander anzeigen</strong>auswählen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-trayproperties.md"><strong>Trayproperties</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Eigenschaften von Taskleiste und Startmenü</strong> an. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und <strong>Eigenschaften</strong>auswählen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-undominimizeall.md"><strong>Undominimizeall</strong></a></td>
<td style="text-align: left;">Stellt alle Desktop Fenster in dem Zustand wieder her, in dem Sie sich vor dem letzten <a href="shell-minimizeall.md"><strong>minimizeall</strong></a> -Befehl befanden. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von " <strong>alle Fenster minimieren</strong> (auf älteren Systemen)" oder ein zweites klicken auf das Symbol " <strong>Desktop anzeigen</strong> " in der Taskleiste.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Erstellt ein <a href="shellwindows.md"><strong>shellwindows</strong></a> -Objekt und gibt es zurück. Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Eigenschaften

Das **ishelldispatch** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                     | Zugriffstyp          | BESCHREIBUNG                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Application**](ishelldispatch-application.md)<br/> | Schreibgeschützt<br/> | Enthält ein-Objekt, das eine Anwendung darstellt.<br/>                    |
| [**Parent**](ishelldispatch-parent.md)<br/>           | Schreibgeschützt<br/> | Ruft ein-Objekt ab, das das übergeordnete Element des aktuellen-Objekts darstellt.<br/> |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shellobjekt**](shell.md)
</dt> </dl>

 

 
