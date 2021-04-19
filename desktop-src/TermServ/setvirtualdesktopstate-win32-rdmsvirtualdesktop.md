---
title: Setvirtualdesktopstate-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Aktualisiert den Zustand des virtuellen Desktops.
ms.assetid: 8f4f3d31-0434-4018-a33a-2ffd62c09669
ms.tgt_platform: multiple
keywords:
- Setvirtualdesktopstate-Methode Remotedesktopdienste
- Setvirtualdesktopstate-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste, setvirtualdesktopstate-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetVirtualDesktopState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af913e29857a59cacf283bff6a1642e0ea4cef9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344679"
---
# <a name="setvirtualdesktopstate-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="ed140-106">Setvirtualdesktopstate-Methode der Win32 \_ -Klasse rdmsvirtualdesktop</span><span class="sxs-lookup"><span data-stu-id="ed140-106">SetVirtualDesktopState method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="ed140-107">Aktualisiert den Zustand des virtuellen Desktops.</span><span class="sxs-lookup"><span data-stu-id="ed140-107">Updates the state of the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed140-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed140-108">Syntax</span></span>


```mof
uint32 SetVirtualDesktopState(
  [in] uint32 VMState
);
```



## <a name="parameters"></a><span data-ttu-id="ed140-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed140-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed140-110">*Vmstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed140-110">*VMState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed140-111">Ein-Wert, der den neuen Zustand des virtuellen Computers angibt.</span><span class="sxs-lookup"><span data-stu-id="ed140-111">A value that specifies the new state of the virtual machine.</span></span>

<span data-ttu-id="ed140-112">Mit diesem Parameter kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ed140-112">This parameter can bet set to one of the following values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ed140-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0 (Standard))</span><span class="sxs-lookup"><span data-stu-id="ed140-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0 (Default))</span></span>


</dt> <dd>

<span data-ttu-id="ed140-114">Der Status der virtuellen Maschine konnte nicht ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="ed140-114">The state of the virtual machine could not be determined.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ed140-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="ed140-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ed140-116">Der virtuelle Computer wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed140-116">The virtual machine is running.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ed140-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="ed140-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ed140-118">Der virtuelle Computer ist ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="ed140-118">The virtual machine is turned off.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ed140-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (32768)</span><span class="sxs-lookup"><span data-stu-id="ed140-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="ed140-120">Der virtuelle Computer wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="ed140-120">The virtual machine is paused.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="ed140-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>Angeh **alten (32769** )</span><span class="sxs-lookup"><span data-stu-id="ed140-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="ed140-122">Der virtuelle Computer befindet sich in einem gespeicherten Zustand.</span><span class="sxs-lookup"><span data-stu-id="ed140-122">The virtual machine is in a saved state.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ed140-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (32770)</span><span class="sxs-lookup"><span data-stu-id="ed140-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="ed140-124">Der virtuelle Computer wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="ed140-124">The virtual machine is starting.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="ed140-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>Wird **gespeichert** (32773)</span><span class="sxs-lookup"><span data-stu-id="ed140-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="ed140-126">Der virtuelle Computer speichert seinen Zustand.</span><span class="sxs-lookup"><span data-stu-id="ed140-126">The virtual machine is saving its state.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ed140-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (32774** )</span><span class="sxs-lookup"><span data-stu-id="ed140-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (32774)</span></span>


</dt> <dd>

<span data-ttu-id="ed140-128">Der virtuelle Computer wird ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="ed140-128">The virtual machine is turning off.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="ed140-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>Wird **angeh** alten (32776)</span><span class="sxs-lookup"><span data-stu-id="ed140-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="ed140-130">Der virtuelle Computer wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="ed140-130">The virtual machine is pausing.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="ed140-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>Wird fort **gesetzt (32777** )</span><span class="sxs-lookup"><span data-stu-id="ed140-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="ed140-132">Der virtuelle Computer wird von einem angehaltenen Zustand fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="ed140-132">The virtual machine is resuming from a paused state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed140-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed140-133">Return value</span></span>

<span data-ttu-id="ed140-134">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ed140-134">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed140-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed140-135">Requirements</span></span>



| <span data-ttu-id="ed140-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed140-136">Requirement</span></span> | <span data-ttu-id="ed140-137">Wert</span><span class="sxs-lookup"><span data-stu-id="ed140-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed140-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed140-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ed140-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ed140-139">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ed140-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed140-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ed140-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed140-141">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="ed140-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed140-142">Namespace</span></span><br/>                | <span data-ttu-id="ed140-143">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="ed140-143">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ed140-144">MOF</span><span class="sxs-lookup"><span data-stu-id="ed140-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed140-145"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ed140-145"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed140-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ed140-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed140-147"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed140-147"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ed140-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed140-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed140-149">**Win32 \_ rdmsvirtualdesktop**</span><span class="sxs-lookup"><span data-stu-id="ed140-149">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





