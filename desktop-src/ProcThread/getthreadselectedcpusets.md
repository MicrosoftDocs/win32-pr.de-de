---
description: Gibt die explizite CPU-Set-Zuweisung des angegebenen Threads zurück, wenn eine Zuweisung mithilfe der SetThreadSelectedCpuSets-API festgelegt wurde. Wenn keine explizite Zuweisung festgelegt ist, wird RequiredIdCount auf 0 festgelegt, und die Funktion gibt TRUE zurück.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: GetThreadSelectedCpuSets-Funktion (Processthreadapi.h)
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
ms.openlocfilehash: 76e8fb9ff9fb540d15c8610a673ff52c5586f0ab57eb06668ef5e586db7513d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978780"
---
# <a name="getthreadselectedcpusets-function"></a>GetThreadSelectedCpuSets-Funktion

Gibt die explizite CPU-Set-Zuweisung des angegebenen Threads zurück, wenn eine Zuweisung mithilfe der [**SetThreadSelectedCpuSets-API**](setthreadselectedcpusets.md) festgelegt wurde. Wenn keine explizite Zuweisung festgelegt ist, wird **RequiredIdCount** auf 0 festgelegt, und die Funktion gibt TRUE zurück.

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

*Thread* \[ In\]
</dt> <dd>

Gibt den Thread an, für den die ausgewählten CPU-Sätze abgefragt werden sollen. Dieses Handle muss über das Zugriffsrecht THREAD \_ QUERY LIMITED \_ INFORMATION \_ verfügen. Der von [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) zurückgegebene Wert kann hier ebenfalls angegeben werden.

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

Gibt die erforderliche Kapazität des Puffers an, um die gesamte Liste der vom Thread ausgewählten CPU-Sätze aufzunehmen. Bei erfolgreicher Rückgabe gibt dies die Anzahl der IDs an, die in den Puffer gefüllt sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese API gibt BEI Erfolg TRUE zurück. Wenn der Puffer nicht groß genug ist, lautet der **GetLastError-Wert** ERROR \_ INSUFFICIENT \_ BUFFER. Diese API kann nicht fehlschlagen, wenn gültige Parameter übergeben werden und der Rückgabepuffer groß genug ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 \|Desktop-Apps UWP-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 \|Desktop-Apps UWP-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

