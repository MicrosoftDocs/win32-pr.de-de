---
description: Ruft den Schlüssel Zustand eines Schlüssels ab.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Iskeypressed-Methode der Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 44af7a3dc82c0d4d20a2e4c6aff21f7a47837490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215131"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="bedfc-103">Iskeypressed-Methode der MSVM- \_ Tastatur Klasse</span><span class="sxs-lookup"><span data-stu-id="bedfc-103">IsKeyPressed method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="bedfc-104">Ruft den Schlüssel Zustand eines Schlüssels ab.</span><span class="sxs-lookup"><span data-stu-id="bedfc-104">Retrieves the key state of a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="bedfc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bedfc-105">Syntax</span></span>


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a><span data-ttu-id="bedfc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bedfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bedfc-107">*Keycode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bedfc-107">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bedfc-108">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bedfc-108">Type: **uint32**</span></span>

<span data-ttu-id="bedfc-109">Der virtuelle Schlüsselcode des abzufragende Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="bedfc-109">The virtual key code of the key to query.</span></span> <span data-ttu-id="bedfc-110">Die Liste der Codes für virtuelle Schlüssel finden Sie unter [**Code für virtuelle**](../inputdev/virtual-key-codes.md)Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="bedfc-110">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="bedfc-111">*KeyState* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bedfc-111">*keyState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bedfc-112">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="bedfc-112">Type: **boolean**</span></span>

<span data-ttu-id="bedfc-113">Der aktuelle Zustand des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="bedfc-113">The current down state of the key.</span></span> <span data-ttu-id="bedfc-114">Ein **true** -Wert bedeutet, dass der Schlüssel nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bedfc-114">A **True** value means the key is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bedfc-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bedfc-115">Return value</span></span>

<span data-ttu-id="bedfc-116">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bedfc-116">Type: **uint32**</span></span>

<span data-ttu-id="bedfc-117">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="bedfc-117">A return value of zero indicates success.</span></span> <span data-ttu-id="bedfc-118">Ein Wert ungleich NULL gibt an, dass der Schlüssel Zustand nicht abgefragt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="bedfc-118">A nonzero value indicates a failure to query the key state.</span></span>

<dl> <dt>

<span data-ttu-id="bedfc-119">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="bedfc-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bedfc-120">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="bedfc-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bedfc-121">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="bedfc-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bedfc-122">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="bedfc-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bedfc-123">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="bedfc-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bedfc-124">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="bedfc-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bedfc-125">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="bedfc-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bedfc-126">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="bedfc-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bedfc-127">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="bedfc-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bedfc-128">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="bedfc-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bedfc-129">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="bedfc-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bedfc-130">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="bedfc-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bedfc-131">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="bedfc-131">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bedfc-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bedfc-132">Remarks</span></span>

<span data-ttu-id="bedfc-133">Die **iskeypressed** -Methode gibt immer **false** für das **VK- \_ Menü** (18), **VK- \_ Steuer** Element (17) und **VK \_ Shift** (16) zurück, da es sich hierbei nicht um echte Tasten auf einer Tastatur handelt.</span><span class="sxs-lookup"><span data-stu-id="bedfc-133">The **IsKeyPressed** method will always return **False** for the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) because these are not real keys on a keyboard.</span></span> <span data-ttu-id="bedfc-134">Diese virtuellen Schlüsselcodes werden immer " **VK \_ lmenu** (164)", **" \_ VK lcontrol** (162)" und " **VK \_ LShift** (160)" durch die Methoden " [**presskey**](presskey-msvm-keyboard.md) " und " [**releasekey**](releasekey-msvm-keyboard.md) " zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="bedfc-134">These virtual key codes are always mapped to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, by the [**PressKey**](presskey-msvm-keyboard.md) and [**ReleaseKey**](releasekey-msvm-keyboard.md) methods.</span></span>

<span data-ttu-id="bedfc-135">Der Zugriff auf die [**MSVM- \_ Tastatur**](msvm-keyboard.md) Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="bedfc-135">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bedfc-136">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bedfc-136">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bedfc-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bedfc-137">Requirements</span></span>



| <span data-ttu-id="bedfc-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bedfc-138">Requirement</span></span> | <span data-ttu-id="bedfc-139">Wert</span><span class="sxs-lookup"><span data-stu-id="bedfc-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bedfc-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bedfc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="bedfc-141">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bedfc-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bedfc-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bedfc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="bedfc-143">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bedfc-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bedfc-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="bedfc-144">Namespace</span></span><br/>                | <span data-ttu-id="bedfc-145">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="bedfc-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bedfc-146">MOF</span><span class="sxs-lookup"><span data-stu-id="bedfc-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bedfc-147"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bedfc-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bedfc-148">DLL</span><span class="sxs-lookup"><span data-stu-id="bedfc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bedfc-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bedfc-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bedfc-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bedfc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bedfc-151">**MSVM- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="bedfc-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="bedfc-152">**Codes von virtuellen Schlüsseln**</span><span class="sxs-lookup"><span data-stu-id="bedfc-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

