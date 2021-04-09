---
description: Die CIM \_ participatesinset-Klasse identifiziert physische Elemente, die zusammen ersetzt werden sollen.
ms.assetid: 417607a3-6682-4745-a5ca-0538a0d4853d
ms.tgt_platform: multiple
title: CIM_ParticipatesInSet-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParticipatesInSet
- CIM_ParticipatesInSet.Element
- CIM_ParticipatesInSet.Set
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1a581452ad6ce032dcb8d3ec5c6c0caa505f7bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861392"
---
# <a name="cim_participatesinset-class"></a><span data-ttu-id="2c286-103">CIM \_ participatesinset-Klasse</span><span class="sxs-lookup"><span data-stu-id="2c286-103">CIM\_ParticipatesInSet class</span></span>

<span data-ttu-id="2c286-104">Die **CIM \_ participatesinset** -Klasse identifiziert physische Elemente, die zusammen ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2c286-104">The **CIM\_ParticipatesInSet** class identifies physical elements that should be replaced together.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c286-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2c286-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2c286-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2c286-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2c286-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2c286-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2c286-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2c286-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c286-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c286-109">Syntax</span></span>

``` syntax
[Abstract, Association, Aggregation, UUID("{FAF76B6D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ParticipatesInSet
{
  CIM_PhysicalElement REF Element;
  CIM_ReplacementSet  REF Set;
};
```

## <a name="members"></a><span data-ttu-id="2c286-110">Member</span><span class="sxs-lookup"><span data-stu-id="2c286-110">Members</span></span>

<span data-ttu-id="2c286-111">Die **CIM- \_ partiatesinset** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2c286-111">The **CIM\_ParticipatesInSet** class has these types of members:</span></span>

-   [<span data-ttu-id="2c286-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c286-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c286-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c286-113">Properties</span></span>

<span data-ttu-id="2c286-114">Die **CIM- \_ partiatesinset** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2c286-114">The **CIM\_ParticipatesInSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c286-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c286-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c286-116">Datentyp: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="2c286-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="2c286-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c286-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c286-118">Verweis auf das physische Element, das als Satz durch andere Elemente ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c286-118">Reference to the physical element that should be replaced with other elements, as a set.</span></span>

</dd> <dt>

<span data-ttu-id="2c286-119">**Set**</span><span class="sxs-lookup"><span data-stu-id="2c286-119">**Set**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c286-120">Datentyp: **CIM \_ replacementset**</span><span class="sxs-lookup"><span data-stu-id="2c286-120">Data type: **CIM\_ReplacementSet**</span></span>
</dt> <dt>

<span data-ttu-id="2c286-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2c286-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c286-122">Qualifizierer: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2c286-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2c286-123">Verweis auf den Ersetzungs Satz von Elementen.</span><span class="sxs-lookup"><span data-stu-id="2c286-123">Reference to the replacement set of elements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c286-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c286-124">Remarks</span></span>

<span data-ttu-id="2c286-125">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="2c286-125">WMI does not implement this class.</span></span>

<span data-ttu-id="2c286-126">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2c286-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2c286-127">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2c286-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c286-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c286-128">Requirements</span></span>



| <span data-ttu-id="2c286-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c286-129">Requirement</span></span> | <span data-ttu-id="2c286-130">Wert</span><span class="sxs-lookup"><span data-stu-id="2c286-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c286-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c286-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2c286-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c286-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c286-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c286-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2c286-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c286-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c286-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c286-135">Namespace</span></span><br/>                | <span data-ttu-id="2c286-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2c286-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2c286-137">MOF</span><span class="sxs-lookup"><span data-stu-id="2c286-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c286-138"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2c286-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c286-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2c286-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c286-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c286-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

