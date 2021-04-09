---
title: Methode ' ivmvirtualmachine Turnoff ' (vpccominterfaces. h)
description: Der virtuelle Computer wird heruntergefahren.
ms.assetid: 4ea00314-8f1e-47d9-bbb8-b5791af1fb86
keywords:
- Turnoff-Methode Virtual PC
- Turnoff-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Turnoff-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.TurnOff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27a5b14955fcc8a060c49932e3fa4f238497a567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040866"
---
# <a name="ivmvirtualmachineturnoff-method"></a><span data-ttu-id="1e6b0-106">Ivmvirtualmachine:: Turnoff-Methode</span><span class="sxs-lookup"><span data-stu-id="1e6b0-106">IVMVirtualMachine::TurnOff method</span></span>

<span data-ttu-id="1e6b0-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1e6b0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1e6b0-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1e6b0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1e6b0-109">Der virtuelle Computer wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="1e6b0-109">Turns off the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e6b0-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e6b0-110">Syntax</span></span>


```C++
HRESULT TurnOff(
  [out, retval] IVMTask **turnOffTask
);
```



## <a name="parameters"></a><span data-ttu-id="1e6b0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e6b0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e6b0-112">*turnofftask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1e6b0-112">*turnOffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6b0-113">Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss Status der Umstellungs Sequenz der virtuellen Maschine zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="1e6b0-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's turnoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e6b0-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e6b0-114">Return value</span></span>

<span data-ttu-id="1e6b0-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1e6b0-115">This method can return one of these values.</span></span>



| <span data-ttu-id="1e6b0-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="1e6b0-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="1e6b0-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e6b0-117">Description</span></span>                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e6b0-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1e6b0-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="1e6b0-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e6b0-119">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="1e6b0-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1e6b0-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="1e6b0-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="1e6b0-121">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="1e6b0-122"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="1e6b0-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="1e6b0-123">Der Aufrufer muss über Berechtigungen zum Ausführen des Zugriffs verfügen, um diesen virtuellen Computer zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1e6b0-123">The caller must have execute access permissions to turn off this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="1e6b0-124"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="1e6b0-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="1e6b0-125">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e6b0-125">The virtual machine is not running.</span></span><br/>                                               |
| <dl> <span data-ttu-id="1e6b0-126"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="1e6b0-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="1e6b0-127">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="1e6b0-127">The configuration is unknown.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="1e6b0-128"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1e6b0-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="1e6b0-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1e6b0-129">An unexpected error has occurred.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="1e6b0-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e6b0-130">Remarks</span></span>

<span data-ttu-id="1e6b0-131">Mit dieser Methode wird der virtuelle Computer auf die gleiche Weise ausgeschaltet wie das Ausschalten auf einem physischen Computer.</span><span class="sxs-lookup"><span data-stu-id="1e6b0-131">This method turns off the virtual machine in the same manner as turning the power off on a physical machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e6b0-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e6b0-132">Requirements</span></span>



| <span data-ttu-id="1e6b0-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e6b0-133">Requirement</span></span> | <span data-ttu-id="1e6b0-134">Wert</span><span class="sxs-lookup"><span data-stu-id="1e6b0-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e6b0-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e6b0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1e6b0-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e6b0-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e6b0-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e6b0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1e6b0-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1e6b0-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1e6b0-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1e6b0-139">End of client support</span></span><br/>    | <span data-ttu-id="1e6b0-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e6b0-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1e6b0-141">Produkt</span><span class="sxs-lookup"><span data-stu-id="1e6b0-141">Product</span></span><br/>                  | <span data-ttu-id="1e6b0-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1e6b0-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1e6b0-143">Header</span><span class="sxs-lookup"><span data-stu-id="1e6b0-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e6b0-144"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e6b0-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1e6b0-145">IID</span><span class="sxs-lookup"><span data-stu-id="1e6b0-145">IID</span></span><br/>                      | <span data-ttu-id="1e6b0-146">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="1e6b0-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="1e6b0-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e6b0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e6b0-148">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="1e6b0-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

