---
title: Ivmguestos Shutdown-Methode (vpccominterfaces. h)
description: Fährt das Gast Betriebssystem auf dem virtuellen Computer herunter.
ms.assetid: a1453ad1-c4c2-47bb-a612-d203a6ee8c18
keywords:
- Methode zum Herunterfahren des virtuellen PCs
- Shutdown-Methode Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, Shutdown-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.Shutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63025270752af044a572cf9b6299e54b31b89ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742064"
---
# <a name="ivmguestosshutdown-method"></a><span data-ttu-id="8b925-106">Ivmguestos:: Shutdown-Methode</span><span class="sxs-lookup"><span data-stu-id="8b925-106">IVMGuestOS::Shutdown method</span></span>

<span data-ttu-id="8b925-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8b925-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8b925-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8b925-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8b925-109">Fährt das Gast Betriebssystem auf dem virtuellen Computer (VM) herunter.</span><span class="sxs-lookup"><span data-stu-id="8b925-109">Shuts down the guest operating system in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b925-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b925-110">Syntax</span></span>


```C++
HRESULT Shutdown(
  [in]          VARIANT_BOOL isForced,
  [out, retval] IVMTask      **outShutdownTask
);
```



## <a name="parameters"></a><span data-ttu-id="8b925-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b925-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b925-112">*isforced* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b925-112">*isForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b925-113">**Variant \_ "True** ", wenn das Herunterfahren erzwungen werden soll, andernfalls " **\_ false** ".</span><span class="sxs-lookup"><span data-stu-id="8b925-113">**VARIANT\_TRUE** if the shutdown is to be forced, **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="8b925-114">*outshutdowntask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8b925-114">*outShutdownTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8b925-115">Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss des Beendigungs Vorgangs zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="8b925-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the shutdown process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b925-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b925-116">Return value</span></span>

<span data-ttu-id="8b925-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8b925-117">This method can return one of these values.</span></span>



| <span data-ttu-id="8b925-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="8b925-118">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="8b925-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b925-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b925-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8b925-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="8b925-121">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b925-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8b925-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8b925-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="8b925-123">Der *outshutdowntask* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="8b925-123">The *outShutdownTask* parameter is **NULL**.</span></span><br/>                    |
| <dl> <span data-ttu-id="8b925-124"><dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt></span><span class="sxs-lookup"><span data-stu-id="8b925-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="8b925-125">Der Vorgang wurde nicht rechtzeitig beendet.</span><span class="sxs-lookup"><span data-stu-id="8b925-125">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="8b925-126"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="8b925-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="8b925-127">Die VM wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="8b925-127">The VM could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="8b925-128"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="8b925-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="8b925-129">Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8b925-129">The VM must be running for this operation.</span></span><br/>                      |
| <dl> <span data-ttu-id="8b925-130"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="8b925-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="8b925-131">Der Aufrufer muss über Berechtigungen zum Ausführen des Zugriffs auf diese VM verfügen.</span><span class="sxs-lookup"><span data-stu-id="8b925-131">The caller must have execute access permissions for this VM.</span></span><br/>    |
| <dl> <span data-ttu-id="8b925-132"><dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="8b925-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="8b925-133">Das Feature "Integrations Komponenten" ist auf dieser VM nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="8b925-133">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="8b925-134"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8b925-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="8b925-135">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8b925-135">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="8b925-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b925-136">Remarks</span></span>

<span data-ttu-id="8b925-137">Der virtuelle Computer muss ausgeführt werden, und das Feature "Integrations Komponenten" muss installiert sein, wenn diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8b925-137">The VM must be running and integration components feature must be installed when this method is invoked.</span></span> <span data-ttu-id="8b925-138">Diese Methode wird nur für Windows-basierte Gast Betriebssysteme unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b925-138">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="8b925-139">Die folgenden Werte können durch die [**Error**](ivmtask-error.md) -Eigenschaft des zurückgegebenen [**ivmtask**](ivmtask.md) -Objekts zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8b925-139">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="8b925-140">[**Fehler**](ivmtask-error.md) Code/Wert</span><span class="sxs-lookup"><span data-stu-id="8b925-140">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="8b925-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b925-141">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8b925-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005</span><span class="sxs-lookup"><span data-stu-id="8b925-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="8b925-143">Der Aufrufer muss über Berechtigungen zum Ausführen des Zugriffs auf diese VM verfügen.</span><span class="sxs-lookup"><span data-stu-id="8b925-143">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="8b925-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704, f)</span><span class="sxs-lookup"><span data-stu-id="8b925-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="8b925-145">Der Computer ist gesperrt und kann nicht ohne die Option "Force" heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="8b925-145">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="8b925-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span><span class="sxs-lookup"><span data-stu-id="8b925-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="8b925-147">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="8b925-147">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="8b925-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span><span class="sxs-lookup"><span data-stu-id="8b925-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="8b925-149">Ein System wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="8b925-149">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="8b925-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b925-150">Requirements</span></span>



| <span data-ttu-id="8b925-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b925-151">Requirement</span></span> | <span data-ttu-id="8b925-152">Wert</span><span class="sxs-lookup"><span data-stu-id="8b925-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b925-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b925-153">Minimum supported client</span></span><br/> | <span data-ttu-id="8b925-154">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b925-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b925-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b925-155">Minimum supported server</span></span><br/> | <span data-ttu-id="8b925-156">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8b925-156">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8b925-157">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8b925-157">End of client support</span></span><br/>    | <span data-ttu-id="8b925-158">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8b925-158">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8b925-159">Produkt</span><span class="sxs-lookup"><span data-stu-id="8b925-159">Product</span></span><br/>                  | <span data-ttu-id="8b925-160">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8b925-160">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8b925-161">Header</span><span class="sxs-lookup"><span data-stu-id="8b925-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b925-162"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b925-162"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8b925-163">IID</span><span class="sxs-lookup"><span data-stu-id="8b925-163">IID</span></span><br/>                      | <span data-ttu-id="8b925-164">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="8b925-164">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8b925-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b925-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b925-166">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="8b925-166">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

