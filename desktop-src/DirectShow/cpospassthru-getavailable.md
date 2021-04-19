---
description: 'Die getavailable-Methode ruft den Bereich der Zeiten ab, in denen die Suche effizient ist. Diese Methode implementiert die imediaseeking:: getavailable-Methode.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Cpospassthru. getavailable-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32dbba173caf933185602523dadcf71ce7ca3ef7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360414"
---
# <a name="cpospassthrugetavailable-method"></a>Cpospassthru. getavailable-Methode

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

Ein Zeiger auf eine Variable, die die früheste Zeit für eine effiziente Suche empfängt.

</dd> <dt>

*platest* 
</dt> <dd>

Ein Zeiger auf eine Variable, die den letzten Zeitpunkt für die effiziente Suche empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




