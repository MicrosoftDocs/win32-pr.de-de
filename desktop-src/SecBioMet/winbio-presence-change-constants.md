---
title: WINBIO_PRESENCE_CHANGE Konstanten (winbio \_ types. h)
description: Beschreibt die Arten von Änderungen, die auftreten können, wenn der Windows-Biometrieframework das vorhanden sein von Einzelpersonen überwacht.
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
ms.openlocfilehash: c2c864c82ddca6faec134716778dc2e795675371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040208"
---
# <a name="winbio_presence_change-constants"></a>Winbio- \_ Anwesenheits \_ Änderungs Konstanten

Beschreibt die Arten von Änderungen, die auftreten können, wenn der Windows-Biometrieframework das vorhanden sein von Einzelpersonen überwacht.



| Konstante/Wert                                                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <dt>**Winbio \_ Anwesenheits \_ \_ Änderungstyp \_ unbekannt**</dt> <dt>0</dt> </dl>           | Der Ereignistyp ist unbekannt. Dieser Wert wird für die nicht initialisierte Struktur verwendet.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <dt>**Winbio \_ Anwesenheits \_ \_ Änderungstyp \_ Update \_ alle**</dt> <dt>1</dt> </dl> | Enthält Informationen zu allen Gesichtern, die im Kamera Rahmen aktuell sind.<br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <dt>**Winbio \_ Anwesenheits \_ \_ Änderungstyp \_ Ankunft**</dt> <dt>2</dt> </dl>              | Ein neues Gesicht, das in den Kamera Rahmen gelangt.<br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <dt>**Winbio \_ Anwesenheits \_ \_ Änderungstyp \_ erkennen**</dt> <dt>3</dt> </dl>     | Es wurde ein Gesicht mit einem registrierten Benutzer abgeglichen.<br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <dt>**Winbio \_ Anwesenheits \_ \_ Änderungstyp \_**</dt> <dt>4</dt> . </dl>              | Ein zuvor erkanntes Gesicht befand sich seit einem bestimmten Zeitraum nicht mehr im Kamera Frame.<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <dt>**Winbio \_ Anwesenheits \_ \_ Änderungstyp nach \_ Verfolgung**</dt> <dt>5</dt> </dl>                 | Stellt Update Informationen über das umgebende Feld bereit und gibt Detail Werte für eine Teilmenge der Gesichter zurück, die sich derzeit im Kamera Rahmen befinden.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt> </dl> |



 

 





