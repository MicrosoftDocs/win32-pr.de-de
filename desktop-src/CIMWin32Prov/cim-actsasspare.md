---
description: Die CIM- \_ aczasspare-Zuordnung gibt an, welche Elemente Spares sein können oder andere aggregierte Elemente ersetzen. Ein Ersatz kann in &\# 0034; Hot-Standby&\# 0034;-Modus ausgeführt werden, wie auf Element Weise angegeben.
ms.assetid: bed8c552-f782-4af9-9441-ff3268182c3b
ms.tgt_platform: multiple
title: CIM_ActsAsSpare-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActsAsSpare
- CIM_ActsAsSpare.Group
- CIM_ActsAsSpare.HotStandby
- CIM_ActsAsSpare.Spare
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 975c6317a78789938ea9d34e062d84fe3435498a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958485"
---
# <a name="cim_actsasspare-class"></a><span data-ttu-id="52c48-104">CIM- \_ acsiasspare-Klasse</span><span class="sxs-lookup"><span data-stu-id="52c48-104">CIM\_ActsAsSpare class</span></span>

<span data-ttu-id="52c48-105">Die **CIM- \_ aczasspare-Zuordnung** gibt an, welche Elemente Spares sein können oder andere aggregierte Elemente ersetzen.</span><span class="sxs-lookup"><span data-stu-id="52c48-105">The **CIM\_ActsAsSpare** association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="52c48-106">Ein Ersatz kann im Modus "Hot-Standby" ausgeführt werden, wie auf Element Weise angegeben.</span><span class="sxs-lookup"><span data-stu-id="52c48-106">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52c48-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="52c48-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="52c48-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="52c48-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="52c48-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="52c48-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="52c48-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="52c48-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c48-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="52c48-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{64C1726E-DB21-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ActsAsSpare
{
  CIM_SpareGroup           REF Group;
  boolean                      HotStandby;
  CIM_ManagedSystemElement REF Spare;
};
```

## <a name="members"></a><span data-ttu-id="52c48-112">Member</span><span class="sxs-lookup"><span data-stu-id="52c48-112">Members</span></span>

<span data-ttu-id="52c48-113">Die **CIM- \_ aczasspare** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="52c48-113">The **CIM\_ActsAsSpare** class has these types of members:</span></span>

-   [<span data-ttu-id="52c48-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52c48-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52c48-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52c48-115">Properties</span></span>

<span data-ttu-id="52c48-116">Die **CIM- \_ acsiasspare** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="52c48-116">The **CIM\_ActsAsSpare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52c48-117">**Gruppieren**</span><span class="sxs-lookup"><span data-stu-id="52c48-117">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52c48-118">Datentyp: **CIM \_ SpareGroup**</span><span class="sxs-lookup"><span data-stu-id="52c48-118">Data type: **CIM\_SpareGroup**</span></span>
</dt> <dt>

<span data-ttu-id="52c48-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52c48-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52c48-120">Verweis auf die **Group** -Eigenschaft, die die [**CIM \_ SpareGroup**](cim-sparegroup.md) -Klasse darstellt.</span><span class="sxs-lookup"><span data-stu-id="52c48-120">Reference to the **Group** property that represents the [**CIM\_SpareGroup**](cim-sparegroup.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="52c48-121">**HotStandby**</span><span class="sxs-lookup"><span data-stu-id="52c48-121">**HotStandby**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52c48-122">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="52c48-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52c48-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52c48-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52c48-124">**True** gibt an, dass der Ersatz als Hot Standby betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="52c48-124">If **TRUE**, the spare is operating as a hot standby.</span></span>

</dd> <dt>

<span data-ttu-id="52c48-125">**Schonen**</span><span class="sxs-lookup"><span data-stu-id="52c48-125">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52c48-126">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="52c48-126">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="52c48-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52c48-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52c48-128">Verweis auf ein verwaltetes System Element, das als Ersatz fungiert und Teil der Ersatzgruppe ist.</span><span class="sxs-lookup"><span data-stu-id="52c48-128">Reference to a managed system element acting as a spare and participating in the spare group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52c48-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52c48-129">Remarks</span></span>

<span data-ttu-id="52c48-130">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="52c48-130">WMI does not implement this class.</span></span>

<span data-ttu-id="52c48-131">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="52c48-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="52c48-132">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="52c48-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="52c48-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52c48-133">Requirements</span></span>



| <span data-ttu-id="52c48-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52c48-134">Requirement</span></span> | <span data-ttu-id="52c48-135">Wert</span><span class="sxs-lookup"><span data-stu-id="52c48-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52c48-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52c48-136">Minimum supported client</span></span><br/> | <span data-ttu-id="52c48-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52c48-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52c48-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52c48-138">Minimum supported server</span></span><br/> | <span data-ttu-id="52c48-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52c48-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52c48-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="52c48-140">Namespace</span></span><br/>                | <span data-ttu-id="52c48-141">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="52c48-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="52c48-142">MOF</span><span class="sxs-lookup"><span data-stu-id="52c48-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52c48-143"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="52c48-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="52c48-144">DLL</span><span class="sxs-lookup"><span data-stu-id="52c48-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52c48-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52c48-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52c48-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52c48-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c48-147">CIM-Klassen</span><span class="sxs-lookup"><span data-stu-id="52c48-147">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

