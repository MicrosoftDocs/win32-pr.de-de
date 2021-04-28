---
description: 'SetPowerState-Methode der CIM_NonVolatileStorage-Klasse: Die SetPowerState-Methode legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann ein Gerät in diesen Zustand versetzt werden soll.'
ms.assetid: fdc7dbcb-e2ef-44aa-9a4c-dcae618c5630
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_NonVolatileStorage-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NonVolatileStorage.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af733cf695ac7ac0bcccf7270929ae3b1bc08b8a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100098"
---
# <a name="setpowerstate-method-of-the-cim_nonvolatilestorage-class"></a><span data-ttu-id="57d60-103">SetPowerState-Methode der CIM \_ NonVolatileStorage-Klasse</span><span class="sxs-lookup"><span data-stu-id="57d60-103">SetPowerState method of the CIM\_NonVolatileStorage class</span></span>

<span data-ttu-id="57d60-104">Die **SetPowerState-Methode** legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="57d60-104">The **SetPowerState** method sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="57d60-105">In einer Unterklasse sollte der Satz möglicher Rückgabecodes  mithilfe eines ValueMap-Qualifizierers für die -Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="57d60-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="57d60-106">Die Zeichenfolgen, in die der **ValueMap-Inhalt** übersetzt wird, sollten auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden. </span><span class="sxs-lookup"><span data-stu-id="57d60-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="57d60-107">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="57d60-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57d60-108">Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="57d60-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="57d60-109">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="57d60-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="57d60-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="57d60-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="57d60-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="57d60-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57d60-112">*PowerState* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="57d60-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57d60-113">Ein **ValueMap-Wert,** der den gewünschten Energiezustand für dieses logische Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="57d60-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="57d60-114">1</span><span class="sxs-lookup"><span data-stu-id="57d60-114">1</span></span>
</dt> <dd>

<span data-ttu-id="57d60-115">Volle Leistung.</span><span class="sxs-lookup"><span data-stu-id="57d60-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="57d60-116">2</span><span class="sxs-lookup"><span data-stu-id="57d60-116">2</span></span>
</dt> <dd>

<span data-ttu-id="57d60-117">Energiesparmodus mit geringer Leistung.</span><span class="sxs-lookup"><span data-stu-id="57d60-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="57d60-118">3</span><span class="sxs-lookup"><span data-stu-id="57d60-118">3</span></span>
</dt> <dd>

<span data-ttu-id="57d60-119">Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="57d60-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="57d60-120">4</span><span class="sxs-lookup"><span data-stu-id="57d60-120">4</span></span>
</dt> <dd>

<span data-ttu-id="57d60-121">Andere Energie speichern.</span><span class="sxs-lookup"><span data-stu-id="57d60-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="57d60-122">5</span><span class="sxs-lookup"><span data-stu-id="57d60-122">5</span></span>
</dt> <dd>

<span data-ttu-id="57d60-123">Energiezyklus.</span><span class="sxs-lookup"><span data-stu-id="57d60-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="57d60-124">6</span><span class="sxs-lookup"><span data-stu-id="57d60-124">6</span></span>
</dt> <dd>

<span data-ttu-id="57d60-125">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="57d60-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="57d60-126">*Zeit* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="57d60-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57d60-127">Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervallwert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="57d60-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="57d60-128">Wenn der *PowerState-Parameter* gleich 5 ist ("Power Cycle"), gibt der *Time-Parameter* an, wann das Gerät erneut eingeschaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="57d60-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="57d60-129">Das Ausschalten ist sofort.</span><span class="sxs-lookup"><span data-stu-id="57d60-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57d60-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57d60-130">Return value</span></span>

<span data-ttu-id="57d60-131">Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState-* und *Time-Anforderung* nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="57d60-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="57d60-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57d60-132">Remarks</span></span>

<span data-ttu-id="57d60-133">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="57d60-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="57d60-134">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="57d60-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="57d60-135">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="57d60-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="57d60-136">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="57d60-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="57d60-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57d60-137">Requirements</span></span>



| <span data-ttu-id="57d60-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57d60-138">Requirement</span></span> | <span data-ttu-id="57d60-139">Wert</span><span class="sxs-lookup"><span data-stu-id="57d60-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57d60-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57d60-140">Minimum supported client</span></span><br/> | <span data-ttu-id="57d60-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57d60-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="57d60-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57d60-142">Minimum supported server</span></span><br/> | <span data-ttu-id="57d60-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57d60-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="57d60-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="57d60-144">Namespace</span></span><br/>                | <span data-ttu-id="57d60-145">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="57d60-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="57d60-146">MOF</span><span class="sxs-lookup"><span data-stu-id="57d60-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57d60-147"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="57d60-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="57d60-148">DLL</span><span class="sxs-lookup"><span data-stu-id="57d60-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57d60-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57d60-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57d60-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="57d60-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57d60-151">CIM \_ NonVolatileStorage</span><span class="sxs-lookup"><span data-stu-id="57d60-151">CIM\_NonVolatileStorage</span></span>](setpowerstate-method-in-class-cim-nonvolatilestorage.md)
</dt> <dt>

[<span data-ttu-id="57d60-152">**CIM \_ NonVolatileStorage**</span><span class="sxs-lookup"><span data-stu-id="57d60-152">**CIM\_NonVolatileStorage**</span></span>](cim-nonvolatilestorage.md)
</dt> </dl>

 

 




