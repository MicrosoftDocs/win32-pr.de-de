---
description: Enthält den Bezeichner des Wiedergabelisten Elements in der Präsentation.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: MF_PD_PLAYBACK_ELEMENT_ID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359551"
---
# <a name="mf_pd_playback_element_id-attribute"></a>\_Attribut- \_ ID \_ - \_ Attribut der MF-PD

Enthält den Bezeichner des Wiedergabelisten Elements in der Präsentation.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Bemerkungen

Medienquellen, die Wiedergabelisten übermitteln, können dieses Attribut optional für die Präsentations Deskriptoren festlegen.

Wenn eine Medienquelle eine Wiedergabeliste bereitstellt, sendet Sie ein [menewpresentation](menewpresentation.md) -Ereignis für jedes Wiedergabelisten Element nach dem ersten. Dieses Ereignis enthält einen Präsentations Deskriptor für das neue Wiedergabelisten Element. Die Medienquelle kann den Elementen Bezeichner zuweisen, indem Sie \_ \_ \_ \_ für jeden Präsentations Deskriptor, einschließlich der von [**imfmediasource:: kreatepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)erstellten, das Attribut "MF PD Playback" ID-Attribut, festgelegt wird.

Eine Medienquelle kann das [menewpresentation](menewpresentation.md) -Ereignis auch aufgrund eines dynamischen streamschalters oder einer Änderung in der Anzahl der Streams senden. In dieser Situation sollte der Wert der MF-ID für die \_ \_ Wiedergabe \_ Element-ID in \_ beiden Präsentationen gleich bleiben, um anzugeben, dass beide Präsentationen dasselbe Wiedergabelisten Element darstellen. Wenn zwei aufeinander folgende Präsentationen denselben Wert für dieses Attribut aufweisen, erwartet die Microsoft Media Foundation Pipeline, dass die Zeitstempel während des Übergangs fortlaufend bleiben. Daher darf die Medienquelle das [ \_ \_ \_ tatsächliche \_ Start Attribut der MF-Ereignis Quelle](mf-event-source-actual-start-attribute.md) nicht verwenden, wenn Sie zur nächsten Präsentation übergeht.

Medienquellen, die [**imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) implementieren, sollten das Element " [MF \_ toponode \_ Sequence \_ elementId](mf-toponode-sequence-elementid-attribute.md) " anstelle des "MF PD"- \_ \_ \_ \_ Attributs "ID" verwenden.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




