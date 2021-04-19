---
description: Konstruktormethode.
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: Ctransforminputpin. ctransforminputpin-Konstruktor (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39b99e3e2cf1437c1b35f68d9863a692746bd98d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370144"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a>Ctransforminputpin. ctransforminputpin-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CTransformInputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pobjectname* 
</dt> <dd>

Zeichenfolge, die den debugnamen des-Objekts enthält. Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).

</dd> <dt>

*ptransformfilter* 
</dt> <dd>

Ein Zeiger auf den Filter, der diese Pin erstellt hat, wobei es sich um ein [**ctransformfilter**](ctransformfilter.md) -Objekt handeln muss.

</dd> <dt>

*PHR* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist. Initialisieren Sie den Wert \_ vor dem Erstellen des-Objekts auf S OK. Der Wert wird nur geändert, wenn ein Fehler auftritt.

</dd> <dt>

*pName* 
</dt> <dd>

Breit Zeichen-Zeichenfolge, die den Pin-Namen enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der *PName* -Parameter gibt den Pin-Namen an, der von der [**IPin:: querypininfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) -Methode zurückgegeben wird. Die Zeichenfolge wird jedoch nicht für den PIN-Bezeichner verwendet. Der PIN-Bezeichner für diese Klasse ist immer "in". Weitere Informationen finden Sie unter [**QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




