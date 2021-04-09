---
description: Die CIM \_ associatedsensor-Klasse ordnet einen installierten Sensor einem logischen Gerät zu. Der Sensor misst wichtige Eingabe-und Ausgabe Eigenschaften und kann im Gerät enthalten oder in der Nähe installiert werden.
ms.assetid: 8ccaa37f-b95f-4582-a694-23bdc15b8c8b
ms.tgt_platform: multiple
title: CIM_AssociatedSensor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSensor
- CIM_AssociatedSensor.Dependent
- CIM_AssociatedSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50eac6b8bd933762df0da0213c420f5895b74640
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861420"
---
# <a name="cim_associatedsensor-class"></a><span data-ttu-id="0abd7-104">CIM \_ associatedsensor-Klasse</span><span class="sxs-lookup"><span data-stu-id="0abd7-104">CIM\_AssociatedSensor class</span></span>

<span data-ttu-id="0abd7-105">Die **CIM \_ associatedsensor** -Klasse ordnet einen installierten Sensor einem logischen Gerät zu.</span><span class="sxs-lookup"><span data-stu-id="0abd7-105">The **CIM\_AssociatedSensor** class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="0abd7-106">Der Sensor misst wichtige Eingabe-und Ausgabe Eigenschaften und kann im Gerät enthalten oder in der Nähe installiert werden.</span><span class="sxs-lookup"><span data-stu-id="0abd7-106">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0abd7-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0abd7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0abd7-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0abd7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0abd7-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0abd7-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0abd7-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0abd7-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0abd7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="0abd7-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A0-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedSensor : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Sensor        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0abd7-112">Member</span><span class="sxs-lookup"><span data-stu-id="0abd7-112">Members</span></span>

<span data-ttu-id="0abd7-113">Die **CIM \_ associatedsensor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0abd7-113">The **CIM\_AssociatedSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="0abd7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0abd7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0abd7-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0abd7-115">Properties</span></span>

<span data-ttu-id="0abd7-116">Die **CIM \_ associatedsensor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0abd7-116">The **CIM\_AssociatedSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0abd7-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="0abd7-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0abd7-118">Datentyp: **CIM- \_ Sensor**</span><span class="sxs-lookup"><span data-stu-id="0abd7-118">Data type: **CIM\_Sensor**</span></span>
</dt> <dt>

<span data-ttu-id="0abd7-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0abd7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0abd7-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="0abd7-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0abd7-121">Ein [**CIM- \_ Sensor**](cim-sensor.md) , der den Sensor beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0abd7-121">A [**CIM\_Sensor**](cim-sensor.md) that describes the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="0abd7-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="0abd7-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0abd7-123">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="0abd7-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="0abd7-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0abd7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0abd7-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="0abd7-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0abd7-126">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät beschreibt, für das Informationen vom Sensor gemessen werden.</span><span class="sxs-lookup"><span data-stu-id="0abd7-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device for which information is measured by the sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0abd7-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0abd7-127">Remarks</span></span>

<span data-ttu-id="0abd7-128">Die **CIM \_ associatedsensor** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0abd7-128">The **CIM\_AssociatedSensor** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0abd7-129">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0abd7-129">WMI does not implement this class.</span></span> <span data-ttu-id="0abd7-130">Weitere Informationen zu Klassen, die von **CIM \_ associatedsensor** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0abd7-130">For more information about classes derived from **CIM\_AssociatedSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0abd7-131">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0abd7-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0abd7-132">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0abd7-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0abd7-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0abd7-133">Requirements</span></span>



| <span data-ttu-id="0abd7-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0abd7-134">Requirement</span></span> | <span data-ttu-id="0abd7-135">Wert</span><span class="sxs-lookup"><span data-stu-id="0abd7-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0abd7-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0abd7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0abd7-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0abd7-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0abd7-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0abd7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0abd7-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0abd7-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0abd7-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="0abd7-140">Namespace</span></span><br/>                | <span data-ttu-id="0abd7-141">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0abd7-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0abd7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0abd7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0abd7-143"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0abd7-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0abd7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0abd7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0abd7-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0abd7-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0abd7-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0abd7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abd7-147">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="0abd7-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

