---
description: Die Verbinden-Methode schließt eine Verbindung mit dem Ausgabepin ab.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: CPullPin. Verbinden-Methode (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37240be1b732410d1e91974922f8ed7dc464b57b2596faa381c646a7513daf26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073504"
---
# <a name="cpullpinconnect-method"></a>CPullPin. Verbinden-Methode

Die `Connect` -Methode schließt eine Verbindung mit dem Ausgabepin ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Punk* 
</dt> <dd>

Zeiger auf die **IUnknown-Schnittstelle** des Ausgabepins.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der bevorzugten Zuweisung des Eingabepins oder **NULL.**

</dd> <dt>

*bSync* 
</dt> <dd>

Boolescher Wert, der angibt, ob synchrone Lesefunktionen verwendet werden sollen. True gibt an, dass der Pin synchrone Lesevorgänge auf dem Ausgabepin ausführt. False gibt an, dass der Pin asynchrone Leseanforderungen stellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **HRESULT zurück.** Die folgenden Werte sind möglich.



| Rückgabecode                                                                                               | Beschreibung                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Erfolg.<br/>                                                             |
| <dl> <dt>**VFW \_ E \_ BEREITS \_ VERBUNDEN**</dt> </dl> | Der Eingabepin ist bereits verbunden.<br/>                                  |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>             | Der Ausgabepin macht [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)nicht verfügbar.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode während des Verbindungsprozesses des Eingabepins auf. Wenn die Methode fehlschlägt, sollte die Verbindung mit dem Pin fehlschlagen.

Diese Methode fragt den Ausgabepin für die **IAsyncReader-Schnittstelle** ab. Bei Erfolg ruft sie [**CPullPin::D ecideAllocator**](cpullpin-decideallocator.md) auf, um die Zuweisung für die Verbindung auszuhandeln. Wenn Ihr Eingabepin über eine bevorzugte Zuweisung verfügt, geben Sie ihn im *pAlloc-Parameter* an. Die **DecideAllocator-Methode** übergibt diesen Zeiger an die [**IAsyncReader::RequestAllocator-Methode**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) des Ausgabepins. Legen Sie andernfalls *pAlloc* auf **NULL** fest.

Wenn der Wert von *bSync* **TRUE** ist, stellt das **CPullPin-Objekt** synchrone Leseanforderungen, indem das [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)des Ausgabepins aufgerufen wird. Andernfalls wird die [**IAsyncReader::Request-Methode**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) aufgerufen, um überlappende Leseanforderungen zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




