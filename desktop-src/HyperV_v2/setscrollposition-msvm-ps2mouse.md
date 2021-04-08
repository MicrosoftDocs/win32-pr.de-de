---
description: Passt die z-Koordinate des Rad-Steuer Elements des Zeige Geräts an.
ms.assetid: FF1929EE-4A2D-4761-8919-488369FAEE1F
title: Setscrollposition-Methode der Msvm_Ps2Mouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffec8e05acf2210c55038edde5def8373e900ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866383"
---
# <a name="setscrollposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="1c35a-103">Setscrollposition-Methode der Ps2Mouse-Klasse von MSVM \_</span><span class="sxs-lookup"><span data-stu-id="1c35a-103">SetScrollPosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="1c35a-104">Passt die z-Koordinate des Rad-Steuer Elements des Zeige Geräts an.</span><span class="sxs-lookup"><span data-stu-id="1c35a-104">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span> <span data-ttu-id="1c35a-105">Werte, die in diese Eigenschaft geschrieben werden, sind immer relative Koordinaten Offsets.</span><span class="sxs-lookup"><span data-stu-id="1c35a-105">Values written to this property are always relative coordinate offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c35a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c35a-106">Syntax</span></span>


```mof
uint32 SetScrollPosition(
  [in] sint8 scrollPositionDelta
);
```



## <a name="parameters"></a><span data-ttu-id="1c35a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c35a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c35a-108">*scrollpositiondelta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c35a-108">*scrollPositionDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c35a-109">Typ: **sint8**</span><span class="sxs-lookup"><span data-stu-id="1c35a-109">Type: **sint8**</span></span>

<span data-ttu-id="1c35a-110">Das Delta der Scrollposition.</span><span class="sxs-lookup"><span data-stu-id="1c35a-110">The delta of the scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c35a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c35a-111">Return value</span></span>

<span data-ttu-id="1c35a-112">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c35a-112">Type: **uint32**</span></span>

<span data-ttu-id="1c35a-113">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="1c35a-113">A return value of zero indicates success.</span></span> <span data-ttu-id="1c35a-114">Ein Wert ungleich 0 (null) gibt an, dass die Scrollposition nicht geändert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="1c35a-114">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="1c35a-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="1c35a-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1c35a-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="1c35a-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1c35a-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="1c35a-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1c35a-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="1c35a-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1c35a-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="1c35a-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1c35a-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="1c35a-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1c35a-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="1c35a-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1c35a-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="1c35a-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1c35a-123">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="1c35a-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1c35a-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="1c35a-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1c35a-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="1c35a-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1c35a-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="1c35a-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1c35a-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="1c35a-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="1c35a-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c35a-128">Remarks</span></span>

<span data-ttu-id="1c35a-129">Der Zugriff auf die [**MSVM- \_ Ps2Mouse**](msvm-ps2mouse.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="1c35a-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1c35a-130">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1c35a-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c35a-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c35a-131">Requirements</span></span>



| <span data-ttu-id="1c35a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c35a-132">Requirement</span></span> | <span data-ttu-id="1c35a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1c35a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c35a-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c35a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1c35a-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c35a-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1c35a-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c35a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1c35a-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c35a-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1c35a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c35a-138">Namespace</span></span><br/>                | <span data-ttu-id="1c35a-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1c35a-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1c35a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1c35a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c35a-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1c35a-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c35a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1c35a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c35a-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1c35a-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1c35a-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c35a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c35a-145">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="1c35a-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

