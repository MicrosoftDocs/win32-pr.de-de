---
description: Leitet die Arbeit zum Auflösen von verzögert geladenen Importen aus der übergeordneten Binärdatei in eine Ziel Binärdatei weiter.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: Resolvedelta-loadsfromdll-Funktion
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
ms.openlocfilehash: a0fb517de7384a964c21c9e1a0a3e695a0d6e6cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370816"
---
# <a name="resolvedelayloadsfromdll-function"></a>Resolvedelta-loadsfromdll-Funktion

Leitet die Arbeit zum Auflösen von verzögert geladenen Importen aus der übergeordneten Binärdatei in eine Ziel Binärdatei weiter.

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

*Parametribase* \[ in\]
</dt> <dd>

Die Basisadresse des Moduls, das verzögert eine andere Binärdatei lädt.

</dd> <dt>

*Targetdllname* \[ in\]
</dt> <dd>

Der Name der Ziel-dll.

</dd> <dt>

*Flags* 
</dt> <dd>

Bleiben muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Adresse des Deskriptors für verzögertes Laden, wenn Sie gefunden wird. andernfalls **null**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Linker-Unterstützung für Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




