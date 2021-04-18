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
# <a name="getsystemcpusetinformation-function"></a><span data-ttu-id="ba1eb-103">Getsystemcpusetinformation-Funktion</span><span class="sxs-lookup"><span data-stu-id="ba1eb-103">GetSystemCpuSetInformation function</span></span>

<span data-ttu-id="ba1eb-104">Ermöglicht einer Anwendung das Abfragen der verfügbaren CPU-Sätze im System und Ihres aktuellen Zustands.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-104">Allows an application to query the available CPU Sets on the system, and their current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba1eb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba1eb-105">Syntax</span></span>


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a><span data-ttu-id="ba1eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba1eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba1eb-107">*Informationen* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="ba1eb-107">*Information* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1eb-108">Ein Zeiger auf eine [**System- \_ CPU- \_ Satz \_ Informations**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) Struktur, die die CPU-Satz Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-108">A pointer to a [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure that receives the CPU Set data.</span></span> <span data-ttu-id="ba1eb-109">Übergeben Sie NULL mit der Pufferlänge 0, um die erforderliche Puffergröße zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-109">Pass NULL with a buffer length of 0 to determine the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="ba1eb-110">*BufferLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba1eb-110">*BufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1eb-111">Die Länge (in Byte) des Ausgabepuffers, der als Informations Argument übergangen wird.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-111">The length, in bytes, of the output buffer passed as the Information argument.</span></span>

</dd> <dt>

<span data-ttu-id="ba1eb-112">*Rückkehrnedlength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ba1eb-112">*ReturnedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1eb-113">Die Länge (in Byte) der gültigen Daten im Ausgabepuffer, wenn der Puffer groß genug ist, oder die erforderliche Größe des Ausgabepuffers.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-113">The length, in bytes, of the valid data in the output buffer if the buffer is large enough, or the required size of the output buffer.</span></span> <span data-ttu-id="ba1eb-114">Wenn keine CPU-Sätze vorhanden sind, ist dieser Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ba1eb-114">If no CPU Sets exist, this value will be 0.</span></span>

</dd> <dt>

<span data-ttu-id="ba1eb-115">*Prozess* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ba1eb-115">*Process* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1eb-116">Ein optionales Handle für einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-116">An optional handle to a process.</span></span> <span data-ttu-id="ba1eb-117">Dieser Prozess wird verwendet, um den Wert des "  zugsverzeichnis"-Flags in der System- \_ CPU \_ - \_ Informationsstruktur festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-117">This process is used to determine the value of the **AllocatedToTargetProcess** flag in the SYSTEM\_CPU\_SET\_INFORMATION structure.</span></span> <span data-ttu-id="ba1eb-118">Wenn eine CPU-Menge dem angegebenen Prozess zugeordnet ist, wird das-Flag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-118">If a CPU Set is allocated to the specified process, the flag is set.</span></span> <span data-ttu-id="ba1eb-119">Andernfalls ist es eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-119">Otherwise, it is clear.</span></span> <span data-ttu-id="ba1eb-120">Dieses Handle muss über das Recht "Prozess \_ Abfrage \_ beschränkte Informationen" verfügen \_ .</span><span class="sxs-lookup"><span data-stu-id="ba1eb-120">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="ba1eb-121">Der von [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) zurückgegebene Wert kann hier ebenfalls angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-121">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) may also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="ba1eb-122">*Flags*</span><span class="sxs-lookup"><span data-stu-id="ba1eb-122">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="ba1eb-123">Reserviert, muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-123">Reserved, must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba1eb-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba1eb-124">Return value</span></span>

<span data-ttu-id="ba1eb-125">Wenn die API erfolgreich ist, wird true zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-125">If the API succeeds it returns TRUE.</span></span> <span data-ttu-id="ba1eb-126">Wenn dies nicht möglich ist, ist die Fehlerursache über **GetLastError** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-126">If it fails, the error reason is available through **GetLastError**.</span></span> <span data-ttu-id="ba1eb-127">Wenn der Informations Puffer NULL oder nicht groß genug ist, wird der Fehlercode Fehler "nicht \_ genügend \_ Puffer" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-127">If the Information buffer was NULL or not large enough, the error code ERROR\_INSUFFICIENT\_BUFFER is returned.</span></span> <span data-ttu-id="ba1eb-128">Diese API kann nicht fehlschlagen, wenn gültige Parameter und ein Puffer bestanden werden, der groß genug ist, um alle Rückgabe Daten aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="ba1eb-128">This API cannot fail when passed valid parameters and a buffer that is large enough to hold all of the return data.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba1eb-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba1eb-129">Requirements</span></span>



| <span data-ttu-id="ba1eb-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba1eb-130">Requirement</span></span> | <span data-ttu-id="ba1eb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ba1eb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba1eb-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba1eb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ba1eb-133">Windows 10 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ba1eb-133">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="ba1eb-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba1eb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ba1eb-135">Windows Server 2016 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ba1eb-135">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="ba1eb-136">Header</span><span class="sxs-lookup"><span data-stu-id="ba1eb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba1eb-137"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba1eb-137"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="ba1eb-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ba1eb-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba1eb-139"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba1eb-139"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="ba1eb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ba1eb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba1eb-141"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba1eb-141"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

