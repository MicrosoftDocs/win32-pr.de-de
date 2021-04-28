---
description: 'SetPowerState-Methode der CIM_BinarySensor-Klasse: Die SetPowerState-Methode legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann das Gerät in diesen Zustand versetzt werden soll.'
ms.assetid: bf5bdc90-9735-47b8-87d5-8f2482e603ed
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_BinarySensor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BinarySensor.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fd18c9f5761cac208f8682bbc3c8f189cf0aefe0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089508"
---
# <a name="setpowerstate-method-of-the-cim_binarysensor-class"></a><span data-ttu-id="a2c49-103">SetPowerState-Methode der CIM \_ BinarySensor-Klasse</span><span class="sxs-lookup"><span data-stu-id="a2c49-103">SetPowerState method of the CIM\_BinarySensor class</span></span>

<span data-ttu-id="a2c49-104">Die **SetPowerState-Methode** legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann das Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2c49-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span>

<span data-ttu-id="a2c49-105">In einer Unterklasse sollte der Satz möglicher Rückgabecodes mithilfe eines **ValueMap-Qualifizierers** für die -Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a2c49-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="a2c49-106">Die Zeichenfolgen, in die der **ValueMap-Inhalt** übersetzt wird, sollten auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden. </span><span class="sxs-lookup"><span data-stu-id="a2c49-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="a2c49-107">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a2c49-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2c49-108">Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a2c49-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a2c49-109">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="a2c49-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a2c49-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2c49-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="a2c49-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2c49-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2c49-112">*PowerState* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a2c49-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2c49-113">Ein **ValueMap-Wert,** der den gewünschten Energiezustand für das logische Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="a2c49-113">A **ValueMap** value that specifies the desired power state for the logical device.</span></span>

<dt>

<span data-ttu-id="a2c49-114">1</span><span class="sxs-lookup"><span data-stu-id="a2c49-114">1</span></span>
</dt> <dd>

<span data-ttu-id="a2c49-115">Volle Leistung.</span><span class="sxs-lookup"><span data-stu-id="a2c49-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="a2c49-116">2</span><span class="sxs-lookup"><span data-stu-id="a2c49-116">2</span></span>
</dt> <dd>

<span data-ttu-id="a2c49-117">Energiesparmodus mit geringer Leistung.</span><span class="sxs-lookup"><span data-stu-id="a2c49-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="a2c49-118">3</span><span class="sxs-lookup"><span data-stu-id="a2c49-118">3</span></span>
</dt> <dd>

<span data-ttu-id="a2c49-119">Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="a2c49-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="a2c49-120">4</span><span class="sxs-lookup"><span data-stu-id="a2c49-120">4</span></span>
</dt> <dd>

<span data-ttu-id="a2c49-121">Andere Energie speichern.</span><span class="sxs-lookup"><span data-stu-id="a2c49-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="a2c49-122">5</span><span class="sxs-lookup"><span data-stu-id="a2c49-122">5</span></span>
</dt> <dd>

<span data-ttu-id="a2c49-123">Energiezyklus.</span><span class="sxs-lookup"><span data-stu-id="a2c49-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="a2c49-124">6</span><span class="sxs-lookup"><span data-stu-id="a2c49-124">6</span></span>
</dt> <dd>

<span data-ttu-id="a2c49-125">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="a2c49-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a2c49-126">*Zeit* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a2c49-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2c49-127">Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervallwert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="a2c49-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="a2c49-128">Wenn der *PowerState-Parameter* gleich 5 ist ("Power Cycle"), gibt der *Time-Parameter* an, wann das Gerät erneut eingeschaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2c49-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power-on again.</span></span> <span data-ttu-id="a2c49-129">Das Ausschalten ist sofort.</span><span class="sxs-lookup"><span data-stu-id="a2c49-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2c49-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2c49-130">Return value</span></span>

<span data-ttu-id="a2c49-131">Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState-* und *Time-Anforderung* nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a2c49-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2c49-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2c49-132">Remarks</span></span>

<span data-ttu-id="a2c49-133">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="a2c49-133">Currently, this method is not implemented by WMI.</span></span> <span data-ttu-id="a2c49-134">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="a2c49-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a2c49-135">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="a2c49-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a2c49-136">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="a2c49-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2c49-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2c49-137">Requirements</span></span>



| <span data-ttu-id="a2c49-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2c49-138">Requirement</span></span> | <span data-ttu-id="a2c49-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a2c49-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c49-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2c49-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a2c49-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2c49-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2c49-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2c49-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a2c49-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2c49-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2c49-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2c49-144">Namespace</span></span><br/>                | <span data-ttu-id="a2c49-145">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="a2c49-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2c49-146">MOF</span><span class="sxs-lookup"><span data-stu-id="a2c49-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2c49-147"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2c49-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2c49-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a2c49-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2c49-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2c49-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2c49-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a2c49-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c49-151">CIM \_ BinarySensor</span><span class="sxs-lookup"><span data-stu-id="a2c49-151">CIM\_BinarySensor</span></span>](setpowerstate-method-in-class-cim-binarysensor.md)
</dt> <dt>

[<span data-ttu-id="a2c49-152">**CIM \_ BinarySensor**</span><span class="sxs-lookup"><span data-stu-id="a2c49-152">**CIM\_BinarySensor**</span></span>](cim-binarysensor.md)
</dt> </dl>

 

 




