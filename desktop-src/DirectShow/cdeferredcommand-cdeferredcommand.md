---
description: CDeferredCommand.CDeferredCommand-Konstruktor – Konstruktormethode.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: CDeferredCommand.CDeferredCommand-Konstruktor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a10d8bba48902ed2d6fd66da8483cea1ba9aacc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119788"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a>CDeferredCommand.CDeferredCommand-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pq* 
</dt> <dd>

Zeiger auf ein Objekt, das die [**IQueueCommand-Schnittstelle verfügbar**](/windows/desktop/api/Control/nn-control-iqueuecommand) macht.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf die äußere **IUnknown-Schnittstelle** für die Aggregation.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen zurückgegebenen **HRESULT-Wert.**

</dd> <dt>

*pUnkExecutor* 
</dt> <dd>

Zeiger auf das Objekt, von dem dieser Befehl ausgeführt wird.

</dd> <dt>

*time* 
</dt> <dd>

Zeitpunkt, zu dem der Befehl ausgeführt wird.

</dd> <dt>

*Iid* 
</dt> <dd>

Zeiger auf den global eindeutigen Bezeichner **(GUID)** der Schnittstelle, die die -Methode enthält.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Methode für die aufrufende Schnittstelle.

</dd> <dt>

*wFlags* 
</dt> <dd>

Kontext des Aufrufs.

</dd> <dt>

*cArgs* 
</dt> <dd>

Anzahl der übergebenen Argumente.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Zeiger auf eine Liste von Argumentvariantentypen.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Zeiger auf eine zurückgegebene Liste von Variantentypen, sofern diese enthalten ist.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Zeiger auf das letzte Argument in der *pDispParams-Parameterliste* mit einem Fehler.

</dd> <dt>

*bStream* 
</dt> <dd>

Wert, der angibt, ob die verzögerte Befehlszeit in der Streamzeit (**TRUE**) oder in der Präsentationszeit ( FALSE )**liegt.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDeferredCommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




