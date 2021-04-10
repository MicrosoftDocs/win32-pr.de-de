---
title: Ivmguestos-Logoff-Methode (vpccominterfaces. h)
description: Protokolliert alle Benutzer vom Gast Betriebssystem.
ms.assetid: 224aa7cb-0892-4e8a-84bd-78dd5cb724df
keywords:
- Abmelde Methode Virtual PC
- Logoff-Methode Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, Logoff-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.Logoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c67e917cc9ff93d162bc340185f426fe9eee3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040967"
---
# <a name="ivmguestoslogoff-method"></a><span data-ttu-id="79c49-106">Ivmguestos:: Logoff-Methode</span><span class="sxs-lookup"><span data-stu-id="79c49-106">IVMGuestOS::Logoff method</span></span>

<span data-ttu-id="79c49-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="79c49-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="79c49-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="79c49-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="79c49-109">Protokolliert alle Benutzer vom Gast Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="79c49-109">Logs off all users from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c49-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="79c49-110">Syntax</span></span>


```C++
HRESULT Logoff(
  [out, retval] IVMTask **outLogoffTask
);
```



## <a name="parameters"></a><span data-ttu-id="79c49-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="79c49-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79c49-112">*outlogofftask* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="79c49-112">*outLogoffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="79c49-113">Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss Status der Abmelde Sequenz zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="79c49-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the logoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79c49-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79c49-114">Return value</span></span>

<span data-ttu-id="79c49-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="79c49-115">This method can return one of these values.</span></span>



| <span data-ttu-id="79c49-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="79c49-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="79c49-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79c49-117">Description</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="79c49-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="79c49-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="79c49-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="79c49-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="79c49-120"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="79c49-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="79c49-121">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="79c49-121">An unexpected error has occurred.</span></span><br/>                                            |
| <dl> <span data-ttu-id="79c49-122"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="79c49-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="79c49-123">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="79c49-123">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="79c49-124"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="79c49-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="79c49-125">Der Aufrufer muss über Berechtigungen zum Ausführen des Zugriffs auf diese VM verfügen.</span><span class="sxs-lookup"><span data-stu-id="79c49-125">The caller must have execute access permissions for this VM.</span></span><br/>                 |
| <dl> <span data-ttu-id="79c49-126"><dt>**VM \_ E \_ \_**</dt> Zeitüberschreitung <dt>0xa0040202</dt></span><span class="sxs-lookup"><span data-stu-id="79c49-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="79c49-127">Der Vorgang wurde nicht rechtzeitig beendet.</span><span class="sxs-lookup"><span data-stu-id="79c49-127">The operation did not complete in a timely manner.</span></span><br/>                           |
| <dl> <span data-ttu-id="79c49-128"><dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> "</span><span class="sxs-lookup"><span data-stu-id="79c49-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="79c49-129">Das Feature "Integrations Komponenten" ist auf diesem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="79c49-129">The integration components feature is not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="79c49-130"><dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus</span><span class="sxs-lookup"><span data-stu-id="79c49-130"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="79c49-131">Der virtuelle Computer (VM) muss für diesen Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="79c49-131">The virtual machine (VM) must be running for this operation.</span></span><br/>                 |
| <dl> <span data-ttu-id="79c49-132"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="79c49-132"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="79c49-133">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="79c49-133">The configuration is unknown.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="79c49-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79c49-134">Remarks</span></span>

<span data-ttu-id="79c49-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) wird durch die [**Error**](ivmtask-error.md) -Eigenschaft des zurückgegebenen [**ivmtask**](ivmtask.md) -Objekts zurückgegeben. es sind keine Anmelde Sitzungen im Gast Betriebssystem vorhanden.</span><span class="sxs-lookup"><span data-stu-id="79c49-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) is returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object there are no logon sessions in the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="79c49-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79c49-136">Requirements</span></span>



| <span data-ttu-id="79c49-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79c49-137">Requirement</span></span> | <span data-ttu-id="79c49-138">Wert</span><span class="sxs-lookup"><span data-stu-id="79c49-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="79c49-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79c49-139">Minimum supported client</span></span><br/> | <span data-ttu-id="79c49-140">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79c49-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79c49-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79c49-141">Minimum supported server</span></span><br/> | <span data-ttu-id="79c49-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="79c49-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="79c49-143">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="79c49-143">End of client support</span></span><br/>    | <span data-ttu-id="79c49-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="79c49-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="79c49-145">Produkt</span><span class="sxs-lookup"><span data-stu-id="79c49-145">Product</span></span><br/>                  | <span data-ttu-id="79c49-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="79c49-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="79c49-147">Header</span><span class="sxs-lookup"><span data-stu-id="79c49-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="79c49-148"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="79c49-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="79c49-149">IID</span><span class="sxs-lookup"><span data-stu-id="79c49-149">IID</span></span><br/>                      | <span data-ttu-id="79c49-150">IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.</span><span class="sxs-lookup"><span data-stu-id="79c49-150">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="79c49-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79c49-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c49-152">**Ivmguestos**</span><span class="sxs-lookup"><span data-stu-id="79c49-152">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

