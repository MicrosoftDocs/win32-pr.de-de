---
description: Offset zwischen dem Zeitstempel jedes Beispiels, das von der Sample Webbannergrabber empfangen wurde, und dem Zeitpunkt, zu dem der Sample Webbannergrabber das Beispiel darstellt.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359906"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a>MF \_ samplegrabbersink- \_ Beispiel für \_ Zeit \_ Offset Attribut

Offset zwischen dem Zeitstempel jedes Beispiels, das von der Sample Webbannergrabber empfangen wurde, und dem Zeitpunkt, zu dem der Sample Webbannergrabber das Beispiel darstellt.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Bemerkungen

Sie können dieses Attribut für das [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Objekt festlegen, das von der [**mfikreatesamplegrabbersink Aktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) -Funktion zurückgegeben wird. Mit diesem Attribut kann die Rückruffunktion des beispielgrabers Beispiele vor der Präsentationszeit empfangen.

Wenn der Sample Webbannergrabber ein neues Beispiel erhält, wird das Beispiel zum Zeitpunkt *t* - *Offset* dargestellt, wobei *t* der Zeitstempel für das Beispiel und *Offset* der Wert dieses Attributs ist. Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert 0 (null).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**Imbersamplegrabbersinkcallback**](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 




