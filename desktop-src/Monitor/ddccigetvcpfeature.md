---
title: Ddccigetvcpfeature-Funktion
description: Ruft den aktuellen Wert, den maximalen Wert und den Codetyp eines virtuellen System Steuerungs Codes (VCP) für einen Monitor ab.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- Monitor Konfiguration für ddccigetvcpfeature-Funktion
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5758bbd1c86b9f228b64063fdd05c04cb05bedcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956440"
---
# <a name="ddccigetvcpfeature-function"></a><span data-ttu-id="01630-104">Ddccigetvcpfeature-Funktion</span><span class="sxs-lookup"><span data-stu-id="01630-104">DDCCIGetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01630-105">Diese Funktion wird von der Monitor Konfigurations-API verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="01630-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="01630-106">Anwendungen sollten diese Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="01630-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="01630-107">Ruft den aktuellen Wert, den maximalen Wert und den Codetyp eines virtuellen System Steuerungs Codes (VCP) für einen Monitor ab.</span><span class="sxs-lookup"><span data-stu-id="01630-107">Gets the current value, maximum value, and code type of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="01630-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="01630-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
);
```



## <a name="parameters"></a><span data-ttu-id="01630-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="01630-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01630-110">*Hmonitor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01630-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01630-111">Ein Handle für einen physischen Monitor.</span><span class="sxs-lookup"><span data-stu-id="01630-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="01630-112">*dwvcpcode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01630-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01630-113">Der VCP-Code, der abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="01630-113">The VCP code to query.</span></span>

</dd> <dt>

<span data-ttu-id="01630-114">*PVCT* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="01630-114">*pvct* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01630-115">Empfängt den VCP-Codetyp als Member der [**MC \_ VCP- \_ \_ Codetyp**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="01630-115">Receives the VCP code type, as a member of the [**MC\_VCP\_CODE\_TYPE**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="01630-116">*pdwcurrentvalue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="01630-116">*pdwCurrentValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01630-117">Empfängt den aktuellen Wert des VCP-Codes.</span><span class="sxs-lookup"><span data-stu-id="01630-117">Receives the current value of the VCP code.</span></span>

</dd> <dt>

<span data-ttu-id="01630-118">*pdwmaximumvalue* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="01630-118">*pdwMaximumValue* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01630-119">Empfängt den maximalen Wert des VCP-Codes.</span><span class="sxs-lookup"><span data-stu-id="01630-119">Receives the maximum value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01630-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01630-120">Return value</span></span>

<span data-ttu-id="01630-121">Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="01630-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="01630-122">Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="01630-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="01630-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01630-123">Remarks</span></span>

<span data-ttu-id="01630-124">Anwendungen sollten [**getvcpfeatureandvcpfeaturereply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) aufrufen, anstatt diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="01630-124">Applications should call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) instead of calling this function.</span></span>

<span data-ttu-id="01630-125">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="01630-125">This function has no associated import library.</span></span> <span data-ttu-id="01630-126">Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="01630-126">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="01630-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01630-127">Requirements</span></span>



| <span data-ttu-id="01630-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01630-128">Requirement</span></span> | <span data-ttu-id="01630-129">Wert</span><span class="sxs-lookup"><span data-stu-id="01630-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="01630-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01630-130">Minimum supported client</span></span><br/> | <span data-ttu-id="01630-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01630-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="01630-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01630-132">Minimum supported server</span></span><br/> | <span data-ttu-id="01630-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01630-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="01630-134">DLL</span><span class="sxs-lookup"><span data-stu-id="01630-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01630-135"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01630-135"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01630-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01630-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01630-137">Überwachen von Konfigurationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="01630-137">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

