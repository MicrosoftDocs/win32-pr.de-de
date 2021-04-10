---
description: Das CIM \_ CollectionOfMSEs-Objekt ermöglicht das Gruppieren von CIM \_ ManagedSystemElement-Objekten zum Zweck der Zuordnung von Einstellungen und Konfigurationen. Es ist abstrakt, eine weitere Definition und semantische Optimierung in Unterklassen zu erfordern.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: CIM_CollectionOfMSEs-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127109"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="02252-104">CIM_CollectionOfMSEs-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="02252-104">CIM_CollectionOfMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="02252-105">Das **CIM \_ CollectionOfMSEs** -Objekt ermöglicht das Gruppieren von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Objekten zum Zweck der Zuordnung von Einstellungen und Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="02252-105">The **CIM\_CollectionOfMSEs** object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="02252-106">Es ist abstrakt, eine weitere Definition und semantische Optimierung in Unterklassen zu erfordern.</span><span class="sxs-lookup"><span data-stu-id="02252-106">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

<span data-ttu-id="02252-107">Das **CIM \_ CollectionOfMSEs** -Objekt enthält keine Zustands-oder Statusinformationen, sondern stellt nur eine Gruppierung von Elementen dar.</span><span class="sxs-lookup"><span data-stu-id="02252-107">The **CIM\_CollectionOfMSEs** object does not carry any state or status information, but only represents a grouping of elements.</span></span> <span data-ttu-id="02252-108">Aus diesem Grund ist es nicht möglich, Unterklassen Gruppen mit dem Status/Status von **CIM \_ CollectionOfMSEs** zu unterordnen. ein Beispiel hierfür ist [**CIM \_ redundant cygroup**](cim-redundancygroup.md) (die ordnungsgemäß von [**CIM \_ LogicalElement**](cim-logicalelement.md)untergeordnet ist).</span><span class="sxs-lookup"><span data-stu-id="02252-108">For this reason, it is incorrect to subclass groups that have state/status from **CIM\_CollectionOfMSEs**, An example is [**CIM\_RedundancyGroup**](cim-redundancygroup.md) (which is correctly subclassed from [**CIM\_LogicalElement**](cim-logicalelement.md)).</span></span> <span data-ttu-id="02252-109">Auflistungen aggregieren üblicherweise "like"-Objekte und stellen eine Optimierung dar.</span><span class="sxs-lookup"><span data-stu-id="02252-109">Collections typically aggregate 'like' objects, and represent an optimization.</span></span> <span data-ttu-id="02252-110">Ohne Auflistungen ist es gezwungen, einzelne [**CIM- \_ Element Setting**](cim-elementsetting.md) -und [**CIM \_ Element Configuration**](cim-elementconfiguration.md) -Zuordnungen zu definieren, um Einstellungen und Konfigurationsobjekte an einzelne [**CIM \_ ManagedSystemElements**](cim-managedsystemelement.md)zu binden.</span><span class="sxs-lookup"><span data-stu-id="02252-110">Without collections, one is forced to define individual [**CIM\_ElementSetting**](cim-elementsetting.md) and [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) associations, to tie settings and configuration objects to individual [**CIM\_ManagedSystemElements**](cim-managedsystemelement.md).</span></span> <span data-ttu-id="02252-111">Es kann sehr viel dupliziert werden, wenn die gleiche Einstellung mehreren Objekten zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="02252-111">There may be much duplication in assigning the same setting to multiple objects.</span></span> <span data-ttu-id="02252-112">Außerdem ermöglicht die Verwendung des Auflistungs Objekts die Bestimmung, dass die Einstellungs-und Konfigurations Zuordnungen für die Mitglieder der Auflistung tatsächlich identisch sind.</span><span class="sxs-lookup"><span data-stu-id="02252-112">In addition, using the collection object allows the determination that the setting and configuration associations are indeed the same for the collection's members.</span></span> <span data-ttu-id="02252-113">Diese Informationen würden Sie andernfalls erhalten, indem Sie die Auflistung auf proprietäre Weise definieren und dann die CIM- **\_ Element Setting** -und **CIM \_ ElementConfiguration** -Zuordnungen Abfragen, um zu ermitteln, ob der Sammlungs Satz vollständig abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="02252-113">This information would otherwise be obtained by defining the collection in a proprietary manner, and then querying the **CIM\_ElementSetting** and **CIM\_ElementConfiguration** associations to determine if the collection set is completely covered.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02252-114">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="02252-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="02252-115">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="02252-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="02252-116">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="02252-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="02252-117">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="02252-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="02252-118">Syntax</span><span class="sxs-lookup"><span data-stu-id="02252-118">Syntax</span></span>

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a><span data-ttu-id="02252-119">Member</span><span class="sxs-lookup"><span data-stu-id="02252-119">Members</span></span>

<span data-ttu-id="02252-120">Die **CIM \_ CollectionOfMSEs** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="02252-120">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="02252-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02252-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02252-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02252-122">Properties</span></span>

<span data-ttu-id="02252-123">Die **CIM \_ CollectionOfMSEs** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02252-123">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02252-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="02252-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02252-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="02252-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02252-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02252-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02252-127">Kurze Textbeschreibung für das CollectionOfMSEs-Objekt.</span><span class="sxs-lookup"><span data-stu-id="02252-127">Short textual description of the CollectionOfMSEs object.</span></span>

</dd> <dt>

<span data-ttu-id="02252-128">**Sammlungs**</span><span class="sxs-lookup"><span data-stu-id="02252-128">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02252-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="02252-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02252-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02252-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02252-131">Identifikation des Auflistungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="02252-131">Identification of the Collection object.</span></span> <span data-ttu-id="02252-132">Bei einer Unterklasse kann die CollectionId-Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="02252-132">When subclassed, the CollectionID property can be overridden to be a Key property.</span></span>

</dd> <dt>

<span data-ttu-id="02252-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="02252-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02252-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="02252-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02252-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02252-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02252-136">Textbeschreibung des CollectionOfMSEs-Objekts.</span><span class="sxs-lookup"><span data-stu-id="02252-136">Textual description of the CollectionOfMSEs object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02252-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02252-137">Remarks</span></span>

<span data-ttu-id="02252-138">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="02252-138">WMI does not implement this class.</span></span> <span data-ttu-id="02252-139">Siehe [Win32-Klassen](win32-provider.md) für WMI-Klassen, die von **CIM \_ CollectionOfMSEs** abgeleitet sind.</span><span class="sxs-lookup"><span data-stu-id="02252-139">See [Win32 Classes](win32-provider.md) for WMI classes derived from **CIM\_CollectionOfMSEs**.</span></span>

<span data-ttu-id="02252-140">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="02252-140">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="02252-141">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="02252-141">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="02252-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02252-142">Requirements</span></span>



| <span data-ttu-id="02252-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02252-143">Requirement</span></span> | <span data-ttu-id="02252-144">Wert</span><span class="sxs-lookup"><span data-stu-id="02252-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02252-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02252-145">Minimum supported client</span></span><br/> | <span data-ttu-id="02252-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02252-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02252-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02252-147">Minimum supported server</span></span><br/> | <span data-ttu-id="02252-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02252-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02252-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="02252-149">Namespace</span></span><br/>                | <span data-ttu-id="02252-150">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="02252-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="02252-151">MOF</span><span class="sxs-lookup"><span data-stu-id="02252-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02252-152"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="02252-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="02252-153">DLL</span><span class="sxs-lookup"><span data-stu-id="02252-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02252-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02252-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




