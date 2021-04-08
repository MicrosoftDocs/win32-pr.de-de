---
title: Ivmvirtualmachineevents onguestlogoff-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass sich ein Benutzer vom Gast Betriebssystem abgemeldet hat.
ms.assetid: 3771ba28-eea9-4c8b-9224-231b00d2f2f5
keywords:
- Onguestlogoff-Methode Virtual PC
- Onguestlogoff-Methode Virtual PC, ivmvirtualmachineevents-Schnittstelle
- Ivmvirtualmachineevents Interface Virtual PC, onguestlogoff-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestLogoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce5100c3901b3de32a769b6bae0e16fcffe26a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949378"
---
# <a name="ivmvirtualmachineeventsonguestlogoff-method"></a><span data-ttu-id="16081-106">Ivmvirtualmachineevents:: onguestlogoff-Methode</span><span class="sxs-lookup"><span data-stu-id="16081-106">IVMVirtualMachineEvents::OnGuestLogoff method</span></span>

<span data-ttu-id="16081-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="16081-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="16081-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="16081-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="16081-109">Empfängt eine Benachrichtigung, dass sich ein Benutzer vom Gast Betriebssystem abgemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="16081-109">Receives notification that a user has logged off from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="16081-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="16081-110">Syntax</span></span>


```C++
HRESULT OnGuestLogoff(
  [in] VMLogoffType logoffType
);
```



## <a name="parameters"></a><span data-ttu-id="16081-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="16081-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16081-112">*logofftype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16081-112">*logoffType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16081-113">Der Wert aus der [**vmlogofftype**](vmlogofftype.md) -Enumeration, der den Typ der Abmeldung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="16081-113">Value from the [**VMLogoffType**](vmlogofftype.md) enumeration that describes the type of logoff.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16081-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16081-114">Return value</span></span>

<span data-ttu-id="16081-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="16081-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="16081-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="16081-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="16081-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16081-117">Requirements</span></span>



| <span data-ttu-id="16081-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16081-118">Requirement</span></span> | <span data-ttu-id="16081-119">Wert</span><span class="sxs-lookup"><span data-stu-id="16081-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="16081-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16081-120">Minimum supported client</span></span><br/> | <span data-ttu-id="16081-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16081-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="16081-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16081-122">Minimum supported server</span></span><br/> | <span data-ttu-id="16081-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="16081-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="16081-124">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="16081-124">End of client support</span></span><br/>    | <span data-ttu-id="16081-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="16081-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="16081-126">Produkt</span><span class="sxs-lookup"><span data-stu-id="16081-126">Product</span></span><br/>                  | <span data-ttu-id="16081-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="16081-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="16081-128">Header</span><span class="sxs-lookup"><span data-stu-id="16081-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="16081-129"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="16081-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="16081-130">IID</span><span class="sxs-lookup"><span data-stu-id="16081-130">IID</span></span><br/>                      | <span data-ttu-id="16081-131">Diid \_ ivmvirtualmachineevents ist als 9d84f560-bb67-4961-BD12-a4da780c67e4 definiert.</span><span class="sxs-lookup"><span data-stu-id="16081-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="16081-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16081-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16081-133">**Ivmvirtualmachineevents**</span><span class="sxs-lookup"><span data-stu-id="16081-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> <dt>

[<span data-ttu-id="16081-134">**Vmlogofftype**</span><span class="sxs-lookup"><span data-stu-id="16081-134">**VMLogoffType**</span></span>](vmlogofftype.md)
</dt> </dl>

 

