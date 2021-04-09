---
description: Legt die horizontale und vertikale Position des Mauszeigers fest.
ms.assetid: 7845E10A-7F61-4134-BF81-AED5483F36AD
title: Die Methode "settabsoluteposition" der Msvm_SyntheticMouse Klasse ("dbdao. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetAbsolutePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b8ffb3a4d415f76dedf30acba5869b4cc585eb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864888"
---
# <a name="setabsoluteposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="3fb3c-103">SetAbsolutePosition-Methode der MSVM- \_ syntheticmouse-Klasse</span><span class="sxs-lookup"><span data-stu-id="3fb3c-103">SetAbsolutePosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="3fb3c-104">Legt die horizontale und vertikale Position des Mauszeigers fest.</span><span class="sxs-lookup"><span data-stu-id="3fb3c-104">Sets the horizontal and vertical position of the mouse cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb3c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fb3c-105">Syntax</span></span>


```mof
uint32 SetAbsolutePosition(
  [in] sint32 horizontalPosition,
  [in] sint32 verticalPosition
);
```



## <a name="parameters"></a><span data-ttu-id="3fb3c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fb3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fb3c-107">*HorizontalPosition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fb3c-107">*horizontalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb3c-108">Typ: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3fb3c-108">Type: **sint32**</span></span>

<span data-ttu-id="3fb3c-109">Die neue horizontale Position des Mauszeigers in Pixel.</span><span class="sxs-lookup"><span data-stu-id="3fb3c-109">The new horizontal position of the mouse cursor, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="3fb3c-110">*VerticalPosition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fb3c-110">*verticalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb3c-111">Typ: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3fb3c-111">Type: **sint32**</span></span>

<span data-ttu-id="3fb3c-112">Die neue vertikale Position des Mauszeigers in Pixel.</span><span class="sxs-lookup"><span data-stu-id="3fb3c-112">The new vertical position of the mouse cursor, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fb3c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3fb3c-113">Return value</span></span>

<span data-ttu-id="3fb3c-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3fb3c-114">Type: **uint32**</span></span>

<span data-ttu-id="3fb3c-115">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="3fb3c-115">A return value of zero indicates success.</span></span> <span data-ttu-id="3fb3c-116">Ein Wert ungleich 0 (null) gibt an, dass die Scrollposition nicht geändert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="3fb3c-116">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="3fb3c-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="3fb3c-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3fb3c-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="3fb3c-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3fb3c-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="3fb3c-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3fb3c-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="3fb3c-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3fb3c-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="3fb3c-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3fb3c-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="3fb3c-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3fb3c-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3fb3c-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3fb3c-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="3fb3c-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3fb3c-125">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="3fb3c-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3fb3c-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="3fb3c-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3fb3c-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="3fb3c-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3fb3c-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="3fb3c-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3fb3c-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="3fb3c-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3fb3c-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fb3c-130">Remarks</span></span>

<span data-ttu-id="3fb3c-131">Der Zugriff auf die [**MSVM \_ syntheticmouse**](msvm-syntheticmouse.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="3fb3c-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3fb3c-132">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3fb3c-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb3c-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fb3c-133">Requirements</span></span>



| <span data-ttu-id="3fb3c-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fb3c-134">Requirement</span></span> | <span data-ttu-id="3fb3c-135">Wert</span><span class="sxs-lookup"><span data-stu-id="3fb3c-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb3c-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3fb3c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb3c-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fb3c-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3fb3c-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3fb3c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb3c-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fb3c-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3fb3c-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="3fb3c-140">Namespace</span></span><br/>                | <span data-ttu-id="3fb3c-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3fb3c-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3fb3c-142">Header</span><span class="sxs-lookup"><span data-stu-id="3fb3c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fb3c-143"><dt>Dbdao. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fb3c-143"><dt>Dbdao.h</dt></span></span> </dl>                      |
| <span data-ttu-id="3fb3c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="3fb3c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fb3c-145"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3fb3c-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fb3c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="3fb3c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fb3c-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3fb3c-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3fb3c-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fb3c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb3c-149">**MSVM \_ syntheticmouse**</span><span class="sxs-lookup"><span data-stu-id="3fb3c-149">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

