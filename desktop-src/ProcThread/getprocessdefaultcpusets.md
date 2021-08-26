---
description: Ruft die Liste der CPU-Sätze im Prozessstandardsatz ab, der von SetProcessDefaultCpuSets festgelegt wurde. Wenn für einen bestimmten Prozess keine CPU-Standardsätze festgelegt sind, wird RequiredIdCount auf 0 festgelegt, und die Funktion wird erfolgreich ausgeführt.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: GetProcessDefaultCpuSets-Funktion (Processthreadapi.h)
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
ms.openlocfilehash: 3c5d71e4811411756719177647fda8dd76224f756629ad01794720d291565b21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886700"
---
# <a name="getprocessdefaultcpusets-function"></a>GetProcessDefaultCpuSets-Funktion

Ruft die Liste der CPU-Sätze im Prozessstandardsatz ab, der von [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md)festgelegt wurde. Wenn für einen bestimmten Prozess keine CPU-Standardsätze festgelegt sind, wird **RequiredIdCount** auf 0 festgelegt, und die Funktion wird erfolgreich ausgeführt.

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

*Prozess* \[ In\]
</dt> <dd>

Gibt ein Prozesshandle für den abzufragenden Prozess an. Dieses Handle muss über das Zugriffsrecht PROCESS \_ QUERY LIMITED \_ INFORMATION \_ verfügen. Der von [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) zurückgegebene Wert kann hier ebenfalls angegeben werden.

</dd> <dt>

*CpuSetIds* \[ out, optional\]
</dt> <dd>

Gibt einen optionalen Puffer an, um die Liste der CPU-Satzbezeichner abzurufen.

</dd> <dt>

*CpuSetIdCount* \[ In\]
</dt> <dd>

Gibt die Kapazität des puffers an, der in **CpuSetIds** angegeben ist. Wenn der Puffer NULL ist, muss er 0 sein.

</dd> <dt>

*RequiredIdCount* \[ out\]
</dt> <dd>

Gibt die erforderliche Kapazität des Puffers an, um die gesamte Liste der Prozessstandard-CPU-Sätze aufzunehmen. Bei erfolgreicher Rückgabe gibt dies die Anzahl der IDs an, die in den Puffer gefüllt sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese API gibt BEI Erfolg TRUE zurück. Wenn der Puffer nicht groß genug ist, gibt die API FALSE zurück, und der **GetLastError-Wert** ist ERROR \_ INSUFFICIENT \_ BUFFER. Diese API kann nicht fehlschlagen, wenn gültige Parameter übergeben werden und der Rückgabepuffer groß genug ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 \|Desktop-Apps UWP-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 \|Desktop-Apps UWP-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

