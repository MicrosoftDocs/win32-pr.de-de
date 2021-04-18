---
description: Die CIM- \_ softwarefeaturesoftwareelements-Zuordnung identifiziert die Software Elemente, die ein bestimmtes Software Feature bilden.
ms.assetid: 933586c5-b85e-4136-b557-5151a48abc32
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureSoftwareElements-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSoftwareElements
- CIM_SoftwareFeatureSoftwareElements.PartComponent
- CIM_SoftwareFeatureSoftwareElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71712ebb3f8bf2ab2067325f16cf31af7fb1dc38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344345"
---
# <a name="cim_softwarefeaturesoftwareelements-class"></a><span data-ttu-id="4e26d-103">CIM \_ softwarefeaturesoftwareelements-Klasse</span><span class="sxs-lookup"><span data-stu-id="4e26d-103">CIM\_SoftwareFeatureSoftwareElements class</span></span>

<span data-ttu-id="4e26d-104">Die **CIM- \_ softwarefeaturesoftwareelements** -Zuordnung identifiziert die Software Elemente, die ein bestimmtes Software Feature bilden.</span><span class="sxs-lookup"><span data-stu-id="4e26d-104">The **CIM\_SoftwareFeatureSoftwareElements** association identifies the software elements that make up a specific software feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e26d-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4e26d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4e26d-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4e26d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4e26d-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4e26d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4e26d-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4e26d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e26d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e26d-109">Syntax</span></span>

``` syntax
[UUID("{A91081E2-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSoftwareElements : CIM_Component
{
  CIM_SoftwareElement REF PartComponent;
  CIM_SoftwareFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="4e26d-110">Member</span><span class="sxs-lookup"><span data-stu-id="4e26d-110">Members</span></span>

<span data-ttu-id="4e26d-111">Die **CIM- \_ softwarefeaturesoftwareelements** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4e26d-111">The **CIM\_SoftwareFeatureSoftwareElements** class has these types of members:</span></span>

-   [<span data-ttu-id="4e26d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4e26d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e26d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4e26d-113">Properties</span></span>

<span data-ttu-id="4e26d-114">Die **CIM- \_ softwarefeaturesoftwareelements** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4e26d-114">The **CIM\_SoftwareFeatureSoftwareElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e26d-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4e26d-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e26d-116">Datentyp: **CIM \_ Softwarefeature**</span><span class="sxs-lookup"><span data-stu-id="4e26d-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="4e26d-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e26d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e26d-118">Qualifizierer: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4e26d-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4e26d-119">Die Gruppen Komponente.</span><span class="sxs-lookup"><span data-stu-id="4e26d-119">The group component.</span></span>

<span data-ttu-id="4e26d-120">Diese Eigenschaft wird von der [**CIM- \_ Komponente**](cim-component.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e26d-120">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e26d-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4e26d-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e26d-122">Datentyp: **CIM \_ Softwareelement**</span><span class="sxs-lookup"><span data-stu-id="4e26d-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="4e26d-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e26d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e26d-124">Die Komponente Part.</span><span class="sxs-lookup"><span data-stu-id="4e26d-124">The part component.</span></span>

<span data-ttu-id="4e26d-125">Diese Eigenschaft wird von der [**CIM- \_ Komponente**](cim-component.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e26d-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e26d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e26d-126">Remarks</span></span>

<span data-ttu-id="4e26d-127">Die **CIM- \_ softwarefeaturesoftwareelements** -Zuordnung wird von der [**CIM- \_ Komponente**](cim-component.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4e26d-127">The **CIM\_SoftwareFeatureSoftwareElements** association is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="4e26d-128">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4e26d-128">WMI does not implement this class.</span></span> <span data-ttu-id="4e26d-129">Informationen zu WMI-Klassen, die von **CIM \_ softwarefeaturesoftwareelements** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4e26d-129">For WMI classes derived from **CIM\_SoftwareFeatureSoftwareElements**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4e26d-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4e26d-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4e26d-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4e26d-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e26d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e26d-132">Requirements</span></span>



| <span data-ttu-id="4e26d-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e26d-133">Requirement</span></span> | <span data-ttu-id="4e26d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="4e26d-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e26d-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e26d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4e26d-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e26d-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e26d-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e26d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4e26d-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e26d-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e26d-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e26d-139">Namespace</span></span><br/>                | <span data-ttu-id="4e26d-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4e26d-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e26d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="4e26d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e26d-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4e26d-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e26d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4e26d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e26d-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e26d-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e26d-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e26d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e26d-146">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="4e26d-146">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

