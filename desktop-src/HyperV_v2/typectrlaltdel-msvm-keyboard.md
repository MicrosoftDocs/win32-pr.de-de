---
description: Simuliert eine Tastenkombination STRG + ALT + ENTF.
ms.assetid: C24C9C42-844F-4560-B8C1-0054F5E913D6
title: Typectrlaltdel-Methode der Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeCtrlAltDel
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 64ebc4bddf8adccd7098cafed1df43d1cf1cb4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348169"
---
# <a name="typectrlaltdel-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="69235-103">Typectrlaltdel-Methode der MSVM- \_ Tastatur Klasse</span><span class="sxs-lookup"><span data-stu-id="69235-103">TypeCtrlAltDel method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="69235-104">Simuliert eine Tastenkombination STRG + ALT + ENTF.</span><span class="sxs-lookup"><span data-stu-id="69235-104">Simulates a Ctrl+Alt+Del key sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="69235-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69235-105">Syntax</span></span>


```mof
uint32 TypeCtrlAltDel();
```



## <a name="parameters"></a><span data-ttu-id="69235-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="69235-106">Parameters</span></span>

<span data-ttu-id="69235-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="69235-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69235-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69235-108">Return value</span></span>

<span data-ttu-id="69235-109">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69235-109">Type: **uint32**</span></span>

<span data-ttu-id="69235-110">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="69235-110">A return value of zero indicates success.</span></span> <span data-ttu-id="69235-111">Ein Wert ungleich NULL gibt an, dass ein Fehler beim Senden nicht vorliegt.</span><span class="sxs-lookup"><span data-stu-id="69235-111">A nonzero value indicates a failure to send.</span></span>

<dl> <dt>

<span data-ttu-id="69235-112">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="69235-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="69235-113">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="69235-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="69235-114">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="69235-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="69235-115">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="69235-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="69235-116">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="69235-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="69235-117">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="69235-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="69235-118">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="69235-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="69235-119">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="69235-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="69235-120">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="69235-120">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="69235-121">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="69235-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="69235-122">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="69235-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="69235-123">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="69235-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="69235-124">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="69235-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="69235-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69235-125">Remarks</span></span>

<span data-ttu-id="69235-126">Der Zugriff auf die [**MSVM- \_ Tastatur**](msvm-keyboard.md) Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="69235-126">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="69235-127">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="69235-127">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="69235-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69235-128">Requirements</span></span>



| <span data-ttu-id="69235-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69235-129">Requirement</span></span> | <span data-ttu-id="69235-130">Wert</span><span class="sxs-lookup"><span data-stu-id="69235-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69235-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69235-131">Minimum supported client</span></span><br/> | <span data-ttu-id="69235-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69235-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="69235-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69235-133">Minimum supported server</span></span><br/> | <span data-ttu-id="69235-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69235-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69235-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="69235-135">Namespace</span></span><br/>                | <span data-ttu-id="69235-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="69235-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="69235-137">MOF</span><span class="sxs-lookup"><span data-stu-id="69235-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69235-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="69235-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69235-139">DLL</span><span class="sxs-lookup"><span data-stu-id="69235-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69235-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69235-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="69235-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69235-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69235-142">**MSVM- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="69235-142">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

