---
description: Simuliert eine Schlüssel Version.
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Releasekey-Methode der Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.ReleaseKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2193a4b78128ff3f65e98b4425528a51f6cf5916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530101"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="cbacd-103">Releasekey-Methode der MSVM- \_ Tastatur Klasse</span><span class="sxs-lookup"><span data-stu-id="cbacd-103">ReleaseKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="cbacd-104">Simuliert eine Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="cbacd-104">Simulates a key release.</span></span> <span data-ttu-id="cbacd-105">Bei erfolgreicher Ausführung befindet sich der Schlüssel im Status "up".</span><span class="sxs-lookup"><span data-stu-id="cbacd-105">When successful, the key will be in the up state.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbacd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbacd-106">Syntax</span></span>


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="cbacd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbacd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbacd-108">*Keycode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbacd-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbacd-109">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cbacd-109">Type: **uint32**</span></span>

<span data-ttu-id="cbacd-110">Der virtuelle Schlüsselcode des zu veröffentlichenden Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="cbacd-110">The virtual key code of the key to release.</span></span> <span data-ttu-id="cbacd-111">Die Liste der Codes für virtuelle Schlüssel finden Sie unter [**Code für virtuelle**](../inputdev/virtual-key-codes.md)Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="cbacd-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbacd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cbacd-112">Return value</span></span>

<span data-ttu-id="cbacd-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cbacd-113">Type: **uint32**</span></span>

<span data-ttu-id="cbacd-114">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="cbacd-114">A return value of zero indicates success.</span></span> <span data-ttu-id="cbacd-115">Ein Wert ungleich 0 (null) gibt an, dass der Schlüssel Zustand nicht geändert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="cbacd-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="cbacd-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="cbacd-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cbacd-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="cbacd-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cbacd-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="cbacd-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cbacd-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="cbacd-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cbacd-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="cbacd-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cbacd-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="cbacd-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cbacd-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="cbacd-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cbacd-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="cbacd-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cbacd-124">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="cbacd-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cbacd-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="cbacd-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cbacd-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="cbacd-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cbacd-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="cbacd-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cbacd-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="cbacd-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cbacd-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbacd-129">Remarks</span></span>

<span data-ttu-id="cbacd-130">Die **releasekey** -Methode ordnet Verweise auf **das VK- \_ Menü** (18), das **VK- \_ Steuer** Element (17) und die **VK- \_ UMSCHALT** Taste (16) auf " **VK \_ lmenu** (164)", " **VK \_ lcontrol** (162)" und " **VK \_ LShift** (160)" **zu \_** **\_** **\_**</span><span class="sxs-lookup"><span data-stu-id="cbacd-130">The **ReleaseKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="cbacd-131">Der Zugriff auf die [**MSVM- \_ Tastatur**](msvm-keyboard.md) Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="cbacd-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cbacd-132">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cbacd-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbacd-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbacd-133">Requirements</span></span>



| <span data-ttu-id="cbacd-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbacd-134">Requirement</span></span> | <span data-ttu-id="cbacd-135">Wert</span><span class="sxs-lookup"><span data-stu-id="cbacd-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbacd-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbacd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cbacd-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbacd-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cbacd-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbacd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cbacd-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbacd-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cbacd-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="cbacd-140">Namespace</span></span><br/>                | <span data-ttu-id="cbacd-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cbacd-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cbacd-142">MOF</span><span class="sxs-lookup"><span data-stu-id="cbacd-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbacd-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cbacd-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbacd-144">DLL</span><span class="sxs-lookup"><span data-stu-id="cbacd-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbacd-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cbacd-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cbacd-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbacd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbacd-147">**MSVM- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="cbacd-147">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="cbacd-148">**Codes von virtuellen Schlüsseln**</span><span class="sxs-lookup"><span data-stu-id="cbacd-148">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

