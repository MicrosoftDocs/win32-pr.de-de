---
description: Legt die ausgewählte CPU-Gruppenzuweisung für den angegebenen Thread fest. Diese Zuweisung überschreibt die standardmäßige Prozess Zuweisung, wenn eine festgelegt ist.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: Setthreadselectedcpusets-Funktion (processthreadapi. h)
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
ms.openlocfilehash: b8b1f7c382d034e804d4ac7e63d58b8ec5853620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865059"
---
# <a name="setthreadselectedcpusets-function"></a>Setthreadselectedcpusets-Funktion

Legt die ausgewählte CPU-Gruppenzuweisung für den angegebenen Thread fest. Diese Zuweisung überschreibt die standardmäßige Prozess Zuweisung, wenn eine festgelegt ist.

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

*Thread* \[ in\]
</dt> <dd>

Gibt den Thread an, in dem die CPU-Satz Zuweisung festgelegt werden soll. Dieses Handle muss über den Thread \_ fest \_ gelegtes \_ Zugriffsrecht für den Zugriff verfügen. Der von [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) zurückgegebene Wert kann ebenfalls verwendet werden.

</dd> <dt>

*Cpuabtids* \[ in\]
</dt> <dd>

Gibt die Liste der CPU-Satz-IDs an, die als vom Thread ausgewählte CPU festgelegt werden sollen. Wenn dieser Wert NULL ist, löscht die API jede Zuweisung und setzt die Verarbeitung der Standard Zuweisung wieder her, wenn eine solche festgelegt ist.

</dd> <dt>

*Cpuantidcount* \[ in\]
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



 

 
