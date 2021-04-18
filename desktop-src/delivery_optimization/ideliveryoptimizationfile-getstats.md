---
title: Ideliveryoptimizationfile GetStats-Methode (deliveryoptimization. h)
description: Gibt die Statistiken zum herunterladen und Hochladen für eine bestimmte Datei zurück.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats-Methode
- GetStats-Methode, ideliveryoptimizationfile-Schnittstelle
- Ideliveryoptimizationfile-Schnittstelle, GetStats-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392127"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a><span data-ttu-id="c6ca5-106">Ideliveryoptimizationfile:: GetStats-Methode</span><span class="sxs-lookup"><span data-stu-id="c6ca5-106">IDeliveryOptimizationFile::GetStats method</span></span>

<span data-ttu-id="c6ca5-107">Gibt die Statistiken zum herunterladen und Hochladen für eine bestimmte Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-107">Returns download and upload stats for a specific file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ca5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6ca5-108">Syntax</span></span>


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a><span data-ttu-id="c6ca5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6ca5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6ca5-110">*swarmstats* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c6ca5-110">*swarmStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6ca5-111">Gibt die Statistiken zum herunterladen und Hochladen für eine bestimmte Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-111">Returns download and upload stats for a specific file.</span></span> <span data-ttu-id="c6ca5-112">Weitere Informationen finden Sie in der Struktur " [**doswarmstats**](doswarmstats.md) ".</span><span class="sxs-lookup"><span data-stu-id="c6ca5-112">See the [**DOSwarmStats**](doswarmstats.md) structure for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6ca5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6ca5-113">Return value</span></span>

<span data-ttu-id="c6ca5-114">Diese Methode sollte **S_OK** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-114">This method should return **S_OK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6ca5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6ca5-115">Requirements</span></span>



| <span data-ttu-id="c6ca5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6ca5-116">Requirement</span></span> | <span data-ttu-id="c6ca5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c6ca5-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ca5-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6ca5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ca5-119">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6ca5-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c6ca5-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6ca5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ca5-121">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6ca5-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c6ca5-122">Header</span><span class="sxs-lookup"><span data-stu-id="c6ca5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6ca5-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6ca5-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6ca5-124">IDL</span><span class="sxs-lookup"><span data-stu-id="c6ca5-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6ca5-125"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6ca5-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c6ca5-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c6ca5-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6ca5-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6ca5-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c6ca5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c6ca5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6ca5-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6ca5-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c6ca5-130">IID</span><span class="sxs-lookup"><span data-stu-id="c6ca5-130">IID</span></span><br/>                      | <span data-ttu-id="c6ca5-131">IID_IDeliveryOptimizationFile ist als B76B9699-E99E-4101-803F-A20E325D93E2 definiert.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-131">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="c6ca5-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6ca5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ca5-133">**Ideliveryoptimizationfile**</span><span class="sxs-lookup"><span data-stu-id="c6ca5-133">**IDeliveryOptimizationFile**</span></span>](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





