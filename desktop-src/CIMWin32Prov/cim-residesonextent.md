---
description: Die CIM \_ residesonblock-Klasse stellt eine Zuordnung zwischen einem Dateisystem und dem Speicherblock dar, in dem es sich befindet. In der Regel befindet sich ein Dateisystem auf einem logischen Datenträger.
ms.assetid: 911a81e9-3032-41ff-a337-044c06d02307
ms.tgt_platform: multiple
title: CIM_ResidesOnExtent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResidesOnExtent
- CIM_ResidesOnExtent.Dependent
- CIM_ResidesOnExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 526023fbcc1c961ecaca068be8b0d4ce3e2f84f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127652"
---
# <a name="cim_residesonextent-class"></a><span data-ttu-id="f31d6-104">CIM \_ residesonblock-Klasse</span><span class="sxs-lookup"><span data-stu-id="f31d6-104">CIM\_ResidesOnExtent class</span></span>

<span data-ttu-id="f31d6-105">Die **CIM \_ residesonblock** -Klasse stellt eine Zuordnung zwischen einem Dateisystem und dem Speicherblock dar, in dem es sich befindet.</span><span class="sxs-lookup"><span data-stu-id="f31d6-105">The **CIM\_ResidesOnExtent** class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="f31d6-106">In der Regel befindet sich ein Dateisystem auf einem logischen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="f31d6-106">Typically, a file system resides on a logical disk.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f31d6-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f31d6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f31d6-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f31d6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f31d6-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f31d6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f31d6-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f31d6-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f31d6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f31d6-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{10458E26-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ResidesOnExtent : CIM_Dependency
{
  CIM_FileSystem    REF Dependent;
  CIM_StorageExtent REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f31d6-112">Member</span><span class="sxs-lookup"><span data-stu-id="f31d6-112">Members</span></span>

<span data-ttu-id="f31d6-113">Die **CIM \_ residesonblock** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f31d6-113">The **CIM\_ResidesOnExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="f31d6-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f31d6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f31d6-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f31d6-115">Properties</span></span>

<span data-ttu-id="f31d6-116">Die **CIM \_ residesonblock** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f31d6-116">The **CIM\_ResidesOnExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f31d6-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="f31d6-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f31d6-118">Datentyp: **CIM \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="f31d6-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="f31d6-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f31d6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f31d6-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="f31d6-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f31d6-121">Ein [**CIM- \_ storageblock**](cim-storageextent.md) , der den Speicherblock beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f31d6-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="f31d6-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="f31d6-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f31d6-123">Datentyp: **CIM \_ File System**</span><span class="sxs-lookup"><span data-stu-id="f31d6-123">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="f31d6-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f31d6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f31d6-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="f31d6-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f31d6-126">Ein [**CIM- \_ Datei**](cim-filesystem.md) System, das das Dateisystem im Speicherblock beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f31d6-126">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system that is located on the storage extent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f31d6-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f31d6-127">Remarks</span></span>

<span data-ttu-id="f31d6-128">Die **CIM \_ residesonblock** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f31d6-128">The **CIM\_ResidesOnExtent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="f31d6-129">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f31d6-129">WMI does not implement this class.</span></span>

<span data-ttu-id="f31d6-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f31d6-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f31d6-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f31d6-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f31d6-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f31d6-132">Requirements</span></span>



| <span data-ttu-id="f31d6-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f31d6-133">Requirement</span></span> | <span data-ttu-id="f31d6-134">Wert</span><span class="sxs-lookup"><span data-stu-id="f31d6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f31d6-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f31d6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f31d6-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f31d6-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f31d6-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f31d6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f31d6-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f31d6-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f31d6-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="f31d6-139">Namespace</span></span><br/>                | <span data-ttu-id="f31d6-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f31d6-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f31d6-141">MOF</span><span class="sxs-lookup"><span data-stu-id="f31d6-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f31d6-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f31d6-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f31d6-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f31d6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f31d6-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f31d6-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f31d6-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f31d6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31d6-146">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="f31d6-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

