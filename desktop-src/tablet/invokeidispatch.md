---
description: Ruft hilfsfunktionen für die IDispatch-Schnittstelle auf.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: InvokeIDispatch-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 9708ebc5675d918c959be132d16037ac4e128650280b8243dcfe5c48834b602b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041870"
---
# <a name="invokeidispatch-function"></a>InvokeIDispatch-Funktion

Ruft hilfsfunktionen für die IDispatch-Schnittstelle auf.

Diese Funktion ist nicht für die Verwendung durch Anwendungscode vorgesehen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDispatch* 
</dt> <dd>

Die Instanz der IDispatch-Schnittstelle.

</dd> <dt>

*Dispid* 
</dt> <dd>

Die methode, die Eigenschaft oder das Argument, die übergeben werden soll.

</dd> <dt>

*pDisp* 
</dt> <dd>

Die parameter, die übergeben werden.

</dd> <dt>

*pVarResult* \[ out\]
</dt> <dd>

Eine -Struktur, die die abgerufenen Werte empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn dies fehlschlägt, enthalten mögliche Rückgabecodes die in der folgenden Tabelle gezeigten Werte, sind aber nicht darauf beschränkt.



| Rückgabecode                                                                                  | Beschreibung                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der Wert für *pDispatch* ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl> |



 

 




