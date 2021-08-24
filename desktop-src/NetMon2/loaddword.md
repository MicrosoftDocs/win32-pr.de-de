---
description: Die LoadDWORD-Funktion wird vom Monitor aufgerufen, um eine DWORD-Variable mit einem Wert aus einer HTML-Konfigurationszeichenfolgenvariablen zu festlegen.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: LoadDWORD-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8fa0477122548dad30911948a3581d269b22d8d6eb866273f32aa40a9b427545
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778760"
---
# <a name="loaddword-function"></a>LoadDWORD-Funktion

Die **LoadDWORD-Funktion** wird vom Monitor aufgerufen, um eine **DWORD-Variable** mit einem Wert aus einer HTML-Konfigurationszeichenfolgenvariablen zu festlegen.

## <a name="syntax"></a>Syntax


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
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

*pValue* \[ In\]
</dt> <dd>

Zeiger auf die **DWORD-Variable,** die auf den Wert der Konfigurationszeichenfolgenvariablen festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist (wenn der Variablenname gefunden wurde und eine Zeichenfolge der Länge 0 (null) aufwies), wird **das DWORD** eingefügt, und der Rückgabewert ist **TRUE.**

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




