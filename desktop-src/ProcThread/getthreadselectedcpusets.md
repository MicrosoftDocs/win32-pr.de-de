---
description: Gibt die explizite CPU-Satz Zuweisung des angegebenen Threads zurück, wenn eine Zuweisung mithilfe der setthreadselectedcpusets-API festgelegt wurde. Wenn keine explizite Zuweisung festgelegt ist, wird "Requirements didcount" auf 0 festgelegt, und die Funktion gibt "true" zurück.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: Getthreadselectedcpusets-Funktion (processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 26530b1fbb9694ed7ecc8c4e457ad023e971a470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042260"
---
# <a name="getthreadselectedcpusets-function"></a>Getthreadselectedcpusets-Funktion

Gibt die explizite CPU-Satz Zuweisung des angegebenen Threads zurück, wenn eine Zuweisung mithilfe der [**setthreadselectedcpusets**](setthreadselectedcpusets.md) -API festgelegt wurde. Wenn keine explizite Zuweisung festgelegt ist, wird "Requirements **didcount** " auf 0 festgelegt, und die Funktion gibt "true" zurück.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Thread* \[ in\]
</dt> <dd>

Gibt den Thread an, für den die ausgewählten CPU-Sätze abgefragt werden sollen. Dieses Handle muss über den \_ \_ eingeschränkten \_ Informations Zugriff für die Thread Abfrage verfügen. Der von [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) zurückgegebene Wert kann auch hier angegeben werden.

</dd> <dt>

*Cpuabtids* \[ Out, optional\]
</dt> <dd>

Gibt einen optionalen Puffer zum Abrufen der Liste der CPU-Satz Bezeichner an.

</dd> <dt>

*Cpuantidcount* \[ in\]
</dt> <dd>

Gibt die Kapazität des Puffers an, der in **cpuabtids** angegeben ist. Wenn der Puffer NULL ist, muss dieser 0 sein.

</dd> <dt>

Requirements- *count* \[ vorgenommen\]
</dt> <dd>

Gibt die erforderliche Kapazität des Puffers an, der die gesamte Liste der von einem Thread ausgewählten CPU-Sätze enthalten soll. Bei erfolgreicher Rückgabe wird dadurch die Anzahl der in den Puffer gefüllten IDs angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese API gibt bei Erfolg TRUE zurück. Wenn der Puffer nicht groß genug ist, ist der Wert von " **GetLastError** " Fehler \_ unzureichend \_ . Diese API kann nicht ausgeführt werden, wenn gültige Parameter bestanden werden und der Rückgabe Puffer groß genug ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 \[ Desktop Apps \| UWP-apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016 \[ -Desktop-Apps \| UWP-apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

