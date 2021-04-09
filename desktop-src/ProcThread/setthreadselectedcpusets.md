---
description: Legt die ausgewählte CPU-Gruppenzuweisung für den angegebenen Thread fest. Diese Zuweisung überschreibt die standardmäßige Prozess Zuweisung, wenn eine festgelegt ist.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: Setthreadselectedcpusets-Funktion (processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: b8b1f7c382d034e804d4ac7e63d58b8ec5853620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865059"
---
# <a name="setthreadselectedcpusets-function"></a><span data-ttu-id="62e49-104">Setthreadselectedcpusets-Funktion</span><span class="sxs-lookup"><span data-stu-id="62e49-104">SetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="62e49-105">Legt die ausgewählte CPU-Gruppenzuweisung für den angegebenen Thread fest.</span><span class="sxs-lookup"><span data-stu-id="62e49-105">Sets the selected CPU Sets assignment for the specified thread.</span></span> <span data-ttu-id="62e49-106">Diese Zuweisung überschreibt die standardmäßige Prozess Zuweisung, wenn eine festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="62e49-106">This assignment overrides the process default assignment, if one is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="62e49-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="62e49-107">Syntax</span></span>


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="62e49-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="62e49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62e49-109">*Thread* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62e49-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62e49-110">Gibt den Thread an, in dem die CPU-Satz Zuweisung festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="62e49-110">Specifies the thread on which to set the CPU Set assignment.</span></span> <span data-ttu-id="62e49-111">Dieses Handle muss über den Thread \_ fest \_ gelegtes \_ Zugriffsrecht für den Zugriff verfügen.</span><span class="sxs-lookup"><span data-stu-id="62e49-111">This handle must have the THREAD\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="62e49-112">Der von [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) zurückgegebene Wert kann ebenfalls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62e49-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be used.</span></span>

</dd> <dt>

<span data-ttu-id="62e49-113">*Cpuabtids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62e49-113">*CpuSetIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62e49-114">Gibt die Liste der CPU-Satz-IDs an, die als vom Thread ausgewählte CPU festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="62e49-114">Specifies the list of CPU Set IDs to set as the thread selected CPU set.</span></span> <span data-ttu-id="62e49-115">Wenn dieser Wert NULL ist, löscht die API jede Zuweisung und setzt die Verarbeitung der Standard Zuweisung wieder her, wenn eine solche festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="62e49-115">If this is NULL, the API clears out any assignment, reverting to process default assignment if one is set.</span></span>

</dd> <dt>

<span data-ttu-id="62e49-116">*Cpuantidcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62e49-116">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62e49-117">Gibt die Anzahl der IDs in der Liste an, die im **cpucpuds** -Argument übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="62e49-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="62e49-118">Wenn dieser Wert NULL ist, sollte dieser 0 sein.</span><span class="sxs-lookup"><span data-stu-id="62e49-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62e49-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62e49-119">Return value</span></span>

<span data-ttu-id="62e49-120">Diese Funktion kann nicht fehlschlagen, wenn gültige Parameter bestanden wurden.</span><span class="sxs-lookup"><span data-stu-id="62e49-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="62e49-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62e49-121">Requirements</span></span>



| <span data-ttu-id="62e49-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62e49-122">Requirement</span></span> | <span data-ttu-id="62e49-123">Wert</span><span class="sxs-lookup"><span data-stu-id="62e49-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="62e49-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62e49-124">Minimum supported client</span></span><br/> | <span data-ttu-id="62e49-125">Windows 10 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="62e49-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="62e49-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62e49-126">Minimum supported server</span></span><br/> | <span data-ttu-id="62e49-127">Windows Server 2016 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="62e49-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="62e49-128">Header</span><span class="sxs-lookup"><span data-stu-id="62e49-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="62e49-129"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="62e49-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="62e49-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="62e49-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="62e49-131"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="62e49-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="62e49-132">DLL</span><span class="sxs-lookup"><span data-stu-id="62e49-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62e49-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62e49-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 
