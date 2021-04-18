---
description: Die CIM- \_ Aktion "aktionequenz" definiert eine Reihe von Vorgängen, die das Softwareelement (auf das durch die CIM- \_ softwareelementactions-Zuordnung verwiesen wird) in den nächsten Zustand übergehen oder das Softwareelement aus seinem aktuellen Zustand entfernt.
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: CIM_ActionSequence-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71150d1ad9785d81579d8f305fe46bc6b7e57d00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340118"
---
# <a name="cim_actionsequence-class"></a><span data-ttu-id="7aacc-103">CIM- \_ Aktions Sequenz Klasse</span><span class="sxs-lookup"><span data-stu-id="7aacc-103">CIM\_ActionSequence class</span></span>

<span data-ttu-id="7aacc-104">Die CIM-Aktion " **\_ aktionequenz** " definiert eine Reihe von Vorgängen, die das Softwareelement (auf das durch die [**CIM- \_ softwareelementactions**](cim-softwareelementactions.md) -Zuordnung verwiesen wird) in den nächsten Zustand übergehen oder das Softwareelement aus seinem aktuellen Zustand entfernt.</span><span class="sxs-lookup"><span data-stu-id="7aacc-104">The **CIM\_ActionSequence** association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

<span data-ttu-id="7aacc-105">Die Aktionen des nächsten Zustands und die Deinstallations Aktionen, die einem bestimmten Softwareelement zugeordnet sind, müssen eine fortlaufende Sequenz sein.</span><span class="sxs-lookup"><span data-stu-id="7aacc-105">The next-state actions and uninstall actions associated with a particular software element must be a continuous sequence.</span></span> <span data-ttu-id="7aacc-106">Da **CIM \_ Action Sequence** eine Zuordnung ist, bilden die Schleifen für die [**CIM- \_ Aktions**](cim-action.md) Klasse mit Rollen für die Aktion "vorheriger" und "Next" eine Sequenz.</span><span class="sxs-lookup"><span data-stu-id="7aacc-106">Since **CIM\_ActionSequence** is an association, the loops on the [**CIM\_Action**](cim-action.md) class, with roles for the "prior" action and "next" action, form a sequence.</span></span>

<span data-ttu-id="7aacc-107">Die Notwendigkeit einer kontinuierlichen Sequenz impliziert Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7aacc-107">The need for a continuous sequence implies:</span></span>

-   <span data-ttu-id="7aacc-108">Innerhalb des Satzes von Aktionen des nächsten Zustands oder der Deinstallation gibt es nur eine Aktion, die nicht über eine Instanz der CIM-Aktion " **\_ Action Sequence** " verfügt, die in der Rolle "Next" darauf verweist.</span><span class="sxs-lookup"><span data-stu-id="7aacc-108">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "next" role.</span></span> <span data-ttu-id="7aacc-109">Dies ist die erste Aktion in der Sequenz.</span><span class="sxs-lookup"><span data-stu-id="7aacc-109">This is the first action in the sequence.</span></span>
-   <span data-ttu-id="7aacc-110">Innerhalb des Satzes von Aktionen des nächsten Zustands oder der Deinstallation gibt es nur eine Aktion, die nicht über eine Instanz der CIM-Aktion " **\_ Action Sequence** " verfügt, die in der Rolle "vorheriger" darauf verweist.</span><span class="sxs-lookup"><span data-stu-id="7aacc-110">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "prior" role.</span></span> <span data-ttu-id="7aacc-111">Dies ist die letzte Aktion in der Sequenz.</span><span class="sxs-lookup"><span data-stu-id="7aacc-111">This is the last action in the sequence.</span></span>
-   <span data-ttu-id="7aacc-112">Alle anderen Aktionen innerhalb des Satzes von Aktionen vom Typ "Nächster Zustand" und "deinstallieren" müssen an zwei Instanzen der CIM-Aktion " **\_ aktionequenz** " teilnehmen, eine in der Rolle "vorheriger" und eine in der Rolle "Next".</span><span class="sxs-lookup"><span data-stu-id="7aacc-112">All other actions within the set of next-state and uninstall actions must participate in two instances of the **CIM\_ActionSequence** association, one in a "prior" role and one in the "next" role.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7aacc-113">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7aacc-113">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7aacc-114">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7aacc-114">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7aacc-115">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="7aacc-115">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7aacc-116">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7aacc-116">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aacc-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="7aacc-117">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a><span data-ttu-id="7aacc-118">Member</span><span class="sxs-lookup"><span data-stu-id="7aacc-118">Members</span></span>

<span data-ttu-id="7aacc-119">Die **CIM- \_ Aktions Sequenz** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7aacc-119">The **CIM\_ActionSequence** class has these types of members:</span></span>

-   [<span data-ttu-id="7aacc-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7aacc-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7aacc-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7aacc-121">Properties</span></span>

<span data-ttu-id="7aacc-122">Die **CIM- \_ Aktions Sequenz** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7aacc-122">The **CIM\_ActionSequence** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7aacc-123">**Nächste**</span><span class="sxs-lookup"><span data-stu-id="7aacc-123">**Next**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aacc-124">Datentyp: **CIM- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="7aacc-124">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="7aacc-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aacc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aacc-126">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="7aacc-126">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aacc-127">Verweis auf die nächste Aktion.</span><span class="sxs-lookup"><span data-stu-id="7aacc-127">Reference to the next action.</span></span>

</dd> <dt>

<span data-ttu-id="7aacc-128">**Vor**</span><span class="sxs-lookup"><span data-stu-id="7aacc-128">**Prior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aacc-129">Datentyp: **CIM- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="7aacc-129">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="7aacc-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aacc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aacc-131">Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="7aacc-131">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="7aacc-132">Verweis auf die vorherige Aktion.</span><span class="sxs-lookup"><span data-stu-id="7aacc-132">Reference to the prior action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7aacc-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7aacc-133">Remarks</span></span>

<span data-ttu-id="7aacc-134">Die [**CIM- \_ Aktions**](cim-action.md) Klassen, die an dieser Zuordnung beteiligt sind, müssen über denselben Wert für die **Direction** -Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="7aacc-134">The [**CIM\_Action**](cim-action.md) classes participating in this association must have the same value for the **Direction** property.</span></span>

<span data-ttu-id="7aacc-135">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7aacc-135">WMI does not implement this class.</span></span>

<span data-ttu-id="7aacc-136">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7aacc-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7aacc-137">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7aacc-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aacc-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7aacc-138">Requirements</span></span>



| <span data-ttu-id="7aacc-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7aacc-139">Requirement</span></span> | <span data-ttu-id="7aacc-140">Wert</span><span class="sxs-lookup"><span data-stu-id="7aacc-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7aacc-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7aacc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7aacc-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7aacc-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7aacc-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7aacc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7aacc-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7aacc-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7aacc-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="7aacc-145">Namespace</span></span><br/>                | <span data-ttu-id="7aacc-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7aacc-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7aacc-147">MOF</span><span class="sxs-lookup"><span data-stu-id="7aacc-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7aacc-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7aacc-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7aacc-149">DLL</span><span class="sxs-lookup"><span data-stu-id="7aacc-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7aacc-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7aacc-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aacc-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7aacc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aacc-152">CIM-Klassen</span><span class="sxs-lookup"><span data-stu-id="7aacc-152">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

