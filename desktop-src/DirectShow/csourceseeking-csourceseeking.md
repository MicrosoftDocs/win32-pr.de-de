---
description: Konstruktormethode.
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: Csourceseeking. csourceseeking-Konstruktor (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 309e926ddf001cf9933b19334992f5210fc7f17b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371466"
---
# <a name="csourceseekingcsourceseeking-constructor"></a>Csourceseeking. csourceseeking-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält. Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts. Andernfalls legen Sie diesen Parameter auf **null** fest.

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Wert. Ignoriert.

</dd> <dt>

*Plock* 
</dt> <dd>

Zeiger auf ein [**ccritsec**](ccritsec.md) -Objekt. Deklarieren Sie in der abgeleiteten Klasse eine **ccritsec** -Member-Variable, und verwenden Sie die Adresse des Parameters für diesen Parameter. Die- `CSourceSeeking` Klasse verwendet diesen kritischen Abschnitt, um den Zugriff auf die Start-und Endzeit-, Dauer-und Wiedergabe Rate zu synchronisieren. Wenn Sie auf diese Variablen in der abgeleiteten Klasse zugreifen, behalten Sie diese Sperre bei.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




