---
title: Imsrdpdevice-Schnittstelle
description: Enthält Informationen zu einem Geräte Objekt.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- Imsrdpdevice-Schnittstelle Remotedesktopdienste
- Imsrdpdevice-Schnittstelle Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: d7ddfbb739a8cf8e93ee2c2214e14095ac68bd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337914"
---
# <a name="imsrdpdevice-interface"></a>Imsrdpdevice-Schnittstelle

Enthält Informationen zu einem Geräte Objekt.

## <a name="members"></a>Member

Die **imsrdpdevice** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imsrdpdevice** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **imsrdpdevice** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                               | Zugriffstyp           | BESCHREIBUNG                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [**DeviceDescription**](imsrdpdevice-devicedescription.md)<br/> | Schreibgeschützt<br/>  | Ruft die Geräte Beschreibung ab, die dem Benutzer angezeigt werden soll, wenn der Anzeige Name nicht verfügbar ist.<br/> |
| [**Geräte-ID**](imsrdpdevice-deviceinstanceid.md)<br/>   | Schreibgeschützt<br/>  | Ruft den geräteinstanzbezeichner des Geräts ab.<br/>                                            |
| [**FriendlyName**](imsrdpdevice-friendlyname.md)<br/>           | Schreibgeschützt<br/>  | Ruft den anzeigen Amen für das Gerät ab.<br/>                                                         |
| [**Redirectionstate**](imsrdpdevice-redirectionstate.md)<br/>   | Lesen/Schreiben<br/> | Gibt den Umleitungs Status des Geräts an.<br/>                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imsrdpdevice ist als 60c3b9c8-9E92-4fi5e-a3e7-604a912093ea definiert.<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**Imsrdpde vicecollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

