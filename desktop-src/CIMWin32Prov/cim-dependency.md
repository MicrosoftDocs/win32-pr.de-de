---
description: Die CIM- \_ Abhängigkeits Klasse stellt eine Zuordnung dar, die Abhängigkeitsbeziehungen zwischen Objekten herstellt.
ms.assetid: ff0d6b50-0920-443e-a984-e6a9ab4402b1
ms.tgt_platform: multiple
title: CIM_Dependency-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b95d45efff51128b08dc5b6395309f49e85a79e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748497"
---
# <a name="cim_dependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="6ef60-103">CIM_Dependency-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="6ef60-103">CIM_Dependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="6ef60-104">Die **CIM- \_ Abhängigkeits** Klasse stellt eine Zuordnung dar, die Abhängigkeitsbeziehungen zwischen Objekten herstellt.</span><span class="sxs-lookup"><span data-stu-id="6ef60-104">The **CIM\_Dependency** class represents an association that establishes dependency relationships between objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ef60-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6ef60-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6ef60-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6ef60-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6ef60-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="6ef60-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6ef60-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6ef60-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef60-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ef60-109">Syntax</span></span>

``` syntax
[Association, Abstract, UUID("{8502C53A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedSystemElement REF Antecedent;
  CIM_ManagedSystemElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6ef60-110">Member</span><span class="sxs-lookup"><span data-stu-id="6ef60-110">Members</span></span>

<span data-ttu-id="6ef60-111">Die **CIM- \_ Abhängigkeits** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6ef60-111">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="6ef60-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ef60-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ef60-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ef60-113">Properties</span></span>

<span data-ttu-id="6ef60-114">Die **CIM- \_ Abhängigkeits** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6ef60-114">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ef60-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="6ef60-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ef60-116">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="6ef60-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="6ef60-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ef60-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ef60-118">Verweis auf das unabhängige Objekt in dieser Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="6ef60-118">Reference to the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="6ef60-119">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="6ef60-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ef60-120">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="6ef60-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="6ef60-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ef60-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ef60-122">Verweis auf das Objekt, das von der **Vorgänger** Eigenschaft abhängt.</span><span class="sxs-lookup"><span data-stu-id="6ef60-122">Reference to the object that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ef60-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ef60-123">Remarks</span></span>

<span data-ttu-id="6ef60-124">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6ef60-124">WMI does not implement this class.</span></span> <span data-ttu-id="6ef60-125">Weitere Informationen zu Klassen, die von **CIM- \_ Abhängigkeit** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6ef60-125">For more information about classes derived from **CIM\_Dependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6ef60-126">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6ef60-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6ef60-127">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ef60-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef60-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ef60-128">Requirements</span></span>



| <span data-ttu-id="6ef60-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ef60-129">Requirement</span></span> | <span data-ttu-id="6ef60-130">Wert</span><span class="sxs-lookup"><span data-stu-id="6ef60-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef60-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ef60-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6ef60-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ef60-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ef60-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ef60-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6ef60-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ef60-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ef60-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ef60-135">Namespace</span></span><br/>                | <span data-ttu-id="6ef60-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6ef60-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6ef60-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6ef60-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ef60-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6ef60-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ef60-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6ef60-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ef60-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ef60-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




