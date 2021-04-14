---
title: Ivmvirtualmachine removeharddiskconnection-Methode (vpccominterfaces. h)
description: Entfernt die angegebene Festplatten Verbindung von der virtuellen Maschine.
ms.assetid: d31f2442-aae4-4987-9188-fd32778604a1
keywords:
- Removeharddiskconnection-Methode Virtual PC
- Removeharddiskconnection-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, removeharddiskconnection-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62a9bbf8b3aac0dd35c8390343c20a1b67b59101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391954"
---
# <a name="ivmvirtualmachineremoveharddiskconnection-method"></a><span data-ttu-id="99a7d-106">Ivmvirtualmachine:: removeharddiskconnection-Methode</span><span class="sxs-lookup"><span data-stu-id="99a7d-106">IVMVirtualMachine::RemoveHardDiskConnection method</span></span>

<span data-ttu-id="99a7d-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="99a7d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="99a7d-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="99a7d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="99a7d-109">Entfernt die angegebene Festplatten Verbindung von der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="99a7d-109">Removes the specified hard disk connection from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="99a7d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="99a7d-110">Syntax</span></span>


```C++
HRESULT RemoveHardDiskConnection(
  [in] IVMHardDiskConnection *hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="99a7d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="99a7d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99a7d-112">*harddiskconnection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99a7d-112">*hardDiskConnection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99a7d-113">Ein [**ivmharddiskconnection**](ivmharddiskconnection.md) -Objekt, das die zu entfernende Festplatten Verbindung darstellt.</span><span class="sxs-lookup"><span data-stu-id="99a7d-113">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object that represents the hard disk connection to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99a7d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99a7d-114">Return value</span></span>

<span data-ttu-id="99a7d-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="99a7d-115">This method can return one of these values.</span></span>



| <span data-ttu-id="99a7d-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="99a7d-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="99a7d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99a7d-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="99a7d-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="99a7d-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="99a7d-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="99a7d-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="99a7d-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="99a7d-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="99a7d-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="99a7d-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="99a7d-122"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="99a7d-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="99a7d-123">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="99a7d-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="99a7d-124"><dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert</span><span class="sxs-lookup"><span data-stu-id="99a7d-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="99a7d-125">Der virtuelle Computer befindet sich im Zustand "wird ausgeführt" oder "gespeichert".</span><span class="sxs-lookup"><span data-stu-id="99a7d-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="99a7d-126"><dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="99a7d-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="99a7d-127">Das angegebene Laufwerk ist nicht mit diesem Busstandort verbunden.</span><span class="sxs-lookup"><span data-stu-id="99a7d-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="99a7d-128"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="99a7d-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="99a7d-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="99a7d-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="99a7d-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99a7d-130">Remarks</span></span>

<span data-ttu-id="99a7d-131">Sie können eine vorhandene Festplatten Verbindung nur von einem beendeten virtuellen Computer entfernen.</span><span class="sxs-lookup"><span data-stu-id="99a7d-131">You can only remove an existing hard disk connection from a stopped virtual machine.</span></span> <span data-ttu-id="99a7d-132">Eine Liste der Verbindungen, die derzeit an den virtuellen Computer angefügt sind, wird durch Aufzählen der [**harddiskconnections**](ivmvirtualmachine-harddiskconnections.md) -Eigenschaft abgerufen.</span><span class="sxs-lookup"><span data-stu-id="99a7d-132">A list of connections currently attached to the virtual machine is obtained by enumerating the [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="99a7d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99a7d-133">Requirements</span></span>



| <span data-ttu-id="99a7d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99a7d-134">Requirement</span></span> | <span data-ttu-id="99a7d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="99a7d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="99a7d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99a7d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="99a7d-137">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99a7d-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="99a7d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99a7d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="99a7d-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="99a7d-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="99a7d-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="99a7d-140">End of client support</span></span><br/>    | <span data-ttu-id="99a7d-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="99a7d-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="99a7d-142">Produkt</span><span class="sxs-lookup"><span data-stu-id="99a7d-142">Product</span></span><br/>                  | <span data-ttu-id="99a7d-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="99a7d-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="99a7d-144">Header</span><span class="sxs-lookup"><span data-stu-id="99a7d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="99a7d-145"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="99a7d-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="99a7d-146">IID</span><span class="sxs-lookup"><span data-stu-id="99a7d-146">IID</span></span><br/>                      | <span data-ttu-id="99a7d-147">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="99a7d-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="99a7d-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99a7d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99a7d-149">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="99a7d-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

