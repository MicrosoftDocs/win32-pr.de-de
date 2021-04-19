---
description: Die CIM \_ computersystemdma-Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren DMA-Kanälen (Direct Memory Access) dar.
ms.assetid: 7d5bce4b-973f-4452-b403-a2196bd4017a
ms.tgt_platform: multiple
title: CIM_ComputerSystemDMA-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemDMA
- CIM_ComputerSystemDMA.PartComponent
- CIM_ComputerSystemDMA.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23748a3b10c11878069a81cd82f7f69d0ab75792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346854"
---
# <a name="cim_computersystemdma-class"></a><span data-ttu-id="d4865-103">CIM \_ computersystemdma-Klasse</span><span class="sxs-lookup"><span data-stu-id="d4865-103">CIM\_ComputerSystemDMA class</span></span>

<span data-ttu-id="d4865-104">Die **CIM \_ computersystemdma** -Klasse stellt eine Zuordnung zwischen einem Computersystem und den verfügbaren DMA-Kanälen (Direct Memory Access) dar.</span><span class="sxs-lookup"><span data-stu-id="d4865-104">The **CIM\_ComputerSystemDMA** class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4865-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4865-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d4865-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d4865-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d4865-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="d4865-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d4865-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d4865-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4865-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4865-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340B-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemDMA : CIM_ComputerSystemResource
{
  CIM_DMA            REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="d4865-110">Member</span><span class="sxs-lookup"><span data-stu-id="d4865-110">Members</span></span>

<span data-ttu-id="d4865-111">Die **CIM \_ computersystemdma** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d4865-111">The **CIM\_ComputerSystemDMA** class has these types of members:</span></span>

-   [<span data-ttu-id="d4865-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4865-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d4865-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4865-113">Properties</span></span>

<span data-ttu-id="d4865-114">Die **CIM \_ computersystemdma** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d4865-114">The **CIM\_ComputerSystemDMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4865-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d4865-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4865-116">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="d4865-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d4865-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4865-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4865-118">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="d4865-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d4865-119">Ein [**CIM- \_ Computersystem**](cim-computersystem.md) , das den dem DMA zugeordneten Computer beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d4865-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer associated with the DMA.</span></span>

</dd> <dt>

<span data-ttu-id="d4865-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d4865-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4865-121">Datentyp: **CIM \_ DMA**</span><span class="sxs-lookup"><span data-stu-id="d4865-121">Data type: **CIM\_DMA**</span></span>
</dt> <dt>

<span data-ttu-id="d4865-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d4865-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4865-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("PartComponent"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d4865-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d4865-124">Ein [**CIM \_ DMA**](cim-dma.md) , der einen DMA-Kanal des Computer Systems beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d4865-124">A [**CIM\_DMA**](cim-dma.md) that describes a DMA channel of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4865-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4865-125">Remarks</span></span>

<span data-ttu-id="d4865-126">Die **CIM \_ computersystemdma** -Klasse wird von [**CIM \_ computersystemresource**](cim-computersystemresource.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d4865-126">The **CIM\_ComputerSystemDMA** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="d4865-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="d4865-127">WMI does not implement this class.</span></span>

<span data-ttu-id="d4865-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d4865-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d4865-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d4865-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4865-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4865-130">Requirements</span></span>



| <span data-ttu-id="d4865-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4865-131">Requirement</span></span> | <span data-ttu-id="d4865-132">Wert</span><span class="sxs-lookup"><span data-stu-id="d4865-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4865-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4865-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d4865-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4865-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4865-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4865-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d4865-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4865-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4865-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4865-137">Namespace</span></span><br/>                | <span data-ttu-id="d4865-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d4865-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d4865-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d4865-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4865-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d4865-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4865-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d4865-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4865-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4865-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4865-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4865-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4865-144">**CIM \_ computersystemresource**</span><span class="sxs-lookup"><span data-stu-id="d4865-144">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

