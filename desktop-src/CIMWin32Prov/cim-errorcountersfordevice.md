---
description: Die CIM- \_ Klasse errorcountersfordevice ordnet dem \_ logischen Gerät, auf das Sie angewendet wird, die CIM deviceerrorcounts-Klasse zu.
ms.assetid: 200971ab-df85-4a45-beb3-4ffe11ce92dc
ms.tgt_platform: multiple
title: CIM_ErrorCountersForDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ErrorCountersForDevice
- CIM_ErrorCountersForDevice.Element
- CIM_ErrorCountersForDevice.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c4e11b1f58cae7b544b251044657bb737525b37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861264"
---
# <a name="cim_errorcountersfordevice-class"></a><span data-ttu-id="908fd-103">CIM \_ errorcountersfordevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="908fd-103">CIM\_ErrorCountersForDevice class</span></span>

<span data-ttu-id="908fd-104">Die **CIM-Klasse \_ errorcountersfordevice** ordnet dem logischen Gerät, auf das Sie angewendet wird, die [**CIM \_ deviceerrorcounts**](cim-deviceerrorcounts.md) -Klasse zu.</span><span class="sxs-lookup"><span data-stu-id="908fd-104">The **CIM\_ErrorCountersForDevice** class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="908fd-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="908fd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="908fd-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="908fd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="908fd-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="908fd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="908fd-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="908fd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="908fd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="908fd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D79F3A0-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_ErrorCountersForDevice : CIM_Statistics
{
  CIM_LogicalDevice     REF Element;
  CIM_DeviceErrorCounts REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="908fd-110">Member</span><span class="sxs-lookup"><span data-stu-id="908fd-110">Members</span></span>

<span data-ttu-id="908fd-111">Die **CIM \_ errorcountersfordevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="908fd-111">The **CIM\_ErrorCountersForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="908fd-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="908fd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="908fd-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="908fd-113">Properties</span></span>

<span data-ttu-id="908fd-114">Die **CIM \_ errorcountersfordevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="908fd-114">The **CIM\_ErrorCountersForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="908fd-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="908fd-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908fd-116">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="908fd-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="908fd-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="908fd-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="908fd-118">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="908fd-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="908fd-119">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das Gerät beschreibt, auf das die Fehlerindikatoren angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="908fd-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device to which the error counters apply.</span></span>

</dd> <dt>

<span data-ttu-id="908fd-120">**Stats**</span><span class="sxs-lookup"><span data-stu-id="908fd-120">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="908fd-121">Datentyp: **CIM \_ deviceerrorcounts**</span><span class="sxs-lookup"><span data-stu-id="908fd-121">Data type: **CIM\_DeviceErrorCounts**</span></span>
</dt> <dt>

<span data-ttu-id="908fd-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="908fd-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="908fd-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Stats"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="908fd-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stats"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="908fd-124">Eine [**CIM \_ deviceerrorcounts**](cim-deviceerrorcounts.md) , die das statistische Objekt beschreibt (in diesem Fall die Fehler Indikator Klasse).</span><span class="sxs-lookup"><span data-stu-id="908fd-124">A [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) describing the statistical object - in this case, the error counter class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="908fd-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="908fd-125">Remarks</span></span>

<span data-ttu-id="908fd-126">Die **CIM- \_ errorcountersfordevice** -Klasse wird von [**CIM- \_ Statistiken**](cim-statistics.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="908fd-126">The **CIM\_ErrorCountersForDevice** class is inherited from [**CIM\_Statistics**](cim-statistics.md).</span></span>

<span data-ttu-id="908fd-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="908fd-127">WMI does not implement this class.</span></span>

<span data-ttu-id="908fd-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="908fd-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="908fd-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="908fd-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="908fd-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="908fd-130">Requirements</span></span>



| <span data-ttu-id="908fd-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="908fd-131">Requirement</span></span> | <span data-ttu-id="908fd-132">Wert</span><span class="sxs-lookup"><span data-stu-id="908fd-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="908fd-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="908fd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="908fd-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="908fd-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="908fd-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="908fd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="908fd-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="908fd-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="908fd-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="908fd-137">Namespace</span></span><br/>                | <span data-ttu-id="908fd-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="908fd-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="908fd-139">MOF</span><span class="sxs-lookup"><span data-stu-id="908fd-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="908fd-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="908fd-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="908fd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="908fd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="908fd-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="908fd-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="908fd-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="908fd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908fd-144">**CIM- \_ Statistik**</span><span class="sxs-lookup"><span data-stu-id="908fd-144">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> </dl>

 

