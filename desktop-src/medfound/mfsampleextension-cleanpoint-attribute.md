---
description: Gibt an, ob eine Stichprobe ein zufälliger Zugriffspunkt ist.
ms.assetid: 03d4bfd8-1148-4551-8e71-05cfba2e15fa
title: MFSampleExtension_CleanPoint -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7181c08b19382a6b9d9da0475ec0a7a0522bd132dc10a2da1da4531d631d02d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241497"
---
# <a name="mfsampleextension_cleanpoint-attribute"></a>CleanPoint-Attribut "MFSampleExtension" \_

Gibt an, ob eine Stichprobe ein zufälliger Zugriffspunkt ist.

## <a name="data-type"></a>Datentyp

**BOOL als** **UINT32 gespeichert**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**VERERBUNGSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Beispiele. Wenn das Attribut **TRUE ist,** ist das Beispiel ein zufälliger Zugriffspunkt, und die Decodierung kann mit diesem Beispiel beginnen. Andernfalls ist das Beispiel kein zufälliger Zugriffspunkt.

Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert **FALSE.**

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="examples"></a>Beispiele


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Beispielattribute](sample-attributes.md)
</dt> <dt>

[Medienbeispiele](media-samples.md)
</dt> </dl>

 

 




