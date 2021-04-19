---
description: Ruft die Liste der CPU-Sätze im standardmäßigen Prozess Satz ab, der von setprocessdefaultcpusets festgelegt wurde. Wenn für einen bestimmten Prozess keine Standard-CPU-Sätze festgelegt sind, wird der Wert für "Requirements" auf 0 festgelegt, und die Funktion ist erfolgreich.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: Getprocessdefaultcpusets-Funktion (processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: a5bd7c27b76efbbac923317837ac82b3a6700197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350224"
---
# <a name="getprocessdefaultcpusets-function"></a>Getprocessdefaultcpusets-Funktion

Ruft die Liste der CPU-Sätze im standardmäßigen Prozess Satz ab, der von [**setprocessdefaultcpusets**](setprocessdefaultcpusets.md)festgelegt wurde. Wenn für einen bestimmten Prozess keine Standard-CPU-Sätze festgelegt sind, wird der Wert für "Requirements" auf 0 festgelegt, **und die Funktion ist erfolgreich** .

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Prozess* \[ in\]
</dt> <dd>

Gibt ein Prozess Handle für den abzufragende Prozess an. Dieses Handle muss über das Recht "Prozess \_ Abfrage \_ beschränkte Informationen" verfügen \_ . Der von [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) zurückgegebene Wert kann auch hier angegeben werden.

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

Gibt die erforderliche Kapazität des Puffers an, der die gesamte Liste der standardmäßigen Prozess-CPU-Sätze enthalten soll. Bei erfolgreicher Rückgabe wird dadurch die Anzahl der in den Puffer gefüllten IDs angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese API gibt bei Erfolg TRUE zurück. Wenn der Puffer nicht groß genug ist, gibt die API false zurück, und der **GetLastError** -Wert ist Fehler \_ unzureichender \_ Puffer. Diese API kann nicht ausgeführt werden, wenn gültige Parameter bestanden werden und der Rückgabe Puffer groß genug ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 \[ Desktop Apps \| UWP-apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016 \[ -Desktop-Apps \| UWP-apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

