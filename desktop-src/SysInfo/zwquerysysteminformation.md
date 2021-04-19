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
# <a name="zwquerysysteminformation-function"></a><span data-ttu-id="51e65-103">Zwquerysysteminformation-Funktion</span><span class="sxs-lookup"><span data-stu-id="51e65-103">ZwQuerySystemInformation function</span></span>

<span data-ttu-id="51e65-104">\[**Zwquerysysteminformation** ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="51e65-104">\[**ZwQuerySystemInformation** is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="51e65-105">Verwenden Sie stattdessen die in diesem Thema aufgeführten Alternativen Funktionen.\]</span><span class="sxs-lookup"><span data-stu-id="51e65-105">Instead, use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="51e65-106">Ruft die angegebenen Systeminformationen ab.</span><span class="sxs-lookup"><span data-stu-id="51e65-106">Retrieves the specified system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e65-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="51e65-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="51e65-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="51e65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e65-109">*Systeminformationclass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51e65-109">*SystemInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e65-110">Der Typ der Systeminformationen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51e65-110">The type of system information to be retrieved.</span></span> <span data-ttu-id="51e65-111">Dieser Parameter kann einer der folgenden Werte aus dem Enumerationstyp der **System \_ Informations \_ Klasse** sein.</span><span class="sxs-lookup"><span data-stu-id="51e65-111">This parameter can be one of the following values from the **SYSTEM\_INFORMATION\_CLASS** enumeration type.</span></span>

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span data-ttu-id="51e65-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**Systembasicinformation**</span><span class="sxs-lookup"><span data-stu-id="51e65-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-113">Die Anzahl der Prozessoren im System in einer **System \_ grundlegenden \_ Informations** Struktur.</span><span class="sxs-lookup"><span data-stu-id="51e65-113">The number of processors in the system in a **SYSTEM\_BASIC\_INFORMATION** structure.</span></span> <span data-ttu-id="51e65-114">Verwenden Sie stattdessen die [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="51e65-114">Use the [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function instead.</span></span>

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span data-ttu-id="51e65-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**Systemperformanceinformation**</span><span class="sxs-lookup"><span data-stu-id="51e65-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-116">Eine nicht **transparente \_ Systemleistungs \_ Informations** Struktur, die verwendet werden kann, um einen unvorhersehbaren Ausgangswert für einen Zufallszahlengenerator zu generieren.</span><span class="sxs-lookup"><span data-stu-id="51e65-116">An opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="51e65-117">Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ".</span><span class="sxs-lookup"><span data-stu-id="51e65-117">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span data-ttu-id="51e65-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**Systemtimeofdayinformation**</span><span class="sxs-lookup"><span data-stu-id="51e65-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-119">Eine nicht **transparente \_ systemtimeofday- \_ Informations** Struktur, die verwendet werden kann, um einen unvorhersehbaren Ausgangswert für einen Zufallszahlengenerator zu generieren.</span><span class="sxs-lookup"><span data-stu-id="51e65-119">An opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="51e65-120">Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ".</span><span class="sxs-lookup"><span data-stu-id="51e65-120">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span data-ttu-id="51e65-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**Systemprocessinformation**</span><span class="sxs-lookup"><span data-stu-id="51e65-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-122">Ein Array von **System \_ Prozess \_ Informations** Strukturen, eines für jeden Prozess, der im System ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51e65-122">An array of **SYSTEM\_PROCESS\_INFORMATION** structures, one for each process running in the system.</span></span>

<span data-ttu-id="51e65-123">Diese Strukturen enthalten Informationen über die Ressourcenverwendung der einzelnen Prozesse, einschließlich der Anzahl der Handles, die vom Prozess verwendet werden, der Verwendung von Spitzen Seiten Dateien und der Anzahl von Speicherseiten, die vom Prozess zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="51e65-123">These structures contain information about the resource usage of each process, including the number of handles used by the process, the peak page-file usage, and the number of memory pages that the process has allocated.</span></span>

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span data-ttu-id="51e65-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**Systemprocessorperformanceinformation**</span><span class="sxs-lookup"><span data-stu-id="51e65-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-125">Ein Array von **\_ \_ systemprozessorleistungs- \_ Informations** Strukturen, eines für jeden im System installierten Prozessor.</span><span class="sxs-lookup"><span data-stu-id="51e65-125">An array of **SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION** structures, one for each processor installed in the system.</span></span>

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span data-ttu-id="51e65-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**Systeminterruptinformation**</span><span class="sxs-lookup"><span data-stu-id="51e65-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-127">Eine nicht **transparente \_ \_ Informations** Struktur zum Unterbrechen von Systemen, die zum Generieren eines unvorhersehbaren Ausgangswert für einen Zufallszahlen-Generator verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="51e65-127">An opaque **SYSTEM\_INTERRUPT\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="51e65-128">Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ".</span><span class="sxs-lookup"><span data-stu-id="51e65-128">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span data-ttu-id="51e65-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**Systemexceptioninformation**</span><span class="sxs-lookup"><span data-stu-id="51e65-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-130">Eine nicht transparente **System \_ Ausnahme \_ Informations** Struktur, die verwendet werden kann, um einen unvorhersehbaren Ausgangswert für einen Zufallszahlengenerator zu generieren.</span><span class="sxs-lookup"><span data-stu-id="51e65-130">An opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="51e65-131">Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ".</span><span class="sxs-lookup"><span data-stu-id="51e65-131">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span data-ttu-id="51e65-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**Systemregistryquotainformation**</span><span class="sxs-lookup"><span data-stu-id="51e65-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-133">Eine **\_ \_ Kontingent \_ Informationsstruktur der System Registrierung** .</span><span class="sxs-lookup"><span data-stu-id="51e65-133">A **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure.</span></span>

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span data-ttu-id="51e65-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**Systemlookasideinformation**</span><span class="sxs-lookup"><span data-stu-id="51e65-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-135">Eine nicht **transparente \_ systemlookaside- \_ Informations** Struktur, die verwendet werden kann, um einen unvorhersehbaren Ausgangswert für einen Zufallszahlengenerator zu generieren.</span><span class="sxs-lookup"><span data-stu-id="51e65-135">An opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="51e65-136">Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ".</span><span class="sxs-lookup"><span data-stu-id="51e65-136">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="51e65-137">*SystemInformation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="51e65-137">*SystemInformation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="51e65-138">Ein Zeiger auf einen Puffer, der die angeforderten Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="51e65-138">A pointer to a buffer that receives the requested information.</span></span> <span data-ttu-id="51e65-139">Die Größe und die Struktur dieser Informationen variieren abhängig vom Wert des Parameters " *systeminformationclass* ", wie in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="51e65-139">The size and structure of this information varies depending on the value of the *SystemInformationClass* parameter, as indicated in the following table.</span></span>

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span data-ttu-id="51e65-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**\_grundlegende \_ Informationen zu System**</span><span class="sxs-lookup"><span data-stu-id="51e65-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**SYSTEM\_BASIC\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-141">Wenn der *systeminformationclass* -Parameter **systembasicinformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um eine einzelne **System \_ grundlegende \_ Informations** Struktur mit folgendem Layout zu enthalten:</span><span class="sxs-lookup"><span data-stu-id="51e65-141">When the *SystemInformationClass* parameter is **SystemBasicInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

<span data-ttu-id="51e65-142">Das Element " **numofprocessor** " enthält die Anzahl der Prozessoren, die im System vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="51e65-142">The **NumberOfProcessors** member contains the number of processors present in the system.</span></span> <span data-ttu-id="51e65-143">Verwenden Sie stattdessen [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) , um diese Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="51e65-143">Use [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) instead to retrieve this information.</span></span>

<span data-ttu-id="51e65-144">Die anderen Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.</span><span class="sxs-lookup"><span data-stu-id="51e65-144">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span data-ttu-id="51e65-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**Informationen zur System \_ Leistung \_**</span><span class="sxs-lookup"><span data-stu-id="51e65-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**SYSTEM\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-146">Wenn der *systeminformationclass* -Parameter **systemperformanceinformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um eine nicht transparente **\_ Systemleistungs \_ Informations** Struktur zu erhalten, die zum Generieren eines unvorhersehbaren Ausgangswert für einen Zufallszahlen-Generator verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="51e65-146">When the *SystemInformationClass* parameter is **SystemPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="51e65-147">Zu diesem Zweck hat die Struktur folgendes Layout:</span><span class="sxs-lookup"><span data-stu-id="51e65-147">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

<span data-ttu-id="51e65-148">Einzelne Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.</span><span class="sxs-lookup"><span data-stu-id="51e65-148">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="51e65-149">Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ", um kryptografisch zufällige Daten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="51e65-149">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span data-ttu-id="51e65-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**\_Informationen zum systemtimeofday \_**</span><span class="sxs-lookup"><span data-stu-id="51e65-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**SYSTEM\_TIMEOFDAY\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-151">Wenn der *systeminformationclass* -Parameter **systemtimeofdayinformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um eine nicht transparente **\_ systemtimeofday- \_ Informations** Struktur zu verwenden, die zum Generieren eines unvorhersehbaren Ausgangswert für einen Zufallszahlen-Generator verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51e65-151">When the *SystemInformationClass* parameter is **SystemTimeOfDayInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="51e65-152">Zu diesem Zweck hat die Struktur folgendes Layout:</span><span class="sxs-lookup"><span data-stu-id="51e65-152">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

<span data-ttu-id="51e65-153">Einzelne Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.</span><span class="sxs-lookup"><span data-stu-id="51e65-153">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="51e65-154">Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ", um kryptografisch zufällige Daten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="51e65-154">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span data-ttu-id="51e65-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**System \_ Prozess \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="51e65-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**SYSTEM\_PROCESS\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-156">Wenn der *systeminformationclass* -Parameter auf **systemprocessinformation** festgelegt ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um ein Array aufzunehmen, das so viele **System \_ Prozess \_ Informations** Strukturen enthält, wie Prozesse im System ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="51e65-156">When the *SystemInformationClass* parameter is **SystemProcessInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processes running in the system.</span></span> <span data-ttu-id="51e65-157">Jede Struktur verfügt über das folgende Layout:</span><span class="sxs-lookup"><span data-stu-id="51e65-157">Each structure has the following layout:</span></span>

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

<span data-ttu-id="51e65-158">Das Element " **zahlungsthreads** " enthält die Gesamtzahl der derzeit im Prozess laufenden Threads.</span><span class="sxs-lookup"><span data-stu-id="51e65-158">The **NumberOfThreads** member contains the total number of currently running threads in the process.</span></span>

<span data-ttu-id="51e65-159">Das Element " **Lenker Anzahl** " enthält die Gesamtanzahl der Handles, die vom fraglichen Prozess verwendet werden. Verwenden Sie stattdessen [**getprocesshandlecount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) , um diese Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="51e65-159">The **HandleCount** member contains the total number of handles being used by the process in question; use [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) to retrieve this information instead.</span></span>

<span data-ttu-id="51e65-160">Der Member " **etakpagefileusage** " enthält die maximale Anzahl von Bytes, die vom Prozess verwendet werden, und das Element " **PrivatePageCount** " enthält die Anzahl der Speicherseiten, die für die Verwendung dieses Prozesses reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="51e65-160">The **PeakPagefileUsage** member contains the maximum number of bytes of page-file storage used by the process, and the **PrivatePageCount** member contains the number of memory pages allocated for the use of this process.</span></span>

<span data-ttu-id="51e65-161">Sie können diese Informationen auch mit der [**getprocessmemoryinfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) -Funktion oder der [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse abrufen.</span><span class="sxs-lookup"><span data-stu-id="51e65-161">You can also retrieve this information using either the [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) function or the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span>

<span data-ttu-id="51e65-162">Die anderen Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.</span><span class="sxs-lookup"><span data-stu-id="51e65-162">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span data-ttu-id="51e65-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**Informationen zur System \_ Prozessor \_ Leistung \_**</span><span class="sxs-lookup"><span data-stu-id="51e65-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-164">Wenn der *systeminformationclass* -Parameter **systemprocessorperformanceinformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um ein Array aufzunehmen, das so viele **System \_ Prozess \_ Informations** Strukturen enthält, wie Prozessoren (CPUs) im System installiert sind.</span><span class="sxs-lookup"><span data-stu-id="51e65-164">When the *SystemInformationClass* parameter is **SystemProcessorPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processors (CPUs) installed in the system.</span></span> <span data-ttu-id="51e65-165">Jede Struktur verfügt über das folgende Layout:</span><span class="sxs-lookup"><span data-stu-id="51e65-165">Each structure has the following layout:</span></span>

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

<span data-ttu-id="51e65-166">Das **IdleTime** -Element enthält den Zeitraum, in dem sich das System im Leerlauf befunden hat (in 1/Hundertstel einer Nanosekunde).</span><span class="sxs-lookup"><span data-stu-id="51e65-166">The **IdleTime** member contains the amount of time that the system has been idle, in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="51e65-167">Der **kerneltime** -Member enthält die Zeitspanne, die das System für die Ausführung im Kernel Modus aufgewendet hat (einschließlich aller Threads in allen Prozessen auf allen Prozessoren), in 1/Hundertstel einer Nanosekunde.</span><span class="sxs-lookup"><span data-stu-id="51e65-167">The **KernelTime** member contains the amount of time that the system has spent executing in Kernel mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="51e65-168">Das **usertime** -Element enthält die Zeitspanne, die das System für die Ausführung im Benutzermodus aufgewendet hat (einschließlich aller Threads in allen Prozessen, auf allen Prozessoren), in 1/Hundertstel einer Nanosekunde.</span><span class="sxs-lookup"><span data-stu-id="51e65-168">The **UserTime** member contains the amount of time that the system has spent executing in User mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="51e65-169">Verwenden Sie stattdessen [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) , um diese Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="51e65-169">Use [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) instead to retrieve this information.</span></span>

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span data-ttu-id="51e65-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**\_ \_ systeminterruptinformationen**</span><span class="sxs-lookup"><span data-stu-id="51e65-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**SYSTEM\_INTERRUPT\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-171">Wenn der *systeminformationclass* -Parameter **systeminterruptinformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um ein Array aufzunehmen, das so viele nicht transparente **\_ Systeminterrupt- \_ Informations** Strukturen enthält, wie Prozessoren (CPUs) auf dem System installiert sind.</span><span class="sxs-lookup"><span data-stu-id="51e65-171">When the *SystemInformationClass* parameter is **SystemInterruptInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many opaque **SYSTEM\_INTERRUPT\_INFORMATION** structures as there are processors (CPUs) installed on the system.</span></span> <span data-ttu-id="51e65-172">Jede Struktur bzw. das Array als Ganzes kann verwendet werden, um einen unvorhersehbaren Ausgangswert für einen Zufallszahlengenerator zu generieren.</span><span class="sxs-lookup"><span data-stu-id="51e65-172">Each structure, or the array as a whole, can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="51e65-173">Zu diesem Zweck hat die Struktur folgendes Layout:</span><span class="sxs-lookup"><span data-stu-id="51e65-173">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

<span data-ttu-id="51e65-174">Einzelne Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.</span><span class="sxs-lookup"><span data-stu-id="51e65-174">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="51e65-175">Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ", um kryptografisch zufällige Daten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="51e65-175">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span data-ttu-id="51e65-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**System \_ Ausnahme \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="51e65-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**SYSTEM\_EXCEPTION\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-177">Wenn der *systeminformationclass* -Parameter " **systemexceptioninformation**" ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um eine nicht transparente **System \_ Ausnahme \_ Informations** Struktur zu verwenden, die zum Generieren eines unvorhersehbaren Ausgangswert für einen Zufallszahlengenerator verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="51e65-177">When the *SystemInformationClass* parameter is **SystemExceptionInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="51e65-178">Zu diesem Zweck hat die Struktur folgendes Layout:</span><span class="sxs-lookup"><span data-stu-id="51e65-178">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

<span data-ttu-id="51e65-179">Einzelne Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.</span><span class="sxs-lookup"><span data-stu-id="51e65-179">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="51e65-180">Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ", um kryptografisch zufällige Daten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="51e65-180">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span data-ttu-id="51e65-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**Informationen zu System \_ Registrierungs \_ Kontingenten \_**</span><span class="sxs-lookup"><span data-stu-id="51e65-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**SYSTEM\_REGISTRY\_QUOTA\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-182">Wenn der *systeminformationclass* -Parameter **systemregistryquotainformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um eine einzelne **\_ \_ Kontingent \_ Informationsstruktur mit System Registrierung** mit folgendem Layout zu enthalten:</span><span class="sxs-lookup"><span data-stu-id="51e65-182">When the *SystemInformationClass* parameter is **SystemRegistryQuotaInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

<span data-ttu-id="51e65-183">Der **registryquotaallowed** -Member enthält die maximale Größe (in Bytes), die die Registrierung auf diesem System erreichen kann.</span><span class="sxs-lookup"><span data-stu-id="51e65-183">The **RegistryQuotaAllowed** member contains the maximum size, in bytes, that the Registry can attain on this system.</span></span>

<span data-ttu-id="51e65-184">Der **registryquotaused** -Member enthält die aktuelle Größe der Registrierung (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="51e65-184">The **RegistryQuotaUsed** member contains the current size of the Registry, in bytes.</span></span>

<span data-ttu-id="51e65-185">Verwenden Sie stattdessen [**getsystemregistryquota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) , um diese Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="51e65-185">Use [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) instead to retrieve this information.</span></span>

<span data-ttu-id="51e65-186">Der andere Member der Struktur ist für die interne Verwendung durch das Betriebssystem reserviert.</span><span class="sxs-lookup"><span data-stu-id="51e65-186">The other member of the structure is reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span data-ttu-id="51e65-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**Informationen zu System \_ Lookaside \_**</span><span class="sxs-lookup"><span data-stu-id="51e65-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**SYSTEM\_LOOKASIDE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="51e65-188">Wenn der *systeminformationclass* -Parameter **systemlookasideinformation** ist, sollte der Puffer, auf den der *SystemInformation* -Parameter verweist, groß genug sein, um eine nicht transparente **System \_ Lookaside- \_ Informations** Struktur zu erhalten, die zum Generieren eines unvorhersehbaren Ausgangswert für einen Zufallszahlen-Generator verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="51e65-188">When the *SystemInformationClass* parameter is **SystemLookasideInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="51e65-189">Zu diesem Zweck hat die Struktur folgendes Layout:</span><span class="sxs-lookup"><span data-stu-id="51e65-189">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

<span data-ttu-id="51e65-190">Einzelne Mitglieder der Struktur sind für die interne Verwendung durch das Betriebssystem reserviert.</span><span class="sxs-lookup"><span data-stu-id="51e65-190">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="51e65-191">Verwenden Sie stattdessen die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) ", um kryptografisch zufällige Daten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="51e65-191">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="51e65-192">*Systeminformationlength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51e65-192">*SystemInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e65-193">Die Größe des Puffers, auf den der *SystemInformation* -Parameter zeigt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="51e65-193">The size of the buffer pointed to by the *SystemInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="51e65-194">*Returnlength* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="51e65-194">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="51e65-195">Ein optionaler Zeiger auf einen Speicherort, an dem die Funktion die tatsächliche Größe der angeforderten Informationen schreibt.</span><span class="sxs-lookup"><span data-stu-id="51e65-195">An optional pointer to a location where the function writes the actual size of the information requested.</span></span> <span data-ttu-id="51e65-196">Wenn diese Größe kleiner oder gleich dem *systeminformationlength* -Parameter ist, kopiert die Funktion die Informationen in den *SystemInformation* -Puffer. Andernfalls wird ein NTSTATUS-Fehlercode zurückgegeben, und die Größe des Puffers, der zum Empfangen der angeforderten Informationen erforderlich ist, wird zurück *gegeben* .</span><span class="sxs-lookup"><span data-stu-id="51e65-196">If that size is less than or equal to the *SystemInformationLength* parameter, the function copies the information into the *SystemInformation* buffer; otherwise, it returns an NTSTATUS error code and returns in *ReturnLength* the size of buffer required to receive the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e65-197">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51e65-197">Return value</span></span>

<span data-ttu-id="51e65-198">Gibt einen Erfolg von NTSTATUS oder einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="51e65-198">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="51e65-199">Die Formulare und die Bedeutung von NTSTATUS-Fehlercodes werden in der im DDK verfügbaren NTSTATUS. h-Header Datei aufgeführt und in der DDK-Dokumentation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="51e65-199">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="51e65-200">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51e65-200">Remarks</span></span>

<span data-ttu-id="51e65-201">Die **zwquerysysteminformation** -Funktion und die zurückgegebenen Strukturen sind intern für das Betriebssystem und können von einer Version von Windows in eine andere geändert werden.</span><span class="sxs-lookup"><span data-stu-id="51e65-201">The **ZwQuerySystemInformation** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="51e65-202">Um die Kompatibilität Ihrer Anwendung aufrechtzuerhalten, ist es besser, stattdessen die zuvor erwähnten alternativen Funktionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="51e65-202">To maintain the compatibility of your application, it is better to use the alternate functions previously mentioned instead.</span></span>

<span data-ttu-id="51e65-203">Wenn Sie **zwquerysysteminformation** verwenden, greifen Sie über das [dynamische Verknüpfen der Laufzeit](/windows/desktop/Dlls/using-run-time-dynamic-linking)auf die Funktion zu.</span><span class="sxs-lookup"><span data-stu-id="51e65-203">If you do use **ZwQuerySystemInformation**, access the function through [run-time dynamic linking](/windows/desktop/Dlls/using-run-time-dynamic-linking).</span></span> <span data-ttu-id="51e65-204">Dadurch erhält Ihr Code die Möglichkeit, ordnungsgemäß zu reagieren, wenn die Funktion geändert oder aus dem Betriebssystem entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="51e65-204">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="51e65-205">Signatur Änderungen sind jedoch möglicherweise nicht erkennbar.</span><span class="sxs-lookup"><span data-stu-id="51e65-205">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="51e65-206">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="51e65-206">This function has no associated import library.</span></span> <span data-ttu-id="51e65-207">Sie müssen die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="51e65-207">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e65-208">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51e65-208">Requirements</span></span>



| <span data-ttu-id="51e65-209">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51e65-209">Requirement</span></span> | <span data-ttu-id="51e65-210">Wert</span><span class="sxs-lookup"><span data-stu-id="51e65-210">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="51e65-211">DLL</span><span class="sxs-lookup"><span data-stu-id="51e65-211">DLL</span></span><br/> | <dl> <span data-ttu-id="51e65-212"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51e65-212"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51e65-213">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51e65-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e65-214">**GetSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="51e65-214">**GetSystemInfo**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[<span data-ttu-id="51e65-215">**Getprocesshandlecount**</span><span class="sxs-lookup"><span data-stu-id="51e65-215">**GetProcessHandleCount**</span></span>](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[<span data-ttu-id="51e65-216">**Getprocessmemoryinfo**</span><span class="sxs-lookup"><span data-stu-id="51e65-216">**GetProcessMemoryInfo**</span></span>](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[<span data-ttu-id="51e65-217">**GetSystemTimes**</span><span class="sxs-lookup"><span data-stu-id="51e65-217">**GetSystemTimes**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[<span data-ttu-id="51e65-218">**Getsystemregistryquota**</span><span class="sxs-lookup"><span data-stu-id="51e65-218">**GetSystemRegistryQuota**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 

