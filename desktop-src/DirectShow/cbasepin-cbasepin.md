---
description: 'CBasePin.CBasePin-Konstruktor: Konstruktormethode.'
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: CBasePin.CBasePin-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbeead09843aa8bf66471caeaabbdb42ee8d97d01cdaa9a54809f35c437b52d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916900"
---
# <a name="cbasepincbasepin-constructor"></a>CBasePin.CBasePin-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pObjectName* 
</dt> <dd>

Eine Zeichenfolge, die den Debugnamen für das Objekt enthält. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Zeiger auf den Filter, der diesen Pin erstellt hat.

</dd> <dt>

*Plock* 
</dt> <dd>

Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird. Kann derselbe kritische Abschnitt wie die Filtersperre [**sein: CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md).

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt. Initialisieren Sie den Wert auf S \_ OK, bevor Sie das -Objekt erstellen. Der Wert wird nur geändert, wenn ein Fehler auftritt.

</dd> <dt>

*pName* 
</dt> <dd>

Breitzeichenzeichenfolge, die den Namen der Stecknadel enthält. Weitere Informationen finden Sie unter [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).

</dd> <dt>

*dir* 
</dt> <dd>

Member der [**PIN \_ DIRECTION-Enumeration,**](/windows/win32/api/strmif/ne-strmif-pin_direction) der die Richtung des Pins an gibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der von *pLock* angegebene kritische Abschnitt serialisiert den Zustand des Pins, einschließlich des Verbindungsstatus, der Auswahl der Zuweisung, des Medientyps und des Status von Leerungsvorgängen. Verwenden Sie diesen kritischen Abschnitt nicht zum Serialisieren von Streamingvorgängen. Weitere Informationen finden Sie unter [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).

Ein Filter erstellt möglicherweise Pins in seiner Konstruktormethode, sodass der *pFilter-Zeiger* an diesem Punkt möglicherweise nicht auf ein gültiges Objekt verweisen kann. Store den Zeiger, dereferenzieren Sie ihn jedoch nicht, während sie sich im Konstruktor des Pins befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




