---
description: Gibt die Adresse einer Rückruffunktion für Verzögerungs Ladefehler für die angegebene DLL und den Prozess zurück.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: Delta loadfailurehook-Funktion
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
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373737"
---
# <a name="delayloadfailurehook-function"></a>Delta loadfailurehook-Funktion

Gibt die Adresse einer Rückruffunktion für Verzögerungs Ladefehler für die angegebene DLL und den Prozess zurück.

## <a name="syntax"></a>Syntax


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszdllname* \[ in\]
</dt> <dd>

Der Name der dll.

</dd> <dt>

*pszProcName* \[ in\]
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler Hooks](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)
</dt> </dl>

 

 




