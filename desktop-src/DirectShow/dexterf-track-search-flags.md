---
description: Die DEXTERF TRACK SEARCH FLAGS-Enumeration gibt die Begrenzungsbedingungen für eine Suche nach \_ einem Objekt auf der \_ \_ Zeitachse an.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: DEXTERF_TRACK_SEARCH_FLAGS -Enumeration (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 55d7c70dffbf57ae4d9788a10dfea02911a998e21ab5ea8e3d9ad7fffcf91624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952939"
---
# <a name="dexterf_track_search_flags-enumeration"></a>DEXTERF \_ TRACK \_ SEARCH \_ FLAGS-Enumeration

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `DEXTERF_TRACK_SEARCH_FLAGS` -Enumeration gibt die Begrenzungsbedingungen für eine Suche nach einem Objekt in der Zeitachse an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**\_DEXTERF-BEGRENZUNG**
</dt> <dd>

Suchen Sie nach einem Objekt, das sich über die angegebene Zeit erstreckt.

</dd> <dt>

<span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF \_ EXACTLY \_ AT**
</dt> <dd>

Suchen Sie nach einem Objekt, das genau zum angegebenen Zeitpunkt beginnt.

</dd> <dt>

<span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF \_ FORWARDS**
</dt> <dd>

Suchen Sie nach einem Objekt, das zum angegebenen Zeitpunkt oder später beginnt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Begrenzungsbedingungen sind in der folgenden Tabelle zusammengefasst.



| Enumerationswert    | Begrenzungsbedingung                        |
|----------------------|-------------------------------------------|
| \_DEXTERF-BEGRENZUNG    | Start <= TimeStop > Time<br/> |
| DEXTERF \_ EXACTLY \_ AT | Start == Time                             |
| DEXTERF \_ FORWARDS    | Start >= Time                          |



 

-   Start: Startzeit des abgerufenen Objekts.
-   Stop: Die Stoppzeit des abgerufenen Objekts.
-   Zeit: angegebene Suchzeit.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




