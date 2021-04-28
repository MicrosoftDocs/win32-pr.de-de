---
description: 'GetButtonState-Methode der Msvm_SyntheticMouse Klasse: Ruft den aktuellen Zustand der angegebenen Geräteschaltfläche ab.'
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
ms.openlocfilehash: 26839292cf2fb3099e740629b28c7de0fbe3f60f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119388"
---
# <a name="getbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="5a595-103">GetButtonState-Methode der Msvm \_ SyntheticMouse-Klasse</span><span class="sxs-lookup"><span data-stu-id="5a595-103">GetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="5a595-104">Ruft den aktuellen Zustand der angegebenen Geräteschaltfläche ab.</span><span class="sxs-lookup"><span data-stu-id="5a595-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a595-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a595-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="5a595-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a595-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a595-107">*buttonIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5a595-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a595-108">Typ: **uint32**</span><span class="sxs-lookup"><span data-stu-id="5a595-108">Type: **uint32**</span></span>

<span data-ttu-id="5a595-109">Der 1-basierte Index der abfragten Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="5a595-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="5a595-110">*isDown* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5a595-110">*isDown* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a595-111">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="5a595-111">Type: **boolean**</span></span>

<span data-ttu-id="5a595-112">Der aktuelle Zustand der Schaltfläche nach unten.</span><span class="sxs-lookup"><span data-stu-id="5a595-112">The current down state of the button.</span></span> <span data-ttu-id="5a595-113">Ein **True-Wert** bedeutet, dass die Schaltfläche nicht mehr angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5a595-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a595-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a595-114">Return value</span></span>

<span data-ttu-id="5a595-115">Typ: **uint32**</span><span class="sxs-lookup"><span data-stu-id="5a595-115">Type: **uint32**</span></span>

<span data-ttu-id="5a595-116">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="5a595-116">A return value of zero indicates success.</span></span> <span data-ttu-id="5a595-117">Ein Wert ungleich 0 (null) gibt einen Abfragefehler an.</span><span class="sxs-lookup"><span data-stu-id="5a595-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="5a595-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="5a595-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5a595-119">**Überprüfte Methodenparameter – Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="5a595-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5a595-120">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="5a595-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5a595-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="5a595-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5a595-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="5a595-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5a595-123">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="5a595-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5a595-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="5a595-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5a595-125">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="5a595-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5a595-126">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="5a595-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5a595-127">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="5a595-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5a595-128">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="5a595-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5a595-129">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="5a595-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5a595-130">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="5a595-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5a595-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a595-131">Remarks</span></span>

<span data-ttu-id="5a595-132">Der Zugriff auf die [**Msvm \_ SyntheticMouse-Klasse**](msvm-syntheticmouse.md) kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="5a595-132">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5a595-133">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="5a595-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a595-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a595-134">Requirements</span></span>



| <span data-ttu-id="5a595-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a595-135">Requirement</span></span> | <span data-ttu-id="5a595-136">Wert</span><span class="sxs-lookup"><span data-stu-id="5a595-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a595-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a595-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5a595-138">nur Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a595-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5a595-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a595-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5a595-140">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a595-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a595-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a595-141">Namespace</span></span><br/>                | <span data-ttu-id="5a595-142">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="5a595-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5a595-143">MOF</span><span class="sxs-lookup"><span data-stu-id="5a595-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a595-144"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a595-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a595-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5a595-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a595-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5a595-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5a595-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5a595-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a595-148">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="5a595-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

