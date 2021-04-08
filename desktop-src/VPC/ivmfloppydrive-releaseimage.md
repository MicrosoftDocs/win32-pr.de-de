---
title: Ivmfloppydrive ReleaseImage-Methode (vpccominterfaces. h)
description: Gibt ein Disketten Medienbild auf dem Host vom Diskettenlaufwerk aus.
ms.assetid: 12fc6dc4-8450-4122-b0f0-ed11cc10134c
keywords:
- ReleaseImage-Methode Virtual PC
- ReleaseImage-Methode Virtual PC, ivmfloppydrive-Schnittstelle
- Ivmfloppydrive Interface Virtual PC, ReleaseImage-Methode
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece899bbb615fc2d54a3cbdc86193e743168ef23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739768"
---
# <a name="ivmfloppydrivereleaseimage-method"></a><span data-ttu-id="2c35b-106">Ivmfloppydrive:: ReleaseImage-Methode</span><span class="sxs-lookup"><span data-stu-id="2c35b-106">IVMFloppyDrive::ReleaseImage method</span></span>

<span data-ttu-id="2c35b-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2c35b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2c35b-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2c35b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2c35b-109">Gibt ein Disketten Medienbild auf dem Host vom Diskettenlaufwerk aus.</span><span class="sxs-lookup"><span data-stu-id="2c35b-109">Releases a floppy media image on the host from the floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c35b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c35b-110">Syntax</span></span>


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a><span data-ttu-id="2c35b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c35b-111">Parameters</span></span>

<span data-ttu-id="2c35b-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2c35b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c35b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c35b-113">Return value</span></span>

<span data-ttu-id="2c35b-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2c35b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="2c35b-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="2c35b-115">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="2c35b-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c35b-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c35b-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2c35b-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="2c35b-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c35b-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="2c35b-119"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="2c35b-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>          | <span data-ttu-id="2c35b-120">Die Konfiguration für diesen virtuellen Computer ist ungültig oder wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="2c35b-120">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="2c35b-121"><dt>**VM \_ E \_ Medien \_ falscher \_ Typ**</dt> <dt>0xa00400728</dt></span><span class="sxs-lookup"><span data-stu-id="2c35b-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl>  | <span data-ttu-id="2c35b-122">Das an dieses Diskettenlaufwerk angefügte Medium ist kein Disketten Image.</span><span class="sxs-lookup"><span data-stu-id="2c35b-122">The media attached to this floppy drive is not a floppy disk image.</span></span><br/>         |
| <dl> <span data-ttu-id="2c35b-123"><dt>**VM \_ E \_ kein \_ Medium \_ erfasst**</dt> <dt>0xa00400652</dt></span><span class="sxs-lookup"><span data-stu-id="2c35b-123"><dt>**VM\_E\_NO\_MEDIA\_CAPTURED**</dt> <dt>0xA00400652</dt></span></span> </dl> | <span data-ttu-id="2c35b-124">An dieses Diskettenlaufwerk sind keine Medien angefügt.</span><span class="sxs-lookup"><span data-stu-id="2c35b-124">There is no media attached to this floppy drive.</span></span><br/>                            |
| <dl> <span data-ttu-id="2c35b-125"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2c35b-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="2c35b-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2c35b-126">An unexpected error has occurred.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="2c35b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c35b-127">Requirements</span></span>



| <span data-ttu-id="2c35b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c35b-128">Requirement</span></span> | <span data-ttu-id="2c35b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2c35b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c35b-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c35b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2c35b-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c35b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c35b-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c35b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2c35b-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2c35b-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2c35b-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2c35b-134">End of client support</span></span><br/>    | <span data-ttu-id="2c35b-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c35b-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2c35b-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="2c35b-136">Product</span></span><br/>                  | <span data-ttu-id="2c35b-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2c35b-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2c35b-138">Header</span><span class="sxs-lookup"><span data-stu-id="2c35b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c35b-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c35b-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2c35b-140">IID</span><span class="sxs-lookup"><span data-stu-id="2c35b-140">IID</span></span><br/>                      | <span data-ttu-id="2c35b-141">IID \_ ivmfloppydrive ist als 661abee6-112a-4ed9-BABF -3c874969s10e definiert.</span><span class="sxs-lookup"><span data-stu-id="2c35b-141">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="2c35b-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c35b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c35b-143">**Ivmfloppydrive**</span><span class="sxs-lookup"><span data-stu-id="2c35b-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

