---
title: Ivmguestos-Neustart Methode (vpccominterfaces. h)
description: Startet das Gast Betriebssystem neu.
ms.assetid: 328c7aa1-d9bd-452d-95dd-9f6a03fa8c9e
keywords:
- Methode "virtuellen PC neu starten"
- Neustarten der Methode Virtual PC, ivmguestos Interface
- Ivmguestos Interface Virtual PC, Methode neu starten
topic_type:
- apiref
api_name:
- IVMGuestOS.Restart
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 110718e45d04445dd895a2bdb27419fbd24731c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391959"
---
# <a name="ivmguestosrestart-method"></a><span data-ttu-id="46340-106">Ivmguestos:: Restart-Methode</span><span class="sxs-lookup"><span data-stu-id="46340-106">IVMGuestOS::Restart method</span></span>

<span data-ttu-id="46340-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="46340-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="46340-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="46340-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="46340-109">Startet das Gast Betriebssystem neu.</span><span class="sxs-lookup"><span data-stu-id="46340-109">Restarts the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="46340-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="46340-110">Syntax</span></span>


```C++
HRESULT Restart(
  [in]          VARIANT_BOOL inForced,
  [out, retval] IVMTask      **outRestartTask
);
```



## <a name="parameters"></a><span data-ttu-id="46340-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="46340-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46340-112">*Information* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46340-112">*inForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46340-113">**Variant \_ TRUE** , wenn ein erzwungener Neustart erforderlich ist, andernfalls **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="46340-113">**VARIANT\_TRUE** if a forced restart is required and **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="46340-114">" *startstarttask* \[ " Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="46340-114">*outRestartTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="46340-115">Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss Fortschritt der Neustart Sequenz zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="46340-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the restart sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46340-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46340-116">Return value</span></span>

<span data-ttu-id="46340-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="46340-117">This method can return one of these values.</span></span>



| <span data-ttu-id="46340-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="46340-118">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="46340-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46340-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="46340-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="46340-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="46340-121">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="46340-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="46340-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="46340-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="46340-123">Der Parameter " *startstarttask* " ist **null**.</span><span class="sxs-lookup"><span data-stu-id="46340-123">The *outRestartTask* parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="46340-124"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="46340-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="46340-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="46340-125">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="46340-126"><dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt></span><span class="sxs-lookup"><span data-stu-id="46340-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="46340-127">Der Vorgang wurde nicht rechtzeitig beendet.</span><span class="sxs-lookup"><span data-stu-id="46340-127">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="46340-128"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="46340-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="46340-129">Der virtuelle Computer (VM) muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="46340-129">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="46340-130"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="46340-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="46340-131">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="46340-131">The configuration is unknown.</span></span><br/>                                   |
| <dl> <span data-ttu-id="46340-132"><dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="46340-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="46340-133">Das Feature "Integrations Komponenten" ist auf dieser VM nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="46340-133">The integration components feature is not installed in this VM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="46340-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46340-134">Remarks</span></span>

<span data-ttu-id="46340-135">Die folgenden Werte können durch die [**Error**](ivmtask-error.md) -Eigenschaft des zurückgegebenen [**ivmtask**](ivmtask.md) -Objekts zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="46340-135">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="46340-136">[**Fehler**](ivmtask-error.md) Code/Wert</span><span class="sxs-lookup"><span data-stu-id="46340-136">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="46340-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46340-137">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="46340-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005</span><span class="sxs-lookup"><span data-stu-id="46340-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="46340-139">Der Aufrufer muss über Berechtigungen zum Ausführen des Zugriffs auf diese VM verfügen.</span><span class="sxs-lookup"><span data-stu-id="46340-139">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="46340-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704, f)</span><span class="sxs-lookup"><span data-stu-id="46340-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="46340-141">Der Computer ist gesperrt und kann nicht ohne die Option "Force" heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="46340-141">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="46340-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span><span class="sxs-lookup"><span data-stu-id="46340-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="46340-143">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="46340-143">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="46340-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span><span class="sxs-lookup"><span data-stu-id="46340-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="46340-145">Ein System wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="46340-145">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="46340-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46340-146">Requirements</span></span>



| <span data-ttu-id="46340-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46340-147">Requirement</span></span> | <span data-ttu-id="46340-148">Wert</span><span class="sxs-lookup"><span data-stu-id="46340-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="46340-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46340-149">Minimum supported client</span></span><br/> | <span data-ttu-id="46340-150">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46340-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46340-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46340-151">Minimum supported server</span></span><br/> | <span data-ttu-id="46340-152">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="46340-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="46340-153">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="46340-153">End of client support</span></span><br/>    | <span data-ttu-id="46340-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="46340-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="46340-155">Produkt</span><span class="sxs-lookup"><span data-stu-id="46340-155">Product</span></span><br/>                  | <span data-ttu-id="46340-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="46340-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="46340-157">Header</span><span class="sxs-lookup"><span data-stu-id="46340-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="46340-158"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="46340-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="46340-159">IID</span><span class="sxs-lookup"><span data-stu-id="46340-159">IID</span></span><br/>                      | <span data-ttu-id="46340-160">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="46340-160">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="46340-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46340-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46340-162">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="46340-162">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

