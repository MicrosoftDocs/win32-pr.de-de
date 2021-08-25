---
description: Die LoadTCHAR-Funktion wird von Monitoren aufgerufen, um eine Zeichenfolgenvariable auf eine Zeichenfolge festzulegen, die aus einer HTML-Konfigurationszeichenfolge stammt.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: LoadTCHAR-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2d85419485e2442f82c94948b832914fa30e44396f266eed10cd1545b4cc28ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890286"
---
# <a name="loadtchar-function"></a>LoadTCHAR-Funktion

Die **LoadTCHAR-Funktion** wird von Monitoren aufgerufen, um eine Zeichenfolgenvariable auf eine Zeichenfolge festzulegen, die aus einer HTML-Konfigurationszeichenfolge stammt.

## <a name="syntax"></a>Syntax


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
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

*ppszString* \[ out\]
</dt> <dd>

Zeiger auf einen Zeichenfolgenzeiger. Wenn der angeforderte Variablenname gefunden wird, wird die Zeichenfolge diesem Zeiger zugeordnet und zugewiesen. Der Benutzer ist verantwortlich dafür, den der Zeichenfolge zugeordneten Arbeitsspeicher freizugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (wenn der Variablenname gefunden wurde und eine Zeichenfolge ungleich 0 (null) hatte), ist der Rückgabewert **TRUE.**

Wenn die Funktion nicht erfolgreich ist, lautet der Rückgabewert **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




