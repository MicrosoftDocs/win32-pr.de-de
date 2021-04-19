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
# <a name="getprocessdefaultcpusets-function"></a><span data-ttu-id="9628d-104">Getprocessdefaultcpusets-Funktion</span><span class="sxs-lookup"><span data-stu-id="9628d-104">GetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="9628d-105">Ruft die Liste der CPU-Sätze im standardmäßigen Prozess Satz ab, der von [**setprocessdefaultcpusets**](setprocessdefaultcpusets.md)festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="9628d-105">Retrieves the list of CPU Sets in the process default set that was set by [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md).</span></span> <span data-ttu-id="9628d-106">Wenn für einen bestimmten Prozess keine Standard-CPU-Sätze festgelegt sind, wird der Wert für "Requirements" auf 0 festgelegt, **und die Funktion ist erfolgreich** .</span><span class="sxs-lookup"><span data-stu-id="9628d-106">If no default CPU Sets are set for a given process, then the **RequiredIdCount** is set to 0 and the function succeeds.</span></span>

## <a name="syntax"></a><span data-ttu-id="9628d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9628d-107">Syntax</span></span>


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="9628d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9628d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9628d-109">*Prozess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9628d-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9628d-110">Gibt ein Prozess Handle für den abzufragende Prozess an.</span><span class="sxs-lookup"><span data-stu-id="9628d-110">Specifies a process handle for the process to query.</span></span> <span data-ttu-id="9628d-111">Dieses Handle muss über das Recht "Prozess \_ Abfrage \_ beschränkte Informationen" verfügen \_ .</span><span class="sxs-lookup"><span data-stu-id="9628d-111">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="9628d-112">Der von [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) zurückgegebene Wert kann auch hier angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9628d-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="9628d-113">*Cpuabtids* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="9628d-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9628d-114">Gibt einen optionalen Puffer zum Abrufen der Liste der CPU-Satz Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="9628d-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="9628d-115">*Cpuantidcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9628d-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9628d-116">Gibt die Kapazität des Puffers an, der in **cpuabtids** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9628d-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="9628d-117">Wenn der Puffer NULL ist, muss dieser 0 sein.</span><span class="sxs-lookup"><span data-stu-id="9628d-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="9628d-118">Requirements- *count* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9628d-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9628d-119">Gibt die erforderliche Kapazität des Puffers an, der die gesamte Liste der standardmäßigen Prozess-CPU-Sätze enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="9628d-119">Specifies the required capacity of the buffer to hold the entire list of process default CPU Sets.</span></span> <span data-ttu-id="9628d-120">Bei erfolgreicher Rückgabe wird dadurch die Anzahl der in den Puffer gefüllten IDs angegeben.</span><span class="sxs-lookup"><span data-stu-id="9628d-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9628d-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9628d-121">Return value</span></span>

<span data-ttu-id="9628d-122">Diese API gibt bei Erfolg TRUE zurück.</span><span class="sxs-lookup"><span data-stu-id="9628d-122">This API returns TRUE on success.</span></span> <span data-ttu-id="9628d-123">Wenn der Puffer nicht groß genug ist, gibt die API false zurück, und der **GetLastError** -Wert ist Fehler \_ unzureichender \_ Puffer.</span><span class="sxs-lookup"><span data-stu-id="9628d-123">If the buffer is not large enough the API returns FALSE, and the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="9628d-124">Diese API kann nicht ausgeführt werden, wenn gültige Parameter bestanden werden und der Rückgabe Puffer groß genug ist.</span><span class="sxs-lookup"><span data-stu-id="9628d-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="9628d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9628d-125">Requirements</span></span>



| <span data-ttu-id="9628d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9628d-126">Requirement</span></span> | <span data-ttu-id="9628d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9628d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9628d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9628d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9628d-129">Windows 10 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9628d-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="9628d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9628d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9628d-131">Windows Server 2016 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9628d-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="9628d-132">Header</span><span class="sxs-lookup"><span data-stu-id="9628d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9628d-133"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9628d-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="9628d-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9628d-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="9628d-135"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="9628d-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="9628d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9628d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9628d-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9628d-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

