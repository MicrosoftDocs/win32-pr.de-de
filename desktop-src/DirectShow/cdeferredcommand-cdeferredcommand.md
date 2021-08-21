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
ms.openlocfilehash: 03c45979437c153e70aea16c6b6e48b052b0d84491dcd1880075c66c77c777d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822225"
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

Zeiger auf ein Objekt, das die [**IQueueCommand-Schnittstelle**](/windows/desktop/api/Control/nn-control-iqueuecommand) verfügbar macht.

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

Zeiger auf das Objekt, das diesen Befehl ausführt.

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

Methode für die aufzurufende Schnittstelle.

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

Zeiger auf eine zurückgegebene Variantentypliste, falls vorhanden.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Zeiger auf das letzte Argument in der *pDispParams-Parameterliste* mit einem Fehler.

</dd> <dt>

*bStream* 
</dt> <dd>

Wert, der angibt, ob die verzögerte Befehlszeit in der Streamzeit (**TRUE**) oder der Präsentationszeit (**FALSE**) liegt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDeferredCommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




