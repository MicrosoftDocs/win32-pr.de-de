---
description: Mit der SetUrgency-Methode wird die gewünschte Dringlichkeits Stufe für einen Alarm festgelegt.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Die-Methode der CIM_AlarmDevice-Klasse.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35918677e210ac2fe7ac4798a04db9dc628f5fa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958384"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a><span data-ttu-id="402a8-103">Die Methode "tarturgency" der CIM \_ alarmdevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="402a8-103">SetUrgency method of the CIM\_AlarmDevice class</span></span>

<span data-ttu-id="402a8-104">Mit der **SetUrgency** -Methode wird die gewünschte Dringlichkeits Stufe für einen Alarm festgelegt.</span><span class="sxs-lookup"><span data-stu-id="402a8-104">The **SetUrgency** method sets the desired urgency level for an alarm.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="402a8-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="402a8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="402a8-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="402a8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="402a8-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="402a8-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="402a8-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="402a8-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="402a8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="402a8-109">Syntax</span></span>


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a><span data-ttu-id="402a8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="402a8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="402a8-111">*RequestedUrgency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="402a8-111">*RequestedUrgency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="402a8-112">Relative Häufigkeit, mit der der Alarm blinkt, vibriert oder akustische Töne ausgibt.</span><span class="sxs-lookup"><span data-stu-id="402a8-112">Relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span> <span data-ttu-id="402a8-113">Die folgenden Werte stammen aus der Eigenschaft **Dringlichkeit** in [**CIM \_ alarmdevice**](cim-alarmdevice.md).</span><span class="sxs-lookup"><span data-stu-id="402a8-113">The following values are from the **Urgency** property in [**CIM\_AlarmDevice**](cim-alarmdevice.md).</span></span>

<dt>

<span data-ttu-id="402a8-114">0</span><span class="sxs-lookup"><span data-stu-id="402a8-114">0</span></span>
</dt> <dd>

<span data-ttu-id="402a8-115">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="402a8-115">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="402a8-116">1</span><span class="sxs-lookup"><span data-stu-id="402a8-116">1</span></span>
</dt> <dd>

<span data-ttu-id="402a8-117">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="402a8-117">Other.</span></span>

</dd> <dt>

<span data-ttu-id="402a8-118">2</span><span class="sxs-lookup"><span data-stu-id="402a8-118">2</span></span>
</dt> <dd>

<span data-ttu-id="402a8-119">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="402a8-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="402a8-120">3</span><span class="sxs-lookup"><span data-stu-id="402a8-120">3</span></span>
</dt> <dd>

<span data-ttu-id="402a8-121">Zur Information.</span><span class="sxs-lookup"><span data-stu-id="402a8-121">Informational.</span></span>

</dd> <dt>

<span data-ttu-id="402a8-122">4</span><span class="sxs-lookup"><span data-stu-id="402a8-122">4</span></span>
</dt> <dd>

<span data-ttu-id="402a8-123">Nicht kritisch.</span><span class="sxs-lookup"><span data-stu-id="402a8-123">Non-critical.</span></span>

</dd> <dt>

<span data-ttu-id="402a8-124">5</span><span class="sxs-lookup"><span data-stu-id="402a8-124">5</span></span>
</dt> <dd>

<span data-ttu-id="402a8-125">Kritisch.</span><span class="sxs-lookup"><span data-stu-id="402a8-125">Critical.</span></span>

</dd> <dt>

<span data-ttu-id="402a8-126">6</span><span class="sxs-lookup"><span data-stu-id="402a8-126">6</span></span>
</dt> <dd>

<span data-ttu-id="402a8-127">Nicht BEHEB barer.</span><span class="sxs-lookup"><span data-stu-id="402a8-127">Unrecoverable.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="402a8-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="402a8-128">Return value</span></span>

<span data-ttu-id="402a8-129">Gibt bei Erfolg den Wert 0 (null) zurück, 1 (eins), wenn die angeforderte Dringlichkeits Ebene nicht unterstützt wird, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="402a8-129">Returns a value of 0 (zero) on success, 1 (one) if the requested urgency level is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="402a8-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="402a8-130">Remarks</span></span>

<span data-ttu-id="402a8-131">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="402a8-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="402a8-132">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="402a8-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="402a8-133">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="402a8-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="402a8-134">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="402a8-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="402a8-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="402a8-135">Requirements</span></span>



| <span data-ttu-id="402a8-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="402a8-136">Requirement</span></span> | <span data-ttu-id="402a8-137">Wert</span><span class="sxs-lookup"><span data-stu-id="402a8-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="402a8-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="402a8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="402a8-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="402a8-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="402a8-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="402a8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="402a8-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="402a8-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="402a8-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="402a8-142">Namespace</span></span><br/>                | <span data-ttu-id="402a8-143">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="402a8-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="402a8-144">MOF</span><span class="sxs-lookup"><span data-stu-id="402a8-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="402a8-145"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="402a8-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="402a8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="402a8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="402a8-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="402a8-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="402a8-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="402a8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="402a8-149">CIM- \_ alarmdevice</span><span class="sxs-lookup"><span data-stu-id="402a8-149">CIM\_AlarmDevice</span></span>](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[<span data-ttu-id="402a8-150">**CIM- \_ alarmdevice**</span><span class="sxs-lookup"><span data-stu-id="402a8-150">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> </dl>

 

