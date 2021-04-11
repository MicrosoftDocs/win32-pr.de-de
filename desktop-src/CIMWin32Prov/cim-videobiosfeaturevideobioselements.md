---
description: Die CIM \_ videobiosfeaturevideobioselements-Klasse ordnet eine Video-BIOS-Funktion und ihre aggregierten Video-BIOS-Elemente zu.
ms.assetid: f1419505-213f-450e-8c96-45f547dd71da
ms.tgt_platform: multiple
title: CIM_VideoBIOSFeatureVideoBIOSElements-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeatureVideoBIOSElements
- CIM_VideoBIOSFeatureVideoBIOSElements.PartComponent
- CIM_VideoBIOSFeatureVideoBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 421b6814499240b3364ac1aed622e2b7c96e7313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126655"
---
# <a name="cim_videobiosfeaturevideobioselements-class"></a><span data-ttu-id="05bbc-103">CIM \_ videobiosfeaturevideobioselements-Klasse</span><span class="sxs-lookup"><span data-stu-id="05bbc-103">CIM\_VideoBIOSFeatureVideoBIOSElements class</span></span>

<span data-ttu-id="05bbc-104">Die **CIM \_ videobiosfeaturevideobioselements** -Klasse ordnet eine Video-BIOS-Funktion und ihre aggregierten Video-BIOS-Elemente zu.</span><span class="sxs-lookup"><span data-stu-id="05bbc-104">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05bbc-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="05bbc-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="05bbc-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="05bbc-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="05bbc-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="05bbc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="05bbc-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="05bbc-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="05bbc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="05bbc-109">Syntax</span></span>

``` syntax
[UUID("{B3F86390-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeatureVideoBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_VideoBIOSElement REF PartComponent;
  CIM_VideoBIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="05bbc-110">Member</span><span class="sxs-lookup"><span data-stu-id="05bbc-110">Members</span></span>

<span data-ttu-id="05bbc-111">Die **CIM \_ videobiosfeaturevideobioselements** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="05bbc-111">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="05bbc-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="05bbc-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="05bbc-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="05bbc-113">Properties</span></span>

<span data-ttu-id="05bbc-114">Die **CIM \_ videobiosfeaturevideobioselements** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="05bbc-114">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05bbc-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="05bbc-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05bbc-116">Datentyp: **CIM \_ videobiosfeature**</span><span class="sxs-lookup"><span data-stu-id="05bbc-116">Data type: **CIM\_VideoBIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="05bbc-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05bbc-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05bbc-118">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="05bbc-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="05bbc-119">Ein [**CIM \_ videobiosfeature**](cim-videobiosfeature.md) , das die Video-BIOS-Funktion beschreibt.</span><span class="sxs-lookup"><span data-stu-id="05bbc-119">A [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) that describes the video BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="05bbc-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="05bbc-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05bbc-121">Datentyp: **CIM \_ videobioselements**</span><span class="sxs-lookup"><span data-stu-id="05bbc-121">Data type: **CIM\_VideoBIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="05bbc-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="05bbc-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05bbc-123">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="05bbc-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="05bbc-124">Ein [**CIM- \_ videobioselement**](cim-videobioselement.md) , das das Video-BIOS-Element beschreibt, das die Funktionen implementiert, die von der Video-BIOS-Funktion</span><span class="sxs-lookup"><span data-stu-id="05bbc-124">A [**CIM\_VideoBIOSElement**](cim-videobioselement.md) that describes the video BIOS element that implements the capabilities described by video BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05bbc-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05bbc-125">Remarks</span></span>

<span data-ttu-id="05bbc-126">Die **CIM \_ videobiosfeaturevideobioselements** -Klasse wird von [**CIM \_ softwarefeaturesoftwareelements**](cim-softwarefeaturesoftwareelements.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="05bbc-126">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="05bbc-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="05bbc-127">WMI does not implement this class.</span></span>

<span data-ttu-id="05bbc-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="05bbc-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="05bbc-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="05bbc-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="05bbc-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05bbc-130">Requirements</span></span>



| <span data-ttu-id="05bbc-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05bbc-131">Requirement</span></span> | <span data-ttu-id="05bbc-132">Wert</span><span class="sxs-lookup"><span data-stu-id="05bbc-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05bbc-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05bbc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="05bbc-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05bbc-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05bbc-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05bbc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="05bbc-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05bbc-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05bbc-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="05bbc-137">Namespace</span></span><br/>                | <span data-ttu-id="05bbc-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="05bbc-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="05bbc-139">MOF</span><span class="sxs-lookup"><span data-stu-id="05bbc-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05bbc-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="05bbc-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="05bbc-141">DLL</span><span class="sxs-lookup"><span data-stu-id="05bbc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05bbc-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05bbc-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05bbc-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05bbc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05bbc-144">**CIM- \_ softwarefeaturesoftwareelements**</span><span class="sxs-lookup"><span data-stu-id="05bbc-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

