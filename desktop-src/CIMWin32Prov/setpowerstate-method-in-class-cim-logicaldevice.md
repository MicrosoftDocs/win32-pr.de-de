---
description: Die SetPowerState-Methode der CIM \_ LogicalDevice-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll.
ms.assetid: 0d9678e0-a956-45d3-ac41-5c1604478fd7
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_LogicalDevice-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd258a4372c16a7f98f2fe3ea8b84bbfef44f69e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342599"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="598d0-103">SetPowerState-Methode der CIM_LogicalDevice-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="598d0-103">SetPowerState method of the CIM_LogicalDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="598d0-104">Die **SetPowerState** -Methode der CIM \_ LogicalDevice-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="598d0-104">The **SetPowerState** method of the CIM\_LogicalDevice class sets the desired power state for a logical device and when a device should be put into that state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="598d0-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="598d0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="598d0-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="598d0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="598d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="598d0-107">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="598d0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="598d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="598d0-109">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="598d0-109">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="598d0-110">Ein **ValueMap** -Wert, der den gewünschten Energiezustand für dieses logische Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="598d0-110">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="598d0-111"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Vollstrom** (1)</span><span class="sxs-lookup"><span data-stu-id="598d0-111"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="598d0-112">Vollständige Leistung.</span><span class="sxs-lookup"><span data-stu-id="598d0-112">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="598d0-113"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (2)</span><span class="sxs-lookup"><span data-stu-id="598d0-113"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="598d0-114">Energiesparmodus im Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="598d0-114">Power save   low-power mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="598d0-115"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (3)</span><span class="sxs-lookup"><span data-stu-id="598d0-115"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="598d0-116">Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="598d0-116">Power save   standby.</span></span>

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="598d0-117"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Energiespar Speicher-andere** (4)</span><span class="sxs-lookup"><span data-stu-id="598d0-117"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Power Save - Other** (4)</span></span>


</dt> <dd>

<span data-ttu-id="598d0-118">Andere Energie speichern.</span><span class="sxs-lookup"><span data-stu-id="598d0-118">Power save   other.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="598d0-119"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (5)</span><span class="sxs-lookup"><span data-stu-id="598d0-119"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="598d0-120">Leistungs Zyklen.</span><span class="sxs-lookup"><span data-stu-id="598d0-120">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="598d0-121"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (6)</span><span class="sxs-lookup"><span data-stu-id="598d0-121"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="598d0-122">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="598d0-122">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="598d0-123">*Uhrzeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="598d0-123">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="598d0-124">Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervall Wert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="598d0-124">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="598d0-125">Wenn der *PowerState* -Parameter gleich 5 ("Power Cycle") ist, gibt der *Zeit* Parameter an, wann das Gerät erneut einschalten soll.</span><span class="sxs-lookup"><span data-stu-id="598d0-125">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="598d0-126">Der Ausschalten erfolgt sofort.</span><span class="sxs-lookup"><span data-stu-id="598d0-126">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="598d0-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="598d0-127">Return value</span></span>

<span data-ttu-id="598d0-128">Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState* -und *time* -Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="598d0-128">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="598d0-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="598d0-129">Remarks</span></span>

<span data-ttu-id="598d0-130">In einer Unterklasse sollte der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="598d0-130">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="598d0-131">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, sollten in der-Unterklasse auch als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="598d0-131">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="598d0-132">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="598d0-132">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="598d0-133">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="598d0-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="598d0-134">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="598d0-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="598d0-135">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="598d0-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="598d0-136">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="598d0-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="598d0-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="598d0-137">Requirements</span></span>



| <span data-ttu-id="598d0-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="598d0-138">Requirement</span></span> | <span data-ttu-id="598d0-139">Wert</span><span class="sxs-lookup"><span data-stu-id="598d0-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="598d0-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="598d0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="598d0-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="598d0-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="598d0-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="598d0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="598d0-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="598d0-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="598d0-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="598d0-144">Namespace</span></span><br/>                | <span data-ttu-id="598d0-145">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="598d0-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="598d0-146">MOF</span><span class="sxs-lookup"><span data-stu-id="598d0-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="598d0-147"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="598d0-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="598d0-148">DLL</span><span class="sxs-lookup"><span data-stu-id="598d0-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="598d0-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="598d0-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="598d0-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="598d0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="598d0-151">CIM \_ LogicalDevice</span><span class="sxs-lookup"><span data-stu-id="598d0-151">CIM\_LogicalDevice</span></span>](setpowerstate-method-in-class-cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="598d0-152">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="598d0-152">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




