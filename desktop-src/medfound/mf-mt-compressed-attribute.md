---
description: Gibt für einen Medientyp an, ob die Mediendaten komprimiert sind.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: MF_MT_COMPRESSED-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afea99ffb0c9f7f9f53fb6edd0b4b87b2ecd4ff4f451e5fd0e56d47a70aee994
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060690"
---
# <a name="mf_mt_compressed-attribute"></a>MF \_ MT \_ COMPRESSED-Attribut

Gibt für einen Medientyp an, ob die Mediendaten komprimiert sind.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Wenn dieses Attribut **TRUE** ist, ist der Medientyp ein komprimiertes Format. Andernfalls ist entweder der Medientyp unkomprimiert, oder der Komprimierungstyp ist nicht bekannt.

Es ist nicht garantiert, dass dieses Attribut für alle komprimierten Formate auf **TRUE** festgelegt ist. Daher sollten Anwendungen dieses Attribut in der Regel nicht verwenden. Die zuverlässigste Methode, um zu bestimmen, ob ein Format komprimiert ist, besteht darin, eine Liste bekannter Formate zu verwalten. Wenn eine Anwendung kein Format erkennt, wie im [**MF \_ MT \_ SUBTYPE-Attribut**](mf-mt-subtype-attribute.md) angegeben, sollte sie nichts über die Komprimierung des Formats annehmen.

Um zu bestimmen, ob ein Format temporale Komprimierung verwendet (d. h., einige Stichproben werden als Deltas aus früheren Stichproben berechnet), überprüfen Sie das [**MF MT ALL SAMPLES \_ \_ \_ \_ INDEPENDENT-Attribut.**](mf-mt-all-samples-independent-attribute.md)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




