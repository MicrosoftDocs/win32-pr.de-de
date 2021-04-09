---
description: Die CIM \_ packagealarm-Zuordnung stellt die Beziehung dar, in der ein Alarmgerät als Teil eines Pakets installiert wird. Die Installation zeigt Probleme mit der Umgebung des Pakets an \# ,&8212, den Sicherheitsstatus oder den Gesamtzustand.
ms.assetid: 4911502a-de9c-46b4-91f6-a042c69fd052
ms.tgt_platform: multiple
title: CIM_PackageAlarm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageAlarm
- CIM_PackageAlarm.Dependent
- CIM_PackageAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 29aae3a2c1093e026356ea7a096f8b673673f67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126145"
---
# <a name="cim_packagealarm-class"></a><span data-ttu-id="b5ce0-104">CIM \_ packagealarm-Klasse</span><span class="sxs-lookup"><span data-stu-id="b5ce0-104">CIM\_PackageAlarm class</span></span>

<span data-ttu-id="b5ce0-105">Die [**CIM \_ packagealarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) -Zuordnung stellt die Beziehung dar, in der ein Alarmgerät als Teil eines Pakets installiert wird.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-105">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="b5ce0-106">Bei der Installation werden Probleme mit dem Sicherheitsstatus des Pakets oder der Gesamt Integrität des Pakets angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-106">The installation indicates issues with the package's environment its security state or its overall health.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5ce0-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b5ce0-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b5ce0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b5ce0-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b5ce0-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ce0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5ce0-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B90-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageAlarm : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_AlarmDevice     REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="b5ce0-112">Member</span><span class="sxs-lookup"><span data-stu-id="b5ce0-112">Members</span></span>

<span data-ttu-id="b5ce0-113">Die **CIM \_ packagealarm** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b5ce0-113">The **CIM\_PackageAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="b5ce0-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5ce0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5ce0-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b5ce0-115">Properties</span></span>

<span data-ttu-id="b5ce0-116">Die **CIM \_ packagealarm** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-116">The **CIM\_PackageAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5ce0-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="b5ce0-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ce0-118">Datentyp: **CIM \_ alarmdevice**</span><span class="sxs-lookup"><span data-stu-id="b5ce0-118">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="b5ce0-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5ce0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5ce0-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="b5ce0-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b5ce0-121">Ein [**CIM \_ alarmdevice**](cim-alarmdevice.md) , das das Alarmgerät für das Paket beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-121">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that describes the alarm device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="b5ce0-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="b5ce0-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ce0-123">Datentyp: **CIM \_ physicalpackage**</span><span class="sxs-lookup"><span data-stu-id="b5ce0-123">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="b5ce0-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b5ce0-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5ce0-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="b5ce0-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b5ce0-126">Ein [**CIM- \_ physicalpackage**](cim-physicalpackage.md) , das das physische Paket beschreibt, dessen Integrität, Sicherheit, Umgebung usw. alarmiert ist.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-126">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose health, security, environment, etc. is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5ce0-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5ce0-127">Remarks</span></span>

<span data-ttu-id="b5ce0-128">**CIM \_ Packagealarm** ist von [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-128">**CIM\_PackageAlarm** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="b5ce0-129">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-129">WMI does not implement this class.</span></span>

<span data-ttu-id="b5ce0-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b5ce0-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b5ce0-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ce0-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5ce0-132">Requirements</span></span>



| <span data-ttu-id="b5ce0-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5ce0-133">Requirement</span></span> | <span data-ttu-id="b5ce0-134">Wert</span><span class="sxs-lookup"><span data-stu-id="b5ce0-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ce0-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5ce0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ce0-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5ce0-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5ce0-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5ce0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ce0-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5ce0-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5ce0-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5ce0-139">Namespace</span></span><br/>                | <span data-ttu-id="b5ce0-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b5ce0-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5ce0-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b5ce0-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5ce0-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b5ce0-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5ce0-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b5ce0-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5ce0-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5ce0-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5ce0-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5ce0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ce0-146">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="b5ce0-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

