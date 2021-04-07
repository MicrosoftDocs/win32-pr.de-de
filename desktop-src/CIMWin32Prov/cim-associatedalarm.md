---
description: Die CIM \_ associatedalarm-Abhängigkeit ordnet einem logischen Gerät einen Alarm zu.
ms.assetid: ed0ccc81-6d1b-45b0-abf0-7a2bd9a50193
ms.tgt_platform: multiple
title: CIM_AssociatedAlarm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedAlarm
- CIM_AssociatedAlarm.Dependent
- CIM_AssociatedAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe6a637482526feecc7528eadc70dc695dafca9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748705"
---
# <a name="cim_associatedalarm-class"></a><span data-ttu-id="5da9e-103">CIM \_ associatedalarm-Klasse</span><span class="sxs-lookup"><span data-stu-id="5da9e-103">CIM\_AssociatedAlarm class</span></span>

<span data-ttu-id="5da9e-104">Die **CIM \_ associatedalarm** -Abhängigkeit ordnet einem logischen Gerät einen Alarm zu.</span><span class="sxs-lookup"><span data-stu-id="5da9e-104">The **CIM\_AssociatedAlarm** dependency associates an alarm with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5da9e-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5da9e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5da9e-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5da9e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5da9e-107">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="5da9e-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da9e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5da9e-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{2280CB02-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedAlarm : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_AlarmDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="5da9e-109">Member</span><span class="sxs-lookup"><span data-stu-id="5da9e-109">Members</span></span>

<span data-ttu-id="5da9e-110">Die **CIM \_ associatedalarm** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5da9e-110">The **CIM\_AssociatedAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="5da9e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5da9e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5da9e-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5da9e-112">Properties</span></span>

<span data-ttu-id="5da9e-113">Die **CIM \_ associatedalarm** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5da9e-113">The **CIM\_AssociatedAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5da9e-114">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="5da9e-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da9e-115">Datentyp: **CIM \_ alarmdevice**</span><span class="sxs-lookup"><span data-stu-id="5da9e-115">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="5da9e-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5da9e-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5da9e-117">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="5da9e-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5da9e-118">Ein [**CIM \_ alarmdevice**](cim-alarmdevice.md) , das das Wecker-Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="5da9e-118">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that contains the alarm device.</span></span>

</dd> <dt>

<span data-ttu-id="5da9e-119">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="5da9e-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da9e-120">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="5da9e-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="5da9e-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5da9e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5da9e-122">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="5da9e-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5da9e-123">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät enthält, das alarmiert ist.</span><span class="sxs-lookup"><span data-stu-id="5da9e-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device that is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5da9e-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5da9e-124">Remarks</span></span>

<span data-ttu-id="5da9e-125">Die **CIM \_ associatedalarm** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5da9e-125">The **CIM\_AssociatedAlarm** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="5da9e-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5da9e-126">WMI does not implement this class.</span></span>

<span data-ttu-id="5da9e-127">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5da9e-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5da9e-128">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5da9e-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5da9e-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5da9e-129">Requirements</span></span>



| <span data-ttu-id="5da9e-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5da9e-130">Requirement</span></span> | <span data-ttu-id="5da9e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="5da9e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5da9e-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5da9e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5da9e-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5da9e-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5da9e-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5da9e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5da9e-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5da9e-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5da9e-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="5da9e-136">Namespace</span></span><br/>                | <span data-ttu-id="5da9e-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5da9e-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5da9e-138">MOF</span><span class="sxs-lookup"><span data-stu-id="5da9e-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5da9e-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5da9e-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5da9e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5da9e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5da9e-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5da9e-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5da9e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5da9e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da9e-143">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="5da9e-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

