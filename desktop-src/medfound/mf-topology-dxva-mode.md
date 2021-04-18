---
description: Gibt an, ob der topologielader die Microsoft DirectX Video Acceleration (DXVA) in der Topologie aktiviert.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: MF_TOPOLOGY_DXVA_MODE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad75b37a2ca2e971077b05d1bbeb92748530614
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347156"
---
# <a name="mf_topology_dxva_mode-attribute"></a>\_ \_ DXVA-Modusattribut der MF-Topologie \_

Gibt an, ob der topologielader die Microsoft DirectX Video Acceleration (DXVA) in der Topologie aktiviert.

## <a name="data-type"></a>Datentyp

**[**Mftopology \_ \_**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** Als **UInt32** gespeicherter DXVA-Modus

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**Imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist eine Enumerationskonstante für den [**mftopology- \_ DXVA- \_ Modus**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) . Der Standardwert ist **mftopology \_ DXVA \_ default**.

Dieses Attribut steuert, welche MFTs einen Zeiger auf den Direct3D-Geräte-Manager erhalten. Um die vollständige Videobeschleunigung zu aktivieren, legen Sie den Wert auf **mftopology \_ DXVA \_ Full** fest. Der Wert **mftopology \_ DXVA \_ default** ist aus Gründen der Abwärtskompatibilität definiert und entspricht dem Verhalten aller früheren Versionen von Microsoft Media Foundation.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Direct3D Device Manager](direct3d-device-manager.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




