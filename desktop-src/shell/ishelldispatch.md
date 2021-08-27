---
description: Stellt ein Objekt in der Shell dar.
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
ms.openlocfilehash: 322b912ad7332b0862309b0ecc1510adb3aa1a10
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475296"
---
# <a name="ishelldispatch-object"></a>IShellDispatch-Objekt

Stellt ein Objekt in der Shell dar. Methoden werden bereitgestellt, um die Shell zu steuern und Befehle innerhalb der Shell auszuführen. Es gibt auch Methoden, um andere Shell-bezogene Objekte abzurufen.

> [!Note]  
> **IShellDispatch** wird implementiert und über das [**Shell-Objekt**](shell.md) aufgerufen.

 

## <a name="members"></a>Member

Das **IShellDispatch-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **IShellDispatch-Objekt** verfügt über diese Methoden.




| Methode | BESCHREIBUNG | 
|--------|-------------|
| <a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a> | Erstellt ein Dialogfeld, in dem der Benutzer einen Ordner auswählen und dann das <a href="folder.md"><strong>Ordnerobjekt</strong></a> des ausgewählten Ordners zurückgibt.<br /> | 
| <a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a> | Kaskadiert alle Fenster auf dem Desktop. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von Cascade windows ( <strong>Kaskadierende Fenster).</strong><br /> | 
| <a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a> | Führt die angegebene Systemsteuerung Anwendung aus. Wenn die Anwendung bereits geöffnet ist, wird die ausgeführte Instanz aktiviert. <br /><blockquote><p>[!Note]<br />Ab Windows Vista sind die meisten Systemsteuerung Anwendungen Shellelemente und können nicht mit dieser Funktion geöffnet werden. Um diese Systemsteuerung Anwendungen zu öffnen, übergeben Sie den kanonischen Namen an control.exe. Beispiel:</p><pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre></blockquote><br /> | 
| <a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a> | Wirft den Computer von seiner Andockstation aus. Dies entspricht dem Klicken auf das <strong>Startmenü</strong> und dem Auswählen von <strong>PC auswerfen,</strong>wenn ihr Computer diesen Befehl unterstützt.<br /> | 
| <a href="ishelldispatch-explore.md"><strong>Erkunden</strong></a> | Öffnet einen angegebenen Ordner in einem Windows Explorer-Fenster.<br /> | 
| <a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a> | Zeigt das Dialogfeld <strong>Ausführen</strong> für den Benutzer an.<br /> | 
| <a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a> | Zeigt das Dialogfeld <strong>Suchergebnisse: Computer</strong> an. Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.<br /> | 
| <a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a> | Zeigt das Dialogfeld <strong>Suchen: Alle Dateien</strong> an. Dies entspricht dem Klicken auf das <strong>Menü Start</strong> und anschließender Auswahl von <strong>Suchen.</strong><br /> | 
| <a href="ishelldispatch-help.md"><strong>Hilfe</strong></a> | Zeigt das Windows Fenster Hilfe und Support an. Diese Methode hat die gleiche Auswirkung wie das Klicken auf das <strong>Startmenü</strong> und das Auswählen von <strong>Hilfe und Support.</strong><br /> | 
| <a href="ishelldispatch-minimizeall.md"><strong>MinimierenAlle</strong></a> | Minimiert alle Fenster auf dem Desktop. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Minimieren aller Windows</strong> auf älteren Systemen oder Klicken auf das Symbol Desktop <strong>anzeigen</strong> auf der Taskleiste.<br /> | 
| <a href="ishelldispatch-namespace.md"><strong>Namespace</strong></a> | Erstellt ein <a href="folder.md"><strong>Folder-Objekt</strong></a> für den angegebenen Ordner und gibt es zurück.<br /> | 
| <a href="ishelldispatch-open.md"><strong>Öffnen</strong></a> | Öffnet den angegebenen Ordner.<br /> | 
| <a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a> | Aktualisiert den Inhalt <strong></strong> des Startmenüs. Wird nur bei Systemen vor Windows XP verwendet.<br /> | 
| <a href="ishelldispatch-settime.md"><strong>Settime</strong></a> | Zeigt das Dialogfeld <strong>Datum und Uhrzeit</strong> an. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Uhr im Taskleistenstatusbereich und das Auswählen <strong>von Datum/Uhrzeit anpassen.</strong><br /> | 
| <a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a> | Zeigt das Dialogfeld <strong>Herunterfahren Windows</strong> an. Dies entspricht dem Klicken auf das <strong>Menü Start</strong> und der Auswahl von <strong>Herunterfahren.</strong><br /> | 
| <a href="ishelldispatch-suspend.md"><strong>Angehalten</strong></a> | Td | 
| <a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a> | Kachelt alle Fenster auf dem Desktop horizontal. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Fenster gestapelt anzeigen.</strong><br /> | 
| <a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a> | Kachelt alle Fenster auf dem Desktop vertikal. Diese Methode hat den gleichen Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen <strong>von Fenster nebeneinander anzeigen.</strong><br /> | 
| <a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a> | Zeigt das Dialogfeld <strong>Taskleiste und Startmenüeigenschaften</strong> an. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Eigenschaften.</strong><br /> | 
| <a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a> | Stellt alle Desktopfenster in dem Zustand wieder her, in dem sie sich vor dem letzten <a href="shell-minimizeall.md"><strong>MinimizeAll-Befehl</strong></a> befanden. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von <strong>Alle Windows</strong> minimieren rückgängig machen (auf älteren Systemen) oder ein zweites Klicken auf das Symbol <strong>Desktop anzeigen</strong> in der Taskleiste.<br /> | 
| <a href="ishelldispatch-windows.md"><strong>Windows</strong></a> | Erstellt ein <a href="shellwindows.md"><strong>ShellWindows-Objekt</strong></a> und gibt es zurück. Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.<br /> | 




 

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
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shell-Objekt**](shell.md)
</dt> </dl>

 

 
