---
title: IDeliveryOptimizationJob2 AddFile-Methode
description: Die AddFile-Methode fügt einem vorhandenen do-Auftrag eine einzelne Datei hinzu.
keywords:
- AddFile-Methode
- AddFile-Methode, IDeliveryOptimizationJob2-Schnittstelle
- IDeliveryOptimizationJob2-Schnittstelle, AddFile-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8225db8cccb1e1d3bb364ba1dc29f30526fe36b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103246"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a><span data-ttu-id="4d8ff-106">IDeliveryOptimizationJob2:: ADDFILEWITHRANGES-Methode</span><span class="sxs-lookup"><span data-stu-id="4d8ff-106">IDeliveryOptimizationJob2::AddFileWithRanges method</span></span>

<span data-ttu-id="4d8ff-107">Die AddFile-Methode fügt einem vorhandenen do-Auftrag eine einzelne Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d8ff-107">The AddFile method adds a single file to an existing DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d8ff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d8ff-108">Syntax</span></span>

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a><span data-ttu-id="4d8ff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d8ff-110">nicht im  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d8ff-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8ff-111">Die Datei-ID-Zeichenfolge, die die herunter zuladende Datei eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4d8ff-111">The file ID string, which uniquely identifies the file to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="4d8ff-112">*RemoteURL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d8ff-112">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8ff-113">Die Datei-URL, die versucht, eine Verbindung herzustellen, um die Datei herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="4d8ff-113">The file URL that DO will attempt to connect to download the file.</span></span>

</dd> <dt>

<span data-ttu-id="4d8ff-114">*rangecount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d8ff-114">*rangeCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8ff-115">Die Anzahl der in *Bereichen* enthaltenen Elemente.</span><span class="sxs-lookup"><span data-stu-id="4d8ff-115">The number of items contained in *ranges*.</span></span> <span data-ttu-id="4d8ff-116">Ein Wert von 0 (null) bedeutet, dass für die Datei keine Bereiche verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d8ff-116">A zero value means that no ranges are used for the file.</span></span>

</dd> <dt>

<span data-ttu-id="4d8ff-117">*Bereiche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d8ff-117">*ranges* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8ff-118">Die optionale Bereichs Liste.</span><span class="sxs-lookup"><span data-stu-id="4d8ff-118">The optional range list.</span></span> <span data-ttu-id="4d8ff-119">Jeder Bereich in der Liste ist eine [**BG_FILE_RANGE**](bg-file-range.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="4d8ff-119">Each range in the list is a [**BG_FILE_RANGE**](bg-file-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4d8ff-120">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d8ff-120">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8ff-121">Der Typ des Objekts, das im-Objekt enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4d8ff-121">The type of object contained in object.</span></span> <span data-ttu-id="4d8ff-122">Dies muss vom Typ "IID_IDeliveryOptimizationFile" sein.</span><span class="sxs-lookup"><span data-stu-id="4d8ff-122">This must by of type IID_IDeliveryOptimizationFile.</span></span>

</dd> <dt>

<span data-ttu-id="4d8ff-123">*Objekt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4d8ff-123">*object* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8ff-124">Das ideliveryoptimizationfile-Objekt, das die Downloaddatei darstellt.</span><span class="sxs-lookup"><span data-stu-id="4d8ff-124">The IDeliveryOptimizationFile object, which represents the download file.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d8ff-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d8ff-125">Return value</span></span>

<span data-ttu-id="4d8ff-126">Diese Methode gibt S_OK bei Erfolg oder einen der standardmäßigen HRESULT-Werte bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4d8ff-126">This method returns S_OK on success or one of the standard HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d8ff-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d8ff-127">Requirements</span></span>

| <span data-ttu-id="4d8ff-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d8ff-128">Requirement</span></span> | <span data-ttu-id="4d8ff-129">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8ff-129">Value</span></span> |
|---------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4d8ff-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d8ff-130">Minimum supported client</span></span>  | <span data-ttu-id="4d8ff-131">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d8ff-131">Windows 10, version 1803 \[desktop apps only\]</span></span>                                  |
| <span data-ttu-id="4d8ff-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d8ff-132">Minimum supported server</span></span>  | <span data-ttu-id="4d8ff-133">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d8ff-133">Windows Server, version 1709 \[desktop apps only\]</span></span>                              |
| <span data-ttu-id="4d8ff-134">Header</span><span class="sxs-lookup"><span data-stu-id="4d8ff-134">Header</span></span>                    | <span data-ttu-id="4d8ff-135">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="4d8ff-135">Deliveryoptimization.h</span></span>                                                          |
| <span data-ttu-id="4d8ff-136">IDL</span><span class="sxs-lookup"><span data-stu-id="4d8ff-136">IDL</span></span>                       | <span data-ttu-id="4d8ff-137">Deliveryoptimization. idl</span><span class="sxs-lookup"><span data-stu-id="4d8ff-137">DeliveryOptimization.idl</span></span>                                                        |
| <span data-ttu-id="4d8ff-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4d8ff-138">Library</span></span>                   | <span data-ttu-id="4d8ff-139">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="4d8ff-139">Dosvc.lib</span></span>                                                                       |
| <span data-ttu-id="4d8ff-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4d8ff-140">DLL</span></span>                       | <span data-ttu-id="4d8ff-141">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="4d8ff-141">Dosvc.dll</span></span>                                                                       |
| <span data-ttu-id="4d8ff-142">IID</span><span class="sxs-lookup"><span data-stu-id="4d8ff-142">IID</span></span>                       | <span data-ttu-id="4d8ff-143">IID_IDeliveryOptimizationJob ist als EE2584CF-A69C-4848-B633-2649962b3ef7 definiert.</span><span class="sxs-lookup"><span data-stu-id="4d8ff-143">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span> |

## <a name="see-also"></a><span data-ttu-id="4d8ff-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d8ff-144">See also</span></span>

[<span data-ttu-id="4d8ff-145">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="4d8ff-145">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
