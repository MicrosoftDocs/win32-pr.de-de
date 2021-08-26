---
description: Ermöglicht einer Anwendung das Abfragen der verfügbaren CPU-Sätze auf dem System und ihres aktuellen Zustands.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: GetSystemCpuSetInformation-Funktion (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSystemCpuSetInformation
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 011a809c78f2e94e6d16bbe5deb716ee7e97db356765bb771709048d3b00d05a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995370"
---
# <a name="getsystemcpusetinformation-function"></a>GetSystemCpuSetInformation-Funktion

Ermöglicht einer Anwendung das Abfragen der verfügbaren CPU-Sätze auf dem System und ihres aktuellen Zustands.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Informationen* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**SYSTEM \_ CPU SET \_ \_ INFORMATION-Struktur,**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) die die CPU Set-Daten empfängt. Übergeben Sie NULL mit einer Pufferlänge von 0, um die erforderliche Puffergröße zu bestimmen.

</dd> <dt>

*BufferLength* \[ In\]
</dt> <dd>

Die Länge des Als Information-Argument übergebenen Ausgabepuffers in Bytes.

</dd> <dt>

*ReturnedLength* \[ out\]
</dt> <dd>

Die Länge der gültigen Daten im Ausgabepuffer in Bytes, wenn der Puffer groß genug ist, oder die erforderliche Größe des Ausgabepuffers. Wenn keine CPU-Sätze vorhanden sind, ist dieser Wert 0.

</dd> <dt>

*Prozess* \[ in, optional\]
</dt> <dd>

Ein optionales Handle für einen Prozess. Dieser Prozess wird verwendet, um den Wert des **AllocatedToTargetProcess-Flags** in der SYSTEM \_ CPU SET \_ \_ INFORMATION-Struktur zu bestimmen. Wenn dem angegebenen Prozess ein CPU-Satz zugeordnet wird, wird das Flag festgelegt. Andernfalls ist es klar. Dieses Handle muss über das Zugriffsrecht PROCESS \_ QUERY LIMITED \_ INFORMATION \_ verfügen. Der von [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) zurückgegebene Wert kann hier ebenfalls angegeben werden.

</dd> <dt>

*Flags* 
</dt> <dd>

Reserviert, muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die API erfolgreich ist, wird TRUE zurückgegeben. Wenn ein Fehler auftritt, ist die Fehlerursache über **GetLastError** verfügbar. Wenn der Informationspuffer NULL oder nicht groß genug war, wird der Fehlercode ERROR \_ INSUFFICIENT \_ BUFFER zurückgegeben. Diese API kann nicht fehlschlagen, wenn gültige Parameter und ein Puffer übergeben werden, der groß genug ist, um alle Rückgabedaten zu speichern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 \|Desktop-Apps UWP-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 \|Desktop-Apps UWP-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

