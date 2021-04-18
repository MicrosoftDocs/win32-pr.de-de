---
description: Die matchespartial-Methode bestimmt, ob dieser Medientyp mit einem teilweise angegebenen Medientyp übereinstimmt.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Cmediatype. matchespartial-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372632"
---
# <a name="cmediatypematchespartial-method"></a>Cmediatype. matchespartial-Methode

Die- `MatchesPartial` Methode bestimmt, ob dieser Medientyp mit einem teilweise angegebenen Medientyp übereinstimmt.

## <a name="syntax"></a>Syntax


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppartiell* 
</dt> <dd>

Zeiger auf den Medientyp, der abgeglichen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Medientypen Stimmen. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Der von *ppartial* angegebene Medientyp kann den Wert GUID \_ NULL für den Haupttyp, den Untertyp oder den Formattyp aufweisen. Alle Elemente mit GUID- \_ NULL-Werten werden nicht getestet. (In der Tat GUID \_ Null fungiert als Platzhalter.) Member mit anderen Werten als GUID \_ null müssen mit dem Medientyp identisch sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediatype-Klasse**](cmediatype.md)
</dt> </dl>

 

 




