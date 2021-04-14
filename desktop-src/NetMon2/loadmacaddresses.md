---
description: Die loadmacaddress-Funktion wird vom Monitor aufgerufen, um eine Mac-Adressliste mit Adressen auszufüllen, die aus einer HTML-Konfigurations Zeichenfolgen-Variablen entnommen werden.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: Loadmacadressen-Funktion (Netmon. h)
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
ms.openlocfilehash: 62c9422469d7acf061578d1ec093676f6e1d8386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526768"
---
# <a name="loadmacaddresses-function"></a>Loadmacadressen-Funktion

Die **loadmacaddress** -Funktion wird vom Monitor aufgerufen, um eine Mac-Adressliste mit Adressen auszufüllen, die aus einer HTML-Konfigurations Zeichenfolgen-Variablen entnommen werden.

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

*pConfig* \[ in\]
</dt> <dd>

Zeiger auf die HTML-Konfigurations Zeichenfolge, die von der [Imonitor::D oconfigure](imonitor-doconfigure.md) -Methode an den Monitor übermittelt wurde.

</dd> <dt>

*pvarname* \[ in\]
</dt> <dd>

Zeiger auf den Namen der Variablen in der Konfigurations Zeichenfolge.

</dd> <dt>

*ppadressen* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Zeiger auf ein Array von Adressen. Wenn die in *pvarname* angegebene Variable gefunden wird und eine nicht-Null-Länge aufweist, ordnet die Funktion ausreichenden Speicherplatz zu (mithilfe von **heapzucmemory**) und speichert alle Mac-Adressen als Array.

</dd> <dt>

*pnumadkleider* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die **DWORD** -Variable, die auf die Anzahl der Mac-Adressen der Konfigurations Zeichenfolge festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **true**, wenn der Variablenname gefunden wurde und eine Zeichenfolge ungleich 0 (null) aufweist, die Mac-Adressen darstellt).

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




