---
title: Ivmfloppydrive attachimage-Methode (vpccominterfaces. h)
description: Fügt ein Disketten Medienbild auf dem Host an das Diskettenlaufwerk der virtuellen Maschine an.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- Attachimage-Methode Virtual PC
- Attachimage-Methode Virtual PC, ivmfloppydrive-Schnittstelle
- Ivmfloppydrive Interface Virtual PC, attachimage-Methode
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8821a6d9bdae979f45477d1fe2ba666eb6da10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949729"
---
# <a name="ivmfloppydriveattachimage-method"></a><span data-ttu-id="b49a4-106">Ivmfloppydrive:: attachimage-Methode</span><span class="sxs-lookup"><span data-stu-id="b49a4-106">IVMFloppyDrive::AttachImage method</span></span>

<span data-ttu-id="b49a4-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b49a4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b49a4-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b49a4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b49a4-109">Fügt ein Disketten Medienbild auf dem Host an das Diskettenlaufwerk der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="b49a4-109">Attaches a floppy media image on the host to the floppy drive of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b49a4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b49a4-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a><span data-ttu-id="b49a4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b49a4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b49a4-112">*mediaimagepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b49a4-112">*mediaImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b49a4-113">Der vollständige Pfad zu dem Disketten Medienbild, das angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b49a4-113">The full path to the floppy media image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b49a4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b49a4-114">Return value</span></span>

<span data-ttu-id="b49a4-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b49a4-115">This method can return one of these values.</span></span>



| <span data-ttu-id="b49a4-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="b49a4-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="b49a4-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b49a4-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b49a4-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b49a4-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="b49a4-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b49a4-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="b49a4-120"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b49a4-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="b49a4-121">Der *mediaimagepath* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b49a4-121">The *mediaImagePath* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b49a4-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b49a4-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="b49a4-123">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b49a4-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="b49a4-124"><dt>**HRESULT \_ Von \_ Win32 (Error \_ outo-Memory)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="b49a4-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="b49a4-125">Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b49a4-125">There is not enough memory available to complete this request.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="b49a4-126"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="b49a4-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="b49a4-127">Der durch den Parameter " *mediaimagepath* " angegebene Pfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="b49a4-127">The path specified by the *mediaImagePath* parameter is too long.</span></span> <span data-ttu-id="b49a4-128">Der Pfad muss kleiner als der **Maximale \_ Pfad** (260) sein.</span><span class="sxs-lookup"><span data-stu-id="b49a4-128">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="b49a4-129"><dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="b49a4-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="b49a4-130">Der *mediaimagepath* -Parameter enthält ein ungültiges Zeichen (eines der " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="b49a4-130">The *mediaImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="b49a4-131"><dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="b49a4-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="b49a4-132">Der *mediaimagepath* -Parameter gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="b49a4-132">The *mediaImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="b49a4-133">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b49a4-133">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="b49a4-134"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="b49a4-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="b49a4-135">Die Konfiguration für diesen virtuellen Computer ist ungültig oder wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="b49a4-135">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="b49a4-136"><dt>**VM \_ E \_ - \_ Abbild Erfassung \_ fehlschlagen**</dt> <dt>0xa00400650</dt></span><span class="sxs-lookup"><span data-stu-id="b49a4-136"><dt>**VM\_E\_IMAGE\_CAPTURE\_FAIL**</dt> <dt>0xA00400650</dt></span></span> </dl>                  | <span data-ttu-id="b49a4-137">Die angegebene Bilddatei konnte nicht aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b49a4-137">The image file specified could not be captured.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="b49a4-138"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b49a4-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="b49a4-139">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b49a4-139">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="b49a4-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b49a4-140">Requirements</span></span>



| <span data-ttu-id="b49a4-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b49a4-141">Requirement</span></span> | <span data-ttu-id="b49a4-142">Wert</span><span class="sxs-lookup"><span data-stu-id="b49a4-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b49a4-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b49a4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b49a4-144">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b49a4-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b49a4-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b49a4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b49a4-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b49a4-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b49a4-147">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b49a4-147">End of client support</span></span><br/>    | <span data-ttu-id="b49a4-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b49a4-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b49a4-149">Produkt</span><span class="sxs-lookup"><span data-stu-id="b49a4-149">Product</span></span><br/>                  | <span data-ttu-id="b49a4-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b49a4-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b49a4-151">Header</span><span class="sxs-lookup"><span data-stu-id="b49a4-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="b49a4-152"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b49a4-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b49a4-153">IID</span><span class="sxs-lookup"><span data-stu-id="b49a4-153">IID</span></span><br/>                      | <span data-ttu-id="b49a4-154">IID \_ ivmfloppydrive ist als 661abee6-112a-4ed9-BABF -3c874969s10e definiert.</span><span class="sxs-lookup"><span data-stu-id="b49a4-154">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b49a4-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b49a4-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b49a4-156">**Ivmfloppydrive**</span><span class="sxs-lookup"><span data-stu-id="b49a4-156">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

