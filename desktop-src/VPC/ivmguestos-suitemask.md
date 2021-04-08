---
title: Ivmguestos-suitemask-Eigenschaft (vpccominterfaces. h)
description: Ruft den suitemask des Gast Betriebssystems ab, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- Suitemask-Eigenschaft virtueller PC
- Suitemask-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, suitemask-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 348384dd729c5c7e63a45fcb8b3f05d0189a7fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743592"
---
# <a name="ivmguestossuitemask-property"></a><span data-ttu-id="6701f-106">Ivmguestos:: suitemask-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6701f-106">IVMGuestOS::SuiteMask property</span></span>

<span data-ttu-id="6701f-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6701f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6701f-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6701f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6701f-109">Ruft den suitemask des Gast Betriebssystems ab, das auf dem virtuellen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6701f-109">Retrieves the SuiteMask of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="6701f-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6701f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6701f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6701f-111">Syntax</span></span>


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a><span data-ttu-id="6701f-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6701f-112">Property value</span></span>

<span data-ttu-id="6701f-113">Die Sammlungs Maske.</span><span class="sxs-lookup"><span data-stu-id="6701f-113">The suite mask.</span></span> <span data-ttu-id="6701f-114">Die folgenden Zeichen folgen Werte werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6701f-114">The following string values are supported.</span></span>



| <span data-ttu-id="6701f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6701f-115">Value</span></span>                                                                                   | <span data-ttu-id="6701f-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6701f-116">Meaning</span></span>                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6701f-117"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-117"><dt>"0x00000004"</dt></span></span> </dl> | <span data-ttu-id="6701f-118">Microsoft BackOffice-Komponenten werden installiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-118">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="6701f-119"><dt>"0x00000400"</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-119"><dt>"0x00000400"</dt></span></span> </dl> | <span data-ttu-id="6701f-120">Windows Server 2003, Web Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-120">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="6701f-121"><dt>"0x00004000"</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-121"><dt>"0x00004000"</dt></span></span> </dl> | <span data-ttu-id="6701f-122">Windows Server 2003, Compute Cluster Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-122">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="6701f-123"><dt>"0x00000080"</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-123"><dt>"0x00000080"</dt></span></span> </dl> | <span data-ttu-id="6701f-124">Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition oder Windows 2000 Datacenter Server ist installiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-124">Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/> |
| <dl> <span data-ttu-id="6701f-125"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-125"><dt>"0x00000002"</dt></span></span> </dl> | <span data-ttu-id="6701f-126">Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition oder Windows 2000 Advanced Server ist installiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-126">Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span><br/>   |
| <dl> <span data-ttu-id="6701f-127"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-127"><dt>"0x00000040"</dt></span></span> </dl> | <span data-ttu-id="6701f-128">Windows XP Embedded ist installiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-128">Windows XP Embedded is installed.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="6701f-129"><dt>"0x00000200"</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-129"><dt>"0x00000200"</dt></span></span> </dl> | <span data-ttu-id="6701f-130">Windows Vista Home Premium, Windows Vista Home Basic oder Windows XP Home Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-130">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="6701f-131"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-131"><dt>"0x00000100"</dt></span></span> </dl> | <span data-ttu-id="6701f-132">Remotedesktop wird unterstützt, es wird jedoch nur eine interaktive Sitzung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6701f-132">Remote Desktop is supported, but only one interactive session is supported.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="6701f-133"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-133"><dt>"0x00000001"</dt></span></span> </dl> | <span data-ttu-id="6701f-134">Microsoft Small Business Server wurde auf dem System installiert, kann jedoch auf eine andere Version von Windows aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6701f-134">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span><br/>                                 |
| <dl> <span data-ttu-id="6701f-135"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-135"><dt>"0x00000020"</dt></span></span> </dl> | <span data-ttu-id="6701f-136">Microsoft Small Business Server wird mit der eingeschränkten Client Lizenz in Kraft installiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-136">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="6701f-137"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-137"><dt>"0x00002000"</dt></span></span> </dl> | <span data-ttu-id="6701f-138">Windows Storage Server 2003 R2 oder Windows Storage Server 2003 ist installiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-138">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="6701f-139"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-139"><dt>"0x00000010"</dt></span></span> </dl> | <span data-ttu-id="6701f-140">Remotedesktopdienste ist installiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-140">Remote Desktop Services is installed.</span></span> <span data-ttu-id="6701f-141">Dieser Wert ist immer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6701f-141">This value is always set.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="6701f-142"><dt>"0x00008000"</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-142"><dt>"0x00008000"</dt></span></span> </dl> | <span data-ttu-id="6701f-143">Windows Home Server ist installiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-143">Windows Home Server is installed.</span></span><br/>                                                                                                                           |



 

## <a name="error-codes"></a><span data-ttu-id="6701f-144">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6701f-144">Error codes</span></span>



| <span data-ttu-id="6701f-145">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="6701f-145">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="6701f-146">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6701f-146">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6701f-147"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-147"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="6701f-148">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6701f-148">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="6701f-149"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-149"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="6701f-150">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="6701f-150">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="6701f-151"><dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="6701f-151"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="6701f-152">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6701f-152">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="6701f-153"><dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="6701f-153"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="6701f-154">Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-154">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="6701f-155"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-155"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="6701f-156">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6701f-156">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="6701f-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6701f-157">Requirements</span></span>



| <span data-ttu-id="6701f-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6701f-158">Requirement</span></span> | <span data-ttu-id="6701f-159">Wert</span><span class="sxs-lookup"><span data-stu-id="6701f-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6701f-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6701f-160">Minimum supported client</span></span><br/> | <span data-ttu-id="6701f-161">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6701f-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6701f-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6701f-162">Minimum supported server</span></span><br/> | <span data-ttu-id="6701f-163">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6701f-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6701f-164">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6701f-164">End of client support</span></span><br/>    | <span data-ttu-id="6701f-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6701f-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6701f-166">Produkt</span><span class="sxs-lookup"><span data-stu-id="6701f-166">Product</span></span><br/>                  | <span data-ttu-id="6701f-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6701f-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6701f-168">Header</span><span class="sxs-lookup"><span data-stu-id="6701f-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="6701f-169"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6701f-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6701f-170">IID</span><span class="sxs-lookup"><span data-stu-id="6701f-170">IID</span></span><br/>                      | <span data-ttu-id="6701f-171">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="6701f-171">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6701f-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6701f-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6701f-173">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="6701f-173">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

