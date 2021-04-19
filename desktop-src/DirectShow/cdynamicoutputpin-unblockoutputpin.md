---
description: Die unblockoutputpin-Methode hebt die Blockierung der PIN auf. Wenn die Blockierung der PIN aufgehoben wird, kann Sie Beispiele liefern, das Ausgabeformat ändern und die Verbindung wiederherstellen.
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: Cdynamicoutputpin. unblockoutputpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370284"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a>Cdynamicoutputpin. unblockoutputpin-Methode

Die- `UnblockOutputPin` Methode hebt die Blockierung der PIN auf. Wenn die Blockierung der PIN aufgehoben wird, kann Sie Beispiele liefern, das Ausgabeformat ändern und die Verbindung wiederherstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                             | Beschreibung                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Die Blockierung der PIN war bereits aufgehoben.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




