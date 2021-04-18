---
description: Ermöglicht einer Anwendung das Abfragen der verfügbaren CPU-Sätze im System und Ihres aktuellen Zustands.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: Getsystemcpusetinformation-Funktion (processthreadapi. h)
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
ms.openlocfilehash: d8ce490e3377e45a81b24523504d06941755de49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216017"
---
# <a name="getsystemcpusetinformation-function"></a>Getsystemcpusetinformation-Funktion

Ermöglicht einer Anwendung das Abfragen der verfügbaren CPU-Sätze im System und Ihres aktuellen Zustands.

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

*Informationen* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**System- \_ CPU- \_ Satz \_ Informations**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) Struktur, die die CPU-Satz Daten empfängt. Übergeben Sie NULL mit der Pufferlänge 0, um die erforderliche Puffergröße zu bestimmen.

</dd> <dt>

*BufferLength* \[ in\]
</dt> <dd>

Die Länge (in Byte) des Ausgabepuffers, der als Informations Argument übergangen wird.

</dd> <dt>

*Rückkehrnedlength* \[ vorgenommen\]
</dt> <dd>

Die Länge (in Byte) der gültigen Daten im Ausgabepuffer, wenn der Puffer groß genug ist, oder die erforderliche Größe des Ausgabepuffers. Wenn keine CPU-Sätze vorhanden sind, ist dieser Wert 0 (null).

</dd> <dt>

*Prozess* \[ in, optional\]
</dt> <dd>

Ein optionales Handle für einen Prozess. Dieser Prozess wird verwendet, um den Wert des "  zugsverzeichnis"-Flags in der System- \_ CPU \_ - \_ Informationsstruktur festzulegen. Wenn eine CPU-Menge dem angegebenen Prozess zugeordnet ist, wird das-Flag festgelegt. Andernfalls ist es eindeutig. Dieses Handle muss über das Recht "Prozess \_ Abfrage \_ beschränkte Informationen" verfügen \_ . Der von [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) zurückgegebene Wert kann hier ebenfalls angegeben werden.

</dd> <dt>

*Flags* 
</dt> <dd>

Reserviert, muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die API erfolgreich ist, wird true zurückgegeben. Wenn dies nicht möglich ist, ist die Fehlerursache über **GetLastError** verfügbar. Wenn der Informations Puffer NULL oder nicht groß genug ist, wird der Fehlercode Fehler "nicht \_ genügend \_ Puffer" zurückgegeben. Diese API kann nicht fehlschlagen, wenn gültige Parameter und ein Puffer bestanden werden, der groß genug ist, um alle Rückgabe Daten aufzunehmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 \[ Desktop Apps \| UWP-apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016 \[ -Desktop-Apps \| UWP-apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

