---
description: Die completeconnect-Methode schließt eine Verbindung mit einer Eingabe-PIN ab.
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: Cbaseoutputpin. completeconnect-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4614e8531a21d88a1c2f4cfd75fcbe05a9210f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369124"
---
# <a name="cbaseoutputpincompleteconnect-method"></a>Cbaseoutputpin. completeconnect-Methode

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

Zeiger auf die eingabepin.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasepin:: completeconnect**](cbasepin-completeconnect.md) -Methode. Sie ruft die [**decidezuordcator**](cbaseoutputpin-decideallocator.md) -Methode auf, die die für diese Verbindung zu verwendende Speicherzuweisung auswählt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




