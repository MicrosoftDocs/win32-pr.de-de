---
description: Wenn der FILTER DVD Navigator in den Modus "Dvdoke" wechselt, wird der Audiodecoder über die EIGENSCHAFT AM \_ PROPERTY \_ DVDKARAOKE \_ ENABLE informiert.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: DVD-Dvd–Dvd-Eigenschaftssatz (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f3f7674b240934ae7440858b7317fd1abaf9b7833e36f80d7edc6cc185bc932
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016018"
---
# <a name="dvd-karaoke-property-set"></a>DVD-Eigenschaftssatz "Dvd- UndOke"

Wenn der [FILTER DVD Navigator](dvd-navigator-filter.md) in den Modus "Dvdoke" wechselt, wird der Audiodecoder über die EIGENSCHAFT AM PROPERTY **\_ \_ DVDKARAOKE \_ ENABLE informiert.** Der Decoder sollte dann audio channels 2 bis 5 stummschalten, bis er vom DVD-Navigator eine **AM \_ PROPERTY \_ DVDKARAOKE \_ DATA-Eigenschaft** mit einem Zeiger auf eine [**AM \_ DvdKaraokeData-Datenstruktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) empfängt, die angibt, wie die Hilfskanäle gemischt werden sollen.



| Bezeichnung | Wert |
|-------------------|-----------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ DvdKaraoke |



 



| Eigenschafts-ID                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ PROPERTY \_ DVDKARAOKE \_ ENABLE | BOOLESCHER WERT. Der DVD-Navigator sendet dem Decoder eine AM \_ PROPERTY \_ DVDKARAOKE \_ ENABLE-Eigenschaft mit dem Wert **TRUE,** um das Downmixing zu ermöglichen, oder **FALSE,** um es zu deaktivieren.                                                                                                                                    |
| \_AM-EIGENSCHAFT \_ DVDKARAOKE-DATEN \_   | Der DVD-Navigator sendet dem Decoder eine AM \_ PROPERTY \_ DVDKARAOKE \_ DATA-Eigenschaft mit einem Zeiger auf eine [**AM \_ DvdKaraokeData-Struktur,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) um die Downmixkonfiguration zu ändern, d. h., bestimmteLaufokekanäle zu aktivieren oder zu deaktivieren und an den rechten oder linken Ausgabekanal weiterzuleiten. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




