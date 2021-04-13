---
title: Ivmguestos installintegrationcomponents-Methode (vpccominterfaces. h)
description: Hiermit werden die aktuellen Integrations Komponenten in das Gast Betriebssystem eingecheckt und installiert.
ms.assetid: 06f302b3-ec2b-471a-8e2e-095ed6ecbd3d
keywords:
- Installintegrationcomponents-Methode Virtual PC
- Installintegrationcomponents-Methode Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, installintegrationcomponents-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.InstallIntegrationComponents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879ded1464ebd310e1d1da4e3a952dc086600350
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391556"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a><span data-ttu-id="f8fd4-106">Ivmguestos:: installintegrationcomponents-Methode</span><span class="sxs-lookup"><span data-stu-id="f8fd4-106">IVMGuestOS::InstallIntegrationComponents method</span></span>

<span data-ttu-id="f8fd4-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f8fd4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f8fd4-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f8fd4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f8fd4-109">Hiermit werden die aktuellen Integrations Komponenten in das Gast Betriebssystem eingecheckt und installiert.</span><span class="sxs-lookup"><span data-stu-id="f8fd4-109">Locates and installs the latest Integration Components into the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8fd4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8fd4-110">Syntax</span></span>


```C++
HRESULT InstallIntegrationComponents();
```



## <a name="parameters"></a><span data-ttu-id="f8fd4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8fd4-111">Parameters</span></span>

<span data-ttu-id="f8fd4-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f8fd4-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8fd4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8fd4-113">Return value</span></span>

<span data-ttu-id="f8fd4-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f8fd4-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f8fd4-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="f8fd4-115">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="f8fd4-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8fd4-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8fd4-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f8fd4-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="f8fd4-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8fd4-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="f8fd4-119"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="f8fd4-119"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                       | <span data-ttu-id="f8fd4-120">Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f8fd4-120">The virtual machine must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="f8fd4-121"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="f8fd4-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="f8fd4-122">Der virtuelle Computer wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="f8fd4-122">The virtual machine could not be found.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f8fd4-123"><dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="f8fd4-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="f8fd4-124">Der virtuelle Computer verfügt über kein leeres DVD-Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="f8fd4-124">The virtual machine does not have an empty DVD drive.</span></span><br/>                       |
| <dl> <span data-ttu-id="f8fd4-125"><dt>**VM \_ E-of-Media-Bereitstellung \_ \_ \_ fehl**</dt> geschlagen <dt>0xa0040508</dt></span><span class="sxs-lookup"><span data-stu-id="f8fd4-125"><dt>**VM\_E\_MEDIA\_UNMOUNT\_FAIL**</dt> <dt>0xA0040508</dt></span></span> </dl>                   | <span data-ttu-id="f8fd4-126">Fehler beim Versuch, die Bereitstellung des Mediums auf dem DVD-Laufwerk des virtuellen Computers aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="f8fd4-126">The attempt to unmount the media from the virtual machine DVD drive failed.</span></span><br/> |
| <dl> <span data-ttu-id="f8fd4-127"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f8fd4-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="f8fd4-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f8fd4-128">An unexpected error has occurred.</span></span><br/>                                           |
| <dl> <span data-ttu-id="f8fd4-129"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="f8fd4-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="f8fd4-130">Das System kann die ISO-Datei für die Integrations Komponenten nicht finden.</span><span class="sxs-lookup"><span data-stu-id="f8fd4-130">The system cannot find the ISO file for the Integration Components.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="f8fd4-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8fd4-131">Requirements</span></span>



| <span data-ttu-id="f8fd4-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8fd4-132">Requirement</span></span> | <span data-ttu-id="f8fd4-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f8fd4-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8fd4-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8fd4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f8fd4-135">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8fd4-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f8fd4-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8fd4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f8fd4-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f8fd4-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f8fd4-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f8fd4-138">End of client support</span></span><br/>    | <span data-ttu-id="f8fd4-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f8fd4-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f8fd4-140">Produkt</span><span class="sxs-lookup"><span data-stu-id="f8fd4-140">Product</span></span><br/>                  | <span data-ttu-id="f8fd4-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f8fd4-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f8fd4-142">Header</span><span class="sxs-lookup"><span data-stu-id="f8fd4-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8fd4-143"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8fd4-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f8fd4-144">IID</span><span class="sxs-lookup"><span data-stu-id="f8fd4-144">IID</span></span><br/>                      | <span data-ttu-id="f8fd4-145">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="f8fd4-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f8fd4-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8fd4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8fd4-147">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="f8fd4-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

