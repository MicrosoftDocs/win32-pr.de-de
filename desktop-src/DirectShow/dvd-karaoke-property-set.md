---
description: Wenn der DVD-Navigator-Filter in den Karaoke-Modus wechselt, wird der Audiodecoder über die Eigenschaft "am \_ Eigenschaft \_ dvdkaraoke enable" informiert \_ .
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: DVD-Karaoke-Eigenschaften Satz (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e9fe53ad35dac0c3c0f54a8e04a6fbe698fc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371002"
---
# <a name="dvd-karaoke-property-set"></a>DVD-Karaoke-Eigenschaften Satz

Wenn der [DVD-Navigator](dvd-navigator-filter.md) -Filter in den Karaoke-Modus wechselt, wird der Audiodecoder über die Eigenschaft " **am \_ Eigenschaft \_ dvdkaraoke \_ enable** " informiert. Der Decoder sollte dann die Audiokanäle 2 bis 5 stumm schalten, bis er vom DVD-Navigator eine **am \_ Eigenschaft \_ dvdkaraoke- \_ Daten** Eigenschaft mit einem Zeiger auf eine [**am \_ dvdkaraokedata**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) -Datenstruktur empfängt, die angibt, wie die zusätzlichen Kanäle gemischt werden sollen.



|                   |                             |
|-------------------|-----------------------------|
| Eigenschaftensatz-GUID | AM \_ kspropabtid \_ dvdkaraoke |



 



| Eigenschafts-ID                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM- \_ Eigenschaft \_ dvdkaraoke \_ enable | Boolescher Wert. Der DVD-Navigator sendet dem Decoder eine "am- \_ Eigenschaft \_ dvdkaraoke \_ enable" mit dem Wert " **true** ", um das Karaoke-downmischungs-und " **false** " zu aktivieren.                                                                                                                                    |
| AM- \_ Eigenschaft \_ dvdkaraoke- \_ Daten   | Der DVD-Navigator sendet dem Decoder eine "am \_ Eigenschaft \_ dvdkaraoke"- \_ Dateneigenschaft mit einem Zeiger auf eine " [**am \_ dvdkaraokedata**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) "-Struktur, um die downmischungs Konfiguration zu ändern, d. h. um bestimmte Karaoke-Kanäle ein-oder auszuschalten und Sie an den rechten oder linken Ausgabekanal weiterzuleiten. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




