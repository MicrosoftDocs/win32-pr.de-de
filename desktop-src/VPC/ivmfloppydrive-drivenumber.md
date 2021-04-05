---
title: Ivmfloppydrive-drivenenumber-Eigenschaft (vpccominterfaces. h)
description: Ruft den NULL basierten Index des Controllers ab, an den das Diskettenlaufwerk angefügt ist.
ms.assetid: 79a40cad-d280-4c67-9214-0532569e47e4
keywords:
- Drivenumschlag-Eigenschaft virtueller PC
- Drivenumschlag-Eigenschaft Virtual PC, ivmfloppydrive-Schnittstelle
- Ivmfloppydrive Interface Virtual PC, drivenumschlag-Eigenschaft
topic_type:
- apiref
api_name:
- IVMFloppyDrive.DriveNumber
- IVMFloppyDrive.get_DriveNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2f2aeacaf3067515e9e44c58422cd4c9f31fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858970"
---
# <a name="ivmfloppydrivedrivenumber-property"></a><span data-ttu-id="e89ea-106">Ivmfloppydrive::D rivenumber-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e89ea-106">IVMFloppyDrive::DriveNumber property</span></span>

<span data-ttu-id="e89ea-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e89ea-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e89ea-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e89ea-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e89ea-109">Ruft den NULL basierten Index des Controllers ab, an den das Diskettenlaufwerk angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="e89ea-109">Retrieves the zero-based index of the controller to which the floppy drive is attached.</span></span>

<span data-ttu-id="e89ea-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e89ea-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e89ea-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e89ea-111">Syntax</span></span>


```C++
HRESULT get_DriveNumber(
  [out, retval] long *driveNumber
);
```



## <a name="property-value"></a><span data-ttu-id="e89ea-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e89ea-112">Property value</span></span>

<span data-ttu-id="e89ea-113">Der null basierte Index des Controllers.</span><span class="sxs-lookup"><span data-stu-id="e89ea-113">The zero-based index of the controller.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e89ea-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e89ea-114">Error codes</span></span>



| <span data-ttu-id="e89ea-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="e89ea-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e89ea-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e89ea-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e89ea-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e89ea-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e89ea-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e89ea-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e89ea-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e89ea-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e89ea-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="e89ea-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="e89ea-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e89ea-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e89ea-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e89ea-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e89ea-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e89ea-123">Requirements</span></span>



| <span data-ttu-id="e89ea-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e89ea-124">Requirement</span></span> | <span data-ttu-id="e89ea-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e89ea-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e89ea-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e89ea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e89ea-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e89ea-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e89ea-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e89ea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e89ea-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e89ea-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e89ea-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e89ea-130">End of client support</span></span><br/>    | <span data-ttu-id="e89ea-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e89ea-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e89ea-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="e89ea-132">Product</span></span><br/>                  | <span data-ttu-id="e89ea-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e89ea-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e89ea-134">Header</span><span class="sxs-lookup"><span data-stu-id="e89ea-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e89ea-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e89ea-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e89ea-136">IID</span><span class="sxs-lookup"><span data-stu-id="e89ea-136">IID</span></span><br/>                      | <span data-ttu-id="e89ea-137">IID \_ ivmfloppydrive ist als 661abee6-112a-4ed9-BABF -3c874969s10e definiert.</span><span class="sxs-lookup"><span data-stu-id="e89ea-137">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="e89ea-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e89ea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e89ea-139">**Ivmfloppydrive**</span><span class="sxs-lookup"><span data-stu-id="e89ea-139">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

