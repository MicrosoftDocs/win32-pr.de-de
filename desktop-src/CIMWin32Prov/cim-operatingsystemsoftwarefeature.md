---
description: Die CIM \_ operatingsystemsoftwarefeature-Klasse stellt die Softwarefunktionen dar, aus denen das Betriebssystem besteht.
ms.assetid: 9ffc709c-213e-4252-9662-76f01e1685e5
ms.tgt_platform: multiple
title: CIM_OperatingSystemSoftwareFeature-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystemSoftwareFeature
- CIM_OperatingSystemSoftwareFeature.PartComponent
- CIM_OperatingSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b9d74478f211b23e103854cedb09a1e0186618b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346026"
---
# <a name="cim_operatingsystemsoftwarefeature-class"></a><span data-ttu-id="d5c02-103">CIM \_ operatingsystemsoftwarefeature-Klasse</span><span class="sxs-lookup"><span data-stu-id="d5c02-103">CIM\_OperatingSystemSoftwareFeature class</span></span>

<span data-ttu-id="d5c02-104">Die **CIM \_ operatingsystemsoftwarefeature** -Klasse stellt die Softwarefunktionen dar, aus denen das Betriebssystem besteht.</span><span class="sxs-lookup"><span data-stu-id="d5c02-104">The **CIM\_OperatingSystemSoftwareFeature** class represents the software features that make up the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5c02-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d5c02-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d5c02-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d5c02-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d5c02-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d5c02-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d5c02-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d5c02-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c02-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5c02-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{96B4C734-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OperatingSystemSoftwareFeature : CIM_Component
{
  CIM_SoftwareFeature REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="d5c02-110">Member</span><span class="sxs-lookup"><span data-stu-id="d5c02-110">Members</span></span>

<span data-ttu-id="d5c02-111">Die **CIM \_ operatingsystemsoftwarefeature** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d5c02-111">The **CIM\_OperatingSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="d5c02-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d5c02-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5c02-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d5c02-113">Properties</span></span>

<span data-ttu-id="d5c02-114">Die **CIM \_ operatingsystemsoftwarefeature** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d5c02-114">The **CIM\_OperatingSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5c02-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d5c02-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5c02-116">Datentyp: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="d5c02-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d5c02-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d5c02-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5c02-118">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="d5c02-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d5c02-119">Ein [**CIM- \_ OperatingSystem**](cim-operatingsystem.md) , das das Betriebssystem beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d5c02-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="d5c02-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d5c02-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5c02-121">Datentyp: **CIM \_ Softwarefeature**</span><span class="sxs-lookup"><span data-stu-id="d5c02-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="d5c02-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d5c02-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5c02-123">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="d5c02-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d5c02-124">Ein [**CIM- \_ Softwarefeature**](cim-softwarefeature.md) , das die Software Features beschreibt, aus denen das Betriebssystem besteht.</span><span class="sxs-lookup"><span data-stu-id="d5c02-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) describing the software features that make up the operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5c02-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5c02-125">Remarks</span></span>

<span data-ttu-id="d5c02-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d5c02-126">WMI does not implement this class.</span></span>

<span data-ttu-id="d5c02-127">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d5c02-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d5c02-128">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d5c02-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c02-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5c02-129">Requirements</span></span>



| <span data-ttu-id="d5c02-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5c02-130">Requirement</span></span> | <span data-ttu-id="d5c02-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d5c02-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c02-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5c02-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c02-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5c02-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5c02-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5c02-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c02-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5c02-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5c02-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5c02-136">Namespace</span></span><br/>                | <span data-ttu-id="d5c02-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d5c02-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5c02-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d5c02-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5c02-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d5c02-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5c02-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d5c02-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5c02-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5c02-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c02-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5c02-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c02-143">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="d5c02-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

