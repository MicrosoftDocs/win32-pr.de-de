---
description: 'CTransInPlaceOutputPin.CTransInPlaceOutputPin-Konstruktor : Konstruktormethode.'
ms.assetid: fe7b2d62-0e6a-4253-b469-6cede5dc9bb1
title: CTransInPlaceOutputPin.CTransInPlaceOutputPin-Konstruktor (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: faf8b2cf0a4f1def8ea89ad04bd013d3867ff5a456e6c8922f72a078d860df92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654778"
---
# <a name="ctransinplaceoutputpinctransinplaceoutputpin-constructor"></a>CTransInPlaceOutputPin.CTransInPlaceOutputPin-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CTransInPlaceOutputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pObjectName* 
</dt> <dd>

Eine Zeichenfolge, die den Debugnamen des Objekts enthält. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Zeiger auf den Filter, der diesen Pin erstellt hat, der ein [**CTransInPlaceFilter-Objekt sein**](ctransinplacefilter.md) muss.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt. Initialisieren Sie den Wert auf S \_ OK, bevor Sie das -Objekt erstellen. Der Wert wird nur geändert, wenn ein Fehler auftritt.

</dd> <dt>

*pName* 
</dt> <dd>

Breitzeichenzeichenfolge, die den Pinnamen enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der *pName-Parameter* gibt den Pinnamen an, der von der [**IPin::QueryPinInfo-Methode zurückgegeben**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) wird. Die Zeichenfolge wird jedoch nicht für den Pinbezeichner verwendet. Der Pinbezeichner für diese Klasse ist immer "Out". Weitere Informationen finden Sie unter [**QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceOutputPin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




