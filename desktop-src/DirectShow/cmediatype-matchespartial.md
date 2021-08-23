---
description: Die MatchesPartial-Methode bestimmt, ob dieser Medientyp einem teilweise angegebenen Medientyp entspricht.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: CMediaType.MatchesPartial-Methode (Mtype.h)
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
ms.openlocfilehash: a6049ad4526d8776b25e81fe4d75b727196f8fa1251a1959662cca71b161fbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073974"
---
# <a name="cmediatypematchespartial-method"></a>CMediaType.MatchesPartial-Methode

Die `MatchesPartial` -Methode bestimmt, ob dieser Medientyp einem teilweise angegebenen Medientyp entspricht.

## <a name="syntax"></a>Syntax


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppartial* 
</dt> <dd>

Zeiger auf den medientyp, der übereinstimmen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Medientypen übereinstimmen. Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Der von *ppartial* angegebene Medientyp kann den Wert GUID NULL für den Haupttyp, Untertyp oder \_ Formattyp haben. Member mit \_ GUID-NULL-Werten werden nicht getestet. (Tatsächlich GUID \_ NULL fungiert als Platzhalter.) Member mit anderen Werten als GUID \_ NULL müssen übereinstimmen, damit der Medientyp übereinstimmen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




