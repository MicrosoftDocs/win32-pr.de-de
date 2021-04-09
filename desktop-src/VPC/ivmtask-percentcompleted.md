---
title: Ivmtask (prozentuabgeschlossen)-Eigenschaft (vpccominterfaces. h)
description: Ruft den Abschluss Prozentsatz der Aufgabe ab.
ms.assetid: 23ba9696-06ed-44ec-a1ec-ef3bf9122c6f
keywords:
- Der Eigenschaften-PC für die abgeschlossene Eigenschaft
- Prozentuenabgeschlossene Eigenschaft Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, Eigenschaft "prozentuabgeschlossen"
topic_type:
- apiref
api_name:
- IVMTask.PercentCompleted
- IVMTask.get_PercentCompleted
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa820adbbde2fc68632da27a9b146bd0e8f40143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743096"
---
# <a name="ivmtaskpercentcompleted-property"></a><span data-ttu-id="c2972-106">Ivmtask::P ercentabgeschlossene-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c2972-106">IVMTask::PercentCompleted property</span></span>

<span data-ttu-id="c2972-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c2972-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c2972-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c2972-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c2972-109">Ruft den Abschluss Prozentsatz der Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="c2972-109">Retrieves the completion percentage of the task.</span></span>

<span data-ttu-id="c2972-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c2972-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2972-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2972-111">Syntax</span></span>


```C++
HRESULT get_PercentCompleted(
  [out, retval] long *percentCompleted
);
```



## <a name="property-value"></a><span data-ttu-id="c2972-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c2972-112">Property value</span></span>

<span data-ttu-id="c2972-113">Der aktuelle Abschluss Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="c2972-113">The current completion percentage.</span></span> <span data-ttu-id="c2972-114">Der Wert ist eine Zahl zwischen 0 und 100.</span><span class="sxs-lookup"><span data-stu-id="c2972-114">The value is a number between 0 and 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c2972-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c2972-115">Error codes</span></span>



| <span data-ttu-id="c2972-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c2972-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c2972-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c2972-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c2972-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c2972-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c2972-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2972-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c2972-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c2972-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c2972-121">Der Parameterwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c2972-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="c2972-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c2972-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c2972-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c2972-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c2972-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2972-124">Requirements</span></span>



| <span data-ttu-id="c2972-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2972-125">Requirement</span></span> | <span data-ttu-id="c2972-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c2972-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2972-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2972-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c2972-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2972-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2972-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2972-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c2972-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c2972-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c2972-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c2972-131">End of client support</span></span><br/>    | <span data-ttu-id="c2972-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2972-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c2972-133">Produkt</span><span class="sxs-lookup"><span data-stu-id="c2972-133">Product</span></span><br/>                  | <span data-ttu-id="c2972-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c2972-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c2972-135">Header</span><span class="sxs-lookup"><span data-stu-id="c2972-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2972-136"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2972-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c2972-137">IID</span><span class="sxs-lookup"><span data-stu-id="c2972-137">IID</span></span><br/>                      | <span data-ttu-id="c2972-138">IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.</span><span class="sxs-lookup"><span data-stu-id="c2972-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="c2972-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2972-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2972-140">**Ivmtask**</span><span class="sxs-lookup"><span data-stu-id="c2972-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

