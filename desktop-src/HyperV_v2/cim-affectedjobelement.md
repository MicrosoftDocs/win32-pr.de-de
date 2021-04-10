---
description: Stellt eine Zuordnung zwischen einem Auftrag und den CIM \_ managedelta-Objekten dar, die von seiner Ausführung betroffen sein können.
ms.assetid: 94c5e602-214c-4003-921c-8955c3859738
title: CIM_AffectedJobElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AffectedJobElement
- CIM_AffectedJobElement.AffectedElement
- CIM_AffectedJobElement.AffectingElement
- CIM_AffectedJobElement.ElementEffects
- CIM_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 830e798ff12dc87c88126375736f116c044de731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131216"
---
# <a name="cim_affectedjobelement-class"></a><span data-ttu-id="785f4-103">CIM \_ affectedjobelements-Klasse</span><span class="sxs-lookup"><span data-stu-id="785f4-103">CIM\_AffectedJobElement class</span></span>

<span data-ttu-id="785f4-104">Stellt eine Zuordnung zwischen einem Auftrag und den **CIM \_ managedelta** -Objekten dar, die von seiner Ausführung betroffen sein können.</span><span class="sxs-lookup"><span data-stu-id="785f4-104">Represents an association between a job and the **CIM\_ManagedElement** objects that may be affected by its execution.</span></span> <span data-ttu-id="785f4-105">Möglicherweise ist es für den Auftrag nicht möglich, alle betroffenen Elemente zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="785f4-105">It may not be feasible for the job to describe all of the affected elements.</span></span> <span data-ttu-id="785f4-106">Der Hauptzweck dieser Zuordnung besteht darin, Informationen bereitzustellen, wenn für einen Auftrag eine ausschließliche Verwendung der betroffenen verwalteten Elemente erforderlich ist oder wenn die Nebeneffekte beschrieben werden, die möglicherweise entstehen.</span><span class="sxs-lookup"><span data-stu-id="785f4-106">The main purpose of this association is to provide information when a job requires exclusive use of the affected managed elements or when describing the side effects that may result.</span></span>

## <a name="syntax"></a><span data-ttu-id="785f4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="785f4-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.15.0"), UMLPackagePath("CIM::System::Processing"), AMENDMENT]
class CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Job            REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="785f4-108">Member</span><span class="sxs-lookup"><span data-stu-id="785f4-108">Members</span></span>

<span data-ttu-id="785f4-109">Die **CIM \_ affectedjobelements** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="785f4-109">The **CIM\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="785f4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="785f4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="785f4-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="785f4-111">Properties</span></span>

<span data-ttu-id="785f4-112">Die **CIM \_ affectedjobelements** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="785f4-112">The **CIM\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="785f4-113">**Affectedelta-Element**</span><span class="sxs-lookup"><span data-stu-id="785f4-113">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="785f4-114">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="785f4-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="785f4-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="785f4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="785f4-116">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="785f4-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="785f4-117">Das verwaltete Element, das von der Ausführung des Auftrags betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="785f4-117">The managed element affected by the execution of the job.</span></span>

</dd> <dt>

<span data-ttu-id="785f4-118">**Affectingelement**</span><span class="sxs-lookup"><span data-stu-id="785f4-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="785f4-119">Datentyp: **CIM- \_ Auftrag**</span><span class="sxs-lookup"><span data-stu-id="785f4-119">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="785f4-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="785f4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="785f4-121">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="785f4-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="785f4-122">Der Auftrag, der sich auf das verwaltete Element auswirkt.</span><span class="sxs-lookup"><span data-stu-id="785f4-122">The job that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="785f4-123">**Elementeffects**</span><span class="sxs-lookup"><span data-stu-id="785f4-123">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="785f4-124">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="785f4-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="785f4-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="785f4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="785f4-126">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ affectedjobeless**.**Otherelementeffect-Beschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="785f4-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="785f4-127">Die Auswirkung des Auftrags auf das verwaltete Element.</span><span class="sxs-lookup"><span data-stu-id="785f4-127">The effect the job has on the managed element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="785f4-128">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="785f4-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="785f4-129">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="785f4-129">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="785f4-130">**Exklusive Verwendung** (2)</span><span class="sxs-lookup"><span data-stu-id="785f4-130">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="785f4-131">**Leistungs Beeinträchtigung** (3)</span><span class="sxs-lookup"><span data-stu-id="785f4-131">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="785f4-132">**Element Integrität** (4)</span><span class="sxs-lookup"><span data-stu-id="785f4-132">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="785f4-133">**Erstellen** (5)</span><span class="sxs-lookup"><span data-stu-id="785f4-133">**Create** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="785f4-134">**Otherelementeffect-Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="785f4-134">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="785f4-135">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="785f4-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="785f4-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="785f4-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="785f4-137">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ affectedjobeless**.**Elementeffects**")</span><span class="sxs-lookup"><span data-stu-id="785f4-137">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="785f4-138">Weitere Details zu den entsprechenden "1"-Werten (sonstige) im **elementeffects** -Array.</span><span class="sxs-lookup"><span data-stu-id="785f4-138">Additional details for corresponding "1" (Other) values in the **ElementEffects** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="785f4-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="785f4-139">Requirements</span></span>



| <span data-ttu-id="785f4-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="785f4-140">Requirement</span></span> | <span data-ttu-id="785f4-141">Wert</span><span class="sxs-lookup"><span data-stu-id="785f4-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="785f4-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="785f4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="785f4-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="785f4-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="785f4-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="785f4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="785f4-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="785f4-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="785f4-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="785f4-146">Namespace</span></span><br/>                | <span data-ttu-id="785f4-147">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="785f4-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="785f4-148">MOF</span><span class="sxs-lookup"><span data-stu-id="785f4-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="785f4-149"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="785f4-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="785f4-150">DLL</span><span class="sxs-lookup"><span data-stu-id="785f4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="785f4-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="785f4-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

