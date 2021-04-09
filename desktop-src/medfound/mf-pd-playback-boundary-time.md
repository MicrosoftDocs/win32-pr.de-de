---
description: Speichert die Zeit (in 100-Nanosekunden-Einheiten), bei der die Präsentation beginnen muss, relativ zum Anfang der Medienquelle.
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: MF_PD_PLAYBACK_BOUNDARY_TIME-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050500"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a>MF \_ - \_ \_ \_ Zeit Attribut für die Wiedergabe von Begrenzungen

Speichert die Zeit (in 100-Nanosekunden-Einheiten), bei der die Präsentation beginnen muss, relativ zum Anfang der Medienquelle.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Gilt für:

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Bemerkungen

Das MF \_ - \_ \_ \_ Zeit Attribut für die Zeit Wiedergabe Begrenzung ist für Medienquellen in einer Wiedergabeliste optional. Dieser Wert gibt die tatsächliche Startzeit der Präsentation an. Angenommen, eine Wiedergabeliste enthält Medienquellen *Element1*, *Element2* und *Element3* in einer Sequenz. 15 Sekunden nach dem Start der *Element1* -Wiedergabe tritt eine dynamische Datenstrom Änderung auf. Der neue Stream muss 15 Sekunden in der Präsentation wiedergeben. Der Keyframe, der der Präsentationszeit von 15 Sekunden am nächsten liegt, liegt jedoch bei 12 Sekunden für den neuen Stream. Um die neue Präsentation 15 Sekunden zu starten, ist ein Markin erforderlich, damit die decodierten Stichproben von 12 Sekunden auf 15 Sekunden abgelegt werden.

Vor der Umstellung wird das Ereignis [menewpresentation](menewpresentation.md) von der Medienquelle ausgelöst. Dadurch wird der Präsentations Deskriptor zurückgegeben, der das [MF- \_ \_ \_ Element \_ ID](mf-pd-playback-element-id.md) -Attribut für *Element1* enthält. Darüber hinaus enthält es das Attribut für die Begrenzung der MF- \_ \_ Zeit Wiedergabe Begrenzung, \_ \_ das auf 15 Sekunden festgelegt ist, um den Zeitpunkt der Umstellung anzugeben. Die Medienquelle führt das Markin nach 15 Sekunden nach der Decodierung aus, sodass die Anzeige von Frames von 12 Sekunden auf 15 Sekunden verhindert wird.

Dieser Wert wirkt sich nur auf die Markin-Zeit aus und wirkt sich nicht darauf aus, wie die Medien Sitzung Zeitstempel anpasst. Dieses Attribut wird ignoriert, es sei denn, die Medienquelle gibt durch das [MF PD-Attribut \_ \_ \_ \_ ID](mf-pd-playback-element-id.md) -Attribut an, dass diese Präsentation das gleiche Wiedergabe Element wie das vorherige Element ist.

Das MF-Attribut für die \_ \_ wiederwiedergabe Begrenzung \_ \_ ist vergleichbar mit dem MF-Attribut " [ \_ toponode \_ mediastart](mf-toponode-mediastart-attribute.md) ", das für den topologieknoten festgelegt wird. Für Anwendungen, die unter Windows Vista ausgeführt werden, sollten Medienquellen, die [**imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) implementieren, **MF \_ toponode \_ mediastart** anstelle von MF- \_ \_ \_ Zeit Wiedergabe Begrenzungs \_ Zeit verwenden.

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

 

 




