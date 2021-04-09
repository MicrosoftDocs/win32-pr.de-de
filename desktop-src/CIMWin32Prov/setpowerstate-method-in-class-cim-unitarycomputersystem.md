---
description: Die SetPowerState-Methode der CIM \_ unitarycomputersystem-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll.
ms.assetid: a02991d5-3c93-4579-b1f5-f70ad7c7052b
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_UnitaryComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d9b69306c7bb362dceaee254be5dae8f5d37a52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958147"
---
# <a name="setpowerstate-method-of-the-cim_unitarycomputersystem-class"></a><span data-ttu-id="eb667-103">SetPowerState-Methode der CIM \_ unitarycomputersystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="eb667-103">SetPowerState method of the CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="eb667-104">Die **SetPowerState** -Methode der CIM \_ unitarycomputersystem-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb667-104">The **SetPowerState** method of the CIM\_UnitaryComputerSystem class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="eb667-105">In einer Unterklasse sollte der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="eb667-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="eb667-106">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, sollten in der-Unterklasse auch als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="eb667-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="eb667-107">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb667-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb667-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="eb667-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eb667-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eb667-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="eb667-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb667-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="eb667-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb667-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb667-112">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb667-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb667-113">Ein **ValueMap** -Wert, der den gewünschten Energiezustand für dieses logische Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="eb667-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="eb667-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Vollstrom** (1)</span><span class="sxs-lookup"><span data-stu-id="eb667-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eb667-115">Vollständige Leistung.</span><span class="sxs-lookup"><span data-stu-id="eb667-115">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="eb667-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (2)</span><span class="sxs-lookup"><span data-stu-id="eb667-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eb667-117">Energiesparmodus im Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="eb667-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="eb667-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (3)</span><span class="sxs-lookup"><span data-stu-id="eb667-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="eb667-119">Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="eb667-119">Power save   standby.</span></span>

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="eb667-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Energiespar Speicher-andere** (4)</span><span class="sxs-lookup"><span data-stu-id="eb667-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Power Save - Other** (4)</span></span>


</dt> <dd>

<span data-ttu-id="eb667-121">Andere Energie speichern.</span><span class="sxs-lookup"><span data-stu-id="eb667-121">Power save   other.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="eb667-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (5)</span><span class="sxs-lookup"><span data-stu-id="eb667-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="eb667-123">Leistungs Zyklen.</span><span class="sxs-lookup"><span data-stu-id="eb667-123">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="eb667-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (6)</span><span class="sxs-lookup"><span data-stu-id="eb667-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="eb667-125">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="eb667-125">Power off.</span></span>

</dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="eb667-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>Ruhe **Zustand (7** )</span><span class="sxs-lookup"><span data-stu-id="eb667-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Hibernate** (7)</span></span>


</dt> <dd>

<span data-ttu-id="eb667-127">Ruhezustand.</span><span class="sxs-lookup"><span data-stu-id="eb667-127">Hibernate.</span></span>

</dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="eb667-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Soft Off** (8)</span><span class="sxs-lookup"><span data-stu-id="eb667-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Soft Off** (8)</span></span>


</dt> <dd>

<span data-ttu-id="eb667-129">Soft aus.</span><span class="sxs-lookup"><span data-stu-id="eb667-129">Soft off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="eb667-130">*Uhrzeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb667-130">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb667-131">Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervall Wert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="eb667-131">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="eb667-132">Wenn der *PowerState* -Parameter gleich 5 ("Power Cycle") ist, gibt der *Zeit* Parameter an, wann das Gerät erneut einschalten soll.</span><span class="sxs-lookup"><span data-stu-id="eb667-132">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="eb667-133">Der Ausschalten erfolgt sofort.</span><span class="sxs-lookup"><span data-stu-id="eb667-133">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb667-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb667-134">Return value</span></span>

<span data-ttu-id="eb667-135">Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState* -und *time* -Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="eb667-135">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb667-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb667-136">Remarks</span></span>

<span data-ttu-id="eb667-137">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="eb667-137">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="eb667-138">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="eb667-138">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="eb667-139">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="eb667-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eb667-140">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="eb667-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb667-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb667-141">Requirements</span></span>



| <span data-ttu-id="eb667-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb667-142">Requirement</span></span> | <span data-ttu-id="eb667-143">Wert</span><span class="sxs-lookup"><span data-stu-id="eb667-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb667-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb667-144">Minimum supported client</span></span><br/> | <span data-ttu-id="eb667-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb667-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb667-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb667-146">Minimum supported server</span></span><br/> | <span data-ttu-id="eb667-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb667-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb667-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb667-148">Namespace</span></span><br/>                | <span data-ttu-id="eb667-149">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eb667-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb667-150">MOF</span><span class="sxs-lookup"><span data-stu-id="eb667-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb667-151"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eb667-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb667-152">DLL</span><span class="sxs-lookup"><span data-stu-id="eb667-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb667-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb667-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb667-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb667-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb667-155">CIM \_ unitarycomputersystem</span><span class="sxs-lookup"><span data-stu-id="eb667-155">CIM\_UnitaryComputerSystem</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md)
</dt> <dt>

[<span data-ttu-id="eb667-156">**CIM \_ unitarycomputersystem**</span><span class="sxs-lookup"><span data-stu-id="eb667-156">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> </dl>

 

 




