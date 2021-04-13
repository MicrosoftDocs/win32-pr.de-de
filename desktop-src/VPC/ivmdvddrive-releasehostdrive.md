---
title: Ivmdvddrive releasehostdrive-Methode (vpccominterfaces. h)
description: Gibt ein erfasstes Host Laufwerk vom DVD-Laufwerk frei.
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- Releasehostdrive-Methode Virtual PC
- Releasehostdrive-Methode Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, releasehostdrive-Methode
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ed2c551ba619855743266b9b506a0c579f92a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391802"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a><span data-ttu-id="b04ea-106">Ivmdvddrive:: releasehostdrive-Methode</span><span class="sxs-lookup"><span data-stu-id="b04ea-106">IVMDVDDrive::ReleaseHostDrive method</span></span>

<span data-ttu-id="b04ea-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b04ea-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b04ea-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b04ea-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b04ea-109">Gibt ein erfasstes Host Laufwerk vom DVD-Laufwerk frei.</span><span class="sxs-lookup"><span data-stu-id="b04ea-109">Releases a captured host drive from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="b04ea-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b04ea-110">Syntax</span></span>


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a><span data-ttu-id="b04ea-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b04ea-111">Parameters</span></span>

<span data-ttu-id="b04ea-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b04ea-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b04ea-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b04ea-113">Return value</span></span>

<span data-ttu-id="b04ea-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b04ea-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b04ea-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="b04ea-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="b04ea-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b04ea-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b04ea-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b04ea-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="b04ea-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b04ea-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="b04ea-119"><dt>**E \_**</dt> <dt>0x80004005</dt> fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="b04ea-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="b04ea-120">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b04ea-120">An unexpected error has occurred.</span></span><br/>                                  |
| <dl> <span data-ttu-id="b04ea-121"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="b04ea-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="b04ea-122">Der virtuelle Computer wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="b04ea-122">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="b04ea-123"><dt>**VM \_ E \_ Medien \_ falscher \_ Typ**</dt> <dt>0xa00400728</dt></span><span class="sxs-lookup"><span data-stu-id="b04ea-123"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="b04ea-124">Das aktuell erfasste Medium ist kein Host Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="b04ea-124">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="b04ea-125"><dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="b04ea-125"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="b04ea-126">Das Laufwerk konnte aufgrund eines ungültigen busstandorts nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b04ea-126">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="b04ea-127"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b04ea-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="b04ea-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b04ea-128">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="b04ea-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b04ea-129">Requirements</span></span>



| <span data-ttu-id="b04ea-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b04ea-130">Requirement</span></span> | <span data-ttu-id="b04ea-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b04ea-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b04ea-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b04ea-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b04ea-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b04ea-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b04ea-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b04ea-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b04ea-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b04ea-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b04ea-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b04ea-136">End of client support</span></span><br/>    | <span data-ttu-id="b04ea-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b04ea-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b04ea-138">Produkt</span><span class="sxs-lookup"><span data-stu-id="b04ea-138">Product</span></span><br/>                  | <span data-ttu-id="b04ea-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b04ea-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b04ea-140">Header</span><span class="sxs-lookup"><span data-stu-id="b04ea-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b04ea-141"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b04ea-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b04ea-142">IID</span><span class="sxs-lookup"><span data-stu-id="b04ea-142">IID</span></span><br/>                      | <span data-ttu-id="b04ea-143">IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.</span><span class="sxs-lookup"><span data-stu-id="b04ea-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b04ea-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b04ea-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b04ea-145">**Ivmdvddrive**</span><span class="sxs-lookup"><span data-stu-id="b04ea-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

