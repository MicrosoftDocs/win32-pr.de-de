---
description: Konstruktormethode.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Cdeferredcommand. cdeferredcommand-Konstruktor (ctlutil. h)
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
ms.openlocfilehash: 4e92a2ffc5129ee38fc5061b28ea7ffef49da0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371560"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a>Cdeferredcommand. cdeferredcommand-Konstruktor

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

*PQ* 
</dt> <dd>

Zeiger auf ein Objekt, das die [**iqueuecommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) -Schnittstelle verfügbar macht.

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf die äußere **IUnknown** -Schnittstelle für die Aggregation.

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen zurückgegebenen **HRESULT** -Wert.

</dd> <dt>

*punkexecutor* 
</dt> <dd>

Zeiger auf das-Objekt, das diesen Befehl ausführen soll.

</dd> <dt>

*time* 
</dt> <dd>

Der Zeitpunkt, zu dem der Befehl ausgeführt wird.

</dd> <dt>

*IID* 
</dt> <dd>

Ein Zeiger auf die Globally Unique Identifier (**GUID**) der Schnittstelle, die die Methode enthält.

</dd> <dt>

*dispidmethod* 
</dt> <dd>

-Methode für die aufzurufende Schnittstelle.

</dd> <dt>

*wFlags* 
</dt> <dd>

Der Kontext des aufaufruf.

</dd> <dt>

*kargs* 
</dt> <dd>

Anzahl der über gebenen Argumente.

</dd> <dt>

*pdispparameams* 
</dt> <dd>

Zeiger auf eine Liste von Argument Variant-Typen.

</dd> <dt>

*pVarResult* 
</dt> <dd>

Zeiger auf eine zurückgegebene Varianttyp Liste, falls vorhanden.

</dd> <dt>

*gibt puArgErr* 
</dt> <dd>

Zeiger auf das letzte Argument in der *pDispParams* -Parameterliste mit einem Fehler.

</dd> <dt>

*bStream* 
</dt> <dd>

Ein Wert, der angibt, ob die verzögerte Befehls Zeit in der streamzeit (**true**) oder in der Präsentationszeit (**false**) liegt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdeferredcommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




