---
description: Die completeconnect-Methode schließt eine Verbindung mit einer Eingabe-PIN ab.
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: Cdynamicoutputpin. completeconnect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31afa592701b881d39ab4948514aacfe50b345b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367142"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a>Cdynamicoutputpin. completeconnect-Methode

Die- `CompleteConnect` Methode schließt eine Verbindung mit einer Eingabe-PIN ab.

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

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Eingabe-PIN.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbaseoutputpin:: completeconnect**](cbaseoutputpin-completeconnect.md) -Methode. Zur Unterstützung dynamischer Neuverbindungen führt diese Methode einen Commit für die Zuweisung aus, wenn der Filter aktiv ist. In der Basisklasse können Verbindungen nur auftreten, wenn der Filter angehalten wird, sodass für die Zuweisung immer ein Commit in der [**cbaseoutputpin:: Active**](cbaseoutputpin-active.md) -Methode ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




