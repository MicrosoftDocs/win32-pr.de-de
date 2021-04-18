---
description: Konstruktormethode.
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Cbasepin. cbasepin-Konstruktor (amfilter. h)
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
ms.openlocfilehash: dd4883d3d8e906e1da2f377344b735037c5e5cd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372475"
---
# <a name="cbasepincbasepin-constructor"></a>Cbasepin. cbasepin-Konstruktor

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

*pobjectname* 
</dt> <dd>

Zeichenfolge, die den debugnamen für das Objekt enthält. Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Zeiger auf den Filter, der diese Pin erstellt hat.

</dd> <dt>

*Plock* 
</dt> <dd>

Zeiger auf eine [**ccritsec**](ccritsec.md) -Sperre, mit der Zustandsänderungen serialisiert werden. Kann derselbe kritische Abschnitt wie die Filter Sperre sein, [**cbasefilter:: m \_ Plock**](cbasefilter-m-plock.md).

</dd> <dt>

*PHR* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist. Initialisieren Sie den Wert \_ vor dem Erstellen des-Objekts auf S OK. Der Wert wird nur geändert, wenn ein Fehler auftritt.

</dd> <dt>

*pName* 
</dt> <dd>

Zeichenfolge mit breit Zeichen, die den Namen der PIN enthält. Weitere Informationen finden Sie unter [**cbasepin:: querypininfo**](cbasepin-querypininfo.md).

</dd> <dt>

*dir* 
</dt> <dd>

Member der [**Pin- \_ Richtungs**](/windows/win32/api/strmif/ne-strmif-pin_direction) Enumeration, die die Richtung der PIN angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der von *Plock* angegebene kritische Abschnitt serialisiert den Zustand der PIN, einschließlich des Verbindungsstatus, der Auswahl der Zuweisung, des Medientyps und des Status von Leerungs Vorgängen. Verwenden Sie diesen kritischen Abschnitt nicht zum Serialisieren von Streamingvorgängen. Weitere Informationen finden Sie unter [Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md).

Ein Filter kann Pins in seiner Konstruktormethode erstellen. daher verweist der *pFilter* -Zeiger an diesem Punkt möglicherweise nicht auf ein gültiges Objekt. Speichern Sie den Zeiger, aber heben Sie ihn nicht im Konstruktor der PIN auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




