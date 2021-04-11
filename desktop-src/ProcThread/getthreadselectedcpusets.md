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
# <a name="getthreadselectedcpusets-function"></a><span data-ttu-id="f2b2e-104">Getthreadselectedcpusets-Funktion</span><span class="sxs-lookup"><span data-stu-id="f2b2e-104">GetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="f2b2e-105">Gibt die explizite CPU-Satz Zuweisung des angegebenen Threads zurück, wenn eine Zuweisung mithilfe der [**setthreadselectedcpusets**](setthreadselectedcpusets.md) -API festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2b2e-105">Returns the explicit CPU Set assignment of the specified thread, if any assignment was set using the [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) API.</span></span> <span data-ttu-id="f2b2e-106">Wenn keine explizite Zuweisung festgelegt ist, wird "Requirements **didcount** " auf 0 festgelegt, und die Funktion gibt "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="f2b2e-106">If no explicit assignment is set, **RequiredIdCount** is set to 0 and the function returns TRUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2b2e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2b2e-107">Syntax</span></span>


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="f2b2e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2b2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2b2e-109">*Thread* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2b2e-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2b2e-110">Gibt den Thread an, für den die ausgewählten CPU-Sätze abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2b2e-110">Specifies the thread for which to query the selected CPU Sets.</span></span> <span data-ttu-id="f2b2e-111">Dieses Handle muss über den \_ \_ eingeschränkten \_ Informations Zugriff für die Thread Abfrage verfügen.</span><span class="sxs-lookup"><span data-stu-id="f2b2e-111">This handle must have the THREAD\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="f2b2e-112">Der von [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) zurückgegebene Wert kann auch hier angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f2b2e-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="f2b2e-113">*Cpuabtids* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="f2b2e-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2b2e-114">Gibt einen optionalen Puffer zum Abrufen der Liste der CPU-Satz Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="f2b2e-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="f2b2e-115">*Cpuantidcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2b2e-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2b2e-116">Gibt die Kapazität des Puffers an, der in **cpuabtids** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f2b2e-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="f2b2e-117">Wenn der Puffer NULL ist, muss dieser 0 sein.</span><span class="sxs-lookup"><span data-stu-id="f2b2e-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="f2b2e-118">Requirements- *count* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f2b2e-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2b2e-119">Gibt die erforderliche Kapazität des Puffers an, der die gesamte Liste der von einem Thread ausgewählten CPU-Sätze enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="f2b2e-119">Specifies the required capacity of the buffer to hold the entire list of thread selected CPU Sets.</span></span> <span data-ttu-id="f2b2e-120">Bei erfolgreicher Rückgabe wird dadurch die Anzahl der in den Puffer gefüllten IDs angegeben.</span><span class="sxs-lookup"><span data-stu-id="f2b2e-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2b2e-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2b2e-121">Return value</span></span>

<span data-ttu-id="f2b2e-122">Diese API gibt bei Erfolg TRUE zurück.</span><span class="sxs-lookup"><span data-stu-id="f2b2e-122">This API returns TRUE on success.</span></span> <span data-ttu-id="f2b2e-123">Wenn der Puffer nicht groß genug ist, ist der Wert von " **GetLastError** " Fehler \_ unzureichend \_ .</span><span class="sxs-lookup"><span data-stu-id="f2b2e-123">If the buffer is not large enough, the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="f2b2e-124">Diese API kann nicht ausgeführt werden, wenn gültige Parameter bestanden werden und der Rückgabe Puffer groß genug ist.</span><span class="sxs-lookup"><span data-stu-id="f2b2e-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b2e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2b2e-125">Requirements</span></span>



| <span data-ttu-id="f2b2e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2b2e-126">Requirement</span></span> | <span data-ttu-id="f2b2e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f2b2e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b2e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2b2e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f2b2e-129">Windows 10 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f2b2e-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="f2b2e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2b2e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f2b2e-131">Windows Server 2016 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f2b2e-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="f2b2e-132">Header</span><span class="sxs-lookup"><span data-stu-id="f2b2e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2b2e-133"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2b2e-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="f2b2e-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2b2e-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2b2e-135"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2b2e-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="f2b2e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f2b2e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2b2e-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2b2e-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

