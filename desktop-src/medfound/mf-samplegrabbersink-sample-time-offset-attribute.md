---
description: Offset zwischen dem Zeitstempel der einzelnen Stichproben, die vom Stichprobengraber empfangen werden, und dem Zeitpunkt, zu dem der Stichprobengrab das Beispiel zeigt.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad8086d7820a9f7c642fb049af8696521f675be3f7606ff19166a4570ee8000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875990"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a>MF \_ SAMPLEGRABBERSINK \_ SAMPLE TIME \_ \_ OFFSET-Attribut

Offset zwischen dem Zeitstempel der einzelnen Stichproben, die vom Stichprobengraber empfangen werden, und dem Zeitpunkt, zu dem der Stichprobengrab das Beispiel zeigt.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Hinweise

Sie können dieses Attribut für das VON der [**MFCreateSampleGrabberSinkActivate-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) zurückgegebene [**OBJEKT FESTLEGEN.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Dieses Attribut ermöglicht es der Rückruffunktion des Beispielgrabbers, Stichproben vor der Präsentationszeit zu empfangen.

Wenn der Beispielgramper eine neue Stichprobe empfängt, zeigt er das Beispiel zum Zeitpunkt *t* – *Offset* an, wobei *t* der Zeitstempel für die Stichprobe und *offset* der Wert dieses Attributs ist. Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert 0 (null).

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEs::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**VERWALTESampleGrabberSinkCallback**](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 




