---
description: Die loadipaddress-Funktion wird vom Monitor aufgerufen, um eine IP-Adressliste mit Adressen auszufüllen, die aus einer HTML-Konfigurations Zeichenfolgen-Variablen entnommen werden.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: Loadipadressen-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a5c172117081777b2a89b875401ec0645dd643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362791"
---
# <a name="loadipaddresses-function"></a>Loadipadressen-Funktion

Die **loadipaddress** -Funktion wird vom Monitor aufgerufen, um eine IP-Adressliste mit Adressen auszufüllen, die aus einer HTML-Konfigurations Zeichenfolgen-Variablen entnommen werden.

## <a name="syntax"></a>Syntax


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
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

Zeiger auf einen Zeiger auf ein Array von Adressen. Wenn die in *pvarname* angegebene Variable gefunden wird und eine nicht-Null-Länge aufweist, ordnet die Funktion ausreichenden Speicherplatz zu und speichert alle IP-Adressen als Array.

</dd> <dt>

*pnumadkleider* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die **DWORD** -Variable, die auf die Anzahl der IP-Adressen aus der Konfigurations Zeichenfolge festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (der Variablenname wurde gefunden, und eine Zeichenfolge mit einer Länge ungleich Null war, die IP-Adressen repräsentiert), ist der Rückgabewert " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Die IP-Adressen müssen das Format x. x. x. x aufweisen (z. b. 127.0.0.1).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




