---
description: Die SetPowerState-Methode der CIM \_ NetworkAdapter-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll.
ms.assetid: b384bd64-c4a3-4a35-b18a-a4f23cd3d131
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_NetworkAdapter-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkAdapter.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a92777ebff1716c89a8f4c893a6ce99e78858e09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483334"
---
# <a name="setpowerstate-method-of-the-cim_networkadapter-class"></a><span data-ttu-id="22fa0-103">SetPowerState-Methode der CIM \_ NetworkAdapter-Klasse</span><span class="sxs-lookup"><span data-stu-id="22fa0-103">SetPowerState method of the CIM\_NetworkAdapter class</span></span>

<span data-ttu-id="22fa0-104">Die **SetPowerState** -Methode der CIM \_ NetworkAdapter-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="22fa0-104">The **SetPowerState** method of the CIM\_NetworkAdapter class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="22fa0-105">In einer Unterklasse sollte der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="22fa0-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="22fa0-106">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, sollten in der-Unterklasse auch als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="22fa0-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="22fa0-107">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="22fa0-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22fa0-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="22fa0-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="22fa0-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="22fa0-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="22fa0-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="22fa0-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="22fa0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="22fa0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22fa0-112">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22fa0-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22fa0-113">Ein **ValueMap** -Wert, der den gewünschten Energiezustand für dieses logische Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="22fa0-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="22fa0-114">1</span><span class="sxs-lookup"><span data-stu-id="22fa0-114">1</span></span>
</dt> <dd>

<span data-ttu-id="22fa0-115">Vollständige Leistung.</span><span class="sxs-lookup"><span data-stu-id="22fa0-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="22fa0-116">2</span><span class="sxs-lookup"><span data-stu-id="22fa0-116">2</span></span>
</dt> <dd>

<span data-ttu-id="22fa0-117">Energiesparmodus im Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="22fa0-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="22fa0-118">3</span><span class="sxs-lookup"><span data-stu-id="22fa0-118">3</span></span>
</dt> <dd>

<span data-ttu-id="22fa0-119">Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="22fa0-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="22fa0-120">4</span><span class="sxs-lookup"><span data-stu-id="22fa0-120">4</span></span>
</dt> <dd>

<span data-ttu-id="22fa0-121">Andere Energie speichern.</span><span class="sxs-lookup"><span data-stu-id="22fa0-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="22fa0-122">5</span><span class="sxs-lookup"><span data-stu-id="22fa0-122">5</span></span>
</dt> <dd>

<span data-ttu-id="22fa0-123">Leistungs Zyklen.</span><span class="sxs-lookup"><span data-stu-id="22fa0-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="22fa0-124">6</span><span class="sxs-lookup"><span data-stu-id="22fa0-124">6</span></span>
</dt> <dd>

<span data-ttu-id="22fa0-125">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="22fa0-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="22fa0-126">*Uhrzeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22fa0-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22fa0-127">Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervall Wert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="22fa0-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="22fa0-128">Wenn der *PowerState* -Parameter gleich 5 ("Power Cycle") ist, gibt der *Zeit* Parameter an, wann das Gerät erneut einschalten soll.</span><span class="sxs-lookup"><span data-stu-id="22fa0-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="22fa0-129">Der Ausschalten erfolgt sofort.</span><span class="sxs-lookup"><span data-stu-id="22fa0-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22fa0-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22fa0-130">Return value</span></span>

<span data-ttu-id="22fa0-131">Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState* -und *time* -Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="22fa0-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="22fa0-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22fa0-132">Remarks</span></span>

<span data-ttu-id="22fa0-133">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="22fa0-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="22fa0-134">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="22fa0-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="22fa0-135">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="22fa0-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="22fa0-136">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="22fa0-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="22fa0-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22fa0-137">Requirements</span></span>



| <span data-ttu-id="22fa0-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22fa0-138">Requirement</span></span> | <span data-ttu-id="22fa0-139">Wert</span><span class="sxs-lookup"><span data-stu-id="22fa0-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22fa0-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22fa0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="22fa0-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22fa0-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22fa0-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22fa0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="22fa0-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22fa0-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22fa0-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="22fa0-144">Namespace</span></span><br/>                | <span data-ttu-id="22fa0-145">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="22fa0-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="22fa0-146">MOF</span><span class="sxs-lookup"><span data-stu-id="22fa0-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22fa0-147"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="22fa0-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="22fa0-148">DLL</span><span class="sxs-lookup"><span data-stu-id="22fa0-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22fa0-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22fa0-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22fa0-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22fa0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22fa0-151">CIM- \_ Netzwerkadapter</span><span class="sxs-lookup"><span data-stu-id="22fa0-151">CIM\_NetworkAdapter</span></span>](setpowerstate-method-in-class-cim-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="22fa0-152">**CIM- \_ Netzwerkadapter**</span><span class="sxs-lookup"><span data-stu-id="22fa0-152">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> </dl>

 

 




