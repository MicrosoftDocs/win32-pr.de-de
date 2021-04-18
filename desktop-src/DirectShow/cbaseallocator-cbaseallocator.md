---
description: Konstruktormethode.
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Cbasezucator. cbasezucator-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98a1ba1163058f92fba666177d0ff82331dd528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358193"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a>Cbasezucator. cbasezucator-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den debugnamen der Zuweisung enthält. Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts. Andernfalls legen Sie diesen Parameter auf **null** fest.

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Wert. Legen Sie \_ vor dem Erstellen des Objekts den Wert auf S OK fest. Wenn der Konstruktor fehlschlägt, wird der Wert auf einen Fehlercode festgelegt.

</dd> <dt>

*bevent* 
</dt> <dd>

Boolescher Wert, der angibt, ob ein Semaphor erstellt werden soll. Wenn **true**, erstellt die Zuweisung ein Semaphor ([**cbasezucator:: m \_ hsem**](cbaseallocator-m-hsem.md)), das signalisiert wird, wenn ein Beispiel verfügbar wird. Legen Sie den Wert auf **false** fest, wenn Sie eine abgeleitete Klasse implementieren, die keine Semaphore erfordert.

</dd> <dt>

*fenablereleasecallback* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Release-Rückrufmechanismus aktiviert ist. Legen Sie den Wert auf **true** fest, wenn Sie eine Rückruf Schnittstelle angeben möchten, die aufgerufen wird, wenn Puffer freigegeben werden. Geben Sie den Rückruf an, indem Sie die [**cbasezucator:: setnotify**](cbaseallocator-setnotify.md) -Methode aufrufen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




