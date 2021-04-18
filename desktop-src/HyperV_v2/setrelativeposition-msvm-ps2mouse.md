---
description: Versetzt die Position des Mauszeigers um das angegebene horizontale und vertikale Delta.
ms.assetid: C74E4BEA-C7E1-44C7-B4FC-8926F23DF1FE
title: Die Methode "settrelativeposition" der Msvm_Ps2Mouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetRelativePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b7f4d10f48bce4b33cd4965f08633b85b5a738bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348109"
---
# <a name="setrelativeposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="54baa-103">Die Methode "settrelativeposition" der MSVM- \_ Klasse "Ps2Mouse"</span><span class="sxs-lookup"><span data-stu-id="54baa-103">SetRelativePosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="54baa-104">Versetzt die Position des Mauszeigers um das angegebene horizontale und vertikale Delta.</span><span class="sxs-lookup"><span data-stu-id="54baa-104">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span>

## <a name="syntax"></a><span data-ttu-id="54baa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54baa-105">Syntax</span></span>


```mof
uint32 SetRelativePosition(
  [in] sint8 horizontalDelta,
  [in] sint8 verticalDelta
);
```



## <a name="parameters"></a><span data-ttu-id="54baa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54baa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54baa-107">*horizontaldelta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54baa-107">*horizontalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54baa-108">Typ: **sint8**</span><span class="sxs-lookup"><span data-stu-id="54baa-108">Type: **sint8**</span></span>

<span data-ttu-id="54baa-109">Die horizontale Änderung der Mausposition in Pixel.</span><span class="sxs-lookup"><span data-stu-id="54baa-109">The horizontal change for the mouse position, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="54baa-110">*verticaldelta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54baa-110">*verticalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54baa-111">Typ: **sint8**</span><span class="sxs-lookup"><span data-stu-id="54baa-111">Type: **sint8**</span></span>

<span data-ttu-id="54baa-112">Die vertikale Änderung der Mausposition in Pixel.</span><span class="sxs-lookup"><span data-stu-id="54baa-112">The vertical change for the mouse position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54baa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54baa-113">Return value</span></span>

<span data-ttu-id="54baa-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54baa-114">Type: **uint32**</span></span>

<span data-ttu-id="54baa-115">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="54baa-115">A return value of zero indicates success.</span></span> <span data-ttu-id="54baa-116">Ein Wert ungleich 0 (null) gibt an, dass die Mausposition nicht geändert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="54baa-116">A nonzero value indicates a failure to alter the mouse position.</span></span>

<dl> <dt>

<span data-ttu-id="54baa-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="54baa-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="54baa-118">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="54baa-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="54baa-119">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="54baa-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="54baa-120">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="54baa-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="54baa-121">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="54baa-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="54baa-122">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="54baa-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="54baa-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="54baa-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="54baa-124">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="54baa-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="54baa-125">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="54baa-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="54baa-126">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="54baa-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="54baa-127">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="54baa-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="54baa-128">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="54baa-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="54baa-129">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="54baa-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="54baa-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54baa-130">Remarks</span></span>

<span data-ttu-id="54baa-131">Der Zugriff auf die [**MSVM- \_ Ps2Mouse**](msvm-ps2mouse.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="54baa-131">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="54baa-132">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="54baa-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="54baa-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54baa-133">Requirements</span></span>



| <span data-ttu-id="54baa-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54baa-134">Requirement</span></span> | <span data-ttu-id="54baa-135">Wert</span><span class="sxs-lookup"><span data-stu-id="54baa-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54baa-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54baa-136">Minimum supported client</span></span><br/> | <span data-ttu-id="54baa-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54baa-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="54baa-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54baa-138">Minimum supported server</span></span><br/> | <span data-ttu-id="54baa-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54baa-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="54baa-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="54baa-140">Namespace</span></span><br/>                | <span data-ttu-id="54baa-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="54baa-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="54baa-142">MOF</span><span class="sxs-lookup"><span data-stu-id="54baa-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54baa-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="54baa-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="54baa-144">DLL</span><span class="sxs-lookup"><span data-stu-id="54baa-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54baa-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="54baa-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="54baa-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54baa-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54baa-147">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="54baa-147">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

