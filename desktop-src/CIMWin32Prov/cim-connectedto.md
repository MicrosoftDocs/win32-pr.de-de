---
description: Die CIM \_ connectedto-Klasse stellt eine Zuordnung dar, die angibt, dass zwei oder mehr physische Connectors verbunden sind.
ms.assetid: fedd9227-8a3b-461a-995b-08cbceb81181
ms.tgt_platform: multiple
title: CIM_ConnectedTo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectedTo
- CIM_ConnectedTo.Dependent
- CIM_ConnectedTo.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f1a507cb529f2040607024e1a6167ddcd5dc7c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041462"
---
# <a name="cim_connectedto-class"></a><span data-ttu-id="b146d-103">CIM \_ connectedto-Klasse</span><span class="sxs-lookup"><span data-stu-id="b146d-103">CIM\_ConnectedTo class</span></span>

<span data-ttu-id="b146d-104">Die **CIM \_ connectedto** -Klasse stellt eine Zuordnung dar, die angibt, dass zwei oder mehr physische Connectors verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="b146d-104">The **CIM\_ConnectedTo** class represents an association that indicates that two or more physical connectors are connected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b146d-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b146d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b146d-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b146d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b146d-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b146d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b146d-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b146d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b146d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b146d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B85-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectedTo : CIM_Dependency
{
  CIM_PhysicalConnector REF Dependent;
  CIM_PhysicalConnector REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="b146d-110">Member</span><span class="sxs-lookup"><span data-stu-id="b146d-110">Members</span></span>

<span data-ttu-id="b146d-111">Die **CIM- \_ connectedto** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b146d-111">The **CIM\_ConnectedTo** class has these types of members:</span></span>

-   [<span data-ttu-id="b146d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b146d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b146d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b146d-113">Properties</span></span>

<span data-ttu-id="b146d-114">Die **CIM \_ connectedto** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b146d-114">The **CIM\_ConnectedTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b146d-115">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="b146d-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b146d-116">Datentyp: **CIM \_ physicalconnector**</span><span class="sxs-lookup"><span data-stu-id="b146d-116">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="b146d-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b146d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b146d-118">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="b146d-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b146d-119">Ein [**CIM \_ physicalconnector**](cim-physicalconnector.md) , der einen physischen Connector darstellt, der als ein Ende der Verbindung fungiert.</span><span class="sxs-lookup"><span data-stu-id="b146d-119">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents a physical connector that serves as one end of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="b146d-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="b146d-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b146d-121">Datentyp: **CIM \_ physicalconnector**</span><span class="sxs-lookup"><span data-stu-id="b146d-121">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="b146d-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b146d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b146d-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="b146d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b146d-124">Ein [**CIM \_ physicalconnector**](cim-physicalconnector.md) , der einen anderen physischen Connector darstellt, der als das andere Ende der Verbindung fungiert.</span><span class="sxs-lookup"><span data-stu-id="b146d-124">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents another physical connector that serves as the other end of the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b146d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b146d-125">Remarks</span></span>

<span data-ttu-id="b146d-126">Die **CIM- \_ connectedto** -Klasse wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b146d-126">The **CIM\_ConnectedTo** class is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="b146d-127">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b146d-127">WMI does not implement this class.</span></span>

<span data-ttu-id="b146d-128">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b146d-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b146d-129">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b146d-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b146d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b146d-130">Requirements</span></span>



| <span data-ttu-id="b146d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b146d-131">Requirement</span></span> | <span data-ttu-id="b146d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b146d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b146d-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b146d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b146d-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b146d-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b146d-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b146d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b146d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b146d-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b146d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="b146d-137">Namespace</span></span><br/>                | <span data-ttu-id="b146d-138">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b146d-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b146d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b146d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b146d-140"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b146d-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b146d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b146d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b146d-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b146d-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b146d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b146d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b146d-144">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="b146d-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

