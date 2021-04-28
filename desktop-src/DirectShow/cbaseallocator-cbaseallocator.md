---
description: 'CBaseAllocator.CBaseAllocator-Konstruktor : Konstruktormethode.'
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: CBaseAllocator.CBaseAllocator-Konstruktor (Amfilter.h)
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
ms.openlocfilehash: dfda2b03d1ddb3f4a8ad5f4446dbee997da4e790
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096359"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a>CBaseAllocator.CBaseAllocator-Konstruktor

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

Zeiger auf eine Zeichenfolge, die den Debugnamen der Zuweisung enthält. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts. Legen Sie andernfalls diesen Parameter auf **NULL fest.**

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Legen Sie den Wert auf S \_ OK fest, bevor Sie das -Objekt erstellen. Wenn der Konstruktor fehlschlägt, wird der Wert auf einen Fehlercode festgelegt.

</dd> <dt>

*bEvent* 
</dt> <dd>

Boolescher Wert, der angibt, ob ein Semaphor erstellt werden soll. True **gibt an,** dass die Zuweisung ein Semaphor ([**CBaseAllocator::m \_ hSem**](cbaseallocator-m-hsem.md)) erstellt, das signalisiert wird, wenn ein Beispiel verfügbar wird. Legen Sie den Wert auf **FALSE** fest, wenn Sie eine abgeleitete Klasse implementieren, die kein Semaphor erfordert.

</dd> <dt>

*fEnableReleaseCallback* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Releaserückrufmechanismus aktiviert ist. Legen Sie den Wert auf **TRUE** fest, wenn Sie eine Rückrufschnittstelle bereitstellen möchten, die aufgerufen wird, wenn Puffer freigegeben werden. Geben Sie den Rückruf an, indem Sie die [**CBaseAllocator::SetNotify-Methode**](cbaseallocator-setnotify.md) aufrufen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseAllocator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




