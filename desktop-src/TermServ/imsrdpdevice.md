---
title: IMsRdpDevice-Schnittstelle
description: Enthält Informationen zu einem Geräteobjekt.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- IMsRdpDevice-Schnittstelle Remotedesktopdienste
- IMsRdpDevice-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d545bebde1ed2df8a4c67cdf8d32d0a91499ed42076b2c1b31539d96069d3688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033090"
---
# <a name="imsrdpdevice-interface"></a>IMsRdpDevice-Schnittstelle

Enthält Informationen zu einem Geräteobjekt.

## <a name="members"></a>Member

Die **IMsRdpDevice-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpDevice** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpDevice-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                               | Zugriffstyp           | BESCHREIBUNG                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [**DeviceDescription**](imsrdpdevice-devicedescription.md)<br/> | Schreibgeschützt<br/>  | Ruft die Gerätebeschreibung ab, die dem Benutzer angezeigt werden soll, wenn der Anzeigename nicht verfügbar ist.<br/> |
| [**DeviceInstanceId**](imsrdpdevice-deviceinstanceid.md)<br/>   | Schreibgeschützt<br/>  | Ruft den Geräteinstanzbezeichner des Geräts ab.<br/>                                            |
| [**Friendlyname**](imsrdpdevice-friendlyname.md)<br/>           | Schreibgeschützt<br/>  | Ruft den Anzeigenamen für das Gerät ab.<br/>                                                         |
| [**RedirectionState**](imsrdpdevice-redirectionstate.md)<br/>   | Lesen/Schreiben<br/> | Gibt den Umleitungsstatus des Geräts an.<br/>                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice ist als 60c3b9c8-9e92-4f5e-a3e7-604a912093ea definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop-Webverbindung-Referenz](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

