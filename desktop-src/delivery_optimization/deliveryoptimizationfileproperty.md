---
title: Deliveryoptimizationfileproperty-Enumeration (deliveryoptimization. h)
description: Die deliveryoptimizationfileproperty-Enumeration gibt die ID einer optionalen Eigenschaft für die do-Datei an.
keywords:
- Deliveryoptimizationfileproperty-Enumeration
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340998"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a><span data-ttu-id="0ea47-104">Deliveryoptimizationfileproperty-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0ea47-104">DeliveryOptimizationFileProperty enumeration</span></span>

<span data-ttu-id="0ea47-105">Die deliveryoptimizationfileproperty-Enumeration gibt die ID einer optionalen Eigenschaft für die do-Datei an.</span><span class="sxs-lookup"><span data-stu-id="0ea47-105">The DeliveryOptimizationFileProperty enumeration specifies the ID of an optional property for the DO file.</span></span> <span data-ttu-id="0ea47-106">Diese Enumeration wird in der IDeliveryOptimizationFile2-Schnittstelle verwendet, bei der der Eigenschafts Wert des Typs Variant überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="0ea47-106">This enumeration is used in the IDeliveryOptimizationFile2 interface where the property value of type VARIANT is passed</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea47-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ea47-107">Syntax</span></span>

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a><span data-ttu-id="0ea47-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="0ea47-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0ea47-109">DOFilePropertyId_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="0ea47-109">DOFilePropertyId_DecryptionInfo</span></span>
</dt> <dd>

<span data-ttu-id="0ea47-110">Mit der DOFilePropertyId_DecryptionInfo-Eigenschaften-ID werden Entschlüsselungs Informationen in Form einer JSON-Zeichenfolge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0ea47-110">The DOFilePropertyId_DecryptionInfo property ID sets decryption information in the form of a JSON string.</span></span> <span data-ttu-id="0ea47-111">DOFilePropertyId_DecryptionInfo ist eine schreibgeschützte Eigenschaft vom Typ VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="0ea47-111">DOFilePropertyId_DecryptionInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="0ea47-112">DOFilePropertyId_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="0ea47-112">DOFilePropertyId_IntegrityCheckInfo</span></span>
</dt> <dd>

<span data-ttu-id="0ea47-113">Die DOFilePropertyId_IntegrityCheckInfo-Eigenschaften-ID legt den Speicherort der Stück Hash Datei (PHF) fest, der von Do verwendet wird, um Lauf Zeit Integritätsprüfungen für den heruntergeladenen Inhalt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0ea47-113">The DOFilePropertyId_IntegrityCheckInfo property ID sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="0ea47-114">DOFilePropertyId_IntegrityCheckInfo ist eine schreibgeschützte Eigenschaft vom Typ VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="0ea47-114">DOFilePropertyId_IntegrityCheckInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="0ea47-115">DOFilePropertyId_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="0ea47-115">DOFilePropertyId_IntegrityCheckMandatory</span></span>
</dt> <dd>

<span data-ttu-id="0ea47-116">Mit der DOFilePropertyId_IntegrityCheckMandatory-Eigenschaften-ID wird ein boolesches Flag festgelegt, das angibt, ob die Verwendung der PHF obligatorisch ist.</span><span class="sxs-lookup"><span data-stu-id="0ea47-116">The DOFilePropertyId_IntegrityCheckMandatory property ID sets a boolean flag indicating whether usage of the PHF is mandatory.</span></span> <span data-ttu-id="0ea47-117">Wenn der Wert true ist, wird der Download abgebrochen, sobald die Integritätsprüfung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="0ea47-117">If TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="0ea47-118">DOFilePropertyId_IntegrityCheckMandatory ist eine Lese-/Schreibeigenschaft vom Typ VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="0ea47-118">DOFilePropertyId_IntegrityCheckMandatory is a Read/Write property of type VT_BOOL.</span></span>

</dd> <dt>

<span data-ttu-id="0ea47-119">DOFilePropertyId_DownloadSinkFilePath</span><span class="sxs-lookup"><span data-stu-id="0ea47-119">DOFilePropertyId_DownloadSinkFilePath</span></span>
</dt> <dd>

<span data-ttu-id="0ea47-120">Mit der DOFilePropertyId_DownloadSinkFilePath-Eigenschaften-ID wird ein voll qualifizierter Dateisystem Speicherort festgelegt, in dem die heruntergeladenen Elemente gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0ea47-120">The DOFilePropertyId_DownloadSinkFilePath property ID sets a fully qualified file system location where DO should store the downloaded pieces.</span></span> <span data-ttu-id="0ea47-121">DOFilePropertyId_DownloadSinkFilePath ist vom Typ VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="0ea47-121">DOFilePropertyId_DownloadSinkFilePath is of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="0ea47-122">DOFilePropertyId_DownloadSinkMemoryStream</span><span class="sxs-lookup"><span data-stu-id="0ea47-122">DOFilePropertyId_DownloadSinkMemoryStream</span></span>
</dt> <dd>

<span data-ttu-id="0ea47-123">Die DOFilePropertyId_DownloadSinkMemoryStream-Eigenschaften-ID ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="0ea47-123">The DOFilePropertyId_DownloadSinkMemoryStream property ID is deprecated.</span></span> <span data-ttu-id="0ea47-124">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ea47-124">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="0ea47-125">DOFilePropertyId_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="0ea47-125">DOFilePropertyId_TotalSizeBytes</span></span>
</dt> <dd>

<span data-ttu-id="0ea47-126">Die DOFilePropertyId_TotalSizeBytes-Eigenschaften-ID gibt die Gesamtgröße des Downloads an.</span><span class="sxs-lookup"><span data-stu-id="0ea47-126">The DOFilePropertyId_TotalSizeBytes property ID specifies the total download size.</span></span> <span data-ttu-id="0ea47-127">DOFilePropertyId_TotalSizeBytes ist vom Typ VT_UI8.</span><span class="sxs-lookup"><span data-stu-id="0ea47-127">DOFilePropertyId_TotalSizeBytes is of type VT_UI8.</span></span>
</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ea47-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ea47-128">Requirements</span></span>

| <span data-ttu-id="0ea47-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ea47-129">Requirement</span></span> | <span data-ttu-id="0ea47-130">Wert</span><span class="sxs-lookup"><span data-stu-id="0ea47-130">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ea47-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ea47-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0ea47-132">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ea47-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="0ea47-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ea47-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0ea47-134">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ea47-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="0ea47-135">Header</span><span class="sxs-lookup"><span data-stu-id="0ea47-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ea47-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ea47-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
