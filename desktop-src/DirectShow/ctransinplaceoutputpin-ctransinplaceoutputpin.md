---
description: CTransInPlaceOutputPin.CTransInPlaceOutputPin-Konstruktor – Konstruktormethode.
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
ms.openlocfilehash: d6b63ee3aa52bc0363bcab90275be4148659b3bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094708"
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

Zeichenfolge, die den Debugnamen des Objekts enthält. Weitere Informationen finden Sie unter [**CBaseObject.**](cbaseobject.md)

</dd> <dt>

*pFilter* 
</dt> <dd>

Zeiger auf den Filter, der diesen Pin erstellt hat, der ein [**CTransInPlaceFilter-Objekt**](ctransinplacefilter.md) sein muss.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt. Initialisieren Sie den Wert vor dem Erstellen des -Objekts mit S \_ OK. Der Wert wird nur geändert, wenn ein Fehler auftritt.

</dd> <dt>

*pName* 
</dt> <dd>

Breitzeichenzeichenfolge, die den Pinnamen enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der *pName-Parameter* gibt den Pinnamen an, der von der [**IPin::QueryPinInfo-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) zurückgegeben wird. Die Zeichenfolge wird jedoch nicht für den Stecknadelbezeichner verwendet. Der Stecknadelbezeichner für diese Klasse ist immer "Out". Weitere Informationen finden Sie unter [**QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceOutputPin-Klasse**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




