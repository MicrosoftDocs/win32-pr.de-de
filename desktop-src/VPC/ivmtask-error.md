---
title: Ivmtask Error-Eigenschaft (vpccominterfaces. h)
description: Ruft den für diese Aufgabe aufgezeichneten Fehler ab.
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Fehler Eigenschaft Virtual PC
- Fehler Eigenschaft Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, Error-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338553"
---
# <a name="ivmtaskerror-property"></a><span data-ttu-id="31851-106">Ivmtask:: Error-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="31851-106">IVMTask::Error property</span></span>

<span data-ttu-id="31851-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="31851-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="31851-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="31851-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="31851-109">Ruft den für diese Aufgabe aufgezeichneten Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="31851-109">Retrieves the error recorded for this task.</span></span>

<span data-ttu-id="31851-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="31851-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="31851-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="31851-111">Syntax</span></span>


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a><span data-ttu-id="31851-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="31851-112">Property value</span></span>

<span data-ttu-id="31851-113">Der aufgezeichnete Fehler.</span><span class="sxs-lookup"><span data-stu-id="31851-113">The recorded error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="31851-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="31851-114">Error codes</span></span>

<span data-ttu-id="31851-115">Von anderen Schnittstellen zurückgegebene Instanzen von [**ivmtask**](ivmtask.md) können zusätzliche Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="31851-115">Instances of [**IVMTask**](ivmtask.md) returned by other interfaces may return additional values.</span></span> <span data-ttu-id="31851-116">Weitere Informationen finden Sie in der Dokumentation der Methoden, die eine **ivmtask** -Instanz zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="31851-116">For details, see the documentation of the methods that return a **IVMTask** instance.</span></span>



| <span data-ttu-id="31851-117">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="31851-117">Name/value</span></span>                                                                                                                                                                        | <span data-ttu-id="31851-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="31851-118">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="31851-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="31851-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                           | <span data-ttu-id="31851-120">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="31851-120">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="31851-121"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="31851-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                             | <span data-ttu-id="31851-122">Der Parameterwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="31851-122">The parameter value is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="31851-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="31851-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                     | <span data-ttu-id="31851-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="31851-124">An unexpected error has occurred.</span></span><br/>                          |
| <dl> <span data-ttu-id="31851-125"><dt>VM \_ E \_ vmvirtualpc, \_ ältere \_ Version</dt> <dt>0xa0040952</dt></span><span class="sxs-lookup"><span data-stu-id="31851-125"><dt>VM\_E\_VMVIRTUALPC\_OLDER\_VERSION</dt> <dt>0xA0040952</dt></span></span> </dl>     | <span data-ttu-id="31851-126">Sowohl Virtual PC 2007 als auch Windows Virtual PC werden installiert.</span><span class="sxs-lookup"><span data-stu-id="31851-126">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <dl> <span data-ttu-id="31851-127"><dt>VM \_ E \_ Weitere \_ Virtualisierungssoftware \_ </dt> <dt>0xa0040953</dt></span><span class="sxs-lookup"><span data-stu-id="31851-127"><dt>VM\_E\_OTHER\_VIRTUALIZATION\_SOFTWARE</dt> <dt>0xA0040953</dt></span></span> </dl> | <span data-ttu-id="31851-128">Andere Virtualisierungssoftware ist installiert.</span><span class="sxs-lookup"><span data-stu-id="31851-128">Other virtualization software is installed.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="31851-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31851-129">Requirements</span></span>



| <span data-ttu-id="31851-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31851-130">Requirement</span></span> | <span data-ttu-id="31851-131">Wert</span><span class="sxs-lookup"><span data-stu-id="31851-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="31851-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31851-132">Minimum supported client</span></span><br/> | <span data-ttu-id="31851-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31851-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31851-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31851-134">Minimum supported server</span></span><br/> | <span data-ttu-id="31851-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="31851-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="31851-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="31851-136">End of client support</span></span><br/>    | <span data-ttu-id="31851-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="31851-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="31851-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="31851-138">Product</span></span><br/>                  | <span data-ttu-id="31851-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="31851-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="31851-140">Header</span><span class="sxs-lookup"><span data-stu-id="31851-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="31851-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="31851-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="31851-142">IID</span><span class="sxs-lookup"><span data-stu-id="31851-142">IID</span></span><br/>                      | <span data-ttu-id="31851-143">IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.</span><span class="sxs-lookup"><span data-stu-id="31851-143">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="31851-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31851-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31851-145">**Ivmtask**</span><span class="sxs-lookup"><span data-stu-id="31851-145">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

