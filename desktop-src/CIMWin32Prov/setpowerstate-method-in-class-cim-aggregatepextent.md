---
description: Die SetPowerState-Methode legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn das Gerät in diesen Zustand versetzt werden soll.
ms.assetid: 1a1a8d5e-d685-4b7e-99fb-61fa2e7bdafa
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_AggregatePExtent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 47c97f30da1c8b6f2fe9a6032ef9be9ae87a7d6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958430"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepextent-class"></a><span data-ttu-id="5065d-103">SetPowerState-Methode der CIM- \_ aggregatepblock-Klasse</span><span class="sxs-lookup"><span data-stu-id="5065d-103">SetPowerState method of the CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="5065d-104">Die **SetPowerState** -Methode legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn das Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5065d-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="5065d-105">In einer Unterklasse sollte der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5065d-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="5065d-106">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, sollten in der-Unterklasse auch als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5065d-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="5065d-107">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5065d-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5065d-108">Weitere Informationen zur Verwendung dieser Methode mit C/C++ finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5065d-108">For more information about using this method with C/C++, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5065d-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5065d-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5065d-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5065d-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5065d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5065d-111">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="5065d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5065d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5065d-113">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5065d-113">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5065d-114">Der **ValueMap** -Wert, der den gewünschten Energiezustand für dieses logische Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="5065d-114">The **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="5065d-115">1</span><span class="sxs-lookup"><span data-stu-id="5065d-115">1</span></span>
</dt> <dd>

<span data-ttu-id="5065d-116">Vollständige Leistung</span><span class="sxs-lookup"><span data-stu-id="5065d-116">Full power</span></span>

</dd> <dt>

<span data-ttu-id="5065d-117">2</span><span class="sxs-lookup"><span data-stu-id="5065d-117">2</span></span>
</dt> <dd>

<span data-ttu-id="5065d-118">Energiesparmodus im Energiesparmodus</span><span class="sxs-lookup"><span data-stu-id="5065d-118">Power-save   low-power mode</span></span>

</dd> <dt>

<span data-ttu-id="5065d-119">3</span><span class="sxs-lookup"><span data-stu-id="5065d-119">3</span></span>
</dt> <dd>

<span data-ttu-id="5065d-120">Energiesparmodus</span><span class="sxs-lookup"><span data-stu-id="5065d-120">Power-save   standby</span></span>

</dd> <dt>

<span data-ttu-id="5065d-121">4</span><span class="sxs-lookup"><span data-stu-id="5065d-121">4</span></span>
</dt> <dd>

<span data-ttu-id="5065d-122">Anderes Energie speichern</span><span class="sxs-lookup"><span data-stu-id="5065d-122">Power-save   other</span></span>

</dd> <dt>

<span data-ttu-id="5065d-123">5</span><span class="sxs-lookup"><span data-stu-id="5065d-123">5</span></span>
</dt> <dd>

<span data-ttu-id="5065d-124">Energie Zyklen</span><span class="sxs-lookup"><span data-stu-id="5065d-124">Power cycle</span></span>

</dd> <dt>

<span data-ttu-id="5065d-125">6</span><span class="sxs-lookup"><span data-stu-id="5065d-125">6</span></span>
</dt> <dd>

<span data-ttu-id="5065d-126">Ausschalten</span><span class="sxs-lookup"><span data-stu-id="5065d-126">Power off</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5065d-127">*Uhrzeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5065d-127">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5065d-128">Wenn der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervall Wert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="5065d-128">When the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="5065d-129">Wenn der *PowerState* -Parameter gleich 5 (Power Cycle) ist, gibt der *Zeit* Parameter an, wann das Gerät erneut einschalten soll.</span><span class="sxs-lookup"><span data-stu-id="5065d-129">When the *PowerState* parameter is equal to 5 (power cycle), the *Time* parameter indicates when the device should power-on again.</span></span> <span data-ttu-id="5065d-130">Der Ausschalten erfolgt sofort.</span><span class="sxs-lookup"><span data-stu-id="5065d-130">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5065d-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5065d-131">Return value</span></span>

<span data-ttu-id="5065d-132">Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState* -und *time* -Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5065d-132">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="5065d-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5065d-133">Remarks</span></span>

<span data-ttu-id="5065d-134">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="5065d-134">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="5065d-135">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="5065d-135">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="5065d-136">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5065d-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5065d-137">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5065d-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5065d-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5065d-138">Requirements</span></span>



| <span data-ttu-id="5065d-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5065d-139">Requirement</span></span> | <span data-ttu-id="5065d-140">Wert</span><span class="sxs-lookup"><span data-stu-id="5065d-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5065d-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5065d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5065d-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5065d-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5065d-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5065d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5065d-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5065d-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5065d-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="5065d-145">Namespace</span></span><br/>                | <span data-ttu-id="5065d-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5065d-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5065d-147">MOF</span><span class="sxs-lookup"><span data-stu-id="5065d-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5065d-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5065d-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5065d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="5065d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5065d-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5065d-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5065d-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5065d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5065d-152">**CIM- \_ aggregatepblock**</span><span class="sxs-lookup"><span data-stu-id="5065d-152">**CIM\_AggregatePExtent**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md)
</dt> <dt>

[<span data-ttu-id="5065d-153">**CIM- \_ aggregatepblock**</span><span class="sxs-lookup"><span data-stu-id="5065d-153">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> </dl>

 

