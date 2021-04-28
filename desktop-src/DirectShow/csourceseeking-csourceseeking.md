---
description: 'CSourceSeeking.CSourceSeeking-Konstruktor : Konstruktormethode.'
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: CSourceSeeking.CSourceSeeking-Konstruktor (Ctlutil.h)
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
ms.openlocfilehash: 7fcca70408e76466a88c620e3907271d49930973
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098818"
---
# <a name="csourceseekingcsourceseeking-constructor"></a>CSourceSeeking.CSourceSeeking-Konstruktor

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

Zeiger auf eine Zeichenfolge, die den Namen des Objekts enthält. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts. Legen Sie andernfalls diesen Parameter auf **NULL fest.**

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Ignoriert.

</dd> <dt>

*Plock* 
</dt> <dd>

Zeiger auf ein [**CCritSec-Objekt.**](ccritsec.md) Deklarieren Sie in der abgeleiteten Klasse eine **CCritSec-Membervariable,** und verwenden Sie die Adresse für diesen Parameter. Die -Klasse verwendet diesen kritischen Abschnitt, um den Zugriff auf die Start- und `CSourceSeeking` Stoppzeiten, die Dauer und die Wiedergaberate zu synchronisieren. Halten Sie diese Sperre bei jedem Zugriff auf diese Variablen in Ihrer abgeleiteten Klasse bei.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




