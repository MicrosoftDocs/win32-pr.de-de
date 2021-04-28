---
description: 'SetPowerState-Methode der CIM_Controller-Klasse: Die SetPowerState-Methode legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann ein Gerät in diesen Zustand gesetzt werden soll.'
ms.assetid: 442c6c2c-8e9a-476c-bb57-8b1a6439e97f
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_Controller Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7713d892643238233e9ac5469c942fdf16609512
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086228"
---
# <a name="setpowerstate-method-of-the-cim_controller-class"></a><span data-ttu-id="e2c7c-103">SetPowerState-Methode der \_ CIM-Controllerklasse</span><span class="sxs-lookup"><span data-stu-id="e2c7c-103">SetPowerState method of the CIM\_Controller class</span></span>

<span data-ttu-id="e2c7c-104">Die **SetPowerState-Methode** legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann ein Gerät in diesen Zustand gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-104">The **SetPowerState** method sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="e2c7c-105">In einer Unterklasse sollte der Satz möglicher Rückgabecodes mithilfe eines ValueMap-Qualifizierers für die -Methode angegeben werden. </span><span class="sxs-lookup"><span data-stu-id="e2c7c-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="e2c7c-106">Die Zeichenfolgen, in die **der ValueMap-Inhalt** übersetzt wird, sollten auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden. </span><span class="sxs-lookup"><span data-stu-id="e2c7c-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="e2c7c-107">Diese Methode wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="e2c7c-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2c7c-108">Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e2c7c-109">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="e2c7c-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e2c7c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2c7c-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="e2c7c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2c7c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2c7c-112">*PowerState* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e2c7c-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c7c-113">Ein **ValueMap-Wert,** der den gewünschten Energiezustand für das logische Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-113">A **ValueMap** value that specifies the desired power state for the logical device.</span></span>

<dt>

<span data-ttu-id="e2c7c-114">1</span><span class="sxs-lookup"><span data-stu-id="e2c7c-114">1</span></span>
</dt> <dd>

<span data-ttu-id="e2c7c-115">Volle Leistung.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="e2c7c-116">2</span><span class="sxs-lookup"><span data-stu-id="e2c7c-116">2</span></span>
</dt> <dd>

<span data-ttu-id="e2c7c-117">Energiesparmodus mit geringer Leistung.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="e2c7c-118">3</span><span class="sxs-lookup"><span data-stu-id="e2c7c-118">3</span></span>
</dt> <dd>

<span data-ttu-id="e2c7c-119">Standbymodus "Energie sparen".</span><span class="sxs-lookup"><span data-stu-id="e2c7c-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="e2c7c-120">4</span><span class="sxs-lookup"><span data-stu-id="e2c7c-120">4</span></span>
</dt> <dd>

<span data-ttu-id="e2c7c-121">Energie sparen Sie andere.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="e2c7c-122">5</span><span class="sxs-lookup"><span data-stu-id="e2c7c-122">5</span></span>
</dt> <dd>

<span data-ttu-id="e2c7c-123">Energiezyklus.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="e2c7c-124">6</span><span class="sxs-lookup"><span data-stu-id="e2c7c-124">6</span></span>
</dt> <dd>

<span data-ttu-id="e2c7c-125">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e2c7c-126">*Zeit* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e2c7c-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c7c-127">Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervallwert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="e2c7c-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="e2c7c-128">Wenn der *PowerState-Parameter* gleich 5 ("Power Cycle") ist, gibt der *Time-Parameter* an, wann das Gerät wieder ein-/aus netzen soll.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="e2c7c-129">Das Ausschalten erfolgt sofort.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2c7c-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2c7c-130">Return value</span></span>

<span data-ttu-id="e2c7c-131">Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState-* und *Time-Anforderung* nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2c7c-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2c7c-132">Remarks</span></span>

<span data-ttu-id="e2c7c-133">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e2c7c-134">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-134">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="e2c7c-135">Weitere Informationen finden Sie unter [Erstellen von WMI-Anbietern.](/windows/desktop/WmiSdk/creating-wmi-providers)</span><span class="sxs-lookup"><span data-stu-id="e2c7c-135">For more information, see [Creating WMI Providers](/windows/desktop/WmiSdk/creating-wmi-providers).</span></span>

<span data-ttu-id="e2c7c-136">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e2c7c-137">Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e2c7c-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2c7c-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2c7c-138">Requirements</span></span>



| <span data-ttu-id="e2c7c-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2c7c-139">Requirement</span></span> | <span data-ttu-id="e2c7c-140">Wert</span><span class="sxs-lookup"><span data-stu-id="e2c7c-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c7c-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2c7c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e2c7c-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2c7c-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2c7c-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2c7c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e2c7c-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2c7c-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2c7c-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2c7c-145">Namespace</span></span><br/>                | <span data-ttu-id="e2c7c-146">Stamm \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e2c7c-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2c7c-147">MOF</span><span class="sxs-lookup"><span data-stu-id="e2c7c-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2c7c-148"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2c7c-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2c7c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e2c7c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2c7c-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2c7c-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2c7c-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e2c7c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2c7c-152">\_CIM-Controller</span><span class="sxs-lookup"><span data-stu-id="e2c7c-152">CIM\_Controller</span></span>](setpowerstate-method-in-class-cim-controller.md)
</dt> <dt>

[<span data-ttu-id="e2c7c-153">**\_CIM-Controller**</span><span class="sxs-lookup"><span data-stu-id="e2c7c-153">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

