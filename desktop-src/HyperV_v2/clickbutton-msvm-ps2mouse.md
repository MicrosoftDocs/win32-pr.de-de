---
description: Simuliert einen Klick auf die angegebene Geräte Schaltfläche.
ms.assetid: 77CFA2E9-E422-464C-B124-6F7D3D56BA4C
title: ClickButton-Methode der Msvm_Ps2Mouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffaded2a5e9a8e4e37a158e3aa91b27520dff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343829"
---
# <a name="clickbutton-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="cfd40-103">ClickButton-Methode der MSVM \_ Ps2Mouse-Klasse</span><span class="sxs-lookup"><span data-stu-id="cfd40-103">ClickButton method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="cfd40-104">Simuliert einen Klick auf die angegebene Geräte Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="cfd40-104">Simulates a click of the specified device button.</span></span> <span data-ttu-id="cfd40-105">Dies entspricht dem doppelten Aufrufen von [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md) , zuerst zum Drücken der Schaltfläche und erneut zum Freigeben.</span><span class="sxs-lookup"><span data-stu-id="cfd40-105">This is equivalent to calling [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md) twice, first to press the button, and again to release it.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfd40-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfd40-106">Syntax</span></span>


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="cfd40-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfd40-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfd40-108">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfd40-108">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfd40-109">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cfd40-109">Type: **uint32**</span></span>

<span data-ttu-id="cfd40-110">Der 1-basierte Index der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="cfd40-110">The 1-based index of the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfd40-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfd40-111">Return value</span></span>

<span data-ttu-id="cfd40-112">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cfd40-112">Type: **uint32**</span></span>

<span data-ttu-id="cfd40-113">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="cfd40-113">A return value of zero indicates success.</span></span> <span data-ttu-id="cfd40-114">Ein Wert ungleich NULL gibt an, dass der Zustand der Schaltfläche nicht geändert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="cfd40-114">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="cfd40-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="cfd40-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cfd40-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="cfd40-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cfd40-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="cfd40-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cfd40-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="cfd40-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cfd40-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="cfd40-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cfd40-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="cfd40-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cfd40-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="cfd40-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cfd40-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="cfd40-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cfd40-123">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="cfd40-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cfd40-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="cfd40-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cfd40-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="cfd40-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cfd40-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="cfd40-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cfd40-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="cfd40-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cfd40-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfd40-128">Remarks</span></span>

<span data-ttu-id="cfd40-129">Der Zugriff auf die [**MSVM- \_ Ps2Mouse**](msvm-ps2mouse.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="cfd40-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cfd40-130">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cfd40-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfd40-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfd40-131">Requirements</span></span>



| <span data-ttu-id="cfd40-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfd40-132">Requirement</span></span> | <span data-ttu-id="cfd40-133">Wert</span><span class="sxs-lookup"><span data-stu-id="cfd40-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfd40-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfd40-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cfd40-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfd40-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cfd40-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfd40-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cfd40-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfd40-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cfd40-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfd40-138">Namespace</span></span><br/>                | <span data-ttu-id="cfd40-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cfd40-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cfd40-140">MOF</span><span class="sxs-lookup"><span data-stu-id="cfd40-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfd40-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cfd40-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfd40-142">DLL</span><span class="sxs-lookup"><span data-stu-id="cfd40-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfd40-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cfd40-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cfd40-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfd40-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfd40-145">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="cfd40-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

