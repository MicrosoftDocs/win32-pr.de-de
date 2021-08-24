---
description: Die LoadIPAddresses-Funktion wird vom Monitor aufgerufen, um eine IP-Adressliste mit Adressen aus einer HTML-Konfigurationszeichenfolgenvariablen auszufüllen.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: LoadIPAddresses-Funktion (Netmon.h)
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
ms.openlocfilehash: 2f56517fd0caf4762be2848ac9a6f3094ed5e3194b2eb84123bf2fcc2bf67bcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742670"
---
# <a name="loadipaddresses-function"></a>LoadIPAddresses-Funktion

Die **LoadIPAddresses-Funktion** wird vom Monitor aufgerufen, um eine IP-Adressliste mit Adressen aus einer HTML-Konfigurationszeichenfolgenvariablen auszufüllen.

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

*pConfig* \[ In\]
</dt> <dd>

Zeiger auf die HTML-Konfigurationszeichenfolge, die von der [IMonitor::D oConfigure-Methode](imonitor-doconfigure.md) an den Monitor übergeben wird.

</dd> <dt>

*pVarName* \[ In\]
</dt> <dd>

Zeiger auf den Namen der Variablen in der Konfigurationszeichenfolge.

</dd> <dt>

*ppAddresses* \[ out\]
</dt> <dd>

Zeiger auf einen Zeiger auf ein Array von Adressen. Wenn die in *pVarName* angegebene Variable gefunden wird und eine Länge ungleich 0 (null) aufweist, ordnet die Funktion ausreichend Speicherplatz zu und speichert alle IP-Adressen als Array.

</dd> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Zeiger auf die **DWORD-Variable,** die auf die Anzahl der IP-Adressen aus der Konfigurationszeichenfolge festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (der Variablenname wurde gefunden und hatte eine Zeichenfolge ungleich 0 (null), die IP-Adressen darstellte), ist der Rückgabewert **TRUE.**

Wenn die Funktion nicht erfolgreich ist, lautet der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Die IP-Adressen müssen im x.x.x.x-Format vorliegen (z.B. 127.0.0.1).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




