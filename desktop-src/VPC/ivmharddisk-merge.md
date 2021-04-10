---
title: Ivmharddisk-Merge-Methode (vpccominterfaces. h)
description: Führt eine differenzierende virtuelle Festplatte mit dem übergeordneten Datenträger Image zusammen.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Merge-Methode Virtual PC
- Merge-Methode Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, Merge-Methode
topic_type:
- apiref
api_name:
- IVMHardDisk.Merge
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5e4b32cb1df2f754463cee7f8275b00f86513b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956662"
---
# <a name="ivmharddiskmerge-method"></a><span data-ttu-id="96e35-106">Ivmharddisk:: Merge-Methode</span><span class="sxs-lookup"><span data-stu-id="96e35-106">IVMHardDisk::Merge method</span></span>

<span data-ttu-id="96e35-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="96e35-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="96e35-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="96e35-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="96e35-109">Führt eine differenzierende virtuelle Festplatte mit dem übergeordneten Datenträger Image zusammen.</span><span class="sxs-lookup"><span data-stu-id="96e35-109">Merges a differencing virtual hard disk with its parent disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e35-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="96e35-110">Syntax</span></span>


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="96e35-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="96e35-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96e35-112">*mergetask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="96e35-112">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="96e35-113">Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss des Zusammenführungs Vorgangs zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="96e35-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96e35-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96e35-114">Return value</span></span>

<span data-ttu-id="96e35-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="96e35-115">This method can return one of these values.</span></span>



| <span data-ttu-id="96e35-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="96e35-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="96e35-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96e35-117">Description</span></span>                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96e35-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="96e35-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="96e35-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="96e35-119">The operation was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="96e35-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="96e35-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="96e35-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="96e35-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="96e35-122"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Freigabe \_ Verletzung)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="96e35-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="96e35-123">Das von diesem [**ivmharddisk**](ivmharddisk.md) -Objekt referenzierte virtuelle Festplatten Abbild wird verwendet, oder das übergeordnete Element dieses virtuellen Festplatten Abbilds wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="96e35-123">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use or the parent of this virtual hard disk image is in use.</span></span> <span data-ttu-id="96e35-124">Oder die Festplatten Abbilder können Teil eines gespeicherten Zustands sein.</span><span class="sxs-lookup"><span data-stu-id="96e35-124">Or, these hard disk images could be part of a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="96e35-125"><dt>**VM \_ E \_ falscher \_ HD \_ - \_ Abbildtyp**</dt> <dt>0xa004067b</dt></span><span class="sxs-lookup"><span data-stu-id="96e35-125"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="96e35-126">Das Image der virtuellen Festplatte, auf das dieses [**ivmharddisk**](ivmharddisk.md) -Objekt verweist, muss ein differenzierender Datenträger Abbild sein.</span><span class="sxs-lookup"><span data-stu-id="96e35-126">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a differencing disk image.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="96e35-127"><dt>**VM \_ E \_ - \_ Datei \_**</dt> schreibgeschützt <dt>0xa004067a</dt></span><span class="sxs-lookup"><span data-stu-id="96e35-127"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="96e35-128">Das übergeordnete Element des virtuellen Festplatten Abbilds, auf das von diesem [**ivmharddisk**](ivmharddisk.md) -Objekt verwiesen wird, ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="96e35-128">The parent of virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="96e35-129"><dt>**VM \_ E über \_ geordneter \_ Pfad \_ nicht \_ gefunden**</dt> <dt>0xa0040677</dt></span><span class="sxs-lookup"><span data-stu-id="96e35-129"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="96e35-130">Das übergeordnete Element der virtuellen Festplatte, auf die von diesem [**ivmharddisk**](ivmharddisk.md) -Objekt verwiesen wird, ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="96e35-130">The parent of the virtual hard disk referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not exist.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="96e35-131"><dt>**VM \_ E \_ App \_ \_ herunter**</dt> fahren <dt>0xa0040209</dt></span><span class="sxs-lookup"><span data-stu-id="96e35-131"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="96e35-132">Das virtuelle Festplatten Abbild kann nicht zusammengeführt werden, da die Anwendung heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="96e35-132">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="96e35-133"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="96e35-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="96e35-134">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="96e35-134">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="96e35-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96e35-135">Requirements</span></span>



| <span data-ttu-id="96e35-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96e35-136">Requirement</span></span> | <span data-ttu-id="96e35-137">Wert</span><span class="sxs-lookup"><span data-stu-id="96e35-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96e35-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96e35-138">Minimum supported client</span></span><br/> | <span data-ttu-id="96e35-139">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96e35-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96e35-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96e35-140">Minimum supported server</span></span><br/> | <span data-ttu-id="96e35-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="96e35-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="96e35-142">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="96e35-142">End of client support</span></span><br/>    | <span data-ttu-id="96e35-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="96e35-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="96e35-144">Produkt</span><span class="sxs-lookup"><span data-stu-id="96e35-144">Product</span></span><br/>                  | <span data-ttu-id="96e35-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="96e35-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="96e35-146">Header</span><span class="sxs-lookup"><span data-stu-id="96e35-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="96e35-147"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="96e35-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="96e35-148">IID</span><span class="sxs-lookup"><span data-stu-id="96e35-148">IID</span></span><br/>                      | <span data-ttu-id="96e35-149">IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.</span><span class="sxs-lookup"><span data-stu-id="96e35-149">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="96e35-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96e35-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e35-151">**Ivmharddisk**</span><span class="sxs-lookup"><span data-stu-id="96e35-151">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

