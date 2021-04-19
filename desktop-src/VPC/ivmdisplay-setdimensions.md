---
title: Ivmdisplay setdimensions-Methode (vpccominterfaces. h)
description: Legt die Höhe und Breite der VM-Anzeige in Pixel fest.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Setdimensions-Methode Virtual PC
- Setdimensions-Methode Virtual PC, ivmdisplay-Schnittstelle
- Ivmdisplay Interface Virtual PC, setdimensions-Methode
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4730d73e06074714c8e6ed31fda992259d5c19ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343055"
---
# <a name="ivmdisplaysetdimensions-method"></a><span data-ttu-id="8c42e-106">Ivmdisplay:: setdimensions-Methode</span><span class="sxs-lookup"><span data-stu-id="8c42e-106">IVMDisplay::SetDimensions method</span></span>

<span data-ttu-id="8c42e-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8c42e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8c42e-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8c42e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8c42e-109">Legt die Höhe und Breite der Anzeige des virtuellen Computers (VM) in Pixel fest.</span><span class="sxs-lookup"><span data-stu-id="8c42e-109">Sets the height and width of the virtual machine's (VM's) display, in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c42e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c42e-110">Syntax</span></span>


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a><span data-ttu-id="8c42e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c42e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c42e-112">*Display Pixel Width* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c42e-112">*displayPixelWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c42e-113">Die Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="8c42e-113">The width, in pixels.</span></span> <span data-ttu-id="8c42e-114">Der Wert muss zwischen den Werten 640 und 2048 liegen.</span><span class="sxs-lookup"><span data-stu-id="8c42e-114">The value must be between the values of 640 and 2048.</span></span> <span data-ttu-id="8c42e-115">Wenn der Wert nicht gleichmäßig von 8 teilbar ist, wird er auf das nächst niedrigere Vielfache von 8 reduziert.</span><span class="sxs-lookup"><span data-stu-id="8c42e-115">If the value is not evenly divisible by 8, then it will be reduced to the next lower multiple of 8.</span></span>

</dd> <dt>

<span data-ttu-id="8c42e-116">*Display Pixel Height* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c42e-116">*displayPixelHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c42e-117">Die Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="8c42e-117">The height, in pixels.</span></span> <span data-ttu-id="8c42e-118">Der Wert muss zwischen den Werten 480 und 1920 liegen.</span><span class="sxs-lookup"><span data-stu-id="8c42e-118">The value must be between the values of 480 and 1920.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c42e-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c42e-119">Return value</span></span>

<span data-ttu-id="8c42e-120">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8c42e-120">This method can return one of these values.</span></span>



| <span data-ttu-id="8c42e-121">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="8c42e-121">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="8c42e-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c42e-122">Description</span></span>                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8c42e-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c42e-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="8c42e-124">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c42e-124">The operation was successful.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="8c42e-125"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="8c42e-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="8c42e-126">Der *displaypixelwidth* -Parameter ist von 8 nicht gleichmäßig teilbar, oder der *displaypixelwidth* -oder der *displaypixelheight* -Parameter liegt außerhalb des zulässigen Werts (640 x 480) oder Maximum 2048x1920).</span><span class="sxs-lookup"><span data-stu-id="8c42e-126">The *displayPixelWidth* parameter is not evenly divisible by 8 or the *displayPixelWidth* or *displayPixelHeight* parameter is outside of the allowed minimum (640x480) or maximum 2048x1920) values.</span></span><br/> |
| <dl> <span data-ttu-id="8c42e-127"><dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt></span><span class="sxs-lookup"><span data-stu-id="8c42e-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="8c42e-128">Die Auflösungs Änderung wurde nicht rechtzeitig abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8c42e-128">The resolution change did not finish in a timely manner.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="8c42e-129"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="8c42e-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="8c42e-130">Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8c42e-130">The virtual machine must be running for this operation.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="8c42e-131"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="8c42e-131"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="8c42e-132">Der virtuelle Computer ist ungültig oder wird zurzeit nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c42e-132">The virtual machine is not valid or is not currently running.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="8c42e-133"><dt>**VM \_ E \_ keine \_ Anzeige**</dt> <dt>0xa0040850</dt></span><span class="sxs-lookup"><span data-stu-id="8c42e-133"><dt>**VM\_E\_NO\_DISPLAY**</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="8c42e-134">Es konnte keine gültige Anzeige für die VM gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="8c42e-134">Unable to locate a valid display for the VM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="8c42e-135"><dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="8c42e-135"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="8c42e-136">Dieser Vorgang wird von der Version der Integrations Komponenten, die im Gast Betriebssystem installiert sind, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8c42e-136">The version of the integration components installed in the guest operating system does not support this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="8c42e-137"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8c42e-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="8c42e-138">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8c42e-138">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="8c42e-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c42e-139">Remarks</span></span>

<span data-ttu-id="8c42e-140">Die minimale Größe der Anzeige des virtuellen Computers beträgt 640 x 480 Pixel.</span><span class="sxs-lookup"><span data-stu-id="8c42e-140">The minimum size of the virtual machine's display is 640 x 480 pixels.</span></span> <span data-ttu-id="8c42e-141">Die maximale Größe beträgt 2048 x 1920.</span><span class="sxs-lookup"><span data-stu-id="8c42e-141">The maximum size is 2048 x 1920.</span></span> <span data-ttu-id="8c42e-142">Versucht, die Anzeige Größe auf Werte außerhalb dieser Grenzwerte oder auf eine beliebige Breite festzulegen, die nicht gleichmäßig von 8 teilbar ist, führt dazu, dass ein **E \_ invalidArg** -Fehler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c42e-142">Attempts to set the display size to values outside these limits, or to any width not evenly divisible by 8, will result in an **E\_INVALIDARG** error being returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c42e-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c42e-143">Requirements</span></span>



| <span data-ttu-id="8c42e-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c42e-144">Requirement</span></span> | <span data-ttu-id="8c42e-145">Wert</span><span class="sxs-lookup"><span data-stu-id="8c42e-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c42e-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c42e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8c42e-147">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c42e-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c42e-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c42e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8c42e-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8c42e-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8c42e-150">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8c42e-150">End of client support</span></span><br/>    | <span data-ttu-id="8c42e-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c42e-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8c42e-152">Produkt</span><span class="sxs-lookup"><span data-stu-id="8c42e-152">Product</span></span><br/>                  | <span data-ttu-id="8c42e-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8c42e-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8c42e-154">Header</span><span class="sxs-lookup"><span data-stu-id="8c42e-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c42e-155"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c42e-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8c42e-156">IID</span><span class="sxs-lookup"><span data-stu-id="8c42e-156">IID</span></span><br/>                      | <span data-ttu-id="8c42e-157">IID \_ ivmdisplay ist als 960895e9-f 743-4498-96aa-261f 867e7fc5 definiert.</span><span class="sxs-lookup"><span data-stu-id="8c42e-157">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8c42e-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c42e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c42e-159">**Ivmdisplay**</span><span class="sxs-lookup"><span data-stu-id="8c42e-159">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

