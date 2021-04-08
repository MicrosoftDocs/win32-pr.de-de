---
title: Ivmvirtualmachineevents onconfigurationchanged-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass sich ein Wert in der Konfiguration für diesen virtuellen Computer geändert hat.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Onconfigurationchanged-Methode virtueller PC
- Onconfigurationchanged-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onconfigurationchanged-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10459562da2d87b8c883217e003cd822ef923fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949379"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a><span data-ttu-id="2586a-106">Ivmvirtualmachineevents:: onconfigurationchanged-Methode</span><span class="sxs-lookup"><span data-stu-id="2586a-106">IVMVirtualMachineEvents::OnConfigurationChanged method</span></span>

<span data-ttu-id="2586a-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2586a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2586a-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2586a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2586a-109">Empfängt eine Benachrichtigung, dass sich ein Wert in der Konfiguration für diesen virtuellen Computer geändert hat.</span><span class="sxs-lookup"><span data-stu-id="2586a-109">Receives notification that a value in the configuration for this virtual machine has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2586a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2586a-110">Syntax</span></span>


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a><span data-ttu-id="2586a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2586a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2586a-112">*configKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2586a-112">*configKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2586a-113">Der Wert in der Konfiguration, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="2586a-113">The value inside the configuration that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="2586a-114">*ConfigData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2586a-114">*configData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2586a-115">Der neue Wert für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2586a-115">The new value for the configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2586a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2586a-116">Return value</span></span>

<span data-ttu-id="2586a-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2586a-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2586a-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2586a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2586a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2586a-119">Remarks</span></span>

<span data-ttu-id="2586a-120">Diese Methode wird aufgerufen, wenn sich die Konfiguration für diesen virtuellen Computer ändert.</span><span class="sxs-lookup"><span data-stu-id="2586a-120">This method is called when the configuration changes for this virtual machine.</span></span> <span data-ttu-id="2586a-121">Das Client Programm muss diese Schnittstellen Methode implementieren, um eine Benachrichtigung über das vmvirtualmachineevent configurationchanged-Ereignis zu erhalten, das \_ von [**ivmvirtualmachine**](ivmvirtualmachine.md)stammt.</span><span class="sxs-lookup"><span data-stu-id="2586a-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_ConfigurationChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2586a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2586a-122">Requirements</span></span>



| <span data-ttu-id="2586a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2586a-123">Requirement</span></span> | <span data-ttu-id="2586a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2586a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2586a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2586a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2586a-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2586a-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2586a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2586a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2586a-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2586a-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2586a-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2586a-129">End of client support</span></span><br/>    | <span data-ttu-id="2586a-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2586a-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2586a-131">Produkt</span><span class="sxs-lookup"><span data-stu-id="2586a-131">Product</span></span><br/>                  | <span data-ttu-id="2586a-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2586a-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2586a-133">Header</span><span class="sxs-lookup"><span data-stu-id="2586a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2586a-134"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2586a-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2586a-135">IID</span><span class="sxs-lookup"><span data-stu-id="2586a-135">IID</span></span><br/>                      | <span data-ttu-id="2586a-136">Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.</span><span class="sxs-lookup"><span data-stu-id="2586a-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="2586a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2586a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2586a-138">**Ivmvirtualmachineevents**</span><span class="sxs-lookup"><span data-stu-id="2586a-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

