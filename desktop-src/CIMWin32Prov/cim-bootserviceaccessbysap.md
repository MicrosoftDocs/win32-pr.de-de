---
description: Die CIM \_ bootserviceaccessbysap-Klasse ordnet einen Start Dienst und seine Zugriffspunkte zu.
ms.assetid: 993469dd-fb9c-4d21-99e0-03c4b19eb7fd
ms.tgt_platform: multiple
title: CIM_BootServiceAccessBySAP-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootServiceAccessBySAP
- CIM_BootServiceAccessBySAP.Dependent
- CIM_BootServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90548be52defbcf3419d6c7defc21395da5cfbfe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748617"
---
# <a name="cim_bootserviceaccessbysap-class"></a><span data-ttu-id="e82d1-103">CIM \_ bootserviceaccessbysap-Klasse</span><span class="sxs-lookup"><span data-stu-id="e82d1-103">CIM\_BootServiceAccessBySAP class</span></span>

<span data-ttu-id="e82d1-104">Die **CIM \_ bootserviceaccessbysap** -Klasse ordnet einen Start Dienst und seine Zugriffspunkte zu.</span><span class="sxs-lookup"><span data-stu-id="e82d1-104">The **CIM\_BootServiceAccessBySAP** class associates a boot service and its access points.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e82d1-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e82d1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e82d1-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e82d1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e82d1-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e82d1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e82d1-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e82d1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e82d1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e82d1-109">Syntax</span></span>

``` syntax
[UUID("{6EDF1DD2-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_BootSAP     REF Dependent;
  CIM_BootService REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e82d1-110">Member</span><span class="sxs-lookup"><span data-stu-id="e82d1-110">Members</span></span>

<span data-ttu-id="e82d1-111">Die **CIM \_ bootserviceaccessbysap** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e82d1-111">The **CIM\_BootServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="e82d1-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e82d1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e82d1-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e82d1-113">Properties</span></span>

<span data-ttu-id="e82d1-114">Die **CIM \_ bootserviceaccessbysap** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e82d1-114">The **CIM\_BootServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e82d1-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="e82d1-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e82d1-116">Datentyp: **CIM- \_ Bootservice**</span><span class="sxs-lookup"><span data-stu-id="e82d1-116">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="e82d1-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e82d1-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e82d1-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="e82d1-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e82d1-119">Ein [**CIM- \_ Bootservice**](cim-bootservice.md) , der den Start Dienst beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e82d1-119">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service.</span></span>

</dd> <dt>

<span data-ttu-id="e82d1-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="e82d1-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e82d1-121">Datentyp: **CIM \_ bootsap**</span><span class="sxs-lookup"><span data-stu-id="e82d1-121">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="e82d1-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e82d1-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e82d1-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="e82d1-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e82d1-124">Ein [**CIM- \_ bootsap**](cim-bootsap.md) , das einen Zugriffspunkt für den Start Dienst beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e82d1-124">A [**CIM\_BootSAP**](cim-bootsap.md) that describes an access point for the boot service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e82d1-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e82d1-125">Remarks</span></span>

<span data-ttu-id="e82d1-126">Die **CIM \_ bootserviceaccessbysap** -Klasse wird von [**CIM \_ serviceaccessbysap**](cim-serviceaccessbysap.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e82d1-126">The **CIM\_BootServiceAccessBySAP** class is derived from [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span></span>

<span data-ttu-id="e82d1-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="e82d1-127">WMI does not implement this class.</span></span>

<span data-ttu-id="e82d1-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e82d1-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e82d1-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e82d1-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e82d1-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e82d1-130">Requirements</span></span>



| <span data-ttu-id="e82d1-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e82d1-131">Requirement</span></span> | <span data-ttu-id="e82d1-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e82d1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e82d1-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e82d1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e82d1-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e82d1-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e82d1-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e82d1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e82d1-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e82d1-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e82d1-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="e82d1-137">Namespace</span></span><br/>                | <span data-ttu-id="e82d1-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e82d1-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e82d1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e82d1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e82d1-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e82d1-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e82d1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e82d1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e82d1-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e82d1-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e82d1-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e82d1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e82d1-144">**CIM \_ serviceaccessbysap**</span><span class="sxs-lookup"><span data-stu-id="e82d1-144">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> </dl>

 

