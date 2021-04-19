---
description: Ruft die angegebenen Systeminformationen ab.
ms.assetid: c91b9a35-ca2b-4d81-973d-fe709144df90
title: Zwquerysysteminformation-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQuerySystemInformation
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 2e516b12e5109470c1ddb86ea6a665ca29f138b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367073"
---
# <a name="zwquerysysteminformation-function"></a>Zwquerysysteminformation-Funktion

\[**Zwquerysysteminformation** ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen die in diesem Thema aufgeführten Alternativen Funktionen.\]

Ruft die angegebenen Systeminformationen ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Systeminformationclass* \[ in\]
</dt> <dd>

Der Typ der Systeminformationen, die abgerufen werden sollen. Dieser Parameter kann einer der folgenden Werte aus dem Enumerationstyp der **System \_ Informations \_ Klasse** sein.

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**Systembasicinformation**


</dt> <dd>

Die Anzahl der Prozessoren im System in einer **System \_ grundlegenden \_ Informations** Struktur. Verwenden Sie stattdessen die [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) -Funktion.

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**Systemperformanceinformation**


</dt> <dd>

Eine nicht **transparente \_ Systemleistungs \_ Informations** Struktur, die verwendet werden kann, um einen unvorhersehbaren Ausgangswert für einen Zufallszahlengenerator zu generieren. Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ".

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**Systemtimeofdayinformation**


</dt> <dd>

Eine nicht **transparente \_ systemtimeofday- \_ Informations** Struktur, die verwendet werden kann, um einen unvorhersehbaren Ausgangswert für einen Zufallszahlengenerator zu generieren. Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ".

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**Systemprocessinformation**


</dt> <dd>

Ein Array von **System \_ Prozess \_ Informations** Strukturen, eines für jeden Prozess, der im System ausgeführt wird.

Diese Strukturen enthalten Informationen über die Ressourcenverwendung der einzelnen Prozesse, einschließlich der Anzahl der Handles, die vom Prozess verwendet werden, der Verwendung von Spitzen Seiten Dateien und der Anzahl von Speicherseiten, die vom Prozess zugeordnet wurden.

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**Systemprocessorperformanceinformation**


</dt> <dd>

Ein Array von **\_ \_ systemprozessorleistungs- \_ Informations** Strukturen, eines für jeden im System installierten Prozessor.

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**Systeminterruptinformation**


</dt> <dd>

Eine nicht **transparente \_ \_ Informations** Struktur zum Unterbrechen von Systemen, die zum Generieren eines unvorhersehbaren Ausgangswert für einen Zufallszahlen-Generator verwendet werden kann. Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ".

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**Systemexceptioninformation**


</dt> <dd>

Eine nicht transparente **System \_ Ausnahme \_ Informations** Struktur, die verwendet werden kann, um einen unvorhersehbaren Ausgangswert für einen Zufallszahlengenerator zu generieren. Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ".

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**Systemregistryquotainformation**


</dt> <dd>

Eine **\_ \_ Kontingent \_ Informationsstruktur der System Registrierung** .

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**Systemlookasideinformation**


</dt> <dd>

Eine nicht **transparente \_ systemlookaside- \_ Informations** Struktur, die verwendet werden kann, um einen unvorhersehbaren Ausgangswert für einen Zufallszahlengenerator zu generieren. Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ".

</dd> </dl> </dd> <dt>

*SystemInformation* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die angeforderten Informationen empfängt. Die Größe und die Struktur dieser Informationen variieren abhängig vom Wert des Parameters " *systeminformationclass* ", wie in der folgenden Tabelle angegeben.

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**\_grundlegende \_ Informationen zu System**


</dt> <dd>

Wenn der *systeminformationclass* -Parameter **systembasicinformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um eine einzelne **System \_ grundlegende \_ Informations** Struktur mit folgendem Layout zu enthalten:

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

Das Element " **numofprocessor** " enthält die Anzahl der Prozessoren, die im System vorhanden sind. Verwenden Sie stattdessen [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) , um diese Informationen abzurufen.

Die anderen Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**Informationen zur System \_ Leistung \_**


</dt> <dd>

