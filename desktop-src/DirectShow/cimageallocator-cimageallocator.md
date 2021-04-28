---
description: 'CImageAllocator.CImageAllocator-Konstruktor : Konstruktormethode.'
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: CImageAllocator.CImageAllocator-Konstruktor (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f17ae78b668f6cc35e454c5e4e83d38727077ef7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085758"
---
# <a name="cimageallocatorcimageallocator-constructor"></a>CImageAllocator.CImageAllocator-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFilter* 
</dt> <dd>

Zeiger auf den besitzenden Filter.

</dd> <dt>

*pName* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Debugnamen der Zuweisung enthält. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Legen Sie den Wert auf S \_ OK fest, bevor Sie das -Objekt erstellen. Wenn der Konstruktor fehlschlägt, wird der Wert auf einen Fehlercode festgelegt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CImageAllocator-Klasse**](cimageallocator.md)
</dt> </dl>

 

 




