---
title: Ivmvirtualmachineevents onenhancedvideomodechanged-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass die Unterstützung einer virtuellen Maschine für den erweiterten Videomodus geändert wurde.
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- Onenhancedvideomodechanged-Methode virtueller PC
- Onenhancedvideomodechanged-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onenhancedvideomodechanged-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bbc67fe298c1a47d853072d8c58ab5b3ce1988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475027"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a><span data-ttu-id="7a9bb-106">Ivmvirtualmachineevents:: onenhancedvideomodechanged-Methode</span><span class="sxs-lookup"><span data-stu-id="7a9bb-106">IVMVirtualMachineEvents::OnEnhancedVideoModeChanged method</span></span>

<span data-ttu-id="7a9bb-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7a9bb-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7a9bb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7a9bb-109">Empfängt eine Benachrichtigung, dass die Unterstützung einer virtuellen Maschine für den erweiterten Videomodus geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-109">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a9bb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a9bb-110">Syntax</span></span>


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a><span data-ttu-id="7a9bb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a9bb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a9bb-112">*enhancedvideomode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a9bb-112">*enhancedVideoMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a9bb-113">Gibt an, ob der erweiterte Videomodus verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-113">Indicates whether enhanced video mode is available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a9bb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a9bb-114">Return value</span></span>

<span data-ttu-id="7a9bb-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7a9bb-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a9bb-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a9bb-117">Requirements</span></span>



| <span data-ttu-id="7a9bb-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a9bb-118">Requirement</span></span> | <span data-ttu-id="7a9bb-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7a9bb-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a9bb-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a9bb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7a9bb-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a9bb-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a9bb-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a9bb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7a9bb-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7a9bb-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7a9bb-124">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7a9bb-124">End of client support</span></span><br/>    | <span data-ttu-id="7a9bb-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a9bb-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7a9bb-126">Produkt</span><span class="sxs-lookup"><span data-stu-id="7a9bb-126">Product</span></span><br/>                  | <span data-ttu-id="7a9bb-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7a9bb-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7a9bb-128">Header</span><span class="sxs-lookup"><span data-stu-id="7a9bb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a9bb-129"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a9bb-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7a9bb-130">IID</span><span class="sxs-lookup"><span data-stu-id="7a9bb-130">IID</span></span><br/>                      | <span data-ttu-id="7a9bb-131">Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="7a9bb-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a9bb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a9bb-133">**Ivmvirtualmachineevents**</span><span class="sxs-lookup"><span data-stu-id="7a9bb-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

