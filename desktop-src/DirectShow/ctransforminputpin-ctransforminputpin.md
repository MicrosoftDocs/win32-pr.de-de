---
description: CTransformInputPin.CTransformInputPin-Konstruktor – Konstruktormethode.
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: CTransformInputPin.CTransformInputPin-Konstruktor (Transfrm.h)
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
ms.openlocfilehash: 4e893b4e1c7d4f396644a468d3d71fa3046fb712
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095048"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a>CTransformInputPin.CTransformInputPin-Konstruktor

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

*pObjectName* 
</dt> <dd>

Eine Zeichenfolge, die den Debugnamen des Objekts enthält. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pTransformFilter* 
</dt> <dd>

Zeiger auf den Filter, der diesen Pin erstellt hat, der ein [**CTransformFilter-Objekt sein**](ctransformfilter.md) muss.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt. Initialisieren Sie den Wert auf S \_ OK, bevor Sie das -Objekt erstellen. Der Wert wird nur geändert, wenn ein Fehler auftritt.

</dd> <dt>

*pName* 
</dt> <dd>

Breitzeichenzeichenfolge, die den Pinnamen enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der *pName-Parameter* gibt den Pinnamen an, der von der [**IPin::QueryPinInfo-Methode zurückgegeben**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) wird. Die Zeichenfolge wird jedoch nicht für den Pinbezeichner verwendet. Der Pinbezeichner für diese Klasse ist immer "In". Weitere Informationen finden Sie unter [**QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




