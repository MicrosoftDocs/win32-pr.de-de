---
description: Legt die standardcpu-Gruppenzuweisung für Threads im angegebenen Prozess fest. Threads, die erstellt werden und für die keine CPU-Sätze explizit mithilfe von setthreadselectedcpusets festgelegt werden, erben die von setprocessdefaultcpusets angegebenen Mengen automatisch.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: Setprocessdefaultcpusets-Funktion (processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 7998b20815529b41c5e29204c0ef50fbc15e6288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353454"
---
# <a name="setprocessdefaultcpusets-function"></a>Setprocessdefaultcpusets-Funktion

Legt die standardcpu-Gruppenzuweisung für Threads im angegebenen Prozess fest. Threads, die erstellt werden und für die keine CPU-Sätze explizit mithilfe von [**setthreadselectedcpusets**](setthreadselectedcpusets.md)festgelegt werden, erben die von **setprocessdefaultcpusets** angegebenen Mengen automatisch.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Prozess* \[ in\]
</dt> <dd>

Gibt den Prozess an, für den die Standard-CPU-Sätze festgelegt werden sollen. Dieses Handle muss über das \_ Recht zum Festlegen des \_ eingeschränkten \_ Informations Zugriffs verfügen. Der von [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) zurückgegebene Wert kann auch hier angegeben werden.

</dd> <dt>

*Cpuabtids* \[ in, optional\]
</dt> <dd>

Gibt die Liste der CPU-Satz-IDs an, die als Standard-CPU-Prozess festgelegt werden sollen. Wenn dieser Wert NULL ist, löscht **setprocessdefaultcpusets** jede Zuweisung.

</dd> <dt>

*Cpuabtidcoder* \[ in\]
</dt> <dd>

Gibt die Anzahl der IDs in der Liste an, die im **cpucpuds** -Argument übergeben wird. Wenn dieser Wert NULL ist, sollte dieser 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann nicht fehlschlagen, wenn gültige Parameter bestanden wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 \[ Desktop Apps \| UWP-apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016 \[ -Desktop-Apps \| UWP-apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
