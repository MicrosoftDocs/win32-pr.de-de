---
description: Gibt die Arbeit zum Auflösen verzögert geladener Importe aus der übergeordneten Binärdatei an eine Zielbin binär weiter.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: ResolveDelayLoadsFromDll-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 894360a20456b73d0cfad19cd125405caf0c3624821aca21e3e107699d1cc372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571540"
---
# <a name="resolvedelayloadsfromdll-function"></a>ResolveDelayLoadsFromDll-Funktion

Gibt die Arbeit zum Auflösen verzögert geladener Importe aus der übergeordneten Binärdatei an eine Zielbin binär weiter.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ParentBase* \[ In\]
</dt> <dd>

Die Basisadresse des Moduls, das verzögert wird, lädt eine andere Binärdatei.

</dd> <dt>

*TargetDllName* \[ In\]
</dt> <dd>

Der Name der Ziel-DLL.

</dd> <dt>

*Flags* 
</dt> <dd>

Reserviert; muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Adresse des Deskriptors für das verzögerte Laden, sofern gefunden; andernfalls **NULL.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Linkerunterstützung für Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




