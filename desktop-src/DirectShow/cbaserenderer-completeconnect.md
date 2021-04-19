---
description: Die completeconnect-Methode schließt die Verbindung der Eingabe-PIN mit einer anderen Pin ab.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Cbaserderderer. completeconnect-Methode (renbase. h)
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
ms.openlocfilehash: a9d2d35f99a3b3b8dc5b668b8ee9a9f94f0a53dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367658"
---
# <a name="cbaserenderercompleteconnect-method"></a>Cbaserderderer. completeconnect-Methode

Die `CompleteConnect` -Methode schließt die Verbindung der Eingabe-PIN mit einer anderen Pin ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*preceivepin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Ausgabe-PIN.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die Eingabe-PIN des Filters ruft diese Methode in der eigenen `CompleteConnect` Methode auf, die aufgerufen wird, um eine PIN-Verbindung abzuschließen. (Weitere Informationen finden Sie unter [**cbasepin:: completeconnect**](cbasepin-completeconnect.md).) Der Filter Ruft die [**cbaserdenderer:: settrepaintstatus**](cbaserenderer-setrepaintstatus.md) -Methode auf, um [**EC- \_ Repaint**](ec-repaint.md) -Ereignisse zu aktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




