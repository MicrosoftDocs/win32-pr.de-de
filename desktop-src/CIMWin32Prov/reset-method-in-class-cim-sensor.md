---
description: 'Reset-Methode der CIM_Sensor-Klasse: Die Reset-Methode fordert eine Zurücksetzung des logischen Geräts an. Diese Methode wird von CIM \_ LogicalDevice geerbt.'
ms.assetid: d764986b-b512-4f38-8284-d16b1f670871
ms.tgt_platform: multiple
title: Reset-Methode der CIM_Sensor Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Sensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9a17599216226f2420504ee07fccd2174d7eff4e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096858"
---
# <a name="reset-method-of-the-cim_sensor-class"></a><span data-ttu-id="b9f61-104">Reset-Methode der \_ CIM-Sensorklasse</span><span class="sxs-lookup"><span data-stu-id="b9f61-104">Reset method of the CIM\_Sensor class</span></span>

<span data-ttu-id="b9f61-105">Die **Reset-Methode** fordert eine Zurücksetzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="b9f61-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="b9f61-106">Diese Methode wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="b9f61-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9f61-107">Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b9f61-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b9f61-108">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="b9f61-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b9f61-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9f61-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="b9f61-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9f61-110">Parameters</span></span>

<span data-ttu-id="b9f61-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b9f61-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9f61-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9f61-112">Return value</span></span>

<span data-ttu-id="b9f61-113">Gibt 0 (null) zurück, wenn die Anforderung erfolgreich ausgeführt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b9f61-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9f61-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9f61-114">Remarks</span></span>

<span data-ttu-id="b9f61-115">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="b9f61-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b9f61-116">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="b9f61-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b9f61-117">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="b9f61-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b9f61-118">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="b9f61-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9f61-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9f61-119">Requirements</span></span>



| <span data-ttu-id="b9f61-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9f61-120">Requirement</span></span> | <span data-ttu-id="b9f61-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b9f61-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9f61-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9f61-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b9f61-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9f61-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b9f61-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9f61-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b9f61-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9f61-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b9f61-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9f61-126">Namespace</span></span><br/>                | <span data-ttu-id="b9f61-127">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="b9f61-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b9f61-128">MOF</span><span class="sxs-lookup"><span data-stu-id="b9f61-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9f61-129"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9f61-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9f61-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b9f61-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9f61-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9f61-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9f61-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b9f61-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9f61-133">\_CIM-Sensor</span><span class="sxs-lookup"><span data-stu-id="b9f61-133">CIM\_Sensor</span></span>](reset-method-in-class-cim-sensor.md)
</dt> <dt>

[<span data-ttu-id="b9f61-134">**\_CIM-Sensor**</span><span class="sxs-lookup"><span data-stu-id="b9f61-134">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

 




