---
description: Gibt an, ob die diesem Topologieknoten zugeordnete Mediensenke ratenlos ist.
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: MF_TOPONODE_RATELESS-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d4de6b132bf2b49e327be45588a497374043794ec73925eb61f2dab16fd1bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448870"
---
# <a name="mf_toponode_rateless-attribute"></a>MF \_ TOPONODE \_ RATELESS-Attribut

Gibt an, ob die diesem Topologieknoten zugeordnete Mediensenke ratenlos ist.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Ausgabeknoten (**MF \_ TOPOLOGY \_ OUTPUT \_ NODE**).

Wenn der Wert dieses Attributs ungleich 0 (null) ist, behandelt die Mediensitzung die Mediensenke als ratenlose Senke, unabhängig davon, ob die Mediensenke das **MEDIASINK \_ RATELESS-Merkmal** zurückgibt. Wenn dieses Attribut nicht festgelegt ist, wird davon ausgegangen, dass die Mediensenke nicht ratenlos ist.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**TENSMediaSink::GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[**TOPOLOGYNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




