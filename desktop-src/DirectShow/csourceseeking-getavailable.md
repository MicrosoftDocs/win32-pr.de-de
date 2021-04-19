---
description: 'Die getavailable-Methode ruft den Bereich der Zeiten ab, in denen die Suche effizient ist. Diese Methode implementiert die imediaseeking:: getavailable-Methode.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Csourceseeking. getavailable-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc661d81c49798b6fe06dc569b680e5f9839e5a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359407"
---
# <a name="csourceseekinggetavailable-method"></a>Csourceseeking. getavailable-Methode

Die- `GetAvailable` Methode ruft den Bereich der Zeiten ab, in denen die Suche effizient ist. Diese Methode implementiert die [**imediaseeking:: getavailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pearliest* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die früheste Zeit für eine effiziente Suche empfängt. Die-Variable ist auf 0 (null) festgelegt.

</dd> <dt>

*platest* 
</dt> <dd>

Ein Zeiger auf eine Variable, die den letzten Zeitpunkt für die effiziente Suche empfängt. Die-Variable wird auf den Wert der [**csourceseeking:: m \_ rtduration**](csourceseeking-m-rtduration.md) -Element Variablen festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




