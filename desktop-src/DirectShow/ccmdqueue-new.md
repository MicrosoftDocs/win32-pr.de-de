---
description: Die neue Methode initialisiert einen Befehl, der ausgeführt werden soll, und gibt ein neues cdeferredcommand-Objekt zurück.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: Ccmdqueue. New-Methode (winutil. h)
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
ms.openlocfilehash: 58c3aee63005010b9ed7366cfb63a69fcc7348b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361287"
---
# <a name="ccmdqueuenew-method"></a>Ccmdqueue. New-Methode

Die `New` -Methode initialisiert einen Befehl, der ausgeführt werden soll, und gibt ein neues [**cdeferredcommand**](cdeferredcommand.md) -Objekt zurück.

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

Adresse eines Zeigers auf ein [**cdeferredcommand**](cdeferredcommand.md) -Objekt, mit dem eine Anwendung den Befehl abbrechen kann, eine neue Präsentationszeit für Sie festgelegt oder Schätz Informationen abruft.

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf das Objekt, von dem der Befehl ausgeführt wird.

</dd> <dt>

*time* 
</dt> <dd>

Der Zeitpunkt, zu dem der Befehl oder die Befehle in der Warteschlange ausgeführt werden sollen.

</dd> <dt>

*IID* 
</dt> <dd>

Zeiger auf den Globally Unique Identifier (**GUID**) der aufzurufenden Schnittstelle.

</dd> <dt>

*dispidmethod* 
</dt> <dd>

Methode für die aufzurufende Schnittstelle.

</dd> <dt>

*wFlags* 
</dt> <dd>

Flags, die den Kontext des Aufrufs beschreiben. Dieser Parameter unterstützt dieselben Flags wie die **IDispatch:: Aufrufen** -Methode.

</dd> <dt>

*kargs* 
</dt> <dd>

Anzahl der über gebenen Argumente.

</dd> <dt>

*pdispparameams* 
</dt> <dd>

Ein Zeiger auf die Liste der Variant-Typen, die den Dispatch-Parametern zugeordnet sind.

</dd> <dt>

*pVarResult* 
</dt> <dd>

Ein Zeiger auf die Liste, in der Ergebnisse (sofern vorhanden) zurückgegeben werden sollen.

</dd> <dt>

*gibt puArgErr* 
</dt> <dd>

Zeiger auf den Index in der *pdispparameams* -Parameterliste, in der der letzte Fehler aufgetreten ist.

</dd> <dt>

*bStream* 
</dt> <dd>

Ein Wert, der angibt, ob der *Zeit* Parameter ein streamzeitwert (**true**) oder ein Präsentations Zeitwert (**false**) ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK zurück. Gibt "E outo-Memory" zurück, \_ Wenn *ppcmd* von der Erstellung des neuen [**cdeferredcommand**](cdeferredcommand.md) -Objekts mit dem Wert " **null**" zurückgegeben wird. Andernfalls gibt ein **HRESULT** zurück, das einen Fehler beim Versuch angibt, ein neues **cdeferredcommand** -Objekt zu erstellen. Wenn ein Fehler vorliegt, wurde kein Objekt in die Warteschlange eingereiht.

## <a name="remarks"></a>Bemerkungen

Das neue [**cdeferredcommand**](cdeferredcommand.md) -Objekt wird mit den Parametern initialisiert und während der Erstellung der Warteschlange hinzugefügt. Diese Methode ähnelt der **IDispatch:: Aufrufen** -Methode.

Die Werte für den *wFlags* -Parameter umfassen Folgendes:



| Wert                    | BESCHREIBUNG                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dispatch- \_ Methode         | Der Member wird als Methode ausgeführt. Wenn eine Eigenschaft denselben Namen hat, können sowohl dieses als auch das Dispatch \_ PropertyGet-Flag festgelegt werden.                                       |
| Dispatch- \_ PropertyGet    | Der Member wird als Eigenschaft oder Datenmember abgerufen.                                                                                                          |
| Dispatch- \_ PropertyPut    | Der Member wird als Eigenschaft oder Datenmember geändert.                                                                                                            |
| Dispatch \_ propertyputref | Der Member wird über eine Verweis Zuweisung und nicht über eine Wert Zuweisung geändert. Dieser Wert ist nur gültig, wenn die-Eigenschaft einen Verweis auf ein-Objekt akzeptiert. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccmdqueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




