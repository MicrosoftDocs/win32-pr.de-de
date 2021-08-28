---
description: Enthält den Bezeichner des Wiedergabelistenelements in der Präsentation.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: MF_PD_PLAYBACK_ELEMENT_ID -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 775aca29ab1cea36be9a2b87d64566210c03f6d6771d3493c73d34572975671e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102887"
---
# <a name="mf_pd_playback_element_id-attribute"></a>MF \_ PD PLAYBACK ELEMENT \_ \_ \_ ID-Attribut

Enthält den Bezeichner des Wiedergabelistenelements in der Präsentation.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**BESCHRIFTungDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Hinweise

Medienquellen, die Wiedergabelisten liefern, können dieses Attribut optional für ihre Präsentationsdeskriptoren festlegen.

Wenn eine Medienquelle eine Wiedergabeliste übermittelt, sendet sie ein [MENewPresentation-Ereignis](menewpresentation.md) für jedes Wiedergabelistenelement nach dem ersten. Dieses Ereignis enthält einen Präsentationsdeskriptor für das neue Wiedergabelistenelement. Die Medienquelle kann den Elementen Bezeichner zuweisen, indem sie das MF PD PLAYBACK ELEMENT ID-Attribut für jeden Präsentationsdeskriptor festlegen, einschließlich des von \_ \_ \_ \_ [**DERMEDIASOURCE::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)erstellten Attributs.

Eine Medienquelle kann aufgrund eines dynamischen Datenstromschalters oder einer Änderung der Anzahl von Streams auch das [MENewPresentation-Ereignis](menewpresentation.md) senden. In diesem Fall sollte der Wert von MF PD PLAYBACK ELEMENT ID in beiden Präsentationen gleich bleiben, um anzugeben, dass beide Präsentationen das gleiche \_ \_ \_ \_ Wiedergabelistenelement darstellen. Wenn zwei aufeinander folgende Präsentationen denselben Wert für dieses Attribut haben, erwartet Microsoft Media Foundation Pipeline, dass die Zeitstempel während des Übergangs kontinuierlich bleiben. Daher darf die Medienquelle beim Übergang zur nächsten Präsentation nicht das [ATTRIBUT MF \_ EVENT SOURCE \_ ACTUAL \_ \_ START](mf-event-source-actual-start-attribute.md) verwenden.

Medienquellen, die [**EINEMEDIASourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) implementieren, sollten das [MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID-Attribut](mf-toponode-sequence-elementid-attribute.md) anstelle des MF \_ PD PLAYBACK ELEMENT \_ \_ \_ ID-Attributs verwenden.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Präsentationsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




