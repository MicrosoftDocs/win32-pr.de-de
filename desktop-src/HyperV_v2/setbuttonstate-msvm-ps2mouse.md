---
description: 'SetButtonState-Methode der Msvm_Ps2Mouse-Klasse: Legt den aktuellen Zustand der angegebenen Geräteschaltfläche fest.'
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
ms.openlocfilehash: ea6a984b84c7ee17436a7fb4738433edce6d68d8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118528"
---
# <a name="setbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="ff65d-103">SetButtonState-Methode der Msvm \_ Ps2Mouse-Klasse</span><span class="sxs-lookup"><span data-stu-id="ff65d-103">SetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="ff65d-104">Legt den aktuellen Zustand der angegebenen Geräteschaltfläche fest.</span><span class="sxs-lookup"><span data-stu-id="ff65d-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff65d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff65d-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="ff65d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff65d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff65d-107">*buttonIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ff65d-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff65d-108">Typ: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ff65d-108">Type: **uint32**</span></span>

<span data-ttu-id="ff65d-109">Der 1-basierte Index der zu ändernden Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="ff65d-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="ff65d-110">*buttonState* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ff65d-110">*buttonState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff65d-111">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="ff65d-111">Type: **boolean**</span></span>

<span data-ttu-id="ff65d-112">Der neue Nach-unten-Zustand der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="ff65d-112">The new down state of the button.</span></span> <span data-ttu-id="ff65d-113">Ein **True-Wert** bedeutet, dass die Schaltfläche nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ff65d-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff65d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff65d-114">Return value</span></span>

<span data-ttu-id="ff65d-115">Typ: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ff65d-115">Type: **uint32**</span></span>

<span data-ttu-id="ff65d-116">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="ff65d-116">A return value of zero indicates success.</span></span> <span data-ttu-id="ff65d-117">Ein Wert ungleich 0 (null) gibt an, dass der Schaltflächenzustand nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff65d-117">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="ff65d-118">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="ff65d-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ff65d-119">**Methodenparameter überprüft** – Auftrag gestartet (4096)</span><span class="sxs-lookup"><span data-stu-id="ff65d-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ff65d-120">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="ff65d-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ff65d-121">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="ff65d-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ff65d-122">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="ff65d-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ff65d-123">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="ff65d-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ff65d-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ff65d-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ff65d-125">**Ungültiger** Parameter (32773)</span><span class="sxs-lookup"><span data-stu-id="ff65d-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ff65d-126">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="ff65d-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ff65d-127">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="ff65d-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ff65d-128">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="ff65d-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ff65d-129">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="ff65d-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ff65d-130">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="ff65d-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ff65d-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff65d-131">Remarks</span></span>

<span data-ttu-id="ff65d-132">Der Zugriff auf die [**Msvm \_ Ps2Mouse-Klasse**](msvm-ps2mouse.md) kann durch UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="ff65d-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ff65d-133">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="ff65d-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff65d-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff65d-134">Requirements</span></span>



| <span data-ttu-id="ff65d-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff65d-135">Requirement</span></span> | <span data-ttu-id="ff65d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="ff65d-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff65d-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff65d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ff65d-138">Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff65d-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ff65d-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff65d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ff65d-140">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff65d-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff65d-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff65d-141">Namespace</span></span><br/>                | <span data-ttu-id="ff65d-142">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="ff65d-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ff65d-143">MOF</span><span class="sxs-lookup"><span data-stu-id="ff65d-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff65d-144"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff65d-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff65d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ff65d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff65d-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ff65d-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ff65d-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ff65d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff65d-148">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="ff65d-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

