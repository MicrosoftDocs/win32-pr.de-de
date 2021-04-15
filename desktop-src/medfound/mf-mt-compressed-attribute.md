---
description: Gibt für einen Medientyp an, ob die Mediendaten komprimiert sind.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: MF_MT_COMPRESSED-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528238"
---
# <a name="mf_mt_compressed-attribute"></a>\_Komprimiertes MF MT- \_ Attribut

Gibt für einen Medientyp an, ob die Mediendaten komprimiert sind.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut **true** ist, ist der Medientyp ein komprimiertes Format. Andernfalls ist entweder der Medientyp unkomprimiert, oder der Komprimierungstyp ist nicht bekannt.

Es ist nicht garantiert, dass dieses Attribut für alle komprimierten Formate auf **true** festgelegt ist, sodass Anwendungen in der Regel nicht dieses Attribut verlassen sollten. Die zuverlässigste Möglichkeit, um zu bestimmen, ob ein Format komprimiert ist, besteht darin, eine Liste bekannter Formate beizubehalten. Wenn eine Anwendung ein Format nicht erkennt, wie im [**MF \_ MT- \_ SubType**](mf-mt-subtype-attribute.md) -Attribut angegeben, sollte Sie nichts über die Komprimierung des Formats annehmen.

Um zu ermitteln, ob ein Format die Temporale Komprimierung verwendet (was bedeutet, dass einige Beispiele als Delta aus früheren Beispielen berechnet werden), überprüfen Sie das " [**MF \_ MT \_ All \_ Samples \_ Independent**](mf-mt-all-samples-independent-attribute.md) "-Attribut.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




