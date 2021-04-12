---
description: Legt den aktuellen Zustand der angegebenen Geräte Schaltfläche fest.
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: SetButtonState-Methode der Msvm_SyntheticMouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c99915fa8ede9cbb405f4483ac10ca9ff8efaf71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215924"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="cbd8d-103">SetButtonState-Methode der MSVM- \_ syntheticmouse-Klasse</span><span class="sxs-lookup"><span data-stu-id="cbd8d-103">SetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="cbd8d-104">Legt den aktuellen Zustand der angegebenen Geräte Schaltfläche fest.</span><span class="sxs-lookup"><span data-stu-id="cbd8d-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd8d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbd8d-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="cbd8d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbd8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbd8d-107">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbd8d-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbd8d-108">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cbd8d-108">Type: **uint32**</span></span>

<span data-ttu-id="cbd8d-109">Der auf 1 basierende Index der Schaltfläche, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbd8d-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="cbd8d-110">*isdown* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbd8d-110">*isDown* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbd8d-111">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="cbd8d-111">Type: **boolean**</span></span>

<span data-ttu-id="cbd8d-112">Der neue Status der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="cbd8d-112">The new down state of the button.</span></span> <span data-ttu-id="cbd8d-113">Ein **true** -Wert bedeutet, dass die Schaltfläche nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cbd8d-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbd8d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cbd8d-114">Return value</span></span>

<span data-ttu-id="cbd8d-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cbd8d-115">Type: **uint32**</span></span>

<span data-ttu-id="cbd8d-116">Werte ungleich NULL deuten darauf hin, dass der Schaltflächen Zustand nicht geändert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="cbd8d-116">Non zero values indicate a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="cbd8d-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="cbd8d-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cbd8d-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="cbd8d-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cbd8d-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="cbd8d-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cbd8d-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="cbd8d-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cbd8d-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="cbd8d-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cbd8d-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="cbd8d-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cbd8d-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="cbd8d-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cbd8d-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="cbd8d-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cbd8d-125">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="cbd8d-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cbd8d-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="cbd8d-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cbd8d-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="cbd8d-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cbd8d-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="cbd8d-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cbd8d-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="cbd8d-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cbd8d-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbd8d-130">Remarks</span></span>

<span data-ttu-id="cbd8d-131">Der Zugriff auf die [**MSVM \_ syntheticmouse**](msvm-syntheticmouse.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="cbd8d-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cbd8d-132">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cbd8d-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbd8d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbd8d-133">Requirements</span></span>



| <span data-ttu-id="cbd8d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbd8d-134">Requirement</span></span> | <span data-ttu-id="cbd8d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="cbd8d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd8d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbd8d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cbd8d-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbd8d-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cbd8d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbd8d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cbd8d-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbd8d-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cbd8d-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="cbd8d-140">Namespace</span></span><br/>                | <span data-ttu-id="cbd8d-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cbd8d-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cbd8d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="cbd8d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbd8d-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cbd8d-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbd8d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="cbd8d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbd8d-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cbd8d-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cbd8d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbd8d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd8d-147">**MSVM \_ syntheticmouse**</span><span class="sxs-lookup"><span data-stu-id="cbd8d-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

