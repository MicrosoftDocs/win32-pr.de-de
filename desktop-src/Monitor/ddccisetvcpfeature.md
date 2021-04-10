---
title: Ddccisetvcpfeature-Funktion
description: Legt den Wert eines VCP-Codes (Virtual Control Panel) für einen Monitor fest.
ms.assetid: 1069588b-5f8a-49da-b857-6f0a0c737a11
keywords:
- Monitor Konfiguration für ddccisetvcpfeature-Funktion
topic_type:
- apiref
api_name:
- DDCCISetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a72da2b2540c73e023a753a3fdb28507f8cbb40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103602"
---
# <a name="ddccisetvcpfeature-function"></a><span data-ttu-id="3b404-104">Ddccisetvcpfeature-Funktion</span><span class="sxs-lookup"><span data-stu-id="3b404-104">DDCCISetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b404-105">Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="3b404-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="3b404-106">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3b404-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="3b404-107">Legt den Wert eines VCP-Codes (Virtual Control Panel) für einen Monitor fest.</span><span class="sxs-lookup"><span data-stu-id="3b404-107">Sets the value of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b404-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b404-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCISetVCPFeature(
  _In_ HANDLE hMonitor,
  _In_ DWORD  dwVCPCode,
  _In_ DWORD  dwNewValue
);
```



## <a name="parameters"></a><span data-ttu-id="3b404-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b404-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b404-110">*Hmonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b404-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b404-111">Ein Handle für einen physischen Monitor.</span><span class="sxs-lookup"><span data-stu-id="3b404-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="3b404-112">*dwvcpcode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b404-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b404-113">Der festzulegende VCP-Code.</span><span class="sxs-lookup"><span data-stu-id="3b404-113">The VCP code to set.</span></span>

</dd> <dt>

<span data-ttu-id="3b404-114">*dwnewvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b404-114">*dwNewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b404-115">Der Wert des VCP-Codes.</span><span class="sxs-lookup"><span data-stu-id="3b404-115">The value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b404-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b404-116">Return value</span></span>

<span data-ttu-id="3b404-117">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3b404-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="3b404-118">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3b404-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b404-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b404-119">Remarks</span></span>

<span data-ttu-id="3b404-120">Anwendungen sollten [**setvcpfeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) aufrufen, anstatt diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3b404-120">Applications should call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) instead of calling this function.</span></span>

<span data-ttu-id="3b404-121">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="3b404-121">This function has no associated import library.</span></span> <span data-ttu-id="3b404-122">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="3b404-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b404-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b404-123">Requirements</span></span>



| <span data-ttu-id="3b404-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b404-124">Requirement</span></span> | <span data-ttu-id="3b404-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3b404-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3b404-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b404-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3b404-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b404-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3b404-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b404-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3b404-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b404-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3b404-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3b404-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b404-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b404-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b404-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b404-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b404-133">Überwachen von Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="3b404-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

