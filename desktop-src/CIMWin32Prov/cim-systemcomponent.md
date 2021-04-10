---
description: Eine Common Information Model (CIM)-Zuordnungs Klasse, mit der Beziehungen zwischen einem System und den verwalteten Systemelementen hergestellt werden, von denen es zusammengesetzt wird.
ms.assetid: 11ad6dc1-a09a-4bab-bb1d-2131a8fdb812
ms.tgt_platform: multiple
title: CIM_SystemComponent-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.PartComponent
- CIM_SystemComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9aae4e4ef916916f54bddea814844f23ed7315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127101"
---
# <a name="cim_systemcomponent-class-cimwin32-wmi-providers"></a><span data-ttu-id="b1beb-103">CIM_SystemComponent-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="b1beb-103">CIM_SystemComponent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b1beb-104">Die **CIM- \_ SystemComponent** -Klasse ist eine Common Information Model (CIM)-Zuordnungs Klasse, die Beziehungen zwischen einem System und den verwalteten Systemelementen herstellt, aus denen es besteht.</span><span class="sxs-lookup"><span data-stu-id="b1beb-104">The **CIM\_SystemComponent** class is a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1beb-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b1beb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b1beb-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b1beb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b1beb-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1beb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b1beb-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b1beb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1beb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1beb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{527BC6CE-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_ManagedSystemElement REF PartComponent;
  CIM_System               REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="b1beb-110">Member</span><span class="sxs-lookup"><span data-stu-id="b1beb-110">Members</span></span>

<span data-ttu-id="b1beb-111">Die **CIM \_ SystemComponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b1beb-111">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="b1beb-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1beb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1beb-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1beb-113">Properties</span></span>

<span data-ttu-id="b1beb-114">Die **CIM \_ SystemComponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1beb-114">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1beb-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b1beb-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1beb-116">Datentyp: **CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="b1beb-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="b1beb-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1beb-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1beb-118">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="b1beb-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b1beb-119">Ein [**CIM- \_ System**](cim-system.md) , das das übergeordnete System in der Zuordnung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b1beb-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="b1beb-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b1beb-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1beb-121">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="b1beb-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="b1beb-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b1beb-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1beb-123">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="b1beb-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b1beb-124">Ein [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) , das das untergeordnete Element beschreibt, das eine Komponente eines Systems ist.</span><span class="sxs-lookup"><span data-stu-id="b1beb-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1beb-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1beb-125">Remarks</span></span>

<span data-ttu-id="b1beb-126">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b1beb-126">WMI does not implement this class.</span></span> <span data-ttu-id="b1beb-127">Informationen zu WMI-Klassen, die von **CIM \_ SystemComponent** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="b1beb-127">For WMI classes derived from **CIM\_SystemComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b1beb-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b1beb-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b1beb-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b1beb-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1beb-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1beb-130">Requirements</span></span>



| <span data-ttu-id="b1beb-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1beb-131">Requirement</span></span> | <span data-ttu-id="b1beb-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b1beb-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1beb-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1beb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b1beb-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1beb-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1beb-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1beb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b1beb-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1beb-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1beb-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1beb-137">Namespace</span></span><br/>                | <span data-ttu-id="b1beb-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b1beb-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b1beb-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b1beb-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1beb-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b1beb-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1beb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b1beb-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1beb-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1beb-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1beb-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1beb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1beb-144">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="b1beb-144">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