Wenn der *systeminformationclass* -Parameter **systemperformanceinformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um eine nicht transparente **\_ Systemleistungs \_ Informations** Struktur zu erhalten, die zum Generieren eines unvorhersehbaren Ausgangswert für einen Zufallszahlen-Generator verwendet werden kann. Zu diesem Zweck hat die Struktur folgendes Layout:

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

Einzelne Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.

Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ", um kryptografisch zufällige Daten zu generieren.

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**\_Informationen zum systemtimeofday \_**


</dt> <dd>

Wenn der *systeminformationclass* -Parameter **systemtimeofdayinformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um eine nicht transparente **\_ systemtimeofday- \_ Informations** Struktur zu verwenden, die zum Generieren eines unvorhersehbaren Ausgangswert für einen Zufallszahlen-Generator verwendet wird. Zu diesem Zweck hat die Struktur folgendes Layout:

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

Einzelne Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.

Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ", um kryptografisch zufällige Daten zu generieren.

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**System \_ Prozess \_ Informationen**


</dt> <dd>

Wenn der *systeminformationclass* -Parameter auf **systemprocessinformation** festgelegt ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um ein Array aufzunehmen, das so viele **System \_ Prozess \_ Informations** Strukturen enthält, wie Prozesse im System ausgeführt werden. Jede Struktur verfügt über das folgende Layout:

``` syntax
typedef struct _SYSTEM_PROCESS_INFORMATION {
    ULONG NextEntryOffset;
    ULONG NumberOfThreads;
    BYTE Reserved1[48];
    PVOID Reserved2[3];
    HANDLE UniqueProcessId;
    PVOID Reserved3;
    ULONG HandleCount;
    BYTE Reserved4[4];
    PVOID Reserved5[11];
    SIZE_T PeakPagefileUsage;
    SIZE_T PrivatePageCount;
    LARGE_INTEGER Reserved6[6];
} SYSTEM_PROCESS_INFORMATION;
```

Das Element " **zahlungsthreads** " enthält die Gesamtzahl der derzeit im Prozess laufenden Threads.

Das Element " **Lenker Anzahl** " enthält die Gesamtanzahl der Handles, die vom fraglichen Prozess verwendet werden. Verwenden Sie stattdessen [**getprocesshandlecount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) , um diese Informationen abzurufen.

Der Member " **etakpagefileusage** " enthält die maximale Anzahl von Bytes, die vom Prozess verwendet werden, und das Element " **PrivatePageCount** " enthält die Anzahl der Speicherseiten, die für die Verwendung dieses Prozesses reserviert werden.

