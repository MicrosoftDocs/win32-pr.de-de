---
title: Ivmfloppydrivecollection-Element Eigenschaft (vpccominterfaces. h)
description: Disketten Objekt, das dem angegebenen Index entspricht.
ms.assetid: 068a1f1c-ae84-4689-b68a-ce25b68fc06b
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmfloppydrivecollection-Schnittstelle
- Ivmfloppydrivecollection Interface Virtual PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Item
- IVMFloppyDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315eaea13699d78a75457f39c6c915b30fa2fa9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106064"
---
# <a name="ivmfloppydrivecollectionitem-property"></a><span data-ttu-id="35a89-106">Ivmfloppydrivecollection:: Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="35a89-106">IVMFloppyDriveCollection::Item property</span></span>

<span data-ttu-id="35a89-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35a89-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="35a89-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="35a89-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="35a89-109">Ruft das Disketten Objekt ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="35a89-109">Retrieves the floppy object that corresponds to the specified index.</span></span>

<span data-ttu-id="35a89-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="35a89-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a89-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="35a89-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long           index,
  [out, retval] IVMFloppyDrive **floppyDrive
);
```



## <a name="property-value"></a><span data-ttu-id="35a89-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="35a89-112">Property value</span></span>

<span data-ttu-id="35a89-113">Das [**ivmfloppydrive**](ivmfloppydrive.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="35a89-113">The [**IVMFloppyDrive**](ivmfloppydrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35a89-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="35a89-114">Error codes</span></span>



| <span data-ttu-id="35a89-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="35a89-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="35a89-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="35a89-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35a89-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="35a89-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="35a89-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="35a89-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="35a89-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="35a89-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="35a89-120">Der *floppydrive* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="35a89-120">The *floppyDrive* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="35a89-121"><dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="35a89-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="35a89-122">Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="35a89-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="35a89-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="35a89-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="35a89-124">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="35a89-124">The configuration is unknown.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="35a89-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="35a89-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="35a89-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="35a89-126">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="35a89-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35a89-127">Requirements</span></span>



| <span data-ttu-id="35a89-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35a89-128">Requirement</span></span> | <span data-ttu-id="35a89-129">Wert</span><span class="sxs-lookup"><span data-stu-id="35a89-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="35a89-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35a89-130">Minimum supported client</span></span><br/> | <span data-ttu-id="35a89-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35a89-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35a89-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35a89-132">Minimum supported server</span></span><br/> | <span data-ttu-id="35a89-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="35a89-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="35a89-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="35a89-134">End of client support</span></span><br/>    | <span data-ttu-id="35a89-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="35a89-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="35a89-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="35a89-136">Product</span></span><br/>                  | <span data-ttu-id="35a89-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="35a89-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="35a89-138">Header</span><span class="sxs-lookup"><span data-stu-id="35a89-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="35a89-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="35a89-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="35a89-140">IID</span><span class="sxs-lookup"><span data-stu-id="35a89-140">IID</span></span><br/>                      | <span data-ttu-id="35a89-141">IID \_ ivmfloppydrivecollection ist als 8ba70a25-s698-4ee5-85ce-3cc93a925516 definiert.</span><span class="sxs-lookup"><span data-stu-id="35a89-141">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="35a89-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35a89-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a89-143">**Ivmfloppydrive**</span><span class="sxs-lookup"><span data-stu-id="35a89-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="35a89-144">**Ivmfloppydrivecollection**</span><span class="sxs-lookup"><span data-stu-id="35a89-144">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

