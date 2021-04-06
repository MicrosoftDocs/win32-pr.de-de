---
title: Dodownloadpropertyex-Enumeration
description: Gibt die ID der erweiterten Eigenschaften für den Downloadvorgang an.
keywords:
- Dodownloadpropertyex-Enumeration, dodownloadpropertyex
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 5df0f53778d9059ef8767f5b8052940847e36c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858966"
---
# <a name="dodownloadpropertyex-enumeration"></a><span data-ttu-id="e36cc-104">Dodownloadpropertyex-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e36cc-104">DODownloadPropertyEx enumeration</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e36cc-105">Die **dodownloadpropertyex** -Enumeration ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="e36cc-105">The **DODownloadPropertyEx** enumeration is deprecated.</span></span> <span data-ttu-id="e36cc-106">Verwenden Sie stattdessen die [dodownloadproperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) -Enumeration mit [idodownload:: GetProperty](../do/nf-do-idodownload-getproperty.md) und [idodownload:: SetProperty](../do/nf-do-idodownload-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="e36cc-106">Instead, use the [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) enumeration with [IDODownload::GetProperty](../do/nf-do-idodownload-getproperty.md) and [IDODownload::SetProperty](../do/nf-do-idodownload-setproperty.md).</span></span>

<span data-ttu-id="e36cc-107">Die **dodownloadpropertyex** -Enumeration gibt die ID der erweiterten Eigenschaften für den Downloadvorgang an.</span><span class="sxs-lookup"><span data-stu-id="e36cc-107">The **DODownloadPropertyEx** enumeration specifies the ID of extended properties for the DO download operation.</span></span> <span data-ttu-id="e36cc-108">Diese Enumeration wird von der **idodownloadinternal** -Schnittstelle verwendet, und ein **Variant** -Wert wird verwendet, um den Eigenschafts Wert zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e36cc-108">This enumeration is used by the **IDODownloadInternal** interface, and a **VARIANT** value is used to get and set the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e36cc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e36cc-109">Syntax</span></span>

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a><span data-ttu-id="e36cc-110">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e36cc-110">Constants</span></span>

| <span data-ttu-id="e36cc-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e36cc-111">Requirement</span></span> | <span data-ttu-id="e36cc-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e36cc-112">Value</span></span> |
|-|-|
| <span data-ttu-id="e36cc-113">DODownloadPropertyEx_UpdateId</span><span class="sxs-lookup"><span data-stu-id="e36cc-113">DODownloadPropertyEx_UpdateId</span></span> | <span data-ttu-id="e36cc-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e36cc-114">Reserved.</span></span> <span data-ttu-id="e36cc-115">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e36cc-115">Do not use.</span></span> |
| <span data-ttu-id="e36cc-116">DODownloadPropertyEx_CorrelationVector</span><span class="sxs-lookup"><span data-stu-id="e36cc-116">DODownloadPropertyEx_CorrelationVector</span></span> | <span data-ttu-id="e36cc-117">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e36cc-117">Optional.</span></span> <span data-ttu-id="e36cc-118">Legt einen spezifischen Korrelations Vektor für Telemetriezwecke fest.</span><span class="sxs-lookup"><span data-stu-id="e36cc-118">Sets a specific correlation vector for telemetry purposes.</span></span> <span data-ttu-id="e36cc-119">Der Varianttyp ist VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="e36cc-119">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="e36cc-120">DODownloadPropertyEx_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="e36cc-120">DODownloadPropertyEx_DecryptionInfo</span></span> | <span data-ttu-id="e36cc-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e36cc-121">Reserved.</span></span> <span data-ttu-id="e36cc-122">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e36cc-122">Do not use.</span></span> |
| <span data-ttu-id="e36cc-123">DODownloadPropertyEx_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="e36cc-123">DODownloadPropertyEx_IntegrityCheckInfo</span></span> | <span data-ttu-id="e36cc-124">Optionaler Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e36cc-124">Optional write-only.</span></span> <span data-ttu-id="e36cc-125">Legt den Speicherort der Teil Hash Datei (PHF) fest, der von Do verwendet wird, um Lauf Zeit Integritätsprüfungen für den heruntergeladenen Inhalt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e36cc-125">Sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="e36cc-126">Der Varianttyp ist VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="e36cc-126">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="e36cc-127">DODownloadPropertyEx_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="e36cc-127">DODownloadPropertyEx_IntegrityCheckMandatory</span></span> | <span data-ttu-id="e36cc-128">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e36cc-128">Optional.</span></span> <span data-ttu-id="e36cc-129">Legt ein boolesches Flag fest, das angibt, ob die Verwendung der Teil Hash Datei (PHF) obligatorisch ist.</span><span class="sxs-lookup"><span data-stu-id="e36cc-129">Sets a boolean flag indicating whether usage of the piece hash file (PHF) is mandatory.</span></span> <span data-ttu-id="e36cc-130">Wenn VARIANT_TRUE, wird der Download abgebrochen, sobald die Integritätsprüfung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="e36cc-130">If VARIANT_TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="e36cc-131">Der Varianttyp ist VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="e36cc-131">VARIANT type is VT_BOOL.</span></span> |
| <span data-ttu-id="e36cc-132">DODownloadPropertyEx_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="e36cc-132">DODownloadPropertyEx_TotalSizeBytes</span></span> | <span data-ttu-id="e36cc-133">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e36cc-133">Reserved.</span></span> <span data-ttu-id="e36cc-134">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e36cc-134">Do not use.</span></span> |
| <span data-ttu-id="e36cc-135">DODownloadPropertyEx_TempLocalFileUsage</span><span class="sxs-lookup"><span data-stu-id="e36cc-135">DODownloadPropertyEx_TempLocalFileUsage</span></span> | <span data-ttu-id="e36cc-136">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e36cc-136">Reserved.</span></span> <span data-ttu-id="e36cc-137">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e36cc-137">Do not use.</span></span> |

## <a name="requirements"></a><span data-ttu-id="e36cc-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e36cc-138">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e36cc-139">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="e36cc-139">**Minimum supported client**</span></span> | <span data-ttu-id="e36cc-140">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="e36cc-140">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e36cc-141">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="e36cc-141">**Minimum supported server**</span></span> | <span data-ttu-id="e36cc-142">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="e36cc-142">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e36cc-143">**Header**</span><span class="sxs-lookup"><span data-stu-id="e36cc-143">**Header**</span></span> | <span data-ttu-id="e36cc-144">Dodownloadinternal. h</span><span class="sxs-lookup"><span data-stu-id="e36cc-144">DODownloadInternal.h</span></span> |
