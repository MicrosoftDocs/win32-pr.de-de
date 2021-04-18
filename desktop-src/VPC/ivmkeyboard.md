---
title: Ivmkeyboard-Schnittstelle (vpccominterfaces. h)
description: Steuert das Tastatur Gerät innerhalb einer virtuellen Maschine. Die ivmkeyboard für eine virtuelle Maschine kann mithilfe der ivmvirtualmachine-Tastatur Eigenschaft abgerufen werden.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- Ivmkeyboard Interface Virtual PC
- Virtueller Computer für ivmkeyboard Interface, beschrieben
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce2ddddd00de509278760a22fe3ab464f27c1c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340374"
---
# <a name="ivmkeyboard-interface"></a><span data-ttu-id="73308-106">Ivmkeyboard-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="73308-106">IVMKeyboard interface</span></span>

<span data-ttu-id="73308-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="73308-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="73308-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="73308-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="73308-109">Steuert das Tastatur Gerät innerhalb einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="73308-109">Controls the keyboard device within a virtual machine.</span></span> <span data-ttu-id="73308-110">Die **ivmkeyboard** für eine virtuelle Maschine kann mithilfe der [**ivmvirtualmachine:: Keyboard**](ivmvirtualmachine-keyboard.md) -Eigenschaft abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="73308-110">The **IVMKeyboard** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Keyboard**](ivmvirtualmachine-keyboard.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="73308-111">Member</span><span class="sxs-lookup"><span data-stu-id="73308-111">Members</span></span>

<span data-ttu-id="73308-112">Die **ivmkeyboard** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="73308-112">The **IVMKeyboard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="73308-113">**Ivmkeyboard** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="73308-113">**IVMKeyboard** also has these types of members:</span></span>

-   [<span data-ttu-id="73308-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="73308-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="73308-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73308-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="73308-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="73308-116">Methods</span></span>

<span data-ttu-id="73308-117">Die **ivmkeyboard** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="73308-117">The **IVMKeyboard** interface has these methods.</span></span>



| <span data-ttu-id="73308-118">Methode</span><span class="sxs-lookup"><span data-stu-id="73308-118">Method</span></span>                                                       | <span data-ttu-id="73308-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73308-119">Description</span></span>                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="73308-120">**Igestreout**</span><span class="sxs-lookup"><span data-stu-id="73308-120">**IsPressed**</span></span>](ivmkeyboard-ispressed.md)                   | <span data-ttu-id="73308-121">Bestimmt, ob der angegebene Schlüssel nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="73308-121">Determines whether the specified key is down.</span></span><br/>                      |
| [<span data-ttu-id="73308-122">**Pressandreleasekey**</span><span class="sxs-lookup"><span data-stu-id="73308-122">**PressAndReleaseKey**</span></span>](ivmkeyboard-pressandreleasekey.md) | <span data-ttu-id="73308-123">Simuliert, dass eine Taste gedrückt und anschließend freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="73308-123">Simulates a key being pressed down and then released.</span></span><br/>              |
| [<span data-ttu-id="73308-124">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="73308-124">**PressKey**</span></span>](ivmkeyboard-presskey.md)                     | <span data-ttu-id="73308-125">Simuliert, dass eine Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="73308-125">Simulates a key being pressed down.</span></span><br/>                                |
| [<span data-ttu-id="73308-126">**Releasekey**</span><span class="sxs-lookup"><span data-stu-id="73308-126">**ReleaseKey**</span></span>](ivmkeyboard-releasekey.md)                 | <span data-ttu-id="73308-127">Simuliert einen Schlüssel, der freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="73308-127">Simulates a key being released.</span></span><br/>                                    |
| [<span data-ttu-id="73308-128">**Tybäuerciitext**</span><span class="sxs-lookup"><span data-stu-id="73308-128">**TypeAsciiText**</span></span>](ivmkeyboard-typeasciitext.md)           | <span data-ttu-id="73308-129">Simuliert eine Reihe von ASCII-Schlüsseln, die in den Gast eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="73308-129">Simulates a series of ASCII keys being typed into the guest.</span></span><br/>       |
| [<span data-ttu-id="73308-130">**Typekeysequence**</span><span class="sxs-lookup"><span data-stu-id="73308-130">**TypeKeySequence**</span></span>](ivmkeyboard-typekeysequence.md)       | <span data-ttu-id="73308-131">Simuliert eine durch Trennzeichen getrennte Liste mit Schlüsseln, die in den Gast eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="73308-131">Simulates a comma-delimited list of keys being typed in the guest.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="73308-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="73308-132">Properties</span></span>

<span data-ttu-id="73308-133">Die **ivmkeyboard** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="73308-133">The **IVMKeyboard** interface has these properties.</span></span>



| <span data-ttu-id="73308-134">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="73308-134">Property</span></span>                                                                | <span data-ttu-id="73308-135">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="73308-135">Access type</span></span>           | <span data-ttu-id="73308-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73308-136">Description</span></span>                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73308-137">**Hasexclusiveaccess**</span><span class="sxs-lookup"><span data-stu-id="73308-137">**HasExclusiveAccess**</span></span>](ivmkeyboard-hasexclusiveaccess.md)<br/> | <span data-ttu-id="73308-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="73308-138">Read/write</span></span><br/> | <span data-ttu-id="73308-139">Gibt an, ob dieses-Objekt über eine exklusive Kontrolle über das Tastatur Gerät der virtuellen Maschine verfügt.</span><span class="sxs-lookup"><span data-stu-id="73308-139">Indicates whether this object has exclusive control over the virtual machine's keyboard device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="73308-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73308-140">Remarks</span></span>

<span data-ttu-id="73308-141">Schlüssel können auf verschiedene Arten in den virtuellen Computer eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="73308-141">Keys can be typed into the virtual machine in several ways.</span></span> <span data-ttu-id="73308-142">Verwenden Sie die [**tybäuerciitext**](ivmkeyboard-typeasciitext.md) -Methode, um eine normale ASCII-Zeichenfolge einzugeben.</span><span class="sxs-lookup"><span data-stu-id="73308-142">To type a normal ASCII sequence of characters, use the [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) method.</span></span> <span data-ttu-id="73308-143">Wenn mehr Flexibilität erforderlich ist, verfügt **ivmkeyboard** über mehrere Methoden, die für die Verwendung mit den Schlüsselcodes in der folgenden Liste konzipiert sind.</span><span class="sxs-lookup"><span data-stu-id="73308-143">If greater flexibility is required, **IVMKeyboard** has several methods that are designed to be used with the key codes in the following list.</span></span> <span data-ttu-id="73308-144">Die [**typekeysequence**](ivmkeyboard-typekeysequence.md) -Methode kann eine durch Trennzeichen getrennte Zeichenfolge von Schlüsselcodes akzeptieren, die in der angegebenen Reihenfolge innerhalb des virtuellen Computers gedrückt und freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="73308-144">The [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) method can accept a comma-delimited string of key codes, which will be pressed and released, in order, within the virtual machine.</span></span> <span data-ttu-id="73308-145">Zusätzlich zu diesen Schlüsselcodes können die Schlüsselwörter "hoch" und "nach unten" verwendet werden, um zu erzwingen, dass eine Taste gedrückt wird oder nur freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="73308-145">In addition to these key codes, the keywords UP and DOWN can be used to force a key to only be pressed, or only be released.</span></span> <span data-ttu-id="73308-146">Die Schlüsselwörter "up" und "Down" gelten nur für den Schlüsselcode, der direkt auf das Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="73308-146">The UP and DOWN keywords only apply to the key code directly following the keyword.</span></span>

<span data-ttu-id="73308-147">Um zu vermeiden, dass mehrere Skripts, Anwendungen oder Benutzer gleichzeitig versuchen, auf dasselbe Tastatur Gerät zuzugreifen, legen Sie die [**hasexclusiveaccess**](ivmkeyboard-hasexclusiveaccess.md) -Eigenschaft auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="73308-147">To avoid multiple scripts, applications, or users from simultaneously attempting to access the same keyboard device, set the [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) property to **TRUE**.</span></span> <span data-ttu-id="73308-148">Wenn exklusiver Zugriff von einem Prozess abgerufen wird, werden alle Versuche anderer Prozesse, Eingaben an das Tastatur Gerät zu senden, ignoriert, bis der exklusive Zugriff aufgehoben wurde.</span><span class="sxs-lookup"><span data-stu-id="73308-148">If exclusive access is acquired by one process, any attempts by other processes to send input to the keyboard device will be ignored until exclusive access has been released.</span></span>

## <a name="requirements"></a><span data-ttu-id="73308-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73308-149">Requirements</span></span>



| <span data-ttu-id="73308-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73308-150">Requirement</span></span> | <span data-ttu-id="73308-151">Wert</span><span class="sxs-lookup"><span data-stu-id="73308-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="73308-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73308-152">Minimum supported client</span></span><br/> | <span data-ttu-id="73308-153">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73308-153">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73308-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73308-154">Minimum supported server</span></span><br/> | <span data-ttu-id="73308-155">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="73308-155">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="73308-156">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="73308-156">End of client support</span></span><br/>    | <span data-ttu-id="73308-157">Windows 7</span><span class="sxs-lookup"><span data-stu-id="73308-157">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="73308-158">Produkt</span><span class="sxs-lookup"><span data-stu-id="73308-158">Product</span></span><br/>                  | <span data-ttu-id="73308-159">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="73308-159">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="73308-160">Header</span><span class="sxs-lookup"><span data-stu-id="73308-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="73308-161"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="73308-161"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="73308-162">IID</span><span class="sxs-lookup"><span data-stu-id="73308-162">IID</span></span><br/>                      | <span data-ttu-id="73308-163">IID \_ ivmkeyboard ist als 00695b2e-c5ad-4d6e-B1ab-336ed121f 8c4 definiert.</span><span class="sxs-lookup"><span data-stu-id="73308-163">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="73308-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73308-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73308-165">Windows Virtual PC-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="73308-165">Windows Virtual PC Interfaces</span></span>](virtual-pc-interfaces.md)
</dt> <dt>

[<span data-ttu-id="73308-166">Schlüsselsequenzen</span><span class="sxs-lookup"><span data-stu-id="73308-166">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

