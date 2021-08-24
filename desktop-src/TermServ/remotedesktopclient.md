---
title: RemoteDesktopClient-Klasse
description: Implementiert die Microsoft Windows Store App Remotedesktop Clientsteuerung – Version 1.
ms.assetid: 0910883A-BD49-4908-8423-1FC280E0FE0C
ms.tgt_platform: multiple
keywords:
- RemoteDesktopClient-Klasse Remotedesktopdienste
- RemoteDesktopClient-Klasse Remotedesktopdienste beschrieben
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
ms.openlocfilehash: cad76c8c189854a28709765c5677d047590216ae8ab6271d44c595f7b24fdd88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865899"
---
# <a name="remotedesktopclient-class"></a>RemoteDesktopClient-Klasse

Implementiert die Microsoft Windows Store App Remotedesktop-Clientsteuerung – Version 1

Diese Klasse implementiert die folgenden Schnittstellen.

-   [**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
-   [**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)

**RemoteDesktopClient** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **RemoteDesktopClient-Klasse** verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attachevent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-attachevent)                                     | Fügt einen Ereignishandler an ein Ereignis an.<br/>                                                                                                                  |
| [**Verbinden**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-connect)                                             | Initiiert eine Verbindung mithilfe der Eigenschaften, die derzeit für das Clientsteuerelement der Remotedesktopprotokoll-App (RDP) festgelegt sind.<br/>                         |
| [**DeleteSavedCredentials**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-deletesavedcredentials)               | Löscht gespeicherte Anmeldeinformationen für den angegebenen Remotecomputer.<br/>                                                                                            |
| [**Detachevent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-detachevent)                                     | Trennt einen Ereignishandler von einem Ereignis.<br/>                                                                                                                |
| [**Trennen**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-disconnect)                                       | Trennt die aktive Verbindung.<br/>                                                                                                                      |
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Wird aufgerufen, wenn das Clientsteuerelement eine Administrative Nachricht empfängt.<br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Wird aufgerufen, wenn das Clientsteuerelement automatisch wieder eine Verbindung mit einer Remotesitzung hergestellt hat.<br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Wird aufgerufen, wenn das Clientsteuerelement versucht, automatisch eine Verbindung mit einer Remotesitzung wiederherzustellen.<br/>                                                  |
| [**OnConnected**](iremotedesktopclientevents-onconnected.md)                               | Wird aufgerufen, wenn das Clientsteuerelement eine Verbindung mit einer Remotesitzung hergestellt hat.<br/>                                                                                       |
| [**OnConnecting**](iremotedesktopclientevents-onconnecting.md)                             | Wird aufgerufen, wenn das Clientsteuerelement versucht, eine Verbindung mit einer Remotesitzung herzustellen.<br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | Wird aufgerufen, nachdem ein vom Clientsteuerelement angezeigtes Dialogfeld verworfen wurde.<br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Wird aufgerufen, bevor das Steuerelement ein Dialogfeld anzeigt.<br/>                                                                                                        |
| [**OnDisconnected**](iremotedesktopclientevents-ondisconnected.md)                         | Wird aufgerufen, wenn das Clientsteuerelement von einer Remotesitzung getrennt wurde.<br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Wird aufgerufen, wenn in der Remotesitzung spezielle Tastenkombinationen gedrückt werden.<br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | Wird aufgerufen, wenn das Clientsteuerelement erfolgreich bei einer Remotesitzung angemeldet wurde.<br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat.<br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Wird aufgerufen, wenn sich die Größe des Remotedesktops geändert hat.<br/>                                                                                                        |
| [**OnStatusChanged**](iremotedesktopclientevents-onstatuschanged.md)                       | Wird aufgerufen, wenn das Clientsteuerelement seinen Status aktualisiert hat.<br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Wird aufgerufen, wenn der Touchzeigercursor verschoben wurde und die [**EventsEnabled-Eigenschaft**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) auf TRUE festgelegt ist.<br/> |
| [**Verbindung wiederherstellen**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-reconnect)                                         | Initiiert eine automatische erneute Verbindung des Remotedesktopprotokoll(RDP)-App-Containerclientsteuerelements, um die Sitzung an die neue Breite und Höhe anzupassen.<br/>   |
| [**UpdateSessionDisplaySettings**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-updatesessiondisplaysettings)   | Aktualisiert die Breiten- und Höheneinstellungen für das Clientsteuerelement der Remotedesktopprotokoll-App (RDP).<br/>                                               |



 

### <a name="properties"></a>Eigenschaften

Die **RemoteDesktopClient-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                                             | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                            |
|:---------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktionen**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_actions)<br/>           | Schreibgeschützt<br/> | Ruft das Aktionsobjekt für den RDP-App-Containerclient (Remotedesktopprotokoll) ab.<br/>                                                                    |
| [**Einstellungen**](iremotedesktopclient-settings.md)<br/>         | Schreibgeschützt<br/> | Ruft das Einstellungsobjekt für den rdp-App-Containerclient (Remotedesktopprotokoll) ab.<br/>                                                                   |
| [**TouchPointer**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_touchpointer)<br/> | Schreibgeschützt<br/> | Enthält das [**RemoteDesktopClientTouchPointer-Objekt**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer) für den Containerclient der Remotedesktopprotokoll-App (RDP).<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                           |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| CLSID<br/>                    | CLSID \_ RemoteDesktopClient ist als EAB16C5D-EED1-4E95-868B-0FBA1B42C092 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop ActiveX-Steuerelementklassen](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

