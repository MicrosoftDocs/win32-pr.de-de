---
title: IRemoteDesktopClientEvents-Schnittstelle
description: Stellt Methoden bereit, die Informationen vom Server empfangen, die sich auf Clientsteuerungsereignisse beziehen.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- IRemoteDesktopClientEvents-Schnittstelle Remotedesktopdienste
- IRemoteDesktopClientEvents-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bae11edf7e6c603c534afb75fe5c90bcc868f1e359f1d78748dd94b18b5627e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657070"
---
# <a name="iremotedesktopclientevents-interface"></a>IRemoteDesktopClientEvents-Schnittstelle

Stellt Methoden bereit, die Informationen vom Server empfangen, die sich auf Clientsteuerungsereignisse beziehen. Zu den Ereignissen gehören Das Verbinden und Trennen, Anforderungen im Vollbildmodus, erfolgreiche Anmeldung und Fehlerbedingungen.

## <a name="members"></a>Member

Die **IRemoteDesktopClientEvents-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRemoteDesktopClientEvents** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IRemoteDesktopClientEvents-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                      | Beschreibung                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Wird aufgerufen, wenn das Clientsteuerelement eine Administrative Nachricht empfängt. <br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Wird aufgerufen, wenn das Clientsteuerelement automatisch wieder eine Verbindung mit einer Remotesitzung hergestellt hat. <br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Wird aufgerufen, wenn das Clientsteuerelement versucht, automatisch eine Verbindung mit einer Remotesitzung wiederherzustellen. <br/>                                                  |
| [**OnConnected**](iremotedesktopclientevents-onconnected.md)                               | Wird aufgerufen, wenn das Clientsteuerelement eine Verbindung mit einer Remotesitzung hergestellt hat.<br/>                                                                                        |
| [**OnConnecting**](iremotedesktopclientevents-onconnecting.md)                             | Wird aufgerufen, wenn das Clientsteuerelement versucht, eine Verbindung mit einer Remotesitzung herzustellen. <br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | Wird aufgerufen, nachdem ein vom Clientsteuerelement angezeigtes Dialogfeld verworfen wurde. <br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Wird aufgerufen, bevor das Steuerelement ein Dialogfeld anzeigt. <br/>                                                                                                        |
| [**OnDisconnected**](iremotedesktopclientevents-ondisconnected.md)                         | Wird aufgerufen, wenn das Clientsteuerelement von einer Remotesitzung getrennt wurde. <br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Wird aufgerufen, wenn in der Remotesitzung spezielle Tastenkombinationen gedrückt werden. <br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | Wird aufgerufen, wenn das Clientsteuerelement erfolgreich bei einer Remotesitzung angemeldet wurde. <br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat. <br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Wird aufgerufen, wenn sich die Größe des Remotedesktops geändert hat. <br/>                                                                                                        |
| [**OnStatusChanged**](iremotedesktopclientevents-onstatuschanged.md)                       | Wird aufgerufen, wenn das Clientsteuerelement seinen Status aktualisiert hat. <br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Wird aufgerufen, wenn der Touchzeigercursor verschoben wurde und die [**EventsEnabled-Eigenschaft**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) auf TRUE festgelegt ist. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| CLSID<br/>                    | CLSID \_ RemoteDesktopClient ist als EAB16C5D-EED1-4E95-868B-0FBA1B42C092 definiert.<br/>       |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents ist als 079863B7-6D47-4105-8BFE-0CDCB360E67D definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[referenz zum Remotedesktop ActiveX-Steuerelement](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

