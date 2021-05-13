---
description: Stellt ein -Objekt in der Shell dar.
title: IShellDispatch-Objekt (Shldisp.h)
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
ms.openlocfilehash: 02fbead4b2d40a91ec6dab70f536d1ea3241ee84
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840891"
---
# <a name="ishelldispatch-object"></a>IShellDispatch-Objekt

Stellt ein -Objekt in der Shell dar. Methoden werden bereitgestellt, um die Shell zu steuern und Befehle in der Shell auszuführen. Es gibt auch Methoden, um andere Shell-bezogene Objekte zu erhalten.

> [!Note]  
> **IShellDispatch wird** implementiert und über das [**Shell-Objekt aufgerufen.**](shell.md)

 

## <a name="members"></a>Member

Das **IShellDispatch-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **IShellDispatch-Objekt** verfügt über diese Methoden.



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
<td style="text-align: left;"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">Erstellt ein Dialogfeld, in dem der Benutzer einen Ordner auswählen und dann das Ordnerobjekt des ausgewählten <a href="folder.md"><strong>Ordners zurückgibt.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">Kaskadiert alle Fenster auf dem Desktop. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Kaskadieren von Fenstern.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Führt die angegebene Systemsteuerung aus. Wenn die Anwendung bereits geöffnet ist, wird die ausgeführte Instanz aktiviert. <br/>
<blockquote>
<p>[!Note]<br />
Ab Windows Vista sind die meisten Systemsteuerung Shell-Elemente und können mit dieser Funktion nicht geöffnet werden. Um diese anwendungen Systemsteuerung öffnen, übergeben Sie den kanonischen Namen an control.exe. Zum Beispiel:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">Wirft den Computer von seiner Andockstation aus. Dies entspricht dem Klicken auf das <strong>Startmenü</strong> und dem Auswählen von <strong>PC auswerfen,</strong>wenn ihr Computer diesen Befehl unterstützt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-explore.md"><strong>Erkunden</strong></a></td>
<td style="text-align: left;">Öffnet einen angegebenen Ordner in einem Windows-Explorer Fenster.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Ausführen</strong> für den Benutzer an.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Suchergebnisse: Computer an.</strong> Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></td>
<td style="text-align: left;">Zeigt das Dialogfeld <strong>Suchen: Alle Dateien</strong> an. Dies entspricht dem Klicken auf das <strong>Menü Start</strong> und anschließender Auswahl von <strong>Suchen.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-help.md"><strong>Hilfe</strong></a></td>
<td style="text-align: left;">Zeigt das Fenster Hilfe und Support von Windows an. Diese Methode hat die gleiche Auswirkung wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen von <strong>Hilfe und Support.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-minimizeall.md"><strong>MinimierenAlle</strong></a></td>
<td style="text-align: left;">Minimiert alle Fenster auf dem Desktop. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Minimieren aller Windows-Fenster</strong> auf älteren Systemen oder Klicken auf das Symbol <strong>Desktop anzeigen</strong> auf der Taskleiste.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-namespace.md"><strong>Namespace</strong></a></td>
<td style="text-align: left;">Erstellt ein <a href="folder.md"><strong>Folder-Objekt</strong></a> für den angegebenen Ordner und gibt es zurück.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-open.md"><strong>Öffnen</strong></a></td>
<td style="text-align: left;">Öffnet den angegebenen Ordner.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">Aktualisiert den Inhalt des <strong>Startmenüs.</strong> Wird nur mit Systemen vor Windows XP verwendet.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-settime.md"><strong>Settime</strong></a></td>
<td style="text-align: left;">Zeigt das <strong>Dialogfeld Datum und Uhrzeit</strong> an. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen von <strong>Datum/Uhrzeit anpassen.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">Zeigt das <strong>Dialogfeld Windows herunterfahren</strong> an. Dies ist identisch mit dem Klicken auf das <strong>Startmenü</strong> und dem Auswählen <strong>von Herunterfahren.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-suspend.md"><strong>Auszusetzen</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">Kacheln aller Fenster auf dem Desktop horizontal. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen <strong>von Fenstern gestapelt anzeigen.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">Kacheln aller Fenster auf dem Desktop vertikal. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Fenstern nebeneinander anzeigen.</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></td>
<td style="text-align: left;">Zeigt das <strong>Dialogfeld Taskleiste und Eigenschaften des Startmenüs</strong> an. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Eigenschaften.</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">Stellt alle Desktopfenster in dem Zustand wieder her, in dem sie sich vor dem letzten <a href="shell-minimizeall.md"><strong>MinimizeAll-Befehl</strong></a> befanden. Diese Methode hat den gleichen Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Alle Fenster minimieren</strong> rückgängig (auf älteren Systemen) oder ein zweites Klicken auf das Symbol Desktop <strong>anzeigen</strong> in der Taskleiste.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Erstellt ein <a href="shellwindows.md"><strong>ShellWindows-Objekt</strong></a> und gibt es zurück. Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Eigenschaften

Das **IShellDispatch-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                     | Zugriffstyp          | BESCHREIBUNG                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Application**](ishelldispatch-application.md)<br/> | Schreibgeschützt<br/> | Enthält ein -Objekt, das eine Anwendung darstellt.<br/>                    |
| [**Parent**](ishelldispatch-parent.md)<br/>           | Schreibgeschützt<br/> | Ruft ein -Objekt ab, das das übergeordnete Element des aktuellen -Objekts darstellt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shell-Objekt**](shell.md)
</dt> </dl>

 

 
