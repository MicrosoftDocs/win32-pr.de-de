---
title: Übergeordnete ivmharddisk-Eigenschaft (vpccominterfaces. h)
description: Übergeordnetes Element der differenzierenden virtuellen Festplatte.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Virtueller PC der übergeordneten Eigenschaft
- Übergeordnete Eigenschaft Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, Parent-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949385"
---
# <a name="ivmharddiskparent-property"></a><span data-ttu-id="36293-106">Ivmharddisk::P Arent-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="36293-106">IVMHardDisk::Parent property</span></span>

<span data-ttu-id="36293-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="36293-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="36293-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="36293-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="36293-109">Ruft das übergeordnete Element der differenzierenden virtuellen Festplatte ab und legt es fest.</span><span class="sxs-lookup"><span data-stu-id="36293-109">Retrieves and sets the parent of the differencing virtual hard disk.</span></span>

<span data-ttu-id="36293-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="36293-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="36293-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="36293-111">Syntax</span></span>


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a><span data-ttu-id="36293-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="36293-112">Property value</span></span>

<span data-ttu-id="36293-113">Legt das [**ivmharddisk**](ivmharddisk.md) -Objekt fest, das dem übergeordneten Festplatten Abbild zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="36293-113">Sets the [**IVMHardDisk**](ivmharddisk.md) object associated with the parent hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="36293-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="36293-114">Error codes</span></span>



| <span data-ttu-id="36293-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="36293-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="36293-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="36293-116">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36293-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="36293-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="36293-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="36293-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="36293-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="36293-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="36293-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="36293-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="36293-121"><dt>S \_ Falsch</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="36293-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="36293-122">Dabei handelt es sich nicht um eine differenzierende Festplatte, daher hat Sie kein übergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="36293-122">This is not a differencing hard disk, so it has no parent.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="36293-123"><dt>HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="36293-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="36293-124">Das System konnte die übergeordnete virtuelle Festplatten Datei nicht finden.</span><span class="sxs-lookup"><span data-stu-id="36293-124">The system could not find the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="36293-125"><dt>HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="36293-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="36293-126">Das System konnte den Pfad zur übergeordneten virtuellen Festplatten Datei nicht finden.</span><span class="sxs-lookup"><span data-stu-id="36293-126">The system could not find the path to the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="36293-127"><dt>VM \_ E \_ HD- \_ Abbild \_ Öffnen \_ fehlschlagen</dt> <dt>0xa004067c</dt></span><span class="sxs-lookup"><span data-stu-id="36293-127"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="36293-128">Fehler beim Öffnen der aktuellen Festplatten Abbild Datei.</span><span class="sxs-lookup"><span data-stu-id="36293-128">An error occurred while attempting to open the current hard disk image file.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="36293-129"><dt>VM \_ E \_ HD- \_ Abbild \_ Zugriff</dt> <dt>0xa0040681</dt></span><span class="sxs-lookup"><span data-stu-id="36293-129"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="36293-130">Fehler beim Zugriff auf die aktuelle Festplatten Abbild Datei.</span><span class="sxs-lookup"><span data-stu-id="36293-130">An error occurred while attempting to access the current hard disk image file.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="36293-131"><dt>VM \_ E \_ - \_ \_ ID \_ </dt> des übergeordneten untergeordneten Elements <dt>0xa0040685</dt></span><span class="sxs-lookup"><span data-stu-id="36293-131"><dt>VM\_E\_PARENT\_CHILD\_ID\_MISMATCH</dt> <dt>0xA0040685</dt></span></span> </dl>            | <span data-ttu-id="36293-132">Das virtuelle Festplatten Abbild, das vom übergeordneten Parameter gefunden wird, hat nicht die gleiche ID wie das unter *geordnete* Datenträger Image.</span><span class="sxs-lookup"><span data-stu-id="36293-132">The virtual hard disk image located by the *parent* parameter does not have the same ID as the child disk image.</span></span> <span data-ttu-id="36293-133">Stellen Sie sicher, dass das übergeordnete virtuelle Festplatten Image, das vom über *geordneten* Parameter gefunden wird, dem Image entspricht, das zum Erstellen des differenzierenden virtuellen Festplatten Abbilds verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="36293-133">Make sure the parent virtual hard disk image located by the *parent* parameter is the same image used to create the differencing virtual hard disk image.</span></span><br/> |
| <dl> <span data-ttu-id="36293-134"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="36293-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="36293-135">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="36293-135">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="36293-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36293-136">Remarks</span></span>

<span data-ttu-id="36293-137">Diese Eigenschaft ist nur mit differenzierenden Festplatten Abbildern gültig.</span><span class="sxs-lookup"><span data-stu-id="36293-137">This property is only valid with differencing hard disk images.</span></span>

## <a name="requirements"></a><span data-ttu-id="36293-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36293-138">Requirements</span></span>



| <span data-ttu-id="36293-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36293-139">Requirement</span></span> | <span data-ttu-id="36293-140">Wert</span><span class="sxs-lookup"><span data-stu-id="36293-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="36293-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36293-141">Minimum supported client</span></span><br/> | <span data-ttu-id="36293-142">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36293-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36293-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36293-143">Minimum supported server</span></span><br/> | <span data-ttu-id="36293-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="36293-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="36293-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="36293-145">End of client support</span></span><br/>    | <span data-ttu-id="36293-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="36293-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="36293-147">Produkt</span><span class="sxs-lookup"><span data-stu-id="36293-147">Product</span></span><br/>                  | <span data-ttu-id="36293-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="36293-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="36293-149">Header</span><span class="sxs-lookup"><span data-stu-id="36293-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="36293-150"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="36293-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="36293-151">IID</span><span class="sxs-lookup"><span data-stu-id="36293-151">IID</span></span><br/>                      | <span data-ttu-id="36293-152">IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.</span><span class="sxs-lookup"><span data-stu-id="36293-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="36293-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36293-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36293-154">**Ivmharddisk**</span><span class="sxs-lookup"><span data-stu-id="36293-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