Sie können diese Informationen auch mit der [**getprocessmemoryinfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) -Funktion oder der [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse abrufen.

Die anderen Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**Informationen zur System \_ Prozessor \_ Leistung \_**


</dt> <dd>

Wenn der *systeminformationclass* -Parameter **systemprocessorperformanceinformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um ein Array aufzunehmen, das so viele **System \_ Prozess \_ Informations** Strukturen enthält, wie Prozessoren (CPUs) im System installiert sind. Jede Struktur verfügt über das folgende Layout:

``` syntax
typedef struct
_SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION {
    LARGE_INTEGER IdleTime;
    LARGE_INTEGER KernelTime;
    LARGE_INTEGER UserTime;
    LARGE_INTEGER Reserved1[2];
    ULONG Reserved2;
} SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION;
```

Das **IdleTime** -Element enthält den Zeitraum, in dem sich das System im Leerlauf befunden hat (in 1/Hundertstel einer Nanosekunde).

Der **kerneltime** -Member enthält die Zeitspanne, die das System für die Ausführung im Kernel Modus aufgewendet hat (einschließlich aller Threads in allen Prozessen auf allen Prozessoren), in 1/Hundertstel einer Nanosekunde.

Das **usertime** -Element enthält die Zeitspanne, die das System für die Ausführung im Benutzermodus aufgewendet hat (einschließlich aller Threads in allen Prozessen, auf allen Prozessoren), in 1/Hundertstel einer Nanosekunde.

Verwenden Sie stattdessen [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) , um diese Informationen abzurufen.

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**\_ \_ systeminterruptinformationen**


</dt> <dd>

Wenn der *systeminformationclass* -Parameter **systeminterruptinformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um ein Array aufzunehmen, das so viele nicht transparente **\_ Systeminterrupt- \_ Informations** Strukturen enthält, wie Prozessoren (CPUs) auf dem System installiert sind. Jede Struktur bzw. das Array als Ganzes kann verwendet werden, um einen unvorhersehbaren Ausgangswert für einen Zufallszahlengenerator zu generieren. Zu diesem Zweck hat die Struktur folgendes Layout:

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

Einzelne Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.

Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ", um kryptografisch zufällige Daten zu generieren.

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**System \_ Ausnahme \_ Informationen**


</dt> <dd>

Wenn der *systeminformationclass* -Parameter " **systemexceptioninformation**" ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um eine nicht transparente **System \_ Ausnahme \_ Informations** Struktur zu verwenden, die zum Generieren eines unvorhersehbaren Ausgangswert für einen Zufallszahlengenerator verwendet werden kann. Zu diesem Zweck hat die Struktur folgendes Layout:

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

Einzelne Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.

Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ", um kryptografisch zufällige Daten zu generieren.

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**Informationen zu System \_ Registrierungs \_ Kontingenten \_**


</dt> <dd>

Wenn der *systeminformationclass* -Parameter **systemregistryquotainformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um eine einzelne **\_ \_ Kontingent \_ Informationsstruktur mit System Registrierung** mit folgendem Layout zu enthalten:

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

Der **registryquotaallowed** -Member enthält die maximale Größe (in Bytes), die die Registrierung auf diesem System erreichen kann.

Der **registryquotaused** -Member enthält die aktuelle Größe der Registrierung (in Bytes).

Verwenden Sie stattdessen [**getsystemregistryquota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) , um diese Informationen abzurufen.

Der andere Member der Struktur ist für die interne Verwendung durch das Betriebssystem reserviert.

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**Informationen zu System \_ Lookaside \_**


</dt> <dd>

Wenn der *systeminformationclass* -Parameter **systemlookasideinformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um eine nicht transparente **System \_ Lookaside- \_ Informations** Struktur zu erhalten, die zum Generieren eines unvorhersehbaren Ausgangswert für einen Zufallszahlen-Generator verwendet werden kann. Zu diesem Zweck hat die Struktur folgendes Layout:

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

Einzelne Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.

Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ", um kryptografisch zufällige Daten zu generieren.

</dd> </dl> </dd> <dt>

*Systeminformationlength* \[ in\]
</dt> <dd>

Die Größe des Puffers, auf den der *SystemInformation* -Parameter zeigt (in Bytes).

</dd> <dt>

*Returnlength* \[ Out, optional\]
</dt> <dd>

Ein optionaler Zeiger auf einen Speicherort, an dem die Funktion die tatsächliche Größe der angeforderten Informationen schreibt. Wenn diese Größe kleiner oder gleich dem *systeminformationlength* -Parameter ist, kopiert die Funktion die Informationen in den *SystemInformation* -Puffer. Andernfalls wird ein NTSTATUS-Fehlercode zurückgegeben, und die Größe des Puffers, der zum Empfangen der angeforderten Informationen erforderlich ist, wird zurück *gegeben* .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Erfolg von NTSTATUS oder einen Fehlercode zurück.

Die Formulare und die Bedeutung von NTSTATUS-Fehlercodes werden in der im DDK verfügbaren NTSTATUS. h-Header Datei aufgeführt und in der DDK-Dokumentation beschrieben.

## <a name="remarks"></a>Bemerkungen

Die **zwquerysysteminformation** -Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden. Um die Kompatibilität Ihrer Anwendung aufrechtzuerhalten, ist es besser, stattdessen die zuvor erwähnten alternativen Funktionen zu verwenden.

Wenn Sie **zwquerysysteminformation** verwenden, greifen Sie über das [dynamische Verknüpfen der Laufzeit](/windows/desktop/Dlls/using-run-time-dynamic-linking)auf die Funktion zu. Dadurch erhält Ihr Code die Möglichkeit, ordnungsgemäß zu reagieren, wenn die Funktion geändert oder aus dem Betriebssystem entfernt wurde. Signatur Änderungen sind jedoch möglicherweise nicht erkennbar.

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[**Getprocesshandlecount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[**Getprocessmemoryinfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[**Getsystemregistryquota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 

