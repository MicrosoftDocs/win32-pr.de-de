---
title: Ivmparallelportcollection-Element Eigenschaft (vpccominterfaces. h)
description: Ruft das parallele Port Objekt ab, das dem angegebenen Index entspricht.
ms.assetid: f67a4224-ca96-4d68-9f0f-4977ffff859e
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmparallelportcollection-Schnittstelle
- Ivmparallelportcollection-Schnittstelle Virtual PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Item
- IVMParallelPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa450f1859db8af6ed884b37fc693fc4fb1990f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478693"
---
# <a name="ivmparallelportcollectionitem-property"></a><span data-ttu-id="1dc5a-106">Ivmparallelportcollection:: Item-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1dc5a-106">IVMParallelPortCollection::Item property</span></span>

<span data-ttu-id="1dc5a-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1dc5a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1dc5a-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1dc5a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1dc5a-109">Ruft das parallele Port Objekt ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="1dc5a-109">Retrieves the parallel port object that corresponds to the specified index.</span></span>

<span data-ttu-id="1dc5a-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1dc5a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc5a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dc5a-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long            index,
  [out, retval] IVMParallelPort **vmParallelPort
);
```



## <a name="property-value"></a><span data-ttu-id="1dc5a-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1dc5a-112">Property value</span></span>

<span data-ttu-id="1dc5a-113">Das [**ivmparallelport**](ivmparallelport.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1dc5a-113">The [**IVMParallelPort**](ivmparallelport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1dc5a-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1dc5a-114">Error codes</span></span>



| <span data-ttu-id="1dc5a-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="1dc5a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="1dc5a-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1dc5a-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1dc5a-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1dc5a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1dc5a-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="1dc5a-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="1dc5a-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1dc5a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1dc5a-120">Der *vmparallelport* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="1dc5a-120">The *vmParallelPort* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="1dc5a-121"><dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="1dc5a-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="1dc5a-122">Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1dc5a-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="1dc5a-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="1dc5a-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="1dc5a-124">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="1dc5a-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="1dc5a-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1dc5a-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1dc5a-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1dc5a-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="1dc5a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1dc5a-127">Requirements</span></span>



| <span data-ttu-id="1dc5a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1dc5a-128">Requirement</span></span> | <span data-ttu-id="1dc5a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1dc5a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc5a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1dc5a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc5a-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1dc5a-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1dc5a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1dc5a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc5a-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1dc5a-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1dc5a-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1dc5a-134">End of client support</span></span><br/>    | <span data-ttu-id="1dc5a-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1dc5a-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1dc5a-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="1dc5a-136">Product</span></span><br/>                  | <span data-ttu-id="1dc5a-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1dc5a-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1dc5a-138">Header</span><span class="sxs-lookup"><span data-stu-id="1dc5a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dc5a-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dc5a-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1dc5a-140">IID</span><span class="sxs-lookup"><span data-stu-id="1dc5a-140">IID</span></span><br/>                      | <span data-ttu-id="1dc5a-141">IID \_ ivmparallelportcollection ist als 27c3e036-198l-430c-8735-6e652f 7203fd definiert.</span><span class="sxs-lookup"><span data-stu-id="1dc5a-141">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1dc5a-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dc5a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc5a-143">**Ivmparallelport**</span><span class="sxs-lookup"><span data-stu-id="1dc5a-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="1dc5a-144">**Ivmparallelportcollection**</span><span class="sxs-lookup"><span data-stu-id="1dc5a-144">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

