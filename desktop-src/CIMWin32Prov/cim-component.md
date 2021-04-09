---
description: Die CIM- \_ Komponenten Zuordnung stellt die Bestandteile einer Beziehung zwischen MSES dar.
ms.assetid: a074e2f7-b092-4d3c-be5e-2069b643431b
ms.tgt_platform: multiple
title: CIM_Component-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b516118bc0cd6f12285933b1c15e7f2801ad40d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861336"
---
# <a name="cim_component-class-cimwin32-wmi-providers"></a><span data-ttu-id="60cda-103">CIM_Component-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="60cda-103">CIM_Component class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="60cda-104">Die **CIM- \_ Komponenten** Zuordnung stellt die Bestandteile einer Beziehung zwischen MSES dar.</span><span class="sxs-lookup"><span data-stu-id="60cda-104">The **CIM\_Component** association represents the parts of a relationship between MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60cda-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="60cda-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="60cda-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="60cda-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="60cda-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="60cda-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="60cda-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="60cda-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="60cda-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="60cda-109">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, UUID("{8502C573-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="60cda-110">Member</span><span class="sxs-lookup"><span data-stu-id="60cda-110">Members</span></span>

<span data-ttu-id="60cda-111">Die **CIM- \_ Komponenten** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="60cda-111">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="60cda-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60cda-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60cda-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60cda-113">Properties</span></span>

<span data-ttu-id="60cda-114">Die **CIM- \_ Komponenten** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="60cda-114">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60cda-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="60cda-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60cda-116">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="60cda-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="60cda-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60cda-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60cda-118">Qualifizierer: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="60cda-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="60cda-119">Ein [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) , das das übergeordnete Element in der Zuordnung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="60cda-119">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="60cda-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="60cda-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60cda-121">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="60cda-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="60cda-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60cda-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60cda-123">Ein [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) , das das untergeordnete Element in der Zuordnung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="60cda-123">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60cda-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60cda-124">Remarks</span></span>

<span data-ttu-id="60cda-125">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="60cda-125">WMI does not implement this class.</span></span> <span data-ttu-id="60cda-126">Weitere Informationen zu von **CIM- \_ Komponenten** abgeleiteten Klassen finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="60cda-126">For more information about classes derived from **CIM\_Component**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="60cda-127">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="60cda-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="60cda-128">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="60cda-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="60cda-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60cda-129">Requirements</span></span>



| <span data-ttu-id="60cda-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60cda-130">Requirement</span></span> | <span data-ttu-id="60cda-131">Wert</span><span class="sxs-lookup"><span data-stu-id="60cda-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60cda-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60cda-132">Minimum supported client</span></span><br/> | <span data-ttu-id="60cda-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60cda-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60cda-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60cda-134">Minimum supported server</span></span><br/> | <span data-ttu-id="60cda-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60cda-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60cda-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="60cda-136">Namespace</span></span><br/>                | <span data-ttu-id="60cda-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="60cda-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60cda-138">MOF</span><span class="sxs-lookup"><span data-stu-id="60cda-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60cda-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="60cda-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60cda-140">DLL</span><span class="sxs-lookup"><span data-stu-id="60cda-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60cda-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60cda-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

