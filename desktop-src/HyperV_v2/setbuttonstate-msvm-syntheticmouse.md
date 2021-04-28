---
description: 'SetButtonState-Methode der Msvm_SyntheticMouse-Klasse: Legt den aktuellen Zustand der angegebenen Geräteschaltfläche fest.'
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: SetButtonState-Methode der Msvm_SyntheticMouse Klasse
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
ms.openlocfilehash: 161520ac1b7e9dba1a084a8fb3c623155aa135fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109208"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="56e63-103">SetButtonState-Methode der Msvm \_ SyntheticMouse-Klasse</span><span class="sxs-lookup"><span data-stu-id="56e63-103">SetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="56e63-104">Legt den aktuellen Zustand der angegebenen Geräteschaltfläche fest.</span><span class="sxs-lookup"><span data-stu-id="56e63-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e63-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56e63-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="56e63-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56e63-107">*buttonIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="56e63-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56e63-108">Typ: **uint32**</span><span class="sxs-lookup"><span data-stu-id="56e63-108">Type: **uint32**</span></span>

<span data-ttu-id="56e63-109">Der 1-basierte Index der zu ändernden Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="56e63-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="56e63-110">*isDown* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="56e63-110">*isDown* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56e63-111">Typ: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="56e63-111">Type: **boolean**</span></span>

<span data-ttu-id="56e63-112">Der neue Down-Zustand der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="56e63-112">The new down state of the button.</span></span> <span data-ttu-id="56e63-113">Ein **True-Wert** bedeutet, dass die Schaltfläche nicht mehr angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="56e63-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56e63-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56e63-114">Return value</span></span>

<span data-ttu-id="56e63-115">Typ: **uint32**</span><span class="sxs-lookup"><span data-stu-id="56e63-115">Type: **uint32**</span></span>

<span data-ttu-id="56e63-116">Werte, die nicht 0 (null) sind, weisen auf einen Fehler beim Ändern des Schaltflächenzustands hin.</span><span class="sxs-lookup"><span data-stu-id="56e63-116">Non zero values indicate a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="56e63-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="56e63-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="56e63-118">**Überprüfte Methodenparameter – Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="56e63-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="56e63-119">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="56e63-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="56e63-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="56e63-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="56e63-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="56e63-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="56e63-122">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="56e63-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="56e63-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="56e63-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="56e63-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="56e63-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="56e63-125">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="56e63-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="56e63-126">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="56e63-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="56e63-127">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="56e63-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="56e63-128">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="56e63-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="56e63-129">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="56e63-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="56e63-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56e63-130">Remarks</span></span>

<span data-ttu-id="56e63-131">Der Zugriff auf die [**Msvm \_ SyntheticMouse-Klasse**](msvm-syntheticmouse.md) kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="56e63-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="56e63-132">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="56e63-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="56e63-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56e63-133">Requirements</span></span>



| <span data-ttu-id="56e63-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56e63-134">Requirement</span></span> | <span data-ttu-id="56e63-135">Wert</span><span class="sxs-lookup"><span data-stu-id="56e63-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56e63-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56e63-136">Minimum supported client</span></span><br/> | <span data-ttu-id="56e63-137">nur Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56e63-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="56e63-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56e63-138">Minimum supported server</span></span><br/> | <span data-ttu-id="56e63-139">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56e63-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56e63-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="56e63-140">Namespace</span></span><br/>                | <span data-ttu-id="56e63-141">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="56e63-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="56e63-142">MOF</span><span class="sxs-lookup"><span data-stu-id="56e63-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56e63-143"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="56e63-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="56e63-144">DLL</span><span class="sxs-lookup"><span data-stu-id="56e63-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56e63-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="56e63-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="56e63-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="56e63-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e63-147">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="56e63-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

