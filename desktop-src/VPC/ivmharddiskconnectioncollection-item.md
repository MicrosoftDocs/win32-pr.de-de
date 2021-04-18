---
title: Ivmharddiskconnectioncollection-Element Eigenschaft (vpccominterfaces. h)
description: Ruft das Festplatten Verbindungs Objekt ab, das dem angegebenen Index entspricht.
ms.assetid: 24e158fb-b026-4619-9d0d-a59cd782894f
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmharddiskconnectioncollection-Schnittstelle
- Ivmharddiskconnectioncollection-Schnittstelle Virtual PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Item
- IVMHardDiskConnectionCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5558e70cfcf18f67c14e52160737b851fa9ea2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338314"
---
# <a name="ivmharddiskconnectioncollectionitem-property"></a><span data-ttu-id="2792f-106">Ivmharddiskconnectioncollection:: Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2792f-106">IVMHardDiskConnectionCollection::Item property</span></span>

<span data-ttu-id="2792f-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2792f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2792f-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2792f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2792f-109">Ruft das Festplatten Verbindungs Objekt ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="2792f-109">Retrieves the hard disk connection object that corresponds to the specified index.</span></span>

<span data-ttu-id="2792f-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2792f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2792f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2792f-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long                  index,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="property-value"></a><span data-ttu-id="2792f-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2792f-112">Property value</span></span>

<span data-ttu-id="2792f-113">Das [**ivmharddiskconnection**](ivmharddiskconnection.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2792f-113">The [**IVMHardDiskConnection**](ivmharddiskconnection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2792f-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2792f-114">Error codes</span></span>



| <span data-ttu-id="2792f-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="2792f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2792f-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2792f-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2792f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2792f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2792f-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2792f-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="2792f-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2792f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2792f-120">Der *harddiskconnection* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="2792f-120">The *hardDiskConnection* parameter is **NULL**.</span></span> <br/>                                    |
| <dl> <span data-ttu-id="2792f-121"><dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="2792f-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="2792f-122">Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="2792f-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="2792f-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="2792f-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="2792f-124">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="2792f-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="2792f-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2792f-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2792f-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2792f-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="2792f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2792f-127">Requirements</span></span>



| <span data-ttu-id="2792f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2792f-128">Requirement</span></span> | <span data-ttu-id="2792f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2792f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2792f-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2792f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2792f-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2792f-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="2792f-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2792f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2792f-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2792f-133">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="2792f-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2792f-134">End of client support</span></span><br/>    | <span data-ttu-id="2792f-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2792f-135">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="2792f-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="2792f-136">Product</span></span><br/>                  | <span data-ttu-id="2792f-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2792f-137">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="2792f-138">Header</span><span class="sxs-lookup"><span data-stu-id="2792f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2792f-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2792f-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="2792f-140">IID</span><span class="sxs-lookup"><span data-stu-id="2792f-140">IID</span></span><br/>                      | <span data-ttu-id="2792f-141">IID \_ ivmharddiskconnectioncollection ist definiert als b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="2792f-141">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2792f-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2792f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2792f-143">**Ivmharddiskconnection**</span><span class="sxs-lookup"><span data-stu-id="2792f-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> <dt>

[<span data-ttu-id="2792f-144">**Ivmharddiskconnectioncollection**</span><span class="sxs-lookup"><span data-stu-id="2792f-144">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

