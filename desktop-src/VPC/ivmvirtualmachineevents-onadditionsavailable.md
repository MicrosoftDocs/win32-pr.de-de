---
title: Ivmvirtualmachineevents onadditionsavailable-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass Integrations Komponenten auf einem virtuellen Computer verfügbar sind.
ms.assetid: c940104b-4d34-47c2-bf48-9024a7f86c46
keywords:
- Onadditionsavailable-Methode virtueller PC
- Onadditionsavailable-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onadditionsavailable-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsAvailable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 193b44f533079bc957cbb8b297409641814b6e21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478672"
---
# <a name="ivmvirtualmachineeventsonadditionsavailable-method"></a><span data-ttu-id="f1d6a-106">Ivmvirtualmachineevents:: onadditionsavailable-Methode</span><span class="sxs-lookup"><span data-stu-id="f1d6a-106">IVMVirtualMachineEvents::OnAdditionsAvailable method</span></span>

<span data-ttu-id="f1d6a-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f1d6a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f1d6a-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f1d6a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f1d6a-109">Empfängt eine Benachrichtigung, dass Integrations Komponenten auf einem virtuellen Computer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f1d6a-109">Receives notification that integration components are available in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1d6a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1d6a-110">Syntax</span></span>


```C++
HRESULT OnAdditionsAvailable();
```



## <a name="parameters"></a><span data-ttu-id="f1d6a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1d6a-111">Parameters</span></span>

<span data-ttu-id="f1d6a-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f1d6a-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f1d6a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1d6a-113">Return value</span></span>

<span data-ttu-id="f1d6a-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f1d6a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f1d6a-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f1d6a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1d6a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1d6a-116">Requirements</span></span>



| <span data-ttu-id="f1d6a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1d6a-117">Requirement</span></span> | <span data-ttu-id="f1d6a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f1d6a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1d6a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1d6a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f1d6a-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1d6a-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1d6a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1d6a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f1d6a-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f1d6a-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f1d6a-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f1d6a-123">End of client support</span></span><br/>    | <span data-ttu-id="f1d6a-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f1d6a-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f1d6a-125">Produkt</span><span class="sxs-lookup"><span data-stu-id="f1d6a-125">Product</span></span><br/>                  | <span data-ttu-id="f1d6a-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f1d6a-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f1d6a-127">Header</span><span class="sxs-lookup"><span data-stu-id="f1d6a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1d6a-128"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1d6a-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f1d6a-129">IID</span><span class="sxs-lookup"><span data-stu-id="f1d6a-129">IID</span></span><br/>                      | <span data-ttu-id="f1d6a-130">Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.</span><span class="sxs-lookup"><span data-stu-id="f1d6a-130">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="f1d6a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1d6a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1d6a-132">**Ivmvirtualmachineevents**</span><span class="sxs-lookup"><span data-stu-id="f1d6a-132">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

