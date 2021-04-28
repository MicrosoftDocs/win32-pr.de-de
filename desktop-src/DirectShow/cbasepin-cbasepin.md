---
description: 'CBasePin.CBasePin-Konstruktor : Konstruktormethode.'
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
ms.openlocfilehash: f11dea6bd5bc3f766e5f93a04022dab5ba6e51a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099428"
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

Zeichenfolge, die den Debugnamen für das Objekt enthält. Weitere Informationen finden Sie unter [**CBaseObject.**](cbaseobject.md)

</dd> <dt>

*pFilter* 
</dt> <dd>

Zeiger auf den Filter, der diese Stecknadel erstellt hat.

</dd> <dt>

*Plock* 
</dt> <dd>

Zeiger auf eine [**CCritSec-Sperre,**](ccritsec.md) die zum Serialisieren von Zustandsänderungen verwendet wird. Kann derselbe kritische Abschnitt wie die Filtersperre sein, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md).

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt. Initialisieren Sie den Wert vor dem Erstellen des -Objekts mit S \_ OK. Der Wert wird nur geändert, wenn ein Fehler auftritt.

</dd> <dt>

*pName* 
</dt> <dd>

Breitzeichenzeichenfolge, die den Namen der Stecknadel enthält. Weitere Informationen finden Sie unter [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).

</dd> <dt>

*dir* 
</dt> <dd>

Member der [**PIN \_ DIRECTION-Enumeration,**](/windows/win32/api/strmif/ne-strmif-pin_direction) der die Richtung des Pins angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der von *pLock* angegebene kritische Abschnitt serialisiert den Zustand des Pins, einschließlich des Verbindungsstatus, der Auswahl der Zuweisung, des Medientyps und des Status von Leerungsvorgängen. Verwenden Sie diesen kritischen Abschnitt nicht zum Serialisieren von Streamingvorgängen. Weitere Informationen finden Sie unter [Datenfluss im Filterdiagramm](data-flow-in-the-filter-graph.md).

Ein Filter erstellt möglicherweise Pins in seiner Konstruktormethode, sodass der *pFilter-Zeiger* an diesem Punkt möglicherweise nicht auf ein gültiges Objekt verweisen kann. Speichern Sie den Zeiger, dereferenzieren Sie ihn jedoch nicht im Konstruktor des Pins.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




