---
description: Die LoadMACAddresses-Funktion wird vom Monitor aufgerufen, um eine MAC-Adressliste mit Adressen aus einer HTML-Konfigurationszeichenfolgenvariablen zu füllen.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: LoadMACAddresses-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2de609ef0a1e820785ee7d62cbbe1e6af32c633aa29b133974f6f5f6f2a649b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742720"
---
# <a name="loadmacaddresses-function"></a>LoadMACAddresses-Funktion

Die **LoadMACAddresses-Funktion** wird vom Monitor aufgerufen, um eine MAC-Adressliste mit Adressen aus einer HTML-Konfigurationszeichenfolgenvariablen zu füllen.

## <a name="syntax"></a>Syntax


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
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

Zeiger auf einen Zeiger auf ein Array von Adressen. Wenn die in *pVarName* angegebene Variable gefunden wird und eine Länge von nicht 0 hat, weist die Funktion (mithilfe von **HeapAllocMemory)** ausreichend Speicherplatz zu und speichert alle MAC-Adressen als Array.

</dd> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Zeiger auf die **DWORD-Variable,** die auf die Anzahl der MAC-Adressen aus der Konfigurationszeichenfolge festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (der Variablenname wurde gefunden und hatte eine Zeichenfolge mit einer Länge von nicht null, die MAC-Adressen repräsentiert), ist der Rückgabewert **TRUE.**

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




