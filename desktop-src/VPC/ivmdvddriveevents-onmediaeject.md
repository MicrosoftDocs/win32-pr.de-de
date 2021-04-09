---
title: Ivmdvddriveevents onmediaeject-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass Medien vom Laufwerk ausworfen wurden. | Ivmdvddriveevents onmediaeject-Methode (vpccominterfaces. h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- Onmediaeject-Methode Virtual PC
- Onmediaeject-Methode Virtual PC, ivmdvddriveevents-Schnittstelle
- Ivmdvddriveevents Interface Virtual PC, onmediaeject-Methode
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b66091dcc6cc5ee28ab6e0cb3d58e3e647e41cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869735"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a><span data-ttu-id="1d907-107">Ivmdvddriveevents:: onmediaeject-Methode</span><span class="sxs-lookup"><span data-stu-id="1d907-107">IVMDVDDriveEvents::OnMediaEject method</span></span>

<span data-ttu-id="1d907-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1d907-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1d907-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1d907-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1d907-110">Empfängt eine Benachrichtigung, dass Medien vom Laufwerk ausworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="1d907-110">Receives notification that media has been ejected from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d907-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d907-111">Syntax</span></span>


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="1d907-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d907-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d907-113">*mediapath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d907-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d907-114">Der Buchstabe des Host Laufwerks bzw. der Pfad zum ISO-Abbild.</span><span class="sxs-lookup"><span data-stu-id="1d907-114">The host drive letter, or path, to the ISO image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d907-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d907-115">Return value</span></span>

<span data-ttu-id="1d907-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="1d907-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1d907-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1d907-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d907-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d907-118">Remarks</span></span>

<span data-ttu-id="1d907-119">Diese Methode wird aufgerufen, wenn Medien (ein ISO-Image oder ein Laufwerk auf einem Host Laufwerk) ausworfen werden.</span><span class="sxs-lookup"><span data-stu-id="1d907-119">This method is called when media (an ISO image or a disc in a host drive) is ejected.</span></span> <span data-ttu-id="1d907-120">Das Client Programm muss diese Schnittstellen Methode implementieren, um eine Benachrichtigung über das oneject-Ereignis von vmdvddriveevent zu erhalten, das \_ von [**ivmdvddrive**](ivmdvddrive.md)stammt.</span><span class="sxs-lookup"><span data-stu-id="1d907-120">The client program must implement this interface method to receive notification of the vmDVDDriveEvent\_OnEject event originating from [**IVMDVDDrive**](ivmdvddrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d907-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d907-121">Requirements</span></span>



| <span data-ttu-id="1d907-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d907-122">Requirement</span></span> | <span data-ttu-id="1d907-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1d907-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d907-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d907-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1d907-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d907-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d907-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d907-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1d907-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1d907-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1d907-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1d907-128">End of client support</span></span><br/>    | <span data-ttu-id="1d907-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1d907-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1d907-130">Produkt</span><span class="sxs-lookup"><span data-stu-id="1d907-130">Product</span></span><br/>                  | <span data-ttu-id="1d907-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1d907-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1d907-132">Header</span><span class="sxs-lookup"><span data-stu-id="1d907-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d907-133"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d907-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1d907-134">IID</span><span class="sxs-lookup"><span data-stu-id="1d907-134">IID</span></span><br/>                      | <span data-ttu-id="1d907-135">Diid \_ ivmdvddriveevents ist als c2a7d8e9-e76c-4eb8-94f7-71a5122d249b definiert.</span><span class="sxs-lookup"><span data-stu-id="1d907-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="1d907-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d907-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d907-137">**Ivmdvddriveevents**</span><span class="sxs-lookup"><span data-stu-id="1d907-137">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

