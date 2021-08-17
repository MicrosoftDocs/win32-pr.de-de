---
description: Gibt an, ob das Topologielader die Microsoft DirectX-Videobeschleunigung (DXVA) in der Topologie aktiviert.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: MF_TOPOLOGY_DXVA_MODE -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5462ccf575f94935d100eb70a6d806e139f09762151c2dad8d4e155ca5d1d17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875729"
---
# <a name="mf_topology_dxva_mode-attribute"></a>DXVA \_ MODE-Attribut der MF-TOPOLOGIE \_ \_

Gibt an, ob das Topologielader die Microsoft DirectX-Videobeschleunigung (DXVA) in der Topologie aktiviert.

## <a name="data-type"></a>Datentyp

**[**MFTOPOLOGY \_ \_DXVA-MODUS**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** als **UINT32 gespeichert**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**TOPOLOGYTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist eine [**MFTOPOLOGY \_ DXVA \_ MODE-Enumerationskonstanz.**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) Der Standardwert ist **MFTOPOLOGY \_ DXVA \_ DEFAULT.**

Dieses Attribut steuert, welche MFTs einen Zeiger auf den Direct3D-Geräte-Manager erhalten. Um die vollständige Videobeschleunigung zu aktivieren, legen Sie den Wert auf **MFTOPOLOGY \_ DXVA \_ FULL fest.** Der Wert **MFTOPOLOGY \_ DXVA \_ DEFAULT** ist aus Gründen der Abwärtskompatibilität definiert und entspricht dem Verhalten aller früheren Versionen Microsoft Media Foundation.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Direct3D-Geräte-Manager](direct3d-device-manager.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




