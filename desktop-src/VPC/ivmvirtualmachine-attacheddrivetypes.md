---
title: Ivmvirtualmachine attacheddrivetypes-Eigenschaft (vpccominterfaces. h)
description: Ein Array, das den Typ des Laufwerks angibt, das an die einzelnen Speicherorte der VM angeschlossen ist.
ms.assetid: 6896c9cd-5448-4fbb-8c8e-eef306a5cea1
keywords:
- Eigenschaft "attacheddrivetypes" Virtual PC
- Eigenschaft "attacheddrivetypes" Virtual PC, ivmvirtualmachine Interface
- Ivmvirtualmachine Interface Virtual PC, Eigenschaft "attacheddrivetypes"
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachedDriveTypes
- IVMVirtualMachine.get_AttachedDriveTypes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5f01802b7fa7e3a4f1ccbfc1b5c4bf70e06614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105656"
---
# <a name="ivmvirtualmachineattacheddrivetypes-property"></a><span data-ttu-id="af4e6-106">Ivmvirtualmachine:: attacheddrivetypes-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af4e6-106">IVMVirtualMachine::AttachedDriveTypes property</span></span>

<span data-ttu-id="af4e6-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af4e6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="af4e6-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="af4e6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="af4e6-109">Ruft ein Array ab, das den Typ des Laufwerks angibt, das an die einzelnen Speicherorte der virtuellen Maschine (VM) angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="af4e6-109">Retrieves an array indicating the type of drive attached to each location in the virtual machine (VM).</span></span>

<span data-ttu-id="af4e6-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="af4e6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="af4e6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="af4e6-111">Syntax</span></span>


```C++
HRESULT get_AttachedDriveTypes(
  [out, retval] VARIANT *driveTypes
);
```



## <a name="property-value"></a><span data-ttu-id="af4e6-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="af4e6-112">Property value</span></span>

<span data-ttu-id="af4e6-113">Eine Variante vom Typ **VT \_ Array** \| **VT \_** , die Einträge vom Typ **VT \_ UI1** enthält.</span><span class="sxs-lookup"><span data-stu-id="af4e6-113">A variant of type **VT\_ARRAY** \| **VT\_VARIANT** containing entries of type **VT\_UI1**.</span></span> <span data-ttu-id="af4e6-114">Das Array enthält den [**vmdrivetype**](vmdrivetype.md) -Wert jedes Geräts, das mit jedem Busstandort verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="af4e6-114">The array contains the [**VMDriveType**](vmdrivetype.md) value of each device connected to every bus location.</span></span> <span data-ttu-id="af4e6-115">Das Array wird nach \[ *busnumber*-Geräte-ID geordnet \] \[  \] .</span><span class="sxs-lookup"><span data-stu-id="af4e6-115">The array is ordered by \[*busNumber*\]\[*deviceID*\].</span></span>

## <a name="error-codes"></a><span data-ttu-id="af4e6-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="af4e6-116">Error codes</span></span>



| <span data-ttu-id="af4e6-117">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="af4e6-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="af4e6-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="af4e6-118">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="af4e6-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="af4e6-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="af4e6-120">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="af4e6-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="af4e6-121"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="af4e6-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="af4e6-122">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="af4e6-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="af4e6-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="af4e6-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="af4e6-124">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="af4e6-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="af4e6-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="af4e6-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="af4e6-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="af4e6-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="af4e6-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af4e6-127">Requirements</span></span>



| <span data-ttu-id="af4e6-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af4e6-128">Requirement</span></span> | <span data-ttu-id="af4e6-129">Wert</span><span class="sxs-lookup"><span data-stu-id="af4e6-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="af4e6-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af4e6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="af4e6-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af4e6-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af4e6-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af4e6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="af4e6-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="af4e6-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="af4e6-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="af4e6-134">End of client support</span></span><br/>    | <span data-ttu-id="af4e6-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="af4e6-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="af4e6-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="af4e6-136">Product</span></span><br/>                  | <span data-ttu-id="af4e6-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="af4e6-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="af4e6-138">Header</span><span class="sxs-lookup"><span data-stu-id="af4e6-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="af4e6-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="af4e6-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="af4e6-140">IID</span><span class="sxs-lookup"><span data-stu-id="af4e6-140">IID</span></span><br/>                      | <span data-ttu-id="af4e6-141">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="af4e6-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="af4e6-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af4e6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af4e6-143">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="af4e6-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

