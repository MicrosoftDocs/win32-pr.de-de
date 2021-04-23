---
description: Wenn der FILTER DVD Navigator in den Modus "Dvdoke" wechselt, wird der Audiodecoder über die EIGENSCHAFT AM \_ PROPERTY \_ DVDKARAOKE \_ ENABLE informiert.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: DVD-Dvd–Dvd-Eigenschaftssatz (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2918513de06a657436ed99e67f672fe74a113b78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909068"
---
# <a name="dvd-karaoke-property-set"></a>DVD-Eigenschaftssatz "Dvd- UndOke"

Wenn der [FILTER DVD Navigator](dvd-navigator-filter.md) in den Modus "Dvdoke" wechselt, wird der Audiodecoder über die EIGENSCHAFT AM PROPERTY **\_ \_ DVDKARAOKE \_ ENABLE informiert.** Der Decoder sollte dann audio channels 2 bis 5 stummschalten, bis er vom DVD-Navigator eine **AM \_ PROPERTY \_ DVDKARAOKE \_ DATA-Eigenschaft** mit einem Zeiger auf eine [**AM \_ DvdKaraokeData-Datenstruktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) empfängt, die angibt, wie die Hilfskanäle gemischt werden sollen.



| Bezeichnung | Wert |
|-------------------|-----------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ DvdKaraoke |



 



| Eigenschafts-ID                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ PROPERTY \_ DVDKARAOKE \_ ENABLE | BOOLESCHER WERT. Der DVD-Navigator sendet dem Decoder eine AM \_ PROPERTY \_ DVDKARAOKE \_ ENABLE-Eigenschaft mit dem Wert **TRUE,** um die Downmixing-Funktion zu aktivieren, oder **FALSE,** um sie zu deaktivieren.                                                                                                                                    |
| \_AM-EIGENSCHAFT \_ DVDKARAOKE-DATEN \_   | Der DVD-Navigator sendet dem Decoder eine AM \_ PROPERTY \_ DVDKARAOKE \_ DATA-Eigenschaft mit einem Zeiger auf eine [**AM \_ DvdKaraokeData-Struktur,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) um die Downmixkonfiguration zu ändern, d. h., um bestimmteLaufkanäle ein- oder auszuschalten und an den rechten oder linken Ausgabekanal weiterzuleiten. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




