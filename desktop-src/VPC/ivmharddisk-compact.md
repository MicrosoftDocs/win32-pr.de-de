---
title: Ivmharddisk Compact-Methode (vpccominterfaces. h)
description: Komprimiert eine dynamisch erweiterbare virtuelle Festplatten Abbild.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Compact-Methode Virtual PC
- Compact-Methode Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, Compact-Methode
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b28b47709fdf956b679a4f16c50adde4a1b335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743248"
---
# <a name="ivmharddiskcompact-method"></a><span data-ttu-id="f73ec-106">Ivmharddisk:: Compact-Methode</span><span class="sxs-lookup"><span data-stu-id="f73ec-106">IVMHardDisk::Compact method</span></span>

<span data-ttu-id="f73ec-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f73ec-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f73ec-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f73ec-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f73ec-109">Komprimiert eine dynamisch erweiterbare virtuelle Festplatten Abbild.</span><span class="sxs-lookup"><span data-stu-id="f73ec-109">Compacts a dynamically expanding virtual hard disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="f73ec-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f73ec-110">Syntax</span></span>


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a><span data-ttu-id="f73ec-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f73ec-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f73ec-112">*kompakttask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f73ec-112">*compactTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f73ec-113">Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss des Komprimierungsprozesses zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="f73ec-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion the compaction process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f73ec-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f73ec-114">Return value</span></span>

<span data-ttu-id="f73ec-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f73ec-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f73ec-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="f73ec-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="f73ec-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f73ec-117">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f73ec-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f73ec-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="f73ec-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f73ec-119">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="f73ec-120"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f73ec-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="f73ec-121">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f73ec-121">An unexpected error has occurred.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="f73ec-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f73ec-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="f73ec-123">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="f73ec-123">The parameter is **NULL**.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="f73ec-124"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Freigabe \_ Verletzung)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="f73ec-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="f73ec-125">Das von diesem [**ivmharddisk**](ivmharddisk.md) -Objekt referenzierte virtuelle Festplatten Abbild wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="f73ec-125">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use.</span></span><br/>                                  |
| <dl> <span data-ttu-id="f73ec-126"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ \_**</dt> Datenträger voll) <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="f73ec-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="f73ec-127">Auf dem Host Volume ist nicht genügend Speicherplatz vorhanden, um eine temporäre Datei zu erstellen, die für die Komprimierung dieses virtuellen Festplatten Abbilds erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f73ec-127">The host volume does not have enough space to create a temporary file needed for the compaction of this virtual hard disk image.</span></span><br/>     |
| <dl> <span data-ttu-id="f73ec-128"><dt>**VM \_ E \_ App \_ \_ herunter**</dt> fahren <dt>0xa0040209</dt></span><span class="sxs-lookup"><span data-stu-id="f73ec-128"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="f73ec-129">Das Image der virtuellen Festplatte kann nicht komprimiert werden, da die Anwendung heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="f73ec-129">The virtual hard disk image cannot be compacted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="f73ec-130"><dt>**VM \_ E \_ - \_ Datei \_**</dt> schreibgeschützt <dt>0xa004067a</dt></span><span class="sxs-lookup"><span data-stu-id="f73ec-130"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="f73ec-131">Das von diesem [**ivmharddisk**](ivmharddisk.md) -Objekt referenzierte virtuelle Festplatten Abbild ist als schreibgeschützt gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="f73ec-131">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                     |
| <dl> <span data-ttu-id="f73ec-132"><dt>**VM \_ E \_ falscher \_ HD \_ - \_ Abbildtyp**</dt> <dt>0xa004067b</dt></span><span class="sxs-lookup"><span data-stu-id="f73ec-132"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="f73ec-133">Das von diesem [**ivmharddisk**](ivmharddisk.md) -Objekt referenzierte virtuelle Festplatten Abbild muss ein **vmdisktypedynamic** -Bildtyp sein.</span><span class="sxs-lookup"><span data-stu-id="f73ec-133">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a **vmDiskTypeDynamic** image type.</span></span><br/> |
| <dl> <span data-ttu-id="f73ec-134"><dt>**VM \_ E \_ ungültige \_ HD- \_ Datei**</dt> <dt>0xa0040682</dt></span><span class="sxs-lookup"><span data-stu-id="f73ec-134"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="f73ec-135">Das Image der virtuellen Festplatte, auf das dieses [**ivmharddisk**](ivmharddisk.md) -Objekt verweist, scheint kein gültiges Image zu sein.</span><span class="sxs-lookup"><span data-stu-id="f73ec-135">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="f73ec-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f73ec-136">Remarks</span></span>

<span data-ttu-id="f73ec-137">Zum Komprimieren eines dynamisch erweiterbaren Festplatten Abbilds sollte der freie Speicherplatz auf dem Datenträger Abbild zuerst nulfiert werden.</span><span class="sxs-lookup"><span data-stu-id="f73ec-137">To compact a dynamically expanding hard disk image, free space on the disk image should first be zeroed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f73ec-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f73ec-138">Requirements</span></span>



| <span data-ttu-id="f73ec-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f73ec-139">Requirement</span></span> | <span data-ttu-id="f73ec-140">Wert</span><span class="sxs-lookup"><span data-stu-id="f73ec-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f73ec-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f73ec-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f73ec-142">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f73ec-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f73ec-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f73ec-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f73ec-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f73ec-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f73ec-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f73ec-145">End of client support</span></span><br/>    | <span data-ttu-id="f73ec-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f73ec-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f73ec-147">Produkt</span><span class="sxs-lookup"><span data-stu-id="f73ec-147">Product</span></span><br/>                  | <span data-ttu-id="f73ec-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f73ec-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f73ec-149">Header</span><span class="sxs-lookup"><span data-stu-id="f73ec-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="f73ec-150"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f73ec-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f73ec-151">IID</span><span class="sxs-lookup"><span data-stu-id="f73ec-151">IID</span></span><br/>                      | <span data-ttu-id="f73ec-152">IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.</span><span class="sxs-lookup"><span data-stu-id="f73ec-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f73ec-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f73ec-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f73ec-154">**Ivmharddisk**</span><span class="sxs-lookup"><span data-stu-id="f73ec-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

