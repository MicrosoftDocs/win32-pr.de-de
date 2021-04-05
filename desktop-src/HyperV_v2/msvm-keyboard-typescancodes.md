---
description: Simuliert eine Schlüssel Sequenz mithilfe von Scan Codes.
ms.assetid: F67D2FBA-3CE0-4135-9043-FAB59381DE3C
title: Typescancodes-Methode der Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeScancodes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 97479a1a0926894f72472b7459f77cd9325ac6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752360"
---
# <a name="typescancodes-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="84948-103">Typescancodes-Methode der MSVM- \_ Tastatur Klasse</span><span class="sxs-lookup"><span data-stu-id="84948-103">TypeScancodes method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="84948-104">Simuliert eine Schlüssel Sequenz mithilfe von Scan Codes.</span><span class="sxs-lookup"><span data-stu-id="84948-104">Simulates a key sequence using scan codes.</span></span>

## <a name="syntax"></a><span data-ttu-id="84948-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="84948-105">Syntax</span></span>


```mof
uint32 TypeScancodes(
  [in] uint8 Scancodes[]
);
```



## <a name="parameters"></a><span data-ttu-id="84948-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84948-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84948-107">*Scancodes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84948-107">*Scancodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84948-108">Typ: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="84948-108">Type: **uint8\[\]**</span></span>

<span data-ttu-id="84948-109">Ein Array, das die zu Typ enden Scan Codes enthält.</span><span class="sxs-lookup"><span data-stu-id="84948-109">An array that contains the scan codes to type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84948-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84948-110">Return value</span></span>

<span data-ttu-id="84948-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84948-111">Type: **uint32**</span></span>

<span data-ttu-id="84948-112">Diese Methode gibt 0 zurück, wenn Sie erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84948-112">This method returns 0 if it succeeds.</span></span> <span data-ttu-id="84948-113">Jeder andere Rückgabewert gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="84948-113">Any other return value indicates an error.</span></span> <span data-ttu-id="84948-114">Der Rückgabewert kann einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="84948-114">The return value can be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="84948-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="84948-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84948-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="84948-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="84948-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="84948-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="84948-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="84948-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="84948-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="84948-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="84948-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="84948-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="84948-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="84948-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="84948-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="84948-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="84948-123">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="84948-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="84948-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="84948-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="84948-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="84948-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="84948-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="84948-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="84948-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="84948-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="84948-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84948-128">Remarks</span></span>

<span data-ttu-id="84948-129">Der Zugriff auf die [**MSVM- \_ Tastatur**](msvm-keyboard.md) Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="84948-129">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="84948-130">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="84948-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="84948-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84948-131">Requirements</span></span>



| <span data-ttu-id="84948-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84948-132">Requirement</span></span> | <span data-ttu-id="84948-133">Wert</span><span class="sxs-lookup"><span data-stu-id="84948-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84948-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84948-134">Minimum supported client</span></span><br/> | <span data-ttu-id="84948-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84948-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="84948-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84948-136">Minimum supported server</span></span><br/> | <span data-ttu-id="84948-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84948-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84948-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="84948-138">Namespace</span></span><br/>                | <span data-ttu-id="84948-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="84948-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="84948-140">MOF</span><span class="sxs-lookup"><span data-stu-id="84948-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84948-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="84948-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84948-142">DLL</span><span class="sxs-lookup"><span data-stu-id="84948-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84948-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84948-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84948-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84948-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84948-145">**MSVM- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="84948-145">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

