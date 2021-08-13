---
title: WINBIO_PRESENCE_CHANGE Konstanten (Winbio \_ types.h)
description: Beschreibt die Arten von Änderungen, die auftreten können, wenn Windows Biometrieframework das Vorhandensein von Personen überwacht.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08cce9cc74bafdba6cf8d1aa11abccdaf7315370223ff6edf47eaba167af84f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909719"
---
# <a name="winbio_presence_change-constants"></a>WINBIO \_ PRESENCE \_ CHANGE-Konstanten

Beschreibt die Arten von Änderungen, die auftreten können, wenn Windows Biometrieframework das Vorhandensein von Personen überwacht.



| Konstante/Wert                                                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <dt>**WINBIO \_ PRESENCE \_ CHANGE \_ TYPE \_ UNKNOWN**</dt> <dt>0</dt> </dl>           | Der Ereignistyp ist unbekannt. Dieser Wert wird für die nicht initialisierte -Struktur verwendet.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <dt>**WINBIO \_ PRESENCE \_ CHANGE TYPE UPDATE \_ \_ \_ ALL**</dt> <dt>1</dt> </dl> | Stellt Informationen zu allen Gesichtern zur Verfügung, die im Kamerarahmen aktuell sind.<br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <dt>**WINBIO \_ PRESENCE \_ CHANGE \_ TYPE \_ ARRIVE**</dt> <dt>2</dt> </dl>              | Ein neues Gesicht wurde in den Kamerarahmen eingegeben.<br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <dt>**WINBIO \_ PRESENCE \_ CHANGE \_ TYPE \_ RECOGNIZE**</dt> <dt>3</dt> </dl>     | Ein Gesicht wurde mit einem registrierten Benutzer übereinstimmen.<br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <dt>**WINBIO \_ PRESENCE \_ CHANGE \_ TYPE \_ TIPP**</dt> <dt>4</dt> </dl>              | Ein zuvor erkanntes Gesicht war für einen bestimmten Zeitraum nicht mehr im Kamerarahmen.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <dt>**WINBIO \_ PRESENCE \_ CHANGE \_ TYPE \_ TRACK**</dt> <dt>5</dt> </dl>                 | Stellt Aktualisierungsinformationen zum Begrenzungsrahmen bereit und lehnt Detailwerte für eine Teilmenge der Gesichter ab, die sich derzeit im Kamerarahmen befinden.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter enthalten)</dt> </dl> |



 

 





