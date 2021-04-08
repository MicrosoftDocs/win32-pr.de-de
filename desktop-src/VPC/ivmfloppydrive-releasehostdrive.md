---
title: Ivmfloppydrive releasehostdrive-Methode (vpccominterfaces. h)
description: Gibt ein physisches Laufwerk auf dem Host vom Diskettenlaufwerk frei.
ms.assetid: 6d5a8e7c-684c-42bc-84e5-76d3e761b7f0
keywords:
- Releasehostdrive-Methode Virtual PC
- Releasehostdrive-Methode Virtual PC, ivmfloppydrive-Schnittstelle
- Ivmfloppydrive Interface Virtual PC, releasehostdrive-Methode
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ab726ba87dd978a21c4f27b20437926e07c19b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739769"
---
# <a name="ivmfloppydrivereleasehostdrive-method"></a><span data-ttu-id="4742c-106">Ivmfloppydrive:: releasehostdrive-Methode</span><span class="sxs-lookup"><span data-stu-id="4742c-106">IVMFloppyDrive::ReleaseHostDrive method</span></span>

<span data-ttu-id="4742c-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4742c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4742c-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4742c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4742c-109">Gibt ein physisches Laufwerk auf dem Host vom Diskettenlaufwerk frei.</span><span class="sxs-lookup"><span data-stu-id="4742c-109">Releases a physical drive on the host from the floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="4742c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4742c-110">Syntax</span></span>


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a><span data-ttu-id="4742c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4742c-111">Parameters</span></span>

<span data-ttu-id="4742c-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4742c-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4742c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4742c-113">Return value</span></span>

<span data-ttu-id="4742c-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4742c-114">This method can return one of these values.</span></span>



| <span data-ttu-id="4742c-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="4742c-115">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="4742c-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4742c-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4742c-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4742c-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="4742c-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="4742c-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="4742c-119"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="4742c-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>          | <span data-ttu-id="4742c-120">Die Konfiguration für diesen virtuellen Computer ist ungültig oder wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="4742c-120">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="4742c-121"><dt>**VM \_ E \_ Medien \_ falscher \_ Typ**</dt> <dt>0xa00400728</dt></span><span class="sxs-lookup"><span data-stu-id="4742c-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl>  | <span data-ttu-id="4742c-122">Das an dieses Diskettenlaufwerk angefügte Medium ist kein physisches Diskettenlaufwerk.</span><span class="sxs-lookup"><span data-stu-id="4742c-122">The media attached to this floppy drive is not a physical floppy drive.</span></span><br/>     |
| <dl> <span data-ttu-id="4742c-123"><dt>**VM \_ E \_ kein \_ Medium \_ erfasst**</dt> <dt>0xa00400652</dt></span><span class="sxs-lookup"><span data-stu-id="4742c-123"><dt>**VM\_E\_NO\_MEDIA\_CAPTURED**</dt> <dt>0xA00400652</dt></span></span> </dl> | <span data-ttu-id="4742c-124">An dieses Diskettenlaufwerk sind keine Medien angefügt.</span><span class="sxs-lookup"><span data-stu-id="4742c-124">There is no media attached to this floppy drive.</span></span><br/>                            |
| <dl> <span data-ttu-id="4742c-125"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4742c-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="4742c-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4742c-126">An unexpected error has occurred.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="4742c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4742c-127">Requirements</span></span>



| <span data-ttu-id="4742c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4742c-128">Requirement</span></span> | <span data-ttu-id="4742c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="4742c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4742c-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4742c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4742c-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4742c-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4742c-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4742c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4742c-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4742c-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4742c-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4742c-134">End of client support</span></span><br/>    | <span data-ttu-id="4742c-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4742c-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4742c-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="4742c-136">Product</span></span><br/>                  | <span data-ttu-id="4742c-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4742c-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4742c-138">Header</span><span class="sxs-lookup"><span data-stu-id="4742c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4742c-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4742c-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4742c-140">IID</span><span class="sxs-lookup"><span data-stu-id="4742c-140">IID</span></span><br/>                      | <span data-ttu-id="4742c-141">IID \_ ivmfloppydrive ist als 661abee6-112a-4ed9-BABF -3c874969s10e definiert.</span><span class="sxs-lookup"><span data-stu-id="4742c-141">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="4742c-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4742c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4742c-143">**Ivmfloppydrive**</span><span class="sxs-lookup"><span data-stu-id="4742c-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

