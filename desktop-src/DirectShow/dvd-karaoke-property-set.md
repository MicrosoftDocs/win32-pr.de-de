---
description: Wenn der DVD Navigator-Filter in den Modus "Mode" versetzt wird, informiert er den Audiodecoder über die AM \_ PROPERTY \_ DVDKARAOKE \_ ENABLE-Eigenschaft.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: DVD Dvd Dvd Property Set (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f3f7674b240934ae7440858b7317fd1abaf9b7833e36f80d7edc6cc185bc932
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016018"
---
# <a name="dvd-karaoke-property-set"></a>DVD-Dvd : Eigenschaftensatz

Wenn der [DVD Navigator-Filter](dvd-navigator-filter.md) in den Modus "Mode" versetzt wird, informiert er den Audiodecoder über die **AM PROPERTY \_ \_ DVDKARAOKE \_ ENABLE-Eigenschaft.** Der Decoder sollte dann die Audiokanäle 2 bis 5 stummschalten, bis er vom DVD-Navigator eine **AM \_ PROPERTY \_ DVDKARAOKE \_ DATA-Eigenschaft** mit einem Zeiger auf eine [**AM \_ DvdKaraokeData-Datenstruktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) empfängt, die angibt, wie die Hilfskanäle gemischt werden sollen.



| Bezeichnung | Wert |
|-------------------|-----------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ DvdKaraoke |



 



| Eigenschafts-ID                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_AM-EIGENSCHAFT \_ DVDKARAOKE \_ ENABLE | BOOLEAN-Wert. Der DVD-Navigator sendet dem Decoder eine AM PROPERTY DVDKARAOKE ENABLE mit dem Wert TRUE, um das Downmixing zu aktivieren, oder \_ \_ \_ **FALSE,** um es zu deaktivieren.                                                                                                                                     |
| \_AM-EIGENSCHAFT \_ DVDKARAOKE-DATEN \_   | Der DVD-Navigator sendet dem Decoder eine AM PROPERTY DVDKARAOKE DATA-Eigenschaft mit einem Zeiger auf eine \_ \_ AM \_ [**\_ DvdKaraokeData-Struktur,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) um die Downmix-Konfiguration zu ändern, d.> um bestimmte Kanäle zu aktivieren oder zu deaktivieren und sie an den rechten oder linken Ausgabekanal weiterzuverwenden. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




