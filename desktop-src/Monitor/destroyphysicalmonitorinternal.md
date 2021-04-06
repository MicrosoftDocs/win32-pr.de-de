---
title: Destroyphysicalmonitorinternal-Funktion
description: Schließt ein Handle für einen physischen Monitor.
ms.assetid: 86705f1b-6445-444c-8e04-66a435927af3
keywords:
- Konfiguration des destroyphysicalmonitorinternal-Funktions Monitors
topic_type:
- apiref
api_name:
- DestroyPhysicalMonitorInternal
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ea52645e97bc5bec49fba053f9dbab5306bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858871"
---
# <a name="destroyphysicalmonitorinternal-function"></a><span data-ttu-id="c3a44-104">Destroyphysicalmonitorinternal-Funktion</span><span class="sxs-lookup"><span data-stu-id="c3a44-104">DestroyPhysicalMonitorInternal function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3a44-105">Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c3a44-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="c3a44-106">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c3a44-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="c3a44-107">Schließt ein Handle für einen physischen Monitor.</span><span class="sxs-lookup"><span data-stu-id="c3a44-107">Closes a handle to a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a44-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3a44-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyPhysicalMonitorInternal(
  _In_ HANDLE hMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="c3a44-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3a44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3a44-110">*Hmonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3a44-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a44-111">Ein Handle für einen physischen Monitor.</span><span class="sxs-lookup"><span data-stu-id="c3a44-111">A handle to a physical monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3a44-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3a44-112">Return value</span></span>

<span data-ttu-id="c3a44-113">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c3a44-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="c3a44-114">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c3a44-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3a44-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3a44-115">Remarks</span></span>

<span data-ttu-id="c3a44-116">Anwendungen sollten [**destroyphysicalmonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) aufrufen, anstatt diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c3a44-116">Applications should call [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) instead of calling this function.</span></span>

<span data-ttu-id="c3a44-117">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="c3a44-117">This function has no associated import library.</span></span> <span data-ttu-id="c3a44-118">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="c3a44-118">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a44-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3a44-119">Requirements</span></span>



| <span data-ttu-id="c3a44-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3a44-120">Requirement</span></span> | <span data-ttu-id="c3a44-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c3a44-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a44-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3a44-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a44-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3a44-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c3a44-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3a44-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a44-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3a44-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c3a44-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c3a44-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3a44-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3a44-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3a44-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3a44-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a44-129">Überwachen von Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="c3a44-129">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

