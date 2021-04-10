---
title: Ddccigettimingreport-Funktion
description: Ruft die horizontale und vertikale Synchronisierungs Häufigkeit eines Monitors ab.
ms.assetid: d490cb89-082a-42a1-ac0a-335c929cd5d7
keywords:
- Konfiguration der ddccigettimingreport-Funktion
topic_type:
- apiref
api_name:
- DDCCIGetTimingReport
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b87cb4269c2cdff2303bbe763905cb572acfbb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956441"
---
# <a name="ddccigettimingreport-function"></a><span data-ttu-id="034f9-104">Ddccigettimingreport-Funktion</span><span class="sxs-lookup"><span data-stu-id="034f9-104">DDCCIGetTimingReport function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="034f9-105">Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="034f9-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="034f9-106">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="034f9-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="034f9-107">Ruft die horizontale und vertikale Synchronisierungs Häufigkeit eines Monitors ab.</span><span class="sxs-lookup"><span data-stu-id="034f9-107">Gets the horizontal and vertical synchronization frequencies of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="034f9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="034f9-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetTimingReport(
  _In_  HANDLE             hMonitor,
  _Out_ LPMC_TIMING_REPORT pmtr
);
```



## <a name="parameters"></a><span data-ttu-id="034f9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="034f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="034f9-110">*Hmonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="034f9-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="034f9-111">Ein Handle für einen physischen Monitor.</span><span class="sxs-lookup"><span data-stu-id="034f9-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="034f9-112">*pmtr* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="034f9-112">*pmtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="034f9-113">Ein Zeiger auf eine [**MC- \_ Zeit Steuerungs \_ Berichts**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) Struktur, die die Zeit Steuerungsinformationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="034f9-113">A pointer to an [**MC\_TIMING\_REPORT**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) structure that receives the timing information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="034f9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="034f9-114">Return value</span></span>

<span data-ttu-id="034f9-115">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="034f9-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="034f9-116">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="034f9-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="034f9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="034f9-117">Remarks</span></span>

<span data-ttu-id="034f9-118">Anwendungen sollten [**gettimingreport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) aufrufen, anstatt diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="034f9-118">Applications should call [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) instead of calling this function.</span></span>

<span data-ttu-id="034f9-119">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="034f9-119">This function has no associated import library.</span></span> <span data-ttu-id="034f9-120">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="034f9-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="034f9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="034f9-121">Requirements</span></span>



| <span data-ttu-id="034f9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="034f9-122">Requirement</span></span> | <span data-ttu-id="034f9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="034f9-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="034f9-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="034f9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="034f9-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="034f9-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="034f9-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="034f9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="034f9-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="034f9-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="034f9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="034f9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="034f9-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="034f9-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="034f9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="034f9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="034f9-131">Überwachen von Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="034f9-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

