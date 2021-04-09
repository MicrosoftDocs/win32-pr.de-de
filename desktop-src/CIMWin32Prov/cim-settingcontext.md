---
description: Die CIM \_ settingcontext-Klasse ordnet Konfigurationsobjekte Einstellungs Objekten zu.
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: CIM_SettingContext-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingContext
- CIM_SettingContext.Context
- CIM_SettingContext.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 867be99e1630f02c0163516ad7a86cf84c2fac13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958269"
---
# <a name="cim_settingcontext-class"></a><span data-ttu-id="3d721-103">CIM \_ settingcontext-Klasse</span><span class="sxs-lookup"><span data-stu-id="3d721-103">CIM\_SettingContext class</span></span>

<span data-ttu-id="3d721-104">Die **CIM \_ settingcontext** -Klasse ordnet Konfigurationsobjekte Einstellungs Objekten zu.</span><span class="sxs-lookup"><span data-stu-id="3d721-104">The **CIM\_SettingContext** class associates configuration objects with setting objects.</span></span> <span data-ttu-id="3d721-105">Beispielsweise können sich die Einstellungen eines Netzwerkadapters je nach Standort oder Netzwerk ändern, an das das Host Computersystem angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="3d721-105">For example, a network adapter's settings could change based on the site or network to which its hosting computer system is attached.</span></span> <span data-ttu-id="3d721-106">In diesem Fall würde das Computersystem zwei verschiedene Konfigurationsobjekte aufweisen, die den Unterschieden in der Netzwerkkonfiguration für die beiden Netzwerksegmente entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3d721-106">In which case, the computer system would have two different configuration objects, corresponding to the differences in network configuration for the two network segments.</span></span> <span data-ttu-id="3d721-107">Eine Konfiguration würde ein Einstellungs Objekt für den Netzwerkadapter bei der Arbeit in einem Segment aggregieren. während die andere Konfiguration ein anderes Netzwerkadapter-Einstellungs Objekt aggregiert, das für ein anderes Segment spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="3d721-107">One configuration would aggregate a setting object for the network adapter when operating on one segment; whereas, the other configuration would aggregate a different network adapter setting object, specific to another segment.</span></span> <span data-ttu-id="3d721-108">Beachten Sie, dass viele Computereinstellungen unabhängig von der Netzwerkkonfiguration sind.</span><span class="sxs-lookup"><span data-stu-id="3d721-108">Note that many computer settings are independent of the network configuration.</span></span> <span data-ttu-id="3d721-109">Beispielsweise würden beide Konfigurationen das gleiche Einstellungs Objekt für die Monitor Auflösung des Computer Systems aggregieren.</span><span class="sxs-lookup"><span data-stu-id="3d721-109">For example, both configurations would aggregate the same setting object for the computer system's monitor resolution.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d721-110">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3d721-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3d721-111">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3d721-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3d721-112">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3d721-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3d721-113">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3d721-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d721-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d721-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{F0B752E8-DB30-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_SettingContext
{
  CIM_Configuration REF Context;
  CIM_Setting       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="3d721-115">Member</span><span class="sxs-lookup"><span data-stu-id="3d721-115">Members</span></span>

<span data-ttu-id="3d721-116">Die **CIM \_ settingcontext** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3d721-116">The **CIM\_SettingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="3d721-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3d721-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d721-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3d721-118">Properties</span></span>

<span data-ttu-id="3d721-119">Die **CIM \_ settingcontext** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3d721-119">The **CIM\_SettingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d721-120">**Context**</span><span class="sxs-lookup"><span data-stu-id="3d721-120">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d721-121">Datentyp: **CIM- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="3d721-121">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="3d721-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3d721-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d721-123">Qualifizierer: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3d721-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3d721-124">Verweis auf das Konfigurationsobjekt, das die Einstellung aggregiert.</span><span class="sxs-lookup"><span data-stu-id="3d721-124">Reference to the configuration object that aggregates the setting.</span></span>

</dd> <dt>

<span data-ttu-id="3d721-125">**Einstellung**</span><span class="sxs-lookup"><span data-stu-id="3d721-125">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d721-126">Datentyp: **CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="3d721-126">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="3d721-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3d721-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d721-128">Verweis auf eine aggregierte Einstellung.</span><span class="sxs-lookup"><span data-stu-id="3d721-128">Reference to an aggregated setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d721-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d721-129">Remarks</span></span>

<span data-ttu-id="3d721-130">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3d721-130">WMI does not implement this class.</span></span>

<span data-ttu-id="3d721-131">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3d721-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3d721-132">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3d721-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d721-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d721-133">Requirements</span></span>



| <span data-ttu-id="3d721-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d721-134">Requirement</span></span> | <span data-ttu-id="3d721-135">Wert</span><span class="sxs-lookup"><span data-stu-id="3d721-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d721-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d721-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3d721-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d721-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d721-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d721-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3d721-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d721-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d721-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d721-140">Namespace</span></span><br/>                | <span data-ttu-id="3d721-141">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3d721-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d721-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3d721-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d721-143"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3d721-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d721-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3d721-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d721-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d721-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

