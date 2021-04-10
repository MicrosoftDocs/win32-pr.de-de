---
description: Die SetPowerState-Methode der CIM \_ -Klasse uninterruptiblepowersupply legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll.
ms.assetid: 305987cb-930a-4b60-86f3-f94927fb59c4
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_UninterruptiblePowerSupply-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UninterruptiblePowerSupply.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6338830abde000f2a96d9477d77128b6877ea529
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041457"
---
# <a name="setpowerstate-method-of-the-cim_uninterruptiblepowersupply-class"></a><span data-ttu-id="a72c8-103">SetPowerState-Methode der CIM- \_ Klasse uninterruptiblepowersupply</span><span class="sxs-lookup"><span data-stu-id="a72c8-103">SetPowerState method of the CIM\_UninterruptiblePowerSupply class</span></span>

<span data-ttu-id="a72c8-104">Die **SetPowerState** -Methode der CIM \_ -Klasse uninterruptiblepowersupply legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a72c8-104">The **SetPowerState** method of the CIM\_UninterruptiblePowerSupply class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="a72c8-105">In einer Unterklasse sollte der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a72c8-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="a72c8-106">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, sollten in der-Unterklasse auch als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a72c8-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="a72c8-107">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a72c8-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a72c8-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a72c8-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a72c8-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a72c8-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a72c8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a72c8-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="a72c8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a72c8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a72c8-112">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a72c8-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a72c8-113">Ein **ValueMap** -Wert, der den gewünschten Energiezustand für dieses logische Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="a72c8-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="a72c8-114">1</span><span class="sxs-lookup"><span data-stu-id="a72c8-114">1</span></span>
</dt> <dd>

<span data-ttu-id="a72c8-115">Vollständige Leistung.</span><span class="sxs-lookup"><span data-stu-id="a72c8-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="a72c8-116">2</span><span class="sxs-lookup"><span data-stu-id="a72c8-116">2</span></span>
</dt> <dd>

<span data-ttu-id="a72c8-117">Energiesparmodus im Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="a72c8-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="a72c8-118">3</span><span class="sxs-lookup"><span data-stu-id="a72c8-118">3</span></span>
</dt> <dd>

<span data-ttu-id="a72c8-119">Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="a72c8-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="a72c8-120">4</span><span class="sxs-lookup"><span data-stu-id="a72c8-120">4</span></span>
</dt> <dd>

<span data-ttu-id="a72c8-121">Andere Energie speichern.</span><span class="sxs-lookup"><span data-stu-id="a72c8-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="a72c8-122">5</span><span class="sxs-lookup"><span data-stu-id="a72c8-122">5</span></span>
</dt> <dd>

<span data-ttu-id="a72c8-123">Leistungs Zyklen.</span><span class="sxs-lookup"><span data-stu-id="a72c8-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="a72c8-124">6</span><span class="sxs-lookup"><span data-stu-id="a72c8-124">6</span></span>
</dt> <dd>

<span data-ttu-id="a72c8-125">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="a72c8-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a72c8-126">*Uhrzeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a72c8-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a72c8-127">Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervall Wert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="a72c8-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="a72c8-128">Wenn der *PowerState* -Parameter gleich 5 ("Power Cycle") ist, gibt der *Zeit* Parameter an, wann das Gerät erneut einschalten soll.</span><span class="sxs-lookup"><span data-stu-id="a72c8-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="a72c8-129">Der Ausschalten erfolgt sofort.</span><span class="sxs-lookup"><span data-stu-id="a72c8-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a72c8-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a72c8-130">Return value</span></span>

<span data-ttu-id="a72c8-131">Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState* -und *time* -Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a72c8-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="a72c8-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a72c8-132">Remarks</span></span>

<span data-ttu-id="a72c8-133">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="a72c8-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a72c8-134">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="a72c8-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a72c8-135">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a72c8-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a72c8-136">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a72c8-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a72c8-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a72c8-137">Requirements</span></span>



| <span data-ttu-id="a72c8-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a72c8-138">Requirement</span></span> | <span data-ttu-id="a72c8-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a72c8-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a72c8-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a72c8-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a72c8-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a72c8-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a72c8-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a72c8-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a72c8-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a72c8-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a72c8-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="a72c8-144">Namespace</span></span><br/>                | <span data-ttu-id="a72c8-145">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a72c8-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a72c8-146">MOF</span><span class="sxs-lookup"><span data-stu-id="a72c8-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a72c8-147"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a72c8-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a72c8-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a72c8-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a72c8-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a72c8-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a72c8-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a72c8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a72c8-151">CIM- \_ uninterruptiblepowersupply</span><span class="sxs-lookup"><span data-stu-id="a72c8-151">CIM\_UninterruptiblePowerSupply</span></span>](setpowerstate-method-in-class-cim-uninterruptiblepowersupply.md)
</dt> <dt>

[<span data-ttu-id="a72c8-152">**CIM- \_ uninterruptiblepowersupply**</span><span class="sxs-lookup"><span data-stu-id="a72c8-152">**CIM\_UninterruptiblePowerSupply**</span></span>](cim-uninterruptiblepowersupply.md)
</dt> </dl>

 

 




