---
description: 'Die Block-Methode blockiert oder entsperrt den Datenfluss aus der PIN. Diese Methode implementiert die IPinFlowControl:: Block-Methode.'
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Cdynamicoutputpin. Block-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b10e9dfd43f3ad98adf8f6abb0eb7c2223d5970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370847"
---
# <a name="cdynamicoutputpinblock-method"></a>Cdynamicoutputpin. Block-Methode

Die- `Block` Methode blockiert bzw. entsperrt den Datenfluss aus der PIN. Diese Methode implementiert die [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwblockflags* 
</dt> <dd>

Flag, das angibt, ob die PIN blockiert oder freizugeben ist. Dies muss einer der folgenden Werte sein:

Zero: entsperrt den Datenfluss von der PIN.

AM \_ Pin- \_ Fluss \_ Steuerungs \_ Block: blockiert den Datenfluss von der PIN.

</dd> <dt>

*hevent* 
</dt> <dd>

Handle für ein Ereignis Objekt oder **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                                                    | Beschreibung                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                                        | Die Blockierung der PIN wurde bereits aufgehoben.<br/>                     |
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Erfolg.<br/>                                      |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>                                   | Ungültiges Argument.<br/>                             |
| <dl> <dt>**VFW \_ E \_ Pin \_ bereits \_ blockiert**</dt> </dl>                   | Die PIN ist bereits in einem anderen Thread blockiert.<br/>     |
| <dl> <dt>**VFW \_ E \_ Pin \_ ist \_ \_ in \_ diesem \_ Thread bereits blockiert.**</dt> </dl> | Die PIN ist bereits im aufrufenden Thread blockiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu dieser Methode finden Sie unter [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block). Intern ruft diese Methode eine der folgenden geschützten Methoden auf:

-   Block (Asynchronous): [ **cdynamicoutputpin:: asynchronousblockoutputpin**](cdynamicoutputpin-asynchronousblockoutputpin.md)
-   Block (synchron): [ **cdynamicoutputpin:: synchronousblockoutputpin**](cdynamicoutputpin-synchronousblockoutputpin.md)
-   Unblock: [ **cdynamicoutputpin:: unblockoutputpin**](cdynamicoutputpin-unblockoutputpin.md)

Das Aufheben der Blockierung erfolgt immer synchron.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




