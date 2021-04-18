---
description: Die CIM \_ slotinslot-Beziehung stellt die Fähigkeit eines speziellen Adapters dar, die vorhandene slotstruktur zu erweitern, um ansonsten inkompatible Karten zu ermöglichen, die an einem Frame oder einem hostingboard angeschlossen werden.
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: CIM_SlotInSlot-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0102a431393906b5ff98339569a027cbe3ef5b40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343580"
---
# <a name="cim_slotinslot-class"></a><span data-ttu-id="7062f-103">CIM \_ slotinslot-Klasse</span><span class="sxs-lookup"><span data-stu-id="7062f-103">CIM\_SlotInSlot class</span></span>

<span data-ttu-id="7062f-104">Die **CIM \_ slotinslot** -Beziehung stellt die Fähigkeit eines speziellen Adapters dar, die vorhandene slotstruktur zu erweitern, um ansonsten inkompatible Karten zu ermöglichen, die an einem Frame oder einem hostingboard angeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7062f-104">The **CIM\_SlotInSlot** relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span> <span data-ttu-id="7062f-105">Slots sind spezielle Connectortypen, in die normalerweise Adapterkarten eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7062f-105">Slots are special types of connectors into which adapter cards are typically inserted.</span></span> <span data-ttu-id="7062f-106">Der Adapter erstellt effektiv einen neuen Slot und kann sich (konzeptionell) als Slot in einem Slot vorstellen.</span><span class="sxs-lookup"><span data-stu-id="7062f-106">The adapter effectively creates a new slot and can be thought of (conceptually) as a slot in a slot.</span></span> <span data-ttu-id="7062f-107">Karten, die andernfalls physisch oder physisch mit den vorhandenen Slots nicht kompatibel sind, werden durch die Schnittstellen mit dem vom Adapter bereitgestellten Slot unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7062f-107">Cards that would otherwise be physically or electrically incompatible with the existing slots would be supported by interfacing to the slot provided by the adapter.</span></span> <span data-ttu-id="7062f-108">Beispielsweise sind Netzwerk Boards sehr aufwendig.</span><span class="sxs-lookup"><span data-stu-id="7062f-108">For example, networking boards are very expensive.</span></span> <span data-ttu-id="7062f-109">Wenn neue Hardware verfügbar wird, ändern sich Chassis-und Karten Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="7062f-109">As new hardware becomes available, chassis and card configurations change.</span></span> <span data-ttu-id="7062f-110">Um die Investition ihrer Kunden zu schützen, werden Netzwerkhersteller spezielle Adapter bereitstellen, mit denen alte Karten in neue Chassis-oder hostingboards oder neue Karten eingefügt werden können, um Sie in alte Karten einzufügen, indem ein spezieller Adapter verwendet wird, der über einen oder mehrere vorhandene Slots passt und einen neuen Slot anzeigt, in den die Karte passt.</span><span class="sxs-lookup"><span data-stu-id="7062f-110">To protect the investment of their customers, networking vendors will manufacture special adapters that enable old cards to fit into new chassis or hosting boards or new cards to fit into old cards by using a special adapter that fits over one or more existing slots and presents a new slot into which the card can fit.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7062f-111">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7062f-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7062f-112">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7062f-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7062f-113">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7062f-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7062f-114">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7062f-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7062f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="7062f-115">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7062f-116">Member</span><span class="sxs-lookup"><span data-stu-id="7062f-116">Members</span></span>

<span data-ttu-id="7062f-117">Die **CIM \_ slotinslot** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7062f-117">The **CIM\_SlotInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="7062f-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7062f-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7062f-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7062f-119">Properties</span></span>

<span data-ttu-id="7062f-120">Die **CIM \_ slotinslot** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7062f-120">The **CIM\_SlotInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7062f-121">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="7062f-121">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7062f-122">Datentyp: **CIM- \_ Slot**</span><span class="sxs-lookup"><span data-stu-id="7062f-122">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="7062f-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7062f-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7062f-124">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="7062f-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7062f-125">Ein [**CIM- \_ Slot**](cim-slot.md) , der die vorhandenen Slots des hostingboards beschreibt, oder Frame, die an eine Karte angepasst werden, die andernfalls physisch und/oder nicht physisch kompatibel wäre.</span><span class="sxs-lookup"><span data-stu-id="7062f-125">A [**CIM\_Slot**](cim-slot.md) that describes the existing slot(s) of the hosting board, or frame that are being adapted to accommodate a card that would otherwise not be physically and/or electrically compatible with it.</span></span>

</dd> <dt>

<span data-ttu-id="7062f-126">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="7062f-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7062f-127">Datentyp: **CIM- \_ Slot**</span><span class="sxs-lookup"><span data-stu-id="7062f-127">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="7062f-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7062f-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7062f-129">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7062f-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7062f-130">Ein [**CIM- \_ Slot**](cim-slot.md) , der den neuen Slot beschreibt, der vom Adapterboard bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7062f-130">A [**CIM\_Slot**](cim-slot.md) that describes the new slot provided by the adapter board.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7062f-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7062f-131">Remarks</span></span>

<span data-ttu-id="7062f-132">Die **CIM \_ slotinslot** -Klasse wird von [**CIM \_ connectedto**](cim-connectedto.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7062f-132">The **CIM\_SlotInSlot** class is derived from [**CIM\_ConnectedTo**](cim-connectedto.md).</span></span>

<span data-ttu-id="7062f-133">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7062f-133">WMI does not implement this class.</span></span>

<span data-ttu-id="7062f-134">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7062f-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7062f-135">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7062f-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7062f-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7062f-136">Requirements</span></span>



| <span data-ttu-id="7062f-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7062f-137">Requirement</span></span> | <span data-ttu-id="7062f-138">Wert</span><span class="sxs-lookup"><span data-stu-id="7062f-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7062f-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7062f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7062f-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7062f-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7062f-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7062f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7062f-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7062f-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7062f-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="7062f-143">Namespace</span></span><br/>                | <span data-ttu-id="7062f-144">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7062f-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7062f-145">MOF</span><span class="sxs-lookup"><span data-stu-id="7062f-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7062f-146"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7062f-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7062f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7062f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7062f-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7062f-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7062f-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7062f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7062f-150">**CIM \_ connectedto**</span><span class="sxs-lookup"><span data-stu-id="7062f-150">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> </dl>

 

