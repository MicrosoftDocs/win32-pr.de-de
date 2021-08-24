---
description: Die LoadIPXAddresses-Funktion wird vom Monitor aufgerufen, um eine IPX-Adressliste aus einer HTML-Konfigurationszeichenfolgenvariablen zu füllen.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: LoadIPXAddresses-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ed8bb6948102e8d28150edf102fa261c9c7f7adfcf105e377352054304b352df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677310"
---
# <a name="loadipxaddresses-function"></a>LoadIPXAddresses-Funktion

Die **LoadIPXAddresses-Funktion** wird vom Monitor aufgerufen, um eine IPX-Adressliste aus einer HTML-Konfigurationszeichenfolgenvariablen zu füllen.

## <a name="syntax"></a>Syntax


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pConfig* \[ In\]
</dt> <dd>

Zeiger auf die HTML-Konfigurationszeichenfolge, die von der [IMonitor::D oConfigure-Methode an den Monitor übergeben](imonitor-doconfigure.md) wird.

</dd> <dt>

*pVarName* \[ In\]
</dt> <dd>

Zeiger auf den Namen der Variablen in der Konfigurationszeichenfolge.

</dd> <dt>

*ppAddresses* \[ out\]
</dt> <dd>

Zeiger auf einen Zeiger auf ein Array von Adressen. Wenn die in *pVarName* angegebene Variable gefunden wird und eine Länge von nicht 0 hat, wird ausreichend Speicherplatz zugeordnet (mithilfe von **HeapAllocMemory),** und alle IPX-Adressen werden als Array gespeichert.

</dd> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Zeiger auf die **DWORD-Variable,** die auf die Anzahl der IPX-Adressen aus der Konfigurationszeichenfolge festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (der Variablenname wurde gefunden und hatte eine Zeichenfolge der Länge 0 (null), die IPX-Adressen dargestellt hat), ist der Rückgabewert **TRUE.**

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **FALSE.**

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




