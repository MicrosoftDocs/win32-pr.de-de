---
description: Simuliert eine Tastenkombination für die Tastenkombination.
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: Typekey-Methode der Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1b978da48600cc52472ab8bdec011ddbaa5ff624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960572"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="33d41-103">Typekey-Methode der MSVM- \_ Tastatur Klasse</span><span class="sxs-lookup"><span data-stu-id="33d41-103">TypeKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="33d41-104">Simuliert eine Tastenkombination für die Tastenkombination.</span><span class="sxs-lookup"><span data-stu-id="33d41-104">Simulates a press-release key sequence.</span></span> <span data-ttu-id="33d41-105">Dies entspricht dem Aufrufen von [**Press Key**](presskey-msvm-keyboard.md) gefolgt von [**releasekey**](releasekey-msvm-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="33d41-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="33d41-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="33d41-106">Syntax</span></span>


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="33d41-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="33d41-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33d41-108">*Keycode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33d41-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33d41-109">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33d41-109">Type: **uint32**</span></span>

<span data-ttu-id="33d41-110">Der virtuelle Schlüsselcode des zu druckenden Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="33d41-110">The virtual key code of the key to press.</span></span> <span data-ttu-id="33d41-111">Die Liste der Codes für virtuelle Schlüssel finden Sie unter [**Code für virtuelle**](../inputdev/virtual-key-codes.md)Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="33d41-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33d41-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33d41-112">Return value</span></span>

<span data-ttu-id="33d41-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33d41-113">Type: **uint32**</span></span>

<span data-ttu-id="33d41-114">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="33d41-114">A return value of zero indicates success.</span></span> <span data-ttu-id="33d41-115">Ein Wert ungleich 0 (null) gibt an, dass der Schlüssel Zustand nicht geändert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="33d41-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="33d41-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="33d41-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="33d41-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="33d41-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="33d41-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="33d41-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="33d41-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="33d41-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="33d41-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="33d41-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="33d41-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="33d41-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="33d41-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="33d41-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="33d41-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="33d41-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="33d41-124">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="33d41-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="33d41-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="33d41-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="33d41-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="33d41-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="33d41-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="33d41-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="33d41-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="33d41-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="33d41-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33d41-129">Remarks</span></span>

<span data-ttu-id="33d41-130">Der Zugriff auf die [**MSVM- \_ Tastatur**](msvm-keyboard.md) Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="33d41-130">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="33d41-131">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="33d41-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="33d41-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33d41-132">Requirements</span></span>



| <span data-ttu-id="33d41-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33d41-133">Requirement</span></span> | <span data-ttu-id="33d41-134">Wert</span><span class="sxs-lookup"><span data-stu-id="33d41-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33d41-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33d41-135">Minimum supported client</span></span><br/> | <span data-ttu-id="33d41-136">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33d41-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="33d41-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33d41-137">Minimum supported server</span></span><br/> | <span data-ttu-id="33d41-138">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33d41-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33d41-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="33d41-139">Namespace</span></span><br/>                | <span data-ttu-id="33d41-140">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="33d41-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="33d41-141">MOF</span><span class="sxs-lookup"><span data-stu-id="33d41-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33d41-142"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="33d41-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="33d41-143">DLL</span><span class="sxs-lookup"><span data-stu-id="33d41-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33d41-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="33d41-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="33d41-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33d41-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33d41-146">**MSVM- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="33d41-146">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="33d41-147">**Codes von virtuellen Schlüsseln**</span><span class="sxs-lookup"><span data-stu-id="33d41-147">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

