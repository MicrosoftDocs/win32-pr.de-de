---
description: Die CIM \_ -memorywithmedia-Klasse ordnet physischen Speicher einem physischen Medium und der zugehörigen Cartridge zu. Der Arbeitsspeicher bietet Medien Identifikation und speichert benutzerspezifische Daten.
ms.assetid: 99806d2d-6575-431d-9149-dc8ea767146c
ms.tgt_platform: multiple
title: CIM_MemoryWithMedia-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryWithMedia
- CIM_MemoryWithMedia.Dependent
- CIM_MemoryWithMedia.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b990f8ba842f313449b6f24f4e2ce59787f7841
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351638"
---
# <a name="cim_memorywithmedia-class"></a><span data-ttu-id="9b9d7-104">CIM \_ memorywithmedia-Klasse</span><span class="sxs-lookup"><span data-stu-id="9b9d7-104">CIM\_MemoryWithMedia class</span></span>

<span data-ttu-id="9b9d7-105">Die **CIM- \_ memorywithmedia** -Klasse ordnet physischen Speicher einem physischen Medium und der zugehörigen Cartridge zu.</span><span class="sxs-lookup"><span data-stu-id="9b9d7-105">The **CIM\_MemoryWithMedia** class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="9b9d7-106">Der Arbeitsspeicher bietet Medien Identifikation und speichert benutzerspezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="9b9d7-106">The memory provides media identification and stores user-specific data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b9d7-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9b9d7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9b9d7-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9b9d7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9b9d7-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="9b9d7-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9b9d7-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9b9d7-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b9d7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b9d7-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryWithMedia : CIM_Dependency
{
  CIM_PhysicalMedia  REF Dependent;
  CIM_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="9b9d7-112">Member</span><span class="sxs-lookup"><span data-stu-id="9b9d7-112">Members</span></span>

<span data-ttu-id="9b9d7-113">Die **CIM- \_ memorywithmedia** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9b9d7-113">The **CIM\_MemoryWithMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="9b9d7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b9d7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b9d7-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b9d7-115">Properties</span></span>

<span data-ttu-id="9b9d7-116">Die **CIM- \_ memorywithmedia** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9b9d7-116">The **CIM\_MemoryWithMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b9d7-117">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="9b9d7-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b9d7-118">Datentyp: **CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="9b9d7-118">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="9b9d7-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b9d7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b9d7-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="9b9d7-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9b9d7-121">Ein [**CIM- \_ PhysicalMemory**](cim-physicalmemory.md) , der den physischen Medien zugeordneten Arbeitsspeicher beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9b9d7-121">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) that describes the memory associated with physical media.</span></span>

</dd> <dt>

<span data-ttu-id="9b9d7-122">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="9b9d7-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b9d7-123">Datentyp: **CIM \_ physicalmedia**</span><span class="sxs-lookup"><span data-stu-id="9b9d7-123">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="9b9d7-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b9d7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b9d7-125">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="9b9d7-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9b9d7-126">Ein [**CIM- \_ physicalmedia**](cim-physicalmedia.md) , das die physischen Medien beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9b9d7-126">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b9d7-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b9d7-127">Remarks</span></span>

<span data-ttu-id="9b9d7-128">**CIM \_ Memorywithmedia** wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9b9d7-128">**CIM\_MemoryWithMedia** is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="9b9d7-129">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9b9d7-129">WMI does not implement this class.</span></span>

<span data-ttu-id="9b9d7-130">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9b9d7-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9b9d7-131">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9b9d7-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b9d7-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b9d7-132">Requirements</span></span>



| <span data-ttu-id="9b9d7-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b9d7-133">Requirement</span></span> | <span data-ttu-id="9b9d7-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9b9d7-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b9d7-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b9d7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9b9d7-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b9d7-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b9d7-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b9d7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9b9d7-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b9d7-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b9d7-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b9d7-139">Namespace</span></span><br/>                | <span data-ttu-id="9b9d7-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9b9d7-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b9d7-141">MOF</span><span class="sxs-lookup"><span data-stu-id="9b9d7-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b9d7-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9b9d7-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b9d7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9b9d7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b9d7-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b9d7-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b9d7-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b9d7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b9d7-146">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="9b9d7-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

