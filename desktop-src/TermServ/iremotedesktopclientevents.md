---
title: Iremotedesktopclientevents-Schnittstelle
description: Stellt Methoden bereit, die Informationen vom Server empfangen, die mit Client Steuerungs Ereignissen verknüpft sind.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040611"
---
# <a name="iremotedesktopclientevents-interface"></a>Iremotedesktopclientevents-Schnittstelle

Stellt Methoden bereit, die Informationen vom Server empfangen, die mit Client Steuerungs Ereignissen verknüpft sind. Zu den Ereignissen gehören das Herstellen von Verbindungen und trennen von Anforderungen im Vollbildmodus, das erfolgreiche anmelden und Fehlerbedingungen.

## <a name="members"></a>Member

Die **iremotedesktopclientevents** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iremotedesktopclientevents** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iremotedesktopclientevents** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Onadminmessagereceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Wird aufgerufen, wenn das Client Steuerelement eine administrative Nachricht empfängt. <br/>                                                                                      |
| [**Onautoreconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Wird aufgerufen, wenn das Client Steuerelement automatisch eine Verbindung mit einer Remote Sitzung hergestellt hat. <br/>                                                                       |
| [**Onautoreconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Wird aufgerufen, wenn das Client Steuerelement versucht, eine Verbindung mit einer Remote Sitzung automatisch wiederherzustellen. <br/>                                                  |
| [**Onconnected**](iremotedesktopclientevents-onconnected.md)                               | Wird aufgerufen, wenn das Client Steuerelement eine Verbindung mit einer Remote Sitzung hergestellt hat.<br/>                                                                                        |
| [**Verbindung wird hergestellt**](iremotedesktopclientevents-onconnecting.md)                             | Wird aufgerufen, wenn das Client Steuerelement versucht, eine Verbindung mit einer Remote Sitzung herzustellen. <br/>                                                                  |
| [**Ondialogverworfen**](iremotedesktopclientevents-ondialogdismissed.md)                   | Wird aufgerufen, nachdem ein vom Client Steuerelement angezeigtes Dialogfeld verworfen wurde. <br/>                                                                                 |
| [**Ondialogdisplay**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Wird aufgerufen, bevor das-Steuerelement ein Dialogfeld anzeigt. <br/>                                                                                                        |
| [**Nicht getrennt**](iremotedesktopclientevents-ondisconnected.md)                         | Wird aufgerufen, wenn das Client Steuerelement von einer Remote Sitzung getrennt wurde. <br/>                                                                             |
| [**Onkeycombinationpressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Wird aufgerufen, wenn in der Remote Sitzung Sondertasten Kombinationen gedrückt werden. <br/>                                                                                 |
| [**Onloginabgeschlossene**](iremotedesktopclientevents-onlogincompleted.md)                     | Wird aufgerufen, wenn sich das Client Steuerelement erfolgreich bei einer Remote Sitzung angemeldet hat. <br/>                                                                          |
| [**Onnetworkstatuschge**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat. <br/>                                                                                                             |
| [**"Onremotedesktopsizechanged"**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Wird aufgerufen, wenn sich die Remote Desktop Größe geändert hat. <br/>                                                                                                        |
| [**Onstatuschge**](iremotedesktopclientevents-onstatuschanged.md)                       | Wird aufgerufen, wenn das Client Steuerelement seinen Status aktualisiert hat. <br/>                                                                                                  |
| [**Ontouchpointercurrsorverschohe**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Wird aufgerufen, wenn der Fingerabdruck Cursor verschoben wurde und die [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) -Eigenschaft auf true festgelegt ist. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| CLSID<br/>                    | CLSID \_ Remotedesktopclient ist als EAB16C5D-EED1-4E95-868B-0FBA1B42C092 definiert.<br/>       |
| IID<br/>                      | Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop ActiveX-Steuerelement Verweis](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

