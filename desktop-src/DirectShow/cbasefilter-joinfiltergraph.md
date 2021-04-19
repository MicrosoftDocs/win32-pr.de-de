---
description: 'Die joinfiltergraph-Methode benachrichtigt den Filter, dass ein Filter Diagramm verknüpft oder Links ist. Diese Methode implementiert die ibasefilter:: joinfiltergraph-Methode.'
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: Cbasefilter. joinfiltergraph-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45453c6423b8fa9f68e5d8dff86d13b130d65f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367754"
---
# <a name="cbasefilterjoinfiltergraph-method"></a>Cbasefilter. joinfiltergraph-Methode

Mit der- `JoinFilterGraph` Methode wird der Filter benachrichtigt, dass ein Filter Diagramm verknüpft oder Links ist. Diese Methode implementiert die [**ibasefilter:: joinfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PGraph* 
</dt> <dd>

Ein Zeiger auf die [**ifiltergraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) -Schnittstelle des Filter Diagramm-Managers oder **null** , wenn der Filter das Diagramm verlässt.

</dd> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die einen Namen für den Filter enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt die [**cbasefilter:: m \_ PGraph**](cbasefilter-m-pgraph.md) -Member-Variable auf den *PGraph* -Parameter fest. Außerdem wird ein [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstellen Zeiger abgefragt und in der [**cbasefilter:: m \_ psink**](cbasefilter-m-psink.md) -Element Variablen gespeichert. Der Filter behält jedoch keinen Verweis Zähler für eine dieser Schnittstellen bei. Dies würde einen Zirkel Verweis Zähler erzeugen, da der Filter Graph-Manager einen Verweis Zähler für den Filter beibehält.

Die-Methode kopiert die durch " *PName* " angegebene Zeichenfolge in die " [**cbasefilter:: m \_ PName**](cbasefilter-m-pname.md) "-Member-Variable.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




