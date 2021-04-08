---
title: IWMPEvents4 syncschätzationcomplete-Methode
description: Das syncschätzationcomplete-Ereignis tritt auf, wenn eine von IWMPSyncDevice3 estimatesyncsize initiierte Größen Schätzung beendet ist.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- Syncschätzationcomplete-Methode, Windows-Media Player
- Syncschätzationcomplete-Methode, Windows Media Player, IWMPEvents4-Schnittstelle
- IWMPEvents4 Interface, Windows Media Player, syncschätzationcomplete-Methode
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 209ed2f2bd0f075dbaa8d442a276c994d50ce2e5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723384"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a><span data-ttu-id="8a457-106">IWMPEvents4:: syncschätzationcomplete-Methode</span><span class="sxs-lookup"><span data-stu-id="8a457-106">IWMPEvents4::SyncEstimationComplete method</span></span>

<span data-ttu-id="8a457-107">Das **syncschätzationcomplete** -Ereignis tritt auf, wenn eine von [**IWMPSyncDevice3:: estimatesyncsize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)initiierte Größen Schätzung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="8a457-107">The **SyncEstimationComplete** event occurs when a size estimation, previously initiated by [**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize), is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a457-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a457-108">Syntax</span></span>


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a><span data-ttu-id="8a457-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a457-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a457-110">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a457-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a457-111">Ein Zeiger auf die [**iwmpsyncdevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) -Schnittstelle, die das Gerät darstellt, für das die Größen Schätzung initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8a457-111">Pointer to the [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) interface that represents the device for which the size estimation was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="8a457-112">*hrresult* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a457-112">*hrResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a457-113">Ein-Wert, der den Erfolg oder Misserfolg der Schätzung angibt.</span><span class="sxs-lookup"><span data-stu-id="8a457-113">A value that indicates the success or failure of the estimation.</span></span>



| <span data-ttu-id="8a457-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8a457-114">Value</span></span>                                                                                                                                       | <span data-ttu-id="8a457-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8a457-115">Meaning</span></span>                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="8a457-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a457-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8a457-117">Die Schätzung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8a457-117">The estimation succeeded.</span></span><br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <span data-ttu-id="8a457-118"><dt>**E \_ Abbrechen**</dt></span><span class="sxs-lookup"><span data-stu-id="8a457-118"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="8a457-119">Die Schätzung wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="8a457-119">The estimation was aborted.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8a457-120">*lestimatedusedspace* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a457-120">*lEstimatedUsedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a457-121">Der geschätzte Speicherplatz (in Bytes), der auf dem Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8a457-121">The estimated space (in bytes) that would be used on the device.</span></span>

</dd> <dt>

<span data-ttu-id="8a457-122">*lestimatedsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a457-122">*lEstimatedSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a457-123">Die geschätzte Größe der zu synchronisierenden Daten (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="8a457-123">The estimated size (in bytes) of the data to be synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a457-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a457-124">Return value</span></span>

<span data-ttu-id="8a457-125">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8a457-125">This method does not return a value.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a457-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a457-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a457-127">**IWMPEvents4-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8a457-127">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[<span data-ttu-id="8a457-128">**IWMPSyncDevice3:: estimatesyncsize**</span><span class="sxs-lookup"><span data-stu-id="8a457-128">**IWMPSyncDevice3::estimateSyncSize**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





