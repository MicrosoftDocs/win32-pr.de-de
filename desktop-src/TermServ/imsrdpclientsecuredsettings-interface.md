---
title: Imsrdpclientsecuredsettings-Schnittstelle
description: Enthält Methoden zum Abrufen und Festlegen der Eigenschaften des Remotedesktop ActiveX-Steuer Elements, die auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt sind. | Imsrdpclientsecuredsettings-Schnittstelle
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 396e6b58b2be0122076b5529b910423377417fa6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366594"
---
# <a name="imsrdpclientsecuredsettings-interface"></a>Imsrdpclientsecuredsettings-Schnittstelle

Enthält Methoden zum Abrufen und Festlegen der Eigenschaften des Remotedesktop ActiveX-Steuer Elements, die auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt sind.

## <a name="members"></a>Member

Die **imsrdpclientsecuredsettings** -Schnittstelle erbt von [**imstscsecuredsettings**](imstscsecuredsettings-interface.md). **Imsrdpclientsecuredsettings** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **imsrdpclientsecuredsettings** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | BESCHREIBUNG                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**Audioredirectionmode**](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | Lesen/Schreiben<br/> | Die audioumleitungs Einstellungen.<br/>    |
| [**Keyboardhuokmode**](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | Lesen/Schreiben<br/> | Die Einstellungen der Tastatur Umleitung.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften können nicht festgelegt werden, wenn das Steuerelement verbunden ist.

Weitere Informationen zu den Methoden dieser Schnittstelle finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ imsrdpclientsecuredsettings ist als 605befcf-39c1-45cc-a811-068fb7be346d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscsecuredsettings**](imstscsecuredsettings-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





