---
description: Ruft den aktuellen Zustand der angegebenen Geräte Schaltfläche ab.
ms.assetid: 66363AF1-E360-478D-8E62-513DE66EF130
title: GetButtonState-Methode der Msvm_SyntheticMouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3812d3e019a303656305471fc097fb1479fa1ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348806"
---
# <a name="getbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="a93bd-103">GetButtonState-Methode der MSVM \_ syntheticmouse-Klasse</span><span class="sxs-lookup"><span data-stu-id="a93bd-103">GetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="a93bd-104">Ruft den aktuellen Zustand der angegebenen Geräte Schaltfläche ab.</span><span class="sxs-lookup"><span data-stu-id="a93bd-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="a93bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a93bd-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="a93bd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a93bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a93bd-107">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a93bd-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a93bd-108">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a93bd-108">Type: **uint32**</span></span>

<span data-ttu-id="a93bd-109">Der 1-basierte Index der abzufragende Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="a93bd-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="a93bd-110">*isdown* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a93bd-110">*isDown* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a93bd-111">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="a93bd-111">Type: **boolean**</span></span>

<span data-ttu-id="a93bd-112">Der aktuelle Zustand der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="a93bd-112">The current down state of the button.</span></span> <span data-ttu-id="a93bd-113">Ein **true** -Wert bedeutet, dass die Schaltfläche nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a93bd-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a93bd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a93bd-114">Return value</span></span>

<span data-ttu-id="a93bd-115">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a93bd-115">Type: **uint32**</span></span>

<span data-ttu-id="a93bd-116">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="a93bd-116">A return value of zero indicates success.</span></span> <span data-ttu-id="a93bd-117">Ein Wert ungleich 0 (null) gibt einen Abfrage Fehler an.</span><span class="sxs-lookup"><span data-stu-id="a93bd-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="a93bd-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="a93bd-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a93bd-119">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="a93bd-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a93bd-120">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="a93bd-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a93bd-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="a93bd-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a93bd-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="a93bd-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a93bd-123">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="a93bd-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a93bd-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="a93bd-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a93bd-125">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="a93bd-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a93bd-126">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="a93bd-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a93bd-127">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="a93bd-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a93bd-128">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="a93bd-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a93bd-129">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="a93bd-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a93bd-130">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="a93bd-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a93bd-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a93bd-131">Remarks</span></span>

<span data-ttu-id="a93bd-132">Der Zugriff auf die [**MSVM \_ syntheticmouse**](msvm-syntheticmouse.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="a93bd-132">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a93bd-133">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a93bd-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a93bd-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a93bd-134">Requirements</span></span>



| <span data-ttu-id="a93bd-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a93bd-135">Requirement</span></span> | <span data-ttu-id="a93bd-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a93bd-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a93bd-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a93bd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a93bd-138">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a93bd-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a93bd-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a93bd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a93bd-140">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a93bd-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a93bd-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="a93bd-141">Namespace</span></span><br/>                | <span data-ttu-id="a93bd-142">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="a93bd-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a93bd-143">MOF</span><span class="sxs-lookup"><span data-stu-id="a93bd-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a93bd-144"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a93bd-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a93bd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a93bd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a93bd-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a93bd-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a93bd-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a93bd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a93bd-148">**MSVM \_ syntheticmouse**</span><span class="sxs-lookup"><span data-stu-id="a93bd-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

