---
title: Ivmguestos ProductType-Eigenschaft (vpccominterfaces. h)
description: Hiermit wird der Produkttyp des Gast Betriebssystems abgerufen, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- ProductType-Eigenschaft virtueller PC
- ProductType-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, ProductType-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bc79ffd0717ac0949103a05d1bcdaa96da48d7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337320"
---
# <a name="ivmguestosproducttype-property"></a><span data-ttu-id="1f7e2-106">Ivmguestos::P roducttype-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1f7e2-106">IVMGuestOS::ProductType property</span></span>

<span data-ttu-id="1f7e2-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1f7e2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1f7e2-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1f7e2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1f7e2-109">Hiermit wird der Produkttyp des Gast Betriebssystems abgerufen, das auf dem virtuellen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f7e2-109">Retrieves the product type of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="1f7e2-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1f7e2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f7e2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f7e2-111">Syntax</span></span>


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a><span data-ttu-id="1f7e2-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1f7e2-112">Property value</span></span>

<span data-ttu-id="1f7e2-113">Der Produkttyp.</span><span class="sxs-lookup"><span data-stu-id="1f7e2-113">The product type.</span></span> <span data-ttu-id="1f7e2-114">Die folgenden Zeichen folgen Werte werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f7e2-114">The following string values are supported.</span></span>



| <span data-ttu-id="1f7e2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1f7e2-115">Value</span></span>                                                                                  | <span data-ttu-id="1f7e2-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1f7e2-116">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1f7e2-117"><dt>"0x0000002"</dt></span><span class="sxs-lookup"><span data-stu-id="1f7e2-117"><dt>"0x0000002"</dt></span></span> </dl> | <span data-ttu-id="1f7e2-118">Das System ist ein Domänen Controller, und das Betriebssystem ist Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1f7e2-118">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="1f7e2-119"><dt>"0x0000003"</dt></span><span class="sxs-lookup"><span data-stu-id="1f7e2-119"><dt>"0x0000003"</dt></span></span> </dl> | <span data-ttu-id="1f7e2-120">Das Betriebssystem ist Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1f7e2-120">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="1f7e2-121">Beachten Sie, dass ein Server, der auch ein Domänen Controller ist, als **ver- \_ NT- \_ Domänen \_ Controller**, nicht als **ver-NT- \_ \_ Server** gemeldet</span><span class="sxs-lookup"><span data-stu-id="1f7e2-121">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <dl> <span data-ttu-id="1f7e2-122"><dt>"0x0000001"</dt></span><span class="sxs-lookup"><span data-stu-id="1f7e2-122"><dt>"0x0000001"</dt></span></span> </dl> | <span data-ttu-id="1f7e2-123">Das Betriebssystem ist Windows 7, Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1f7e2-123">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="1f7e2-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f7e2-124">Requirements</span></span>



| <span data-ttu-id="1f7e2-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f7e2-125">Requirement</span></span> | <span data-ttu-id="1f7e2-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1f7e2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f7e2-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f7e2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1f7e2-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f7e2-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f7e2-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f7e2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1f7e2-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1f7e2-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1f7e2-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1f7e2-131">End of client support</span></span><br/>    | <span data-ttu-id="1f7e2-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1f7e2-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1f7e2-133">Produkt</span><span class="sxs-lookup"><span data-stu-id="1f7e2-133">Product</span></span><br/>                  | <span data-ttu-id="1f7e2-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1f7e2-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1f7e2-135">Header</span><span class="sxs-lookup"><span data-stu-id="1f7e2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f7e2-136"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f7e2-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1f7e2-137">IID</span><span class="sxs-lookup"><span data-stu-id="1f7e2-137">IID</span></span><br/>                      | <span data-ttu-id="1f7e2-138">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="1f7e2-138">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="1f7e2-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f7e2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f7e2-140">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="1f7e2-140">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

