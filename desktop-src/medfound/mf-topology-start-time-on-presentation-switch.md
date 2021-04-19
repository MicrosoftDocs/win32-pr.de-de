---
description: Gibt die Startzeit für Präsentationen an, die nach der ersten Präsentation in die Warteschlange eingereiht werden.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355530"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a>\_Start Zeitpunkt der MF-Topologie \_ \_ \_ bei \_ Presentation Switch- \_ Attribut

Gibt die Startzeit für Präsentationen an, die nach der ersten Präsentation in die Warteschlange eingereiht werden.

## <a name="data-type"></a>Datentyp

**Int64** als **UINT64** gespeichert

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Gilt für

[**Imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung die erste Präsentation in der Medien Sitzung in die Warteschlange eingereiht, gibt die Anwendung die Startzeit im *pvarstartposition* -Parameter der [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) -Methode an. Bei allen nachfolgenden Präsentationen wird die Startzeit jedoch durch die Start Zeit der MF- \_ Topologie für \_ \_ \_ \_ \_ das Präsentations switchattribut in der Topologie angegeben. Die Startzeit wird in 100-Nanosecond-Einheiten relativ zum Anfang der Präsentation angegeben. Wenn der Wert z. b. 50 Millionen ist, startet die Wiedergabe 5 Sekunden in der Präsentation. Wenn dieses Attribut nicht festgelegt ist, ist die Standard Startzeit 0 (null).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




