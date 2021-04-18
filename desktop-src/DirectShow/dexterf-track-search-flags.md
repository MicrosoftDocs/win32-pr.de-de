---
description: Die dexterf \_ - \_ \_ Suchflags-Enumeration gibt die begrenzungsbedingungen bei einer Suche nach einem Objekt in der Zeitachse an.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: DEXTERF_TRACK_SEARCH_FLAGS-Enumeration (qedit. h)
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
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365699"
---
# <a name="dexterf_track_search_flags-enumeration"></a>Dexterf \_ - \_ \_ Suchflags-Enumeration

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `DEXTERF_TRACK_SEARCH_FLAGS` Enumeration gibt die begrenzungsbedingungen bei einer Suche nach einem Objekt in der Zeitachse an.

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

<span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**dexterf- \_ Begrenzungs Zeichen**
</dt> <dd>

Sucht nach einem Objekt, das die angegebene Zeitspanne überspannt.

</dd> <dt>

<span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**dexterf \_ genau \_ um**
</dt> <dd>

Suchen Sie nach einem Objekt, das genau zum angegebenen Zeitpunkt gestartet wird.

</dd> <dt>

<span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**dexterf \_ weiterleiten**
</dt> <dd>

Suchen Sie nach einem Objekt, das zum angegebenen Zeitpunkt oder später gestartet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese begrenzungsbedingungen werden in der folgenden Tabelle zusammengefasst.



| Enumerationswert    | Begrenzungs Bedingung                        |
|----------------------|-------------------------------------------|
| dexterf- \_ Begrenzungs Zeichen    | Start <= timestoppt > Zeit<br/> |
| dexterf \_ genau \_ um | Start = = Zeit                             |
| dexterf \_ weiterleiten    | Start >= Zeit                          |



 

-   Start: Startzeit des abgerufenen Objekts.
-   Beendigung: die Endzeit des abgerufenen Objekts.
-   Time: angegebene Suchzeit.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Qedit. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimelinetrack:: gezr| Time**](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




