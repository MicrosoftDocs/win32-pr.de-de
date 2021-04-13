---
title: Ivmdvddrive ReleaseImage-Methode (vpccominterfaces. h)
description: Gibt ein erfasstes ISO-Abbild vom DVD-Laufwerk frei.
ms.assetid: 7cc95cf3-9d25-495f-863c-8eddd4068835
keywords:
- ReleaseImage-Methode Virtual PC
- ReleaseImage-Methode Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, ReleaseImage-Methode
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a36a13b258d155760269399d9f25f5eda6f296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475447"
---
# <a name="ivmdvddrivereleaseimage-method"></a><span data-ttu-id="4a7d8-106">Ivmdvddrive:: ReleaseImage-Methode</span><span class="sxs-lookup"><span data-stu-id="4a7d8-106">IVMDVDDrive::ReleaseImage method</span></span>

<span data-ttu-id="4a7d8-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4a7d8-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4a7d8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4a7d8-109">Gibt ein erfasstes ISO-Abbild vom DVD-Laufwerk frei.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-109">Releases a captured ISO image from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a7d8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a7d8-110">Syntax</span></span>


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a><span data-ttu-id="4a7d8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a7d8-111">Parameters</span></span>

<span data-ttu-id="4a7d8-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a7d8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a7d8-113">Return value</span></span>

<span data-ttu-id="4a7d8-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-114">This method can return one of these values.</span></span>



| <span data-ttu-id="4a7d8-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="4a7d8-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="4a7d8-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a7d8-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a7d8-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4a7d8-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="4a7d8-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="4a7d8-119"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="4a7d8-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="4a7d8-120">Der virtuelle Computer wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-120">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="4a7d8-121"><dt>**VM \_ E \_ Medien \_ falscher \_ Typ**</dt> <dt>0xa00400728</dt></span><span class="sxs-lookup"><span data-stu-id="4a7d8-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="4a7d8-122">Das aktuell erfasste Medium ist kein Host Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-122">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="4a7d8-123"><dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="4a7d8-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="4a7d8-124">Das Laufwerk konnte aufgrund eines ungültigen busstandorts nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-124">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="4a7d8-125"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4a7d8-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="4a7d8-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-126">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="4a7d8-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a7d8-127">Requirements</span></span>



| <span data-ttu-id="4a7d8-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a7d8-128">Requirement</span></span> | <span data-ttu-id="4a7d8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="4a7d8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a7d8-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a7d8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4a7d8-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a7d8-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4a7d8-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a7d8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4a7d8-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4a7d8-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4a7d8-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4a7d8-134">End of client support</span></span><br/>    | <span data-ttu-id="4a7d8-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4a7d8-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4a7d8-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="4a7d8-136">Product</span></span><br/>                  | <span data-ttu-id="4a7d8-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4a7d8-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4a7d8-138">Header</span><span class="sxs-lookup"><span data-stu-id="4a7d8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a7d8-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a7d8-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4a7d8-140">IID</span><span class="sxs-lookup"><span data-stu-id="4a7d8-140">IID</span></span><br/>                      | <span data-ttu-id="4a7d8-141">IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.</span><span class="sxs-lookup"><span data-stu-id="4a7d8-141">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="4a7d8-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a7d8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a7d8-143">**Ivmdvddrive**</span><span class="sxs-lookup"><span data-stu-id="4a7d8-143">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

