---
description: Die CIM \_ bootosfromfs-Klasse ordnet das Betriebssystem und die Dateisysteme zu, von denen das Betriebssystem geladen wurde.
ms.assetid: c5697e9c-9031-4787-a03d-cf713c961cdf
ms.tgt_platform: multiple
title: CIM_BootOSFromFS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootOSFromFS
- CIM_BootOSFromFS.Dependent
- CIM_BootOSFromFS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 993ee7a66ef9f8b0cbb47285e38b78e4fd4dd61b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958458"
---
# <a name="cim_bootosfromfs-class"></a><span data-ttu-id="fe0c6-103">CIM \_ bootosfromfs-Klasse</span><span class="sxs-lookup"><span data-stu-id="fe0c6-103">CIM\_BootOSFromFS class</span></span>

<span data-ttu-id="fe0c6-104">Die **CIM \_ bootosfromfs** -Klasse ordnet das Betriebssystem und die Dateisysteme zu, von denen das Betriebssystem geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="fe0c6-104">The **CIM\_BootOSFromFS** class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="fe0c6-105">Die Zuordnung ist m:n-. ein verteiltes Betriebssystem kann davon abhängen, dass mehrere Dateisysteme ordnungsgemäß und vollständig geladen werden.</span><span class="sxs-lookup"><span data-stu-id="fe0c6-105">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe0c6-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fe0c6-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fe0c6-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fe0c6-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fe0c6-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="fe0c6-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fe0c6-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fe0c6-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe0c6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe0c6-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{5F5B101E-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BootOSFromFS : CIM_Dependency
{
  CIM_OperatingSystem REF Dependent;
  CIM_FileSystem      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="fe0c6-111">Member</span><span class="sxs-lookup"><span data-stu-id="fe0c6-111">Members</span></span>

<span data-ttu-id="fe0c6-112">Die **CIM \_ bootosfromfs** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fe0c6-112">The **CIM\_BootOSFromFS** class has these types of members:</span></span>

-   [<span data-ttu-id="fe0c6-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe0c6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe0c6-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe0c6-114">Properties</span></span>

<span data-ttu-id="fe0c6-115">Die **CIM \_ bootosfromfs** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fe0c6-115">The **CIM\_BootOSFromFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe0c6-116">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="fe0c6-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe0c6-117">Datentyp: **CIM \_ File System**</span><span class="sxs-lookup"><span data-stu-id="fe0c6-117">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="fe0c6-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe0c6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe0c6-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="fe0c6-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fe0c6-120">Das Dateisystem, von dem das Betriebssystem geladen wird.</span><span class="sxs-lookup"><span data-stu-id="fe0c6-120">The file system from which the operating system is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="fe0c6-121">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="fe0c6-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe0c6-122">Datentyp: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="fe0c6-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="fe0c6-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fe0c6-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe0c6-124">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="fe0c6-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fe0c6-125">Dem Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="fe0c6-125">The operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe0c6-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe0c6-126">Remarks</span></span>

<span data-ttu-id="fe0c6-127">Die **CIM \_ bootosfromfs** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fe0c6-127">The **CIM\_BootOSFromFS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="fe0c6-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="fe0c6-128">WMI does not implement this class.</span></span>

<span data-ttu-id="fe0c6-129">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fe0c6-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fe0c6-130">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fe0c6-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe0c6-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe0c6-131">Requirements</span></span>



| <span data-ttu-id="fe0c6-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe0c6-132">Requirement</span></span> | <span data-ttu-id="fe0c6-133">Wert</span><span class="sxs-lookup"><span data-stu-id="fe0c6-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0c6-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe0c6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0c6-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe0c6-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fe0c6-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe0c6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0c6-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe0c6-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fe0c6-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe0c6-138">Namespace</span></span><br/>                | <span data-ttu-id="fe0c6-139">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fe0c6-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fe0c6-140">MOF</span><span class="sxs-lookup"><span data-stu-id="fe0c6-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe0c6-141"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fe0c6-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe0c6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fe0c6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe0c6-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe0c6-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe0c6-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe0c6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0c6-145">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="fe0c6-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

