---
description: Die CompleteConnect-Methode schließt die Verbindung des Eingabepins mit einem anderen Pin ab.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: CBaseRenderer.CompleteConnect-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 833e19a6e7b100aac5322a54455c04c263569e33b3422d5957e5eeee15bbd283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157841"
---
# <a name="cbaserenderercompleteconnect-method"></a>CBaseRenderer.CompleteConnect-Methode

Die `CompleteConnect` -Methode schließt die Verbindung des Eingabepins mit einem anderen Pin ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Ausgabepins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Der Eingabepin des Filters ruft diese Methode aus der eigenen Methode heraus `CompleteConnect` auf, die aufgerufen wird, um eine Pinverbindung abzuschließen. (Weitere Informationen finden Sie unter [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md).) Der Filter ruft die [**CBaseRenderer::SetRepaintStatus-Methode**](cbaserenderer-setrepaintstatus.md) auf, um [**EC \_ REPAINT-Ereignisse**](ec-repaint.md) zu aktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




