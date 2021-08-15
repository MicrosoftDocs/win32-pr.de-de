---
description: Gibt an, ob ein Medienbeispiel das erste Beispiel nach einer Lücke im Stream ist.
ms.assetid: f9e1e700-9958-404d-8b83-08f846f5a1b0
title: MFSampleExtension_Discontinuity -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac76b8e4d220ece7c34277bfac031213c1c042615d7ca48677839e54b77e5da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241080"
---
# <a name="mfsampleextension_discontinuity-attribute"></a>MFSampleExtension \_ Discontinuity-Attribut

Gibt an, ob ein Medienbeispiel das erste Beispiel nach einer Lücke im Stream ist.

## <a name="data-type"></a>Datentyp

**BOOL als** **UINT32 gespeichert**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**VERERBUNGSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Medienbeispiele. Wenn dieses Attribut **TRUE ist,** bedeutet dies, dass es eine Diskontinuität im Stream gab, und dieses Beispiel ist das erste, das nach der Lücke angezeigt wird.

Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert **FALSE.**

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

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

 

 




