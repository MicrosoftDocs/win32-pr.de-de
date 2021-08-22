---
description: Die Block-Methode blockiert oder entsperrt den Datenfluss vom Pin. Diese Methode implementiert die IPinFlowControl::Block-Methode.
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: CDynamicOutputPin.Block-Methode (Amfilter.h)
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
ms.openlocfilehash: 6cc0a601ee1adbff9254baeff029c26d0cea359c7b2770b4d518bad916aca09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074284"
---
# <a name="cdynamicoutputpinblock-method"></a>CDynamicOutputPin.Block-Methode

Die `Block` -Methode blockiert oder entsperrt den Datenfluss vom Pin. Diese Methode implementiert die [**IPinFlowControl::Block-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block)

## <a name="syntax"></a>Syntax


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwBlockFlags* 
</dt> <dd>

Flag, das angibt, ob die Stecknadel blockiert oder entsperrt werden soll. Dies muss einer der folgenden Werte sein:

0 (null): Aufheben der Blockierung des Datenflusses vom Pin.

AM \_ PIN FLOW CONTROL \_ \_ \_ BLOCK: Datenfluss vom Pin blockieren.

</dd> <dt>

*hEvent* 
</dt> <dd>

Handle für ein Ereignisobjekt oder **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                                                    | Beschreibung                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                                        | Die Blockierung der Stecknadel wurde bereits aufgehoben.<br/>                     |
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Erfolg.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                   | Ungültiges Argument.<br/>                             |
| <dl> <dt>**VFW \_ \_ E-PIN \_ BEREITS \_ BLOCKIERT**</dt> </dl>                   | Das Anheften ist bereits in einem anderen Thread blockiert.<br/>     |
| <dl> <dt>**VFW \_ \_ E-PIN \_ FÜR \_ DIESEN \_ \_ \_ THREAD BEREITS BLOCKIERT**</dt> </dl> | Pin ist im aufrufenden Thread bereits blockiert.<br/> |



 

## <a name="remarks"></a>Hinweise

Weitere Informationen zu dieser Methode finden Sie unter [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block). Intern ruft diese Methode eine der folgenden geschützten Methoden auf:

-   Blockieren (asynchron): [ **CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)
-   Block (synchron): [ **CDynamicOutputPin::SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)
-   Blockierung aufheben: [ **CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)

Die Blockierung wird immer synchron ausgeführt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




