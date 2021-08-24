---
description: Legt die ausgewählte CPU-Mengenzuweisung für den angegebenen Thread fest. Diese Zuweisung überschreibt die Prozessstandardzuweisung, wenn eine festgelegt ist.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: SetThreadSelectedCpuSets-Funktion (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d627c3ae0499cf19ba533c30d1a3fabb05c2dbf5782d99b2f716579f50125b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031730"
---
# <a name="setthreadselectedcpusets-function"></a>SetThreadSelectedCpuSets-Funktion

Legt die ausgewählte CPU-Mengenzuweisung für den angegebenen Thread fest. Diese Zuweisung überschreibt die Prozessstandardzuweisung, wenn eine festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Thread* \[ In\]
</dt> <dd>

Gibt den Thread an, für den die CPU-Set-Zuweisung festgelegt werden soll. Dieses Handle muss über das \_ THREAD SET \_ LIMITED \_ INFORMATION-Zugriffsrecht verfügen. Der von [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) zurückgegebene Wert kann ebenfalls verwendet werden.

</dd> <dt>

*CpuSetIds* \[ In\]
</dt> <dd>

Gibt die Liste der CPU-Satz-IDs an, die als ausgewählter Cpu-Satz des Threads festgelegt werden sollen. Wenn dies NULL ist, löscht die API alle Zuweisungen und setzt die Standardzuweisung zurück, wenn eine festgelegt ist.

</dd> <dt>

*CpuSetIdCount* \[ In\]
</dt> <dd>

Gibt die Anzahl der IDs in der Liste an, die im **CpuSetIds-Argument** übergeben werden. Wenn dieser Wert NULL ist, sollte dieser Wert 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann nicht fehlschlagen, wenn gültige Parameter übergeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 \|Desktop-Apps UWP-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 \|Desktop-Apps UWP-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
