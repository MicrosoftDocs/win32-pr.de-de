---
title: Remotedesktopclient-Klasse
description: Implementiert die Microsoft Windows Store-App Remotedesktop Client Control-Version 1.
ms.assetid: 0910883A-BD49-4908-8423-1FC280E0FE0C
ms.tgt_platform: multiple
keywords:
- Remotedesktopclient-Klasse Remotedesktopdienste
- Remotedesktopclient-Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- RemoteDesktopClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb10b23f52f53e2d89fd5a81449818a8fe374116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949612"
---
# <a name="remotedesktopclient-class"></a>Remotedesktopclient-Klasse

Implementiert die Microsoft Windows Store-App Remotedesktop Client Control-Version 1

Diese Klasse implementiert die folgenden Schnittstellen.

-   [**Iremotedesktopclient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
-   [**Iremotedesktopclientevents**](iremotedesktopclientevents.md)

**Remotedesktopclient** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Remotedesktopclient** -Klasse verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"AttachEvent"**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-attachevent)                                     | Fügt einem Ereignis einen Ereignishandler an.<br/>                                                                                                                  |
| [**Verbinden**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-connect)                                             | Initiiert eine Verbindung mit den Eigenschaften, die derzeit auf dem Client Steuerelement für die Remotedesktopprotokoll (RDP)-app-Container festgelegt sind.<br/>                         |
| [**Delta Update-Anmelde Informationen**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-deletesavedcredentials)               | Löscht gespeicherte Anmelde Informationen für den angegebenen Remote Computer.<br/>                                                                                            |
| [**DetachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-detachevent)                                     | Trennt einen Ereignishandler von einem Ereignis.<br/>                                                                                                                |
| [**Trennen**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-disconnect)                                       | Trennt die aktive Verbindung.<br/>                                                                                                                      |
| [**Onadminmessagereceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Wird aufgerufen, wenn das Client Steuerelement eine administrative Nachricht empfängt.<br/>                                                                                      |
| [**Onautoreconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Wird aufgerufen, wenn das Client Steuerelement automatisch eine Verbindung mit einer Remote Sitzung hergestellt hat.<br/>                                                                       |
| [**Onautoreconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Wird aufgerufen, wenn das Client Steuerelement versucht, eine Verbindung mit einer Remote Sitzung automatisch wiederherzustellen.<br/>                                                  |
| [**Onconnected**](iremotedesktopclientevents-onconnected.md)                               | Wird aufgerufen, wenn das Client Steuerelement eine Verbindung mit einer Remote Sitzung hergestellt hat.<br/>                                                                                       |
| [**Verbindung wird hergestellt**](iremotedesktopclientevents-onconnecting.md)                             | Wird aufgerufen, wenn das Client Steuerelement versucht, eine Verbindung mit einer Remote Sitzung herzustellen.<br/>                                                                  |
| [**Ondialogverworfen**](iremotedesktopclientevents-ondialogdismissed.md)                   | Wird aufgerufen, nachdem ein vom Client Steuerelement angezeigtes Dialogfeld verworfen wurde.<br/>                                                                                 |
| [**Ondialogdisplay**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Wird aufgerufen, bevor das-Steuerelement ein Dialogfeld anzeigt.<br/>                                                                                                        |
| [**Nicht getrennt**](iremotedesktopclientevents-ondisconnected.md)                         | Wird aufgerufen, wenn das Client Steuerelement von einer Remote Sitzung getrennt wurde.<br/>                                                                             |
| [**Onkeycombinationpressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Wird aufgerufen, wenn in der Remote Sitzung Sondertasten Kombinationen gedrückt werden.<br/>                                                                                 |
| [**Onloginabgeschlossene**](iremotedesktopclientevents-onlogincompleted.md)                     | Wird aufgerufen, wenn sich das Client Steuerelement erfolgreich bei einer Remote Sitzung angemeldet hat.<br/>                                                                          |
| [**Onnetworkstatuschge**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat.<br/>                                                                                                             |
| [**"Onremotedesktopsizechanged"**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Wird aufgerufen, wenn sich die Remote Desktop Größe geändert hat.<br/>                                                                                                        |
| [**Onstatuschge**](iremotedesktopclientevents-onstatuschanged.md)                       | Wird aufgerufen, wenn das Client Steuerelement seinen Status aktualisiert hat.<br/>                                                                                                  |
| [**Ontouchpointercurrsorverschohe**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Wird aufgerufen, wenn der Fingerabdruck Cursor verschoben wurde und die [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) -Eigenschaft auf true festgelegt ist.<br/> |
| [**Verbindung wiederherstellen**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-reconnect)                                         | Initiiert eine automatische erneute Verbindung Remotedesktopprotokoll des Client Steuer Elements (RDP)-app-Container, um die Sitzung an die neue Breite und Höhe anzupassen.<br/>   |
| [**Updatesessiondisplaysettings**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-updatesessiondisplaysettings)   | Aktualisiert die breiten-und Höheneinstellungen für das Client Steuerelement für die Remotedesktopprotokoll (RDP)-app-Container.<br/>                                               |



 

### <a name="properties"></a>Eigenschaften

Die **Remotedesktopclient** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                                             | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                            |
|:---------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktionen**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_actions)<br/>           | Schreibgeschützt<br/> | Ruft das Aktions Objekt für den Remotedesktopprotokoll (RDP)-app-Container Client ab.<br/>                                                                    |
| [**Einstellungen**](iremotedesktopclient-settings.md)<br/>         | Schreibgeschützt<br/> | Ruft das Einstellungs Objekt für den Remotedesktopprotokoll (RDP)-app-Container Client ab.<br/>                                                                   |
| [**TouchPointer**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_touchpointer)<br/> | Schreibgeschützt<br/> | Enthält das [**remotedesktopclienttouchpointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer) -Objekt für den Remotedesktopprotokoll (RDP)-app-Container Client.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| CLSID<br/>                    | CLSID \_ Remotedesktopclient ist als EAB16C5D-EED1-4E95-868B-0FBA1B42C092 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop ActiveX-Steuerelement Klassen](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

