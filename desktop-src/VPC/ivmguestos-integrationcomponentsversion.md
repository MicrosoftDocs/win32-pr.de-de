---
title: Ivmguestos integrationcomponentsversion-Eigenschaft (vpccominterfaces. h)
description: Ruft die Version der Integrations Komponenten ab, die im Gast Betriebssystem installiert sind.
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- Integrationcomponentsversion-Eigenschaft virtueller PC
- Integrationcomponentsversion-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, integrationcomponentsversion (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85352614b89ab208377fe44fe3b970c693d60dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740168"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a><span data-ttu-id="16a38-106">Ivmguestos:: integrationcomponentsversion (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="16a38-106">IVMGuestOS::IntegrationComponentsVersion property</span></span>

<span data-ttu-id="16a38-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="16a38-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="16a38-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="16a38-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="16a38-109">Ruft die Version der Integrations Komponenten ab, die im Gast Betriebssystem installiert sind.</span><span class="sxs-lookup"><span data-stu-id="16a38-109">Retrieves the version of the Integration Components installed in the guest operating system.</span></span>

<span data-ttu-id="16a38-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="16a38-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a38-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="16a38-111">Syntax</span></span>


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a><span data-ttu-id="16a38-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="16a38-112">Property value</span></span>

<span data-ttu-id="16a38-113">Die Version.</span><span class="sxs-lookup"><span data-stu-id="16a38-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="16a38-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="16a38-114">Error codes</span></span>



| <span data-ttu-id="16a38-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="16a38-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="16a38-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="16a38-116">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="16a38-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="16a38-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="16a38-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="16a38-118">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="16a38-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="16a38-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="16a38-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="16a38-120">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="16a38-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="16a38-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="16a38-122">Der virtuelle Computer (VM) wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="16a38-122">The virtual machine (VM) could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="16a38-123"><dt>VM \_ E- \_ Ergänzungen \_ nicht in \_ Anspruch</dt> nehmen <dt>0xa0040504</dt></span><span class="sxs-lookup"><span data-stu-id="16a38-123"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="16a38-124">Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert, oder der virtuelle Computer wurde nie gestartet.</span><span class="sxs-lookup"><span data-stu-id="16a38-124">Integration Components are not installed in this VM, or the VM was never started.</span></span><br/> |
| <dl> <span data-ttu-id="16a38-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="16a38-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="16a38-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="16a38-126">An unexpected error has occurred.</span></span><br/>                                                 |



## <a name="requirements"></a><span data-ttu-id="16a38-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16a38-127">Requirements</span></span>



| <span data-ttu-id="16a38-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16a38-128">Requirement</span></span> | <span data-ttu-id="16a38-129">Wert</span><span class="sxs-lookup"><span data-stu-id="16a38-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="16a38-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16a38-130">Minimum supported client</span></span><br/> | <span data-ttu-id="16a38-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16a38-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="16a38-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16a38-132">Minimum supported server</span></span><br/> | <span data-ttu-id="16a38-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="16a38-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="16a38-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="16a38-134">End of client support</span></span><br/>    | <span data-ttu-id="16a38-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="16a38-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="16a38-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="16a38-136">Product</span></span><br/>                  | <span data-ttu-id="16a38-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="16a38-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="16a38-138">Header</span><span class="sxs-lookup"><span data-stu-id="16a38-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="16a38-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="16a38-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="16a38-140">IID</span><span class="sxs-lookup"><span data-stu-id="16a38-140">IID</span></span><br/>                      | <span data-ttu-id="16a38-141">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="16a38-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="16a38-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16a38-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a38-143">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="16a38-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

