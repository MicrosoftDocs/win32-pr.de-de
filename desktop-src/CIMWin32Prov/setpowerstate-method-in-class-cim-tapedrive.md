---
description: Die SetPowerState-Methode der CIM \_ TapeDrive-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll.
ms.assetid: 73f98d08-49da-4b21-91c4-cbe420c648e4
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_TapeDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a6efcfe08dfddca3477081f65fac35780f713005
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524152"
---
# <a name="setpowerstate-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="62cc5-103">SetPowerState-Methode der CIM \_ TapeDrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="62cc5-103">SetPowerState method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="62cc5-104">Die **SetPowerState** -Methode der CIM \_ TapeDrive-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="62cc5-104">The **SetPowerState** method of the CIM\_TapeDrive class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="62cc5-105">In einer Unterklasse sollte der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="62cc5-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="62cc5-106">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, sollten in der-Unterklasse auch als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="62cc5-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="62cc5-107">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62cc5-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="62cc5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="62cc5-108">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="62cc5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="62cc5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62cc5-110">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62cc5-110">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62cc5-111">Ein **ValueMap** -Wert, der den gewünschten Energiezustand für dieses logische Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="62cc5-111">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="62cc5-112">1</span><span class="sxs-lookup"><span data-stu-id="62cc5-112">1</span></span>
</dt> <dd>

<span data-ttu-id="62cc5-113">Vollständige Leistung.</span><span class="sxs-lookup"><span data-stu-id="62cc5-113">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="62cc5-114">2</span><span class="sxs-lookup"><span data-stu-id="62cc5-114">2</span></span>
</dt> <dd>

<span data-ttu-id="62cc5-115">Energiesparmodus im Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="62cc5-115">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="62cc5-116">3</span><span class="sxs-lookup"><span data-stu-id="62cc5-116">3</span></span>
</dt> <dd>

<span data-ttu-id="62cc5-117">Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="62cc5-117">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="62cc5-118">4</span><span class="sxs-lookup"><span data-stu-id="62cc5-118">4</span></span>
</dt> <dd>

<span data-ttu-id="62cc5-119">Andere Energie speichern.</span><span class="sxs-lookup"><span data-stu-id="62cc5-119">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="62cc5-120">5</span><span class="sxs-lookup"><span data-stu-id="62cc5-120">5</span></span>
</dt> <dd>

<span data-ttu-id="62cc5-121">Leistungs Zyklen.</span><span class="sxs-lookup"><span data-stu-id="62cc5-121">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="62cc5-122">6</span><span class="sxs-lookup"><span data-stu-id="62cc5-122">6</span></span>
</dt> <dd>

<span data-ttu-id="62cc5-123">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="62cc5-123">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="62cc5-124">*Uhrzeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62cc5-124">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62cc5-125">Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervall Wert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="62cc5-125">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="62cc5-126">Wenn der *PowerState* -Parameter gleich 5 ("Power Cycle") ist, gibt der *Zeit* Parameter an, wann das Gerät erneut einschalten soll.</span><span class="sxs-lookup"><span data-stu-id="62cc5-126">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="62cc5-127">Der Ausschalten erfolgt sofort.</span><span class="sxs-lookup"><span data-stu-id="62cc5-127">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62cc5-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62cc5-128">Return value</span></span>

<span data-ttu-id="62cc5-129">Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState* -und *time* -Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="62cc5-129">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="62cc5-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62cc5-130">Remarks</span></span>

<span data-ttu-id="62cc5-131">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="62cc5-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="62cc5-132">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="62cc5-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="62cc5-133">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="62cc5-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="62cc5-134">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="62cc5-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="62cc5-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62cc5-135">Requirements</span></span>



| <span data-ttu-id="62cc5-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62cc5-136">Requirement</span></span> | <span data-ttu-id="62cc5-137">Wert</span><span class="sxs-lookup"><span data-stu-id="62cc5-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62cc5-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62cc5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="62cc5-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62cc5-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62cc5-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62cc5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="62cc5-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62cc5-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62cc5-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="62cc5-142">Namespace</span></span><br/>                | <span data-ttu-id="62cc5-143">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="62cc5-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62cc5-144">MOF</span><span class="sxs-lookup"><span data-stu-id="62cc5-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62cc5-145"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="62cc5-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62cc5-146">DLL</span><span class="sxs-lookup"><span data-stu-id="62cc5-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62cc5-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62cc5-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62cc5-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62cc5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62cc5-149">CIM- \_ TapeDrive</span><span class="sxs-lookup"><span data-stu-id="62cc5-149">CIM\_TapeDrive</span></span>](setpowerstate-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="62cc5-150">**CIM- \_ TapeDrive**</span><span class="sxs-lookup"><span data-stu-id="62cc5-150">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




