---
description: 'Die completeconnect-Methode schließt eine Verbindung mit einer Ausgabe-PIN ab. Diese Methode überschreibt die cbasepin:: completeconnect-Methode.'
ms.assetid: 32d95815-e018-4724-8cf3-8cd093ede517
title: Crendererinputpin. completeconnect-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e868693308d40fb786f201a9d7f056dd88326ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364473"
---
# <a name="crendererinputpincompleteconnect-method"></a>Crendererinputpin. completeconnect-Methode

Die- `CompleteConnect` Methode schließt eine Verbindung mit einer-Ausgabepin ab. Diese Methode überschreibt die [**cbasepin:: completeconnect**](cbasepin-completeconnect.md) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*preceivepin* 
</dt> <dd>

Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Ausgabe-PIN

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Crendererinputpin-Klasse**](crendererinputpin.md)
</dt> </dl>

 

 




