---
description: Legt den aktuellen Zustand der angegebenen Geräte Schaltfläche fest.
ms.assetid: 312A2B8B-D518-4797-9B50-F12493598CD6
title: SetButtonState-Methode der Msvm_Ps2Mouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 34475edfa27d08cbe9de488502686a84e4391eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360522"
---
# <a name="setbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="e2fc6-103">SetButtonState-Methode der Ps2Mouse-Klasse von MSVM \_</span><span class="sxs-lookup"><span data-stu-id="e2fc6-103">SetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="e2fc6-104">Legt den aktuellen Zustand der angegebenen Geräte Schaltfläche fest.</span><span class="sxs-lookup"><span data-stu-id="e2fc6-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2fc6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2fc6-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="e2fc6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2fc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2fc6-107">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2fc6-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fc6-108">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2fc6-108">Type: **uint32**</span></span>

<span data-ttu-id="e2fc6-109">Der auf 1 basierende Index der Schaltfläche, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2fc6-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="e2fc6-110">*ButtonState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2fc6-110">*buttonState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fc6-111">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="e2fc6-111">Type: **boolean**</span></span>

<span data-ttu-id="e2fc6-112">Der neue Status der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="e2fc6-112">The new down state of the button.</span></span> <span data-ttu-id="e2fc6-113">Ein **true** -Wert bedeutet, dass die Schaltfläche nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e2fc6-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2fc6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2fc6-114">Return value</span></span>

<span data-ttu-id="e2fc6-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2fc6-115">Type: **uint32**</span></span>

<span data-ttu-id="e2fc6-116">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="e2fc6-116">A return value of zero indicates success.</span></span> <span data-ttu-id="e2fc6-117">Ein Wert ungleich NULL gibt an, dass der Zustand der Schaltfläche nicht geändert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="e2fc6-117">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="e2fc6-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="e2fc6-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e2fc6-119">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="e2fc6-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e2fc6-120">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="e2fc6-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e2fc6-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="e2fc6-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e2fc6-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="e2fc6-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e2fc6-123">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="e2fc6-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e2fc6-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="e2fc6-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e2fc6-125">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="e2fc6-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e2fc6-126">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="e2fc6-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e2fc6-127">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="e2fc6-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e2fc6-128">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="e2fc6-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e2fc6-129">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="e2fc6-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e2fc6-130">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="e2fc6-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e2fc6-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2fc6-131">Remarks</span></span>

<span data-ttu-id="e2fc6-132">Der Zugriff auf die [**MSVM- \_ Ps2Mouse**](msvm-ps2mouse.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="e2fc6-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e2fc6-133">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e2fc6-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2fc6-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2fc6-134">Requirements</span></span>



| <span data-ttu-id="e2fc6-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2fc6-135">Requirement</span></span> | <span data-ttu-id="e2fc6-136">Wert</span><span class="sxs-lookup"><span data-stu-id="e2fc6-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2fc6-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2fc6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e2fc6-138">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2fc6-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e2fc6-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2fc6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e2fc6-140">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2fc6-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2fc6-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2fc6-141">Namespace</span></span><br/>                | <span data-ttu-id="e2fc6-142">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e2fc6-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e2fc6-143">MOF</span><span class="sxs-lookup"><span data-stu-id="e2fc6-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2fc6-144"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e2fc6-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2fc6-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e2fc6-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2fc6-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2fc6-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e2fc6-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2fc6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2fc6-148">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="e2fc6-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

