---
description: Ruft Hilfsfunktionen für die IDispatch-Schnittstelle auf.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: Invokeidispatch-Funktion
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
ms.openlocfilehash: e4989e3ec23a1ffa97ba317831143ecf0920ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349929"
---
# <a name="invokeidispatch-function"></a>Invokeidispatch-Funktion

Ruft Hilfsfunktionen für die IDispatch-Schnittstelle auf.

Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.

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

*pdispatch* 
</dt> <dd>

Die Instanz der IDispatch-Schnittstelle.

</dd> <dt>

*DISPID* 
</dt> <dd>

Die Methode, die Eigenschaft oder das Argument, das übergeben werden soll.

</dd> <dt>

*pDisp* 
</dt> <dd>

Die Parameter, die übergeben werden sollen.

</dd> <dt>

*pVarResult* \[ vorgenommen\]
</dt> <dd>

Eine-Struktur, die die abgerufenen Werte empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn ein Fehler auftritt, enthalten mögliche Rückgabecodes die in der folgenden Tabelle aufgeführten Werte, sind jedoch nicht darauf beschränkt.



| Rückgabecode                                                                                  | Beschreibung                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der Wert für *pdispatch* ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl> |



 

 




