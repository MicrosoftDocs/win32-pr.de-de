---
title: IWMDRMDevice2 getpartialsynclist-Methode
description: Die getpartialsynclist-Methode ruft eine partielle Synchronisierungs Liste ab.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Getpartialsynclist-Methode, Windows Media Device Manager
- Getpartialsynclist-Methode Windows Media Device Manager, IWMDRMDevice2-Schnittstelle
- IWMDRMDevice2 Interface Windows Media Device Manager, getpartialsynclist-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367776"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a><span data-ttu-id="cf678-106">IWMDRMDevice2:: getpartialsynclist-Methode</span><span class="sxs-lookup"><span data-stu-id="cf678-106">IWMDRMDevice2::GetPartialSyncList method</span></span>

<span data-ttu-id="cf678-107">Die **getpartialsynclist** -Methode ruft eine partielle Synchronisierungs Liste ab.</span><span class="sxs-lookup"><span data-stu-id="cf678-107">The **GetPartialSyncList** method gets a partial synchronization list.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf678-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf678-108">Syntax</span></span>


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="cf678-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf678-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf678-110">*cminzählthreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf678-110">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf678-111">Schwellenwert für minimale Anzahl.</span><span class="sxs-lookup"><span data-stu-id="cf678-111">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="cf678-112">*cminhoursthreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf678-112">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf678-113">Schwellenwert für minimale Stunden.</span><span class="sxs-lookup"><span data-stu-id="cf678-113">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="cf678-114">*dwstartingindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf678-114">*dwStartingIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf678-115">Die Start Position für die Indizierung.</span><span class="sxs-lookup"><span data-stu-id="cf678-115">Start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="cf678-116">*cItems* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf678-116">*cItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf678-117">Anzahl der zu indizierenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="cf678-117">Count of items to be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="cf678-118">*ppbsynclist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cf678-118">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf678-119">Abgerufene Lizenz Synchronisierungs Liste.</span><span class="sxs-lookup"><span data-stu-id="cf678-119">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="cf678-120">*pcbsynclist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cf678-120">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf678-121">Größe der Lizenz Synchronisierungs Liste in Bytes.</span><span class="sxs-lookup"><span data-stu-id="cf678-121">Size of the license synchronization list, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cf678-122">*pdwnextstartingindex* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cf678-122">*pdwNextStartingIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf678-123">Nächste Anfangsposition für die Indizierung.</span><span class="sxs-lookup"><span data-stu-id="cf678-123">Next start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="cf678-124">*pcitemsprocgelassene* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cf678-124">*pcItemsProcessed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf678-125">Anzahl der Elemente, die verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cf678-125">Count of items being processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf678-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf678-126">Return value</span></span>

<span data-ttu-id="cf678-127">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="cf678-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cf678-128">Alle Schnittstellen Methoden in Windows Media Device Manager können eine der folgenden Klassen von Fehlercodes zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="cf678-128">All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:</span></span>

-   <span data-ttu-id="cf678-129">Standard-COM-Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cf678-129">Standard COM error codes</span></span>
-   <span data-ttu-id="cf678-130">In HRESULT-Werte konvertierte Windows-Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cf678-130">Windows error codes converted to HRESULT values</span></span>
-   <span data-ttu-id="cf678-131">Fehlercodes für Windows Media Device Manager</span><span class="sxs-lookup"><span data-stu-id="cf678-131">Windows Media Device Manager error codes</span></span>

<span data-ttu-id="cf678-132">Eine umfassende Liste möglicher Fehlercodes finden Sie unter [Fehlercodes](error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cf678-132">For an extensive list of possible error codes, see [Error Codes](error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf678-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf678-133">Requirements</span></span>



| <span data-ttu-id="cf678-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf678-134">Requirement</span></span> | <span data-ttu-id="cf678-135">Wert</span><span class="sxs-lookup"><span data-stu-id="cf678-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf678-136">Header</span><span class="sxs-lookup"><span data-stu-id="cf678-136">Header</span></span><br/>  | <dl> <span data-ttu-id="cf678-137"><dt>Wmddrmsp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cf678-137"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="cf678-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf678-138">Library</span></span><br/> | <dl> <span data-ttu-id="cf678-139"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf678-139"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf678-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf678-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf678-141">**Iwmdrmdevice:: getsynclist**</span><span class="sxs-lookup"><span data-stu-id="cf678-141">**IWMDRMDevice::GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[<span data-ttu-id="cf678-142">**IWMDRMDevice2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cf678-142">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 





