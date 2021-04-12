---
description: Die CIM \_ biosfeaturebioselements-Klasse ordnet eine BIOS-Funktion und deren aggregierte BIOS-Elemente zu.
ms.assetid: 84ebd6d0-af42-4e82-bad3-1f934789cbfe
ms.tgt_platform: multiple
title: CIM_BIOSFeatureBIOSElements-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeatureBIOSElements
- CIM_BIOSFeatureBIOSElements.PartComponent
- CIM_BIOSFeatureBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a4eecea97b4d82fadcdc521d378b5b32d986b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127197"
---
# <a name="cim_biosfeaturebioselements-class"></a><span data-ttu-id="95d77-103">CIM \_ biosfeaturebioselements-Klasse</span><span class="sxs-lookup"><span data-stu-id="95d77-103">CIM\_BIOSFeatureBIOSElements class</span></span>

<span data-ttu-id="95d77-104">Die **CIM \_ biosfeaturebioselements** -Klasse ordnet eine BIOS-Funktion und deren aggregierte BIOS-Elemente zu.</span><span class="sxs-lookup"><span data-stu-id="95d77-104">The **CIM\_BIOSFeatureBIOSElements** class associates a BIOS feature and its aggregated BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95d77-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="95d77-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="95d77-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="95d77-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="95d77-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="95d77-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="95d77-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="95d77-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d77-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="95d77-109">Syntax</span></span>

``` syntax
[UUID("{42B2EC5C-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeatureBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_BIOSElement REF PartComponent;
  CIM_BIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="95d77-110">Member</span><span class="sxs-lookup"><span data-stu-id="95d77-110">Members</span></span>

<span data-ttu-id="95d77-111">Die CIM-Klasse " **\_ biosfeaturebioselements** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="95d77-111">The **CIM\_BIOSFeatureBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="95d77-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95d77-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95d77-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95d77-113">Properties</span></span>

<span data-ttu-id="95d77-114">Die CIM-Klasse " **\_ biosfeaturebioselements** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="95d77-114">The **CIM\_BIOSFeatureBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95d77-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="95d77-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d77-116">Datentyp: **CIM \_ biosfeature**</span><span class="sxs-lookup"><span data-stu-id="95d77-116">Data type: **CIM\_BIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="95d77-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95d77-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d77-118">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="95d77-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="95d77-119">Ein [**CIM- \_ biosfeature**](cim-biosfeature.md) , das die BIOS-Funktion beschreibt.</span><span class="sxs-lookup"><span data-stu-id="95d77-119">A [**CIM\_BIOSFeature**](cim-biosfeature.md) that describes the BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="95d77-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="95d77-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95d77-121">Datentyp: **CIM \_ bioselements**</span><span class="sxs-lookup"><span data-stu-id="95d77-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="95d77-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="95d77-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95d77-123">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="95d77-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="95d77-124">Ein [**CIM- \_ bioselement**](cim-bioselement.md) , das das BIOS-Element beschreibt, das die von der BIOS-Funktion beschriebenen Funktionen implementiert.</span><span class="sxs-lookup"><span data-stu-id="95d77-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS element that implements the capabilities described by BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95d77-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95d77-125">Remarks</span></span>

<span data-ttu-id="95d77-126">Die CIM-Klasse " **\_ biosfeaturebioselements** " ist von " [**CIM \_ softwarefeaturesoftwareelements**](cim-softwarefeaturesoftwareelements.md)" abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="95d77-126">The **CIM\_BIOSFeatureBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="95d77-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="95d77-127">WMI does not implement this class.</span></span>

<span data-ttu-id="95d77-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="95d77-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="95d77-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="95d77-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="95d77-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95d77-130">Requirements</span></span>



| <span data-ttu-id="95d77-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95d77-131">Requirement</span></span> | <span data-ttu-id="95d77-132">Wert</span><span class="sxs-lookup"><span data-stu-id="95d77-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95d77-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95d77-133">Minimum supported client</span></span><br/> | <span data-ttu-id="95d77-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95d77-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95d77-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95d77-135">Minimum supported server</span></span><br/> | <span data-ttu-id="95d77-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95d77-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95d77-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="95d77-137">Namespace</span></span><br/>                | <span data-ttu-id="95d77-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="95d77-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95d77-139">MOF</span><span class="sxs-lookup"><span data-stu-id="95d77-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95d77-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="95d77-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95d77-141">DLL</span><span class="sxs-lookup"><span data-stu-id="95d77-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95d77-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95d77-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d77-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95d77-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d77-144">**CIM- \_ softwarefeaturesoftwareelements**</span><span class="sxs-lookup"><span data-stu-id="95d77-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

