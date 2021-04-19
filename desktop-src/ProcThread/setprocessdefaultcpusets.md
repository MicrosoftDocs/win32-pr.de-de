---
description: Legt die standardcpu-Gruppenzuweisung für Threads im angegebenen Prozess fest. Threads, die erstellt werden und für die keine CPU-Sätze explizit mithilfe von setthreadselectedcpusets festgelegt werden, erben die von setprocessdefaultcpusets angegebenen Mengen automatisch.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: Setprocessdefaultcpusets-Funktion (processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 7998b20815529b41c5e29204c0ef50fbc15e6288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353454"
---
# <a name="setprocessdefaultcpusets-function"></a><span data-ttu-id="b7b49-104">Setprocessdefaultcpusets-Funktion</span><span class="sxs-lookup"><span data-stu-id="b7b49-104">SetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="b7b49-105">Legt die standardcpu-Gruppenzuweisung für Threads im angegebenen Prozess fest.</span><span class="sxs-lookup"><span data-stu-id="b7b49-105">Sets the default CPU Sets assignment for threads in the specified process.</span></span> <span data-ttu-id="b7b49-106">Threads, die erstellt werden und für die keine CPU-Sätze explizit mithilfe von [**setthreadselectedcpusets**](setthreadselectedcpusets.md)festgelegt werden, erben die von **setprocessdefaultcpusets** angegebenen Mengen automatisch.</span><span class="sxs-lookup"><span data-stu-id="b7b49-106">Threads that are created, which don’t have CPU Sets explicitly set using [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), will inherit the sets specified by **SetProcessDefaultCpuSets** automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b49-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7b49-107">Syntax</span></span>


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a><span data-ttu-id="b7b49-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7b49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7b49-109">*Prozess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7b49-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7b49-110">Gibt den Prozess an, für den die Standard-CPU-Sätze festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b7b49-110">Specifies the process for which to set the default CPU Sets.</span></span> <span data-ttu-id="b7b49-111">Dieses Handle muss über das \_ Recht zum Festlegen des \_ eingeschränkten \_ Informations Zugriffs verfügen.</span><span class="sxs-lookup"><span data-stu-id="b7b49-111">This handle must have the PROCESS\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="b7b49-112">Der von [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) zurückgegebene Wert kann auch hier angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b7b49-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="b7b49-113">*Cpuabtids* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b7b49-113">*CpuSetIds* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7b49-114">Gibt die Liste der CPU-Satz-IDs an, die als Standard-CPU-Prozess festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b7b49-114">Specifies the list of CPU Set IDs to set as the process default CPU set.</span></span> <span data-ttu-id="b7b49-115">Wenn dieser Wert NULL ist, löscht **setprocessdefaultcpusets** jede Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="b7b49-115">If this is NULL, the **SetProcessDefaultCpuSets** clears out any assignment.</span></span>

</dd> <dt>

<span data-ttu-id="b7b49-116">*Cpuabtidcoder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7b49-116">*CpuSetIdCound* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7b49-117">Gibt die Anzahl der IDs in der Liste an, die im **cpucpuds** -Argument übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b7b49-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="b7b49-118">Wenn dieser Wert NULL ist, sollte dieser 0 sein.</span><span class="sxs-lookup"><span data-stu-id="b7b49-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7b49-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7b49-119">Return value</span></span>

<span data-ttu-id="b7b49-120">Diese Funktion kann nicht fehlschlagen, wenn gültige Parameter bestanden wurden.</span><span class="sxs-lookup"><span data-stu-id="b7b49-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7b49-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7b49-121">Requirements</span></span>



| <span data-ttu-id="b7b49-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7b49-122">Requirement</span></span> | <span data-ttu-id="b7b49-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b7b49-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b49-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7b49-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b7b49-125">Windows 10 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b7b49-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="b7b49-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7b49-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b7b49-127">Windows Server 2016 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b7b49-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="b7b49-128">Header</span><span class="sxs-lookup"><span data-stu-id="b7b49-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7b49-129"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7b49-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="b7b49-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b7b49-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7b49-131"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7b49-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="b7b49-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b7b49-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7b49-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7b49-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 
