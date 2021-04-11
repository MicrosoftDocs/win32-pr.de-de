---
description: Mit der SetPowerState-Methode der CIM \_ -Anzeige Klasse wird der gewünschte Energiezustand für ein logisches Gerät festgelegt, und wenn ein Gerät in diesen Zustand versetzt werden soll.
ms.assetid: 949c300c-b01b-4c91-a902-41e940667ee6
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_Display-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Display.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35bcf49419b934e98c63b2151dcdaf3cb55f8d97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126440"
---
# <a name="setpowerstate-method-of-the-cim_display-class"></a><span data-ttu-id="788da-103">SetPowerState-Methode der CIM- \_ Anzeige Klasse</span><span class="sxs-lookup"><span data-stu-id="788da-103">SetPowerState method of the CIM\_Display class</span></span>

<span data-ttu-id="788da-104">Mit der **SetPowerState** -Methode der CIM \_ -Anzeige Klasse wird der gewünschte Energiezustand für ein logisches Gerät festgelegt, und wenn ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="788da-104">The **SetPowerState** method of the CIM\_Display class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="788da-105">In einer Unterklasse sollte der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="788da-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="788da-106">Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, sollten in der-Unterklasse auch als **Werte** Array Qualifizierer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="788da-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="788da-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="788da-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="788da-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="788da-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="788da-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="788da-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="788da-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="788da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="788da-111">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="788da-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="788da-112">Ein **ValueMap** -Wert, der den gewünschten Energiezustand für dieses logische Gerät angibt.</span><span class="sxs-lookup"><span data-stu-id="788da-112">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="788da-113">1</span><span class="sxs-lookup"><span data-stu-id="788da-113">1</span></span>
</dt> <dd>

<span data-ttu-id="788da-114">Vollständige Leistung.</span><span class="sxs-lookup"><span data-stu-id="788da-114">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="788da-115">2</span><span class="sxs-lookup"><span data-stu-id="788da-115">2</span></span>
</dt> <dd>

<span data-ttu-id="788da-116">Energiesparmodus im Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="788da-116">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="788da-117">3</span><span class="sxs-lookup"><span data-stu-id="788da-117">3</span></span>
</dt> <dd>

<span data-ttu-id="788da-118">Energiesparmodus.</span><span class="sxs-lookup"><span data-stu-id="788da-118">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="788da-119">4</span><span class="sxs-lookup"><span data-stu-id="788da-119">4</span></span>
</dt> <dd>

<span data-ttu-id="788da-120">Andere Energie speichern.</span><span class="sxs-lookup"><span data-stu-id="788da-120">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="788da-121">5</span><span class="sxs-lookup"><span data-stu-id="788da-121">5</span></span>
</dt> <dd>

<span data-ttu-id="788da-122">Leistungs Zyklen.</span><span class="sxs-lookup"><span data-stu-id="788da-122">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="788da-123">6</span><span class="sxs-lookup"><span data-stu-id="788da-123">6</span></span>
</dt> <dd>

<span data-ttu-id="788da-124">Ausschalten.</span><span class="sxs-lookup"><span data-stu-id="788da-124">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="788da-125">*Uhrzeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="788da-125">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="788da-126">Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervall Wert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="788da-126">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="788da-127">Wenn der *PowerState* -Parameter gleich 5 ("Power Cycle") ist, gibt der *Zeit* Parameter an, wann das Gerät erneut einschalten soll.</span><span class="sxs-lookup"><span data-stu-id="788da-127">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="788da-128">Der Ausschalten erfolgt sofort.</span><span class="sxs-lookup"><span data-stu-id="788da-128">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="788da-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="788da-129">Return value</span></span>

<span data-ttu-id="788da-130">Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState* -und *time* -Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="788da-130">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="788da-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="788da-131">Remarks</span></span>

<span data-ttu-id="788da-132">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="788da-132">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="788da-133">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="788da-133">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="788da-134">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="788da-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="788da-135">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="788da-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="788da-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="788da-136">Requirements</span></span>



| <span data-ttu-id="788da-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="788da-137">Requirement</span></span> | <span data-ttu-id="788da-138">Wert</span><span class="sxs-lookup"><span data-stu-id="788da-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="788da-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="788da-139">Minimum supported client</span></span><br/> | <span data-ttu-id="788da-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="788da-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="788da-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="788da-141">Minimum supported server</span></span><br/> | <span data-ttu-id="788da-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="788da-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="788da-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="788da-143">Namespace</span></span><br/>                | <span data-ttu-id="788da-144">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="788da-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="788da-145">MOF</span><span class="sxs-lookup"><span data-stu-id="788da-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="788da-146"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="788da-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="788da-147">DLL</span><span class="sxs-lookup"><span data-stu-id="788da-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="788da-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="788da-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="788da-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="788da-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="788da-150">CIM- \_ Anzeige</span><span class="sxs-lookup"><span data-stu-id="788da-150">CIM\_Display</span></span>](setpowerstate-method-in-class-cim-display.md)
</dt> <dt>

[<span data-ttu-id="788da-151">**CIM- \_ Anzeige**</span><span class="sxs-lookup"><span data-stu-id="788da-151">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

 




