---
description: Legt die z-Koordinate des Steuer Elements für das Mausrad fest.
ms.assetid: 02349957-6BAA-42E7-B3D4-F39E748615E6
title: Setscrollposition-Methode der Msvm_SyntheticMouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6d82ad2cd75b41ca914d0db49d5de4709790ea6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131877"
---
# <a name="setscrollposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="67bf5-103">Setscrollposition-Methode der MSVM \_ syntheticmouse-Klasse</span><span class="sxs-lookup"><span data-stu-id="67bf5-103">SetScrollPosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="67bf5-104">Legt die z-Koordinate des Steuer Elements für das Mausrad fest.</span><span class="sxs-lookup"><span data-stu-id="67bf5-104">Sets the z-coordinate of the wheel control of the pointing device.</span></span> <span data-ttu-id="67bf5-105">Werte, die in diese Eigenschaft geschrieben werden, sind immer relative Koordinaten Offsets.</span><span class="sxs-lookup"><span data-stu-id="67bf5-105">Values written to this property are always relative coordinate offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="67bf5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="67bf5-106">Syntax</span></span>


```mof
uint32 SetScrollPosition(
  [in] sint32 scrollPositionDelta
);
```



## <a name="parameters"></a><span data-ttu-id="67bf5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="67bf5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67bf5-108">*scrollpositiondelta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67bf5-108">*scrollPositionDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67bf5-109">Typ: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67bf5-109">Type: **sint32**</span></span>

<span data-ttu-id="67bf5-110">Das Delta der Scrollposition.</span><span class="sxs-lookup"><span data-stu-id="67bf5-110">The delta of the scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67bf5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67bf5-111">Return value</span></span>

<span data-ttu-id="67bf5-112">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67bf5-112">Type: **uint32**</span></span>

<span data-ttu-id="67bf5-113">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="67bf5-113">A return value of zero indicates success.</span></span> <span data-ttu-id="67bf5-114">Ein Wert ungleich 0 (null) gibt an, dass die Scrollposition nicht geändert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="67bf5-114">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="67bf5-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="67bf5-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="67bf5-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="67bf5-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="67bf5-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="67bf5-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="67bf5-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="67bf5-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="67bf5-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="67bf5-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="67bf5-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="67bf5-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="67bf5-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="67bf5-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="67bf5-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="67bf5-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="67bf5-123">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="67bf5-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="67bf5-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="67bf5-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="67bf5-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="67bf5-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="67bf5-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="67bf5-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="67bf5-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="67bf5-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="67bf5-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67bf5-128">Remarks</span></span>

<span data-ttu-id="67bf5-129">Der Zugriff auf die [**MSVM \_ syntheticmouse**](msvm-syntheticmouse.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="67bf5-129">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="67bf5-130">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="67bf5-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="67bf5-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67bf5-131">Requirements</span></span>



| <span data-ttu-id="67bf5-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67bf5-132">Requirement</span></span> | <span data-ttu-id="67bf5-133">Wert</span><span class="sxs-lookup"><span data-stu-id="67bf5-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67bf5-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67bf5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="67bf5-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67bf5-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="67bf5-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67bf5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="67bf5-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67bf5-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67bf5-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="67bf5-138">Namespace</span></span><br/>                | <span data-ttu-id="67bf5-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="67bf5-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="67bf5-140">MOF</span><span class="sxs-lookup"><span data-stu-id="67bf5-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67bf5-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="67bf5-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67bf5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="67bf5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67bf5-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67bf5-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67bf5-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67bf5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67bf5-145">**MSVM \_ syntheticmouse**</span><span class="sxs-lookup"><span data-stu-id="67bf5-145">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

