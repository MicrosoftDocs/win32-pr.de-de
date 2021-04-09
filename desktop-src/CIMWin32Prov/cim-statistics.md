---
description: Die CIM \_ Statistics-Klasse stellt eine Zuordnung dar, die verwaltete Systemelemente mit den statistischen Gruppen verknüpft, die für Sie gelten.
ms.assetid: fc75991b-adcd-4e47-b610-7503f6bb7c03
ms.tgt_platform: multiple
title: CIM_Statistics-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Statistics
- CIM_Statistics.Element
- CIM_Statistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b35299a52c771ee3bcb76673ef1e2164af3b3180
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958207"
---
# <a name="cim_statistics-class"></a><span data-ttu-id="08371-103">CIM- \_ Statistik Klasse</span><span class="sxs-lookup"><span data-stu-id="08371-103">CIM\_Statistics class</span></span>

<span data-ttu-id="08371-104">Die **CIM \_ Statistics** -Klasse stellt eine Zuordnung dar, die verwaltete Systemelemente mit den statistischen Gruppen verknüpft, die für Sie gelten.</span><span class="sxs-lookup"><span data-stu-id="08371-104">The **CIM\_Statistics** class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08371-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="08371-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="08371-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="08371-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="08371-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08371-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="08371-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="08371-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="08371-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="08371-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A3-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_Statistics
{
  CIM_ManagedSystemElement   REF Element;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="08371-110">Member</span><span class="sxs-lookup"><span data-stu-id="08371-110">Members</span></span>

<span data-ttu-id="08371-111">Die **CIM- \_ Statistik** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="08371-111">The **CIM\_Statistics** class has these types of members:</span></span>

-   [<span data-ttu-id="08371-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08371-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08371-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08371-113">Properties</span></span>

<span data-ttu-id="08371-114">Die **CIM \_ Statistics** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08371-114">The **CIM\_Statistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08371-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="08371-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08371-116">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="08371-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="08371-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08371-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08371-118">Verweis auf die [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Klasse, für die statistische Daten oder Metrikdaten definiert werden.</span><span class="sxs-lookup"><span data-stu-id="08371-118">Reference to the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class for which statistical or metric data is defined.</span></span>

</dd> <dt>

<span data-ttu-id="08371-119">**Stats**</span><span class="sxs-lookup"><span data-stu-id="08371-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08371-120">Datentyp: **CIM \_ statisticalinformation**</span><span class="sxs-lookup"><span data-stu-id="08371-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="08371-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08371-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08371-122">Verweis auf die statistischen Informationen oder das Objekt.</span><span class="sxs-lookup"><span data-stu-id="08371-122">Reference to the statistical information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08371-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08371-123">Remarks</span></span>

<span data-ttu-id="08371-124">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="08371-124">WMI does not implement this class.</span></span>

<span data-ttu-id="08371-125">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="08371-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="08371-126">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="08371-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="08371-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08371-127">Requirements</span></span>



| <span data-ttu-id="08371-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08371-128">Requirement</span></span> | <span data-ttu-id="08371-129">Wert</span><span class="sxs-lookup"><span data-stu-id="08371-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08371-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08371-130">Minimum supported client</span></span><br/> | <span data-ttu-id="08371-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08371-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08371-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08371-132">Minimum supported server</span></span><br/> | <span data-ttu-id="08371-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08371-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08371-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="08371-134">Namespace</span></span><br/>                | <span data-ttu-id="08371-135">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="08371-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="08371-136">MOF</span><span class="sxs-lookup"><span data-stu-id="08371-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08371-137"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="08371-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="08371-138">DLL</span><span class="sxs-lookup"><span data-stu-id="08371-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08371-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08371-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




