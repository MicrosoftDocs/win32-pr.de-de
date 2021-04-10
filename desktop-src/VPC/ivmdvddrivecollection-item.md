---
title: Ivmdvddrivecollection-Element Eigenschaft (vpccominterfaces. h)
description: Ruft das CD-oder DVD-Laufwerks Objekt ab, das dem angegebenen Index entspricht.
ms.assetid: ecc94eea-9ddc-46c8-87e2-e67aca83eecc
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmdvddrivecollection-Schnittstelle
- Ivmdvddrivecollection Interface Virtual PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Item
- IVMDVDDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cc631ab6d4de3ab65071bf2b8692236f3ae03ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040568"
---
# <a name="ivmdvddrivecollectionitem-property"></a><span data-ttu-id="ff3a5-106">Ivmdvddrivecollection:: Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ff3a5-106">IVMDVDDriveCollection::Item property</span></span>

<span data-ttu-id="ff3a5-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ff3a5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ff3a5-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ff3a5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ff3a5-109">Ruft das CD-oder DVD-Laufwerks Objekt ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="ff3a5-109">Retrieves the CD or DVD drive object that corresponds to the specified index.</span></span>

<span data-ttu-id="ff3a5-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ff3a5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff3a5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff3a5-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long        index,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="property-value"></a><span data-ttu-id="ff3a5-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ff3a5-112">Property value</span></span>

<span data-ttu-id="ff3a5-113">Das [**ivmdvddrive**](ivmdvddrive.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="ff3a5-113">The [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ff3a5-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ff3a5-114">Error codes</span></span>



| <span data-ttu-id="ff3a5-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="ff3a5-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="ff3a5-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ff3a5-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff3a5-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ff3a5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ff3a5-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff3a5-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="ff3a5-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ff3a5-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ff3a5-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="ff3a5-120">The parameter is **NULL**.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="ff3a5-121"><dt>E \_ </dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="ff3a5-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="ff3a5-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ff3a5-122">An unexpected error has occurred.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="ff3a5-123"><dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="ff3a5-123"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="ff3a5-124">Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="ff3a5-124">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="ff3a5-125"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="ff3a5-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="ff3a5-126">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="ff3a5-126">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="ff3a5-127"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ff3a5-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ff3a5-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ff3a5-128">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="ff3a5-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff3a5-129">Requirements</span></span>



| <span data-ttu-id="ff3a5-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff3a5-130">Requirement</span></span> | <span data-ttu-id="ff3a5-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ff3a5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3a5-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff3a5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ff3a5-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff3a5-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff3a5-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff3a5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ff3a5-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ff3a5-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ff3a5-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ff3a5-136">End of client support</span></span><br/>    | <span data-ttu-id="ff3a5-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ff3a5-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ff3a5-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="ff3a5-138">Product</span></span><br/>                  | <span data-ttu-id="ff3a5-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ff3a5-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ff3a5-140">Header</span><span class="sxs-lookup"><span data-stu-id="ff3a5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff3a5-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff3a5-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ff3a5-142">IID</span><span class="sxs-lookup"><span data-stu-id="ff3a5-142">IID</span></span><br/>                      | <span data-ttu-id="ff3a5-143">IID \_ ivmdvddrivecollection ist als bc86e297-e55f-4742-9614-ad11d3131f68 definiert.</span><span class="sxs-lookup"><span data-stu-id="ff3a5-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="ff3a5-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff3a5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff3a5-145">**Ivmdvddrive**</span><span class="sxs-lookup"><span data-stu-id="ff3a5-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="ff3a5-146">**Ivmdvddrivecollection**</span><span class="sxs-lookup"><span data-stu-id="ff3a5-146">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

