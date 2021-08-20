---
title: IMsRdpClientSecuredSettings-Schnittstelle
description: Enthält Methoden zum Abrufen und Festlegen von Eigenschaften des Remotedesktop ActiveX-Steuerelements, die auf bestimmte Internet Explorer URL-Sicherheitszonen beschränkt sind. | IMsRdpClientSecuredSettings-Schnittstelle
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- IMsRdpClientSecuredSettings-Schnittstelle Remotedesktopdienste
- IMsRdpClientSecuredSettings-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a1b834d42c957998ad2a8eda5cd3790dd16f40dfd82a8e463bc34e510cd742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129790"
---
# <a name="imsrdpclientsecuredsettings-interface"></a>IMsRdpClientSecuredSettings-Schnittstelle

Enthält Methoden zum Abrufen und Festlegen von Eigenschaften des Remotedesktop ActiveX-Steuerelements, die auf bestimmte Internet Explorer URL-Sicherheitszonen beschränkt sind.

## <a name="members"></a>Member

Die **IMsRdpClientSecuredSettings-Schnittstelle** erbt von [**IMsTscSecuredSettings.**](imstscsecuredsettings-interface.md) **IMsRdpClientSecuredSettings** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientSecuredSettings-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | Beschreibung                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | Lesen/Schreiben<br/> | Die Einstellungen für die Audioumleitung.<br/>    |
| [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | Lesen/Schreiben<br/> | Die Einstellungen für die Tastaturumleitung.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaften können nicht festgelegt werden, wenn das Steuerelement verbunden ist.

Weitere Informationen zu den Methoden dieser Schnittstelle finden Sie unter Bereitstellen der [RDP-Clientsicherheit.](providing-for-rdp-client-security.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings ist als 605befcf-39c1-45cc-a811-068fb7be346d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung-Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





