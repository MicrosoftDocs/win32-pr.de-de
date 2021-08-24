---
description: Gibt die Adresse einer Fehlerrückruffunktion für das verzögerte Laden für die angegebene DLL und den angegebenen Prozess zurück.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: DelayLoadFailureHook-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: 8724073a8f5f124cf23d6ba15390c8028d308354aa1e2c896f1d2c9f5030ea45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795281"
---
# <a name="delayloadfailurehook-function"></a>DelayLoadFailureHook-Funktion

Gibt die Adresse einer Fehlerrückruffunktion für das verzögerte Laden für die angegebene DLL und den angegebenen Prozess zurück.

## <a name="syntax"></a>Syntax


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszDllName* \[ In\]
</dt> <dd>

Der Name der DLL.

</dd> <dt>

*pszProcName* \[ In\]
</dt> <dd>

Der Name des Prozesses.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Adresse der Rückruffunktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fehlerhooks](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)
</dt> </dl>

 

 




