---
description: Die New-Methode initialisiert einen auszuführenden Befehl und gibt ein neues CDeferredCommand-Objekt zurück.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: CCmdQueue.New-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b6ad22b67df863e699649f22f513a98ca1306751a1d449a683f306c9cc2938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910390"
---
# <a name="ccmdqueuenew-method"></a>CCmdQueue.New-Methode

Die `New` -Methode initialisiert einen auszuführenden Befehl und gibt ein neues [**CDeferredCommand-Objekt**](cdeferredcommand.md) zurück.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppCmd* 
</dt> <dd>

Adresse eines Zeigers auf ein [**CDeferredCommand-Objekt,**](cdeferredcommand.md) mit dem eine Anwendung den Befehl abbrechen, eine neue Präsentationszeit dafür festlegen oder Schätzungsinformationen abrufen kann.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf das Objekt, das den Befehl ausführen soll.

</dd> <dt>

*time* 
</dt> <dd>

Zeitpunkt, zu dem der Befehl oder die Befehle in der Warteschlange ausgeführt werden sollen.

</dd> <dt>

*Iid* 
</dt> <dd>

Zeiger auf den global eindeutigen Bezeichner **(GUID)** der aufzurufenden Schnittstelle.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Die -Methode für die -Schnittstelle, die aufgerufen werden soll.

</dd> <dt>

*wFlags* 
</dt> <dd>

Flags, die den Kontext des Aufrufs beschreiben. Dieser Parameter unterstützt die gleichen Flags wie die **IDispatch::Invoke-Methode.**

</dd> <dt>

*cArgs* 
</dt> <dd>

Anzahl der übergebenen Argumente.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Zeiger auf die Liste der Variantentypen, die den Dispatchparametern zugeordnet sind.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Zeiger auf die Liste, in der Ggf. Ergebnisse zurückgegeben werden sollen.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Zeiger auf den Index in der *pDispParams-Parameterliste,* an dem der letzte Fehler aufgetreten ist.

</dd> <dt>

*bStream* 
</dt> <dd>

Wert, der angibt, ob der *Time-Parameter* ein Streamzeitwert (**TRUE**) oder ein Präsentationszeitwert (**FALSE**) ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK zurück. Gibt E \_ OUTOFMEMORY zurück, wenn *ppCmd* vom Erstellen des neuen [**CDeferredCommand-Objekts**](cdeferredcommand.md) mit dem Wert **NULL** zurückgibt. Andernfalls gibt ein **HRESULT** zurück, das einen Fehler beim Erstellen eines neuen **CDeferredCommand-Objekts** angibt. Wenn ein Fehler auftritt, wurde kein Objekt in die Warteschlange eingereiht.

## <a name="remarks"></a>Hinweise

Das neue [**CDeferredCommand-Objekt**](cdeferredcommand.md) wird mit den Parametern initialisiert und während der Erstellung der Warteschlange hinzugefügt. Diese Methode ähnelt der **IDispatch::Invoke-Methode.**

Die Werte für den *wFlags-Parameter* umfassen Folgendes:



| Wert                    | BESCHREIBUNG                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_DISPATCH-METHODE         | Der Member wird als Methode ausgeführt. Wenn eine Eigenschaft den gleichen Namen hat, können sowohl dieses als auch das DISPATCH \_ PROPERTYGET-Flag festgelegt werden.                                       |
| DISPATCH \_ PROPERTYGET    | Der Member wird als Eigenschafts- oder Datenmember abgerufen.                                                                                                          |
| DISPATCH \_ PROPERTYPUT    | Der Member wird als Eigenschafts- oder Datenmember geändert.                                                                                                            |
| DISPATCH \_ PROPERTYPUTREF | Der Member wird nicht über eine Wertzuweisung, sondern über eine Verweiszuweisung geändert. Dieser Wert ist nur gültig, wenn die Eigenschaft einen Verweis auf ein Objekt akzeptiert. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CCmdQueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




