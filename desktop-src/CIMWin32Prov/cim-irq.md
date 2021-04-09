---
description: Die CIM- \_ Klasse "iriq" stellt eine Intel Architecture Interrupt Request Line (UNQ) dar.
ms.assetid: d72d4914-c57b-496d-a9fe-d8f5b522504c
ms.tgt_platform: multiple
title: CIM_IRQ-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_IRQ
- CIM_IRQ.Caption
- CIM_IRQ.Description
- CIM_IRQ.InstallDate
- CIM_IRQ.Name
- CIM_IRQ.Status
- CIM_IRQ.Availability
- CIM_IRQ.CreationClassName
- CIM_IRQ.CSCreationClassName
- CIM_IRQ.CSName
- CIM_IRQ.IRQNumber
- CIM_IRQ.Shareable
- CIM_IRQ.TriggerLevel
- CIM_IRQ.TriggerType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03a336caa02c766160fe6501f91b28f06a872ecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861247"
---
# <a name="cim_irq-class"></a><span data-ttu-id="0660b-103">CIM- \_ Klasse "iriq"</span><span class="sxs-lookup"><span data-stu-id="0660b-103">CIM\_IRQ class</span></span>

<span data-ttu-id="0660b-104">Die CIM-Klasse " **\_ iriq** " stellt eine Intel Architecture Interrupt Request Line (UNQ) dar.</span><span class="sxs-lookup"><span data-stu-id="0660b-104">The **CIM\_IRQ** class represents an Intel architecture interrupt request line (IRQ).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0660b-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0660b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0660b-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0660b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0660b-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0660b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0660b-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0660b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0660b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0660b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_IRQ : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint32   IRQNumber;
  boolean  Shareable;
  uint16   TriggerLevel;
  uint16   TriggerType;
};
```

## <a name="members"></a><span data-ttu-id="0660b-110">Member</span><span class="sxs-lookup"><span data-stu-id="0660b-110">Members</span></span>

<span data-ttu-id="0660b-111">Die CIM-Klasse " **\_ iriq** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0660b-111">The **CIM\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="0660b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0660b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0660b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0660b-113">Properties</span></span>

<span data-ttu-id="0660b-114">Die CIM-Klasse " **\_ iriq** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0660b-114">The **CIM\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0660b-115">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="0660b-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0660b-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-118">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| UNQ \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="0660b-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="0660b-119">Verfügbarkeit von "UNQ".</span><span class="sxs-lookup"><span data-stu-id="0660b-119">Availability of the IRQ.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0660b-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0660b-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0660b-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="0660b-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="0660b-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Verfügbar** (3)</span><span class="sxs-lookup"><span data-stu-id="0660b-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="0660b-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Gebrauch/nicht verfügbar** (4)</span><span class="sxs-lookup"><span data-stu-id="0660b-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="0660b-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Verwendung und verfügbar/frei stellbar** (5)</span><span class="sxs-lookup"><span data-stu-id="0660b-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0660b-125">In Verwendung und verfügbar/Sharable</span><span class="sxs-lookup"><span data-stu-id="0660b-125">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0660b-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0660b-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0660b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-129">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0660b-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0660b-130">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0660b-130">A short textual description of the object.</span></span>

<span data-ttu-id="0660b-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0660b-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0660b-132">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="0660b-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0660b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-135">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0660b-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0660b-136">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0660b-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0660b-137">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="0660b-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="0660b-138">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0660b-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0660b-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-141">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0660b-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0660b-142">Der Name der Erstellungs Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="0660b-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="0660b-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="0660b-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0660b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-146">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0660b-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0660b-147">Der Name des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0660b-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="0660b-148">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0660b-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0660b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-151">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0660b-151">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0660b-152">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0660b-152">A textual description of the object.</span></span>

<span data-ttu-id="0660b-153">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0660b-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0660b-154">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0660b-154">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-155">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0660b-155">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-157">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="0660b-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0660b-158">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0660b-158">Indicates when the object was installed.</span></span> <span data-ttu-id="0660b-159">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0660b-159">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0660b-160">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0660b-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0660b-161">**"Unqnumber"**</span><span class="sxs-lookup"><span data-stu-id="0660b-161">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-162">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0660b-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-164">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| UNQ \| 001,1 "), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0660b-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0660b-165">Ein Teil des Schlüssel Werts des Objekts, "UNQ Number".</span><span class="sxs-lookup"><span data-stu-id="0660b-165">Part of the object's key value, IRQ number.</span></span>

</dd> <dt>

<span data-ttu-id="0660b-166">**Name**</span><span class="sxs-lookup"><span data-stu-id="0660b-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0660b-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-169">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0660b-169">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0660b-170">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0660b-170">Label by which the object is known.</span></span> <span data-ttu-id="0660b-171">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0660b-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0660b-172">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0660b-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0660b-173">**Freigegeben**</span><span class="sxs-lookup"><span data-stu-id="0660b-173">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-174">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0660b-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-176">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| UNQ \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="0660b-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="0660b-177">**True** gibt an, dass die UNQ freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="0660b-177">If **TRUE**, the IRQ can be shared.</span></span>

</dd> <dt>

<span data-ttu-id="0660b-178">**Status**</span><span class="sxs-lookup"><span data-stu-id="0660b-178">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0660b-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-181">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0660b-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0660b-182">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="0660b-182">String that indicates the current status of the object.</span></span> <span data-ttu-id="0660b-183">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0660b-183">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0660b-184">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="0660b-184">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0660b-185">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="0660b-185">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0660b-186">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="0660b-186">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0660b-187">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="0660b-187">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0660b-188">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="0660b-188">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0660b-189">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0660b-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0660b-190">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="0660b-190">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0660b-191">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0660b-191">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0660b-192">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="0660b-192">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0660b-193">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="0660b-193">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0660b-194">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="0660b-194">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0660b-195">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0660b-195">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0660b-196">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="0660b-196">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0660b-197">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="0660b-197">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0660b-198">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="0660b-198">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0660b-199">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="0660b-199">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0660b-200">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="0660b-200">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0660b-201">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="0660b-201">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0660b-202">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="0660b-202">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0660b-203">**Triggerlevel**</span><span class="sxs-lookup"><span data-stu-id="0660b-203">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-204">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0660b-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-206">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource UNQ Info \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="0660b-206">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="0660b-207">Gibt an, ob die Unterbrechung durch das hohe oder niedrige Hardware Signal ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="0660b-207">Indicates whether the interruption is triggered by the hardware signal going high or low.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0660b-208">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0660b-208">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0660b-209">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="0660b-209">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="0660b-210">**Aktiv, niedrig** (3)</span><span class="sxs-lookup"><span data-stu-id="0660b-210">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="0660b-211">**Aktiv hoch** (4)</span><span class="sxs-lookup"><span data-stu-id="0660b-211">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0660b-212">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="0660b-212">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0660b-213">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0660b-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0660b-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0660b-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0660b-215">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| UNQ \| 001,3 "," MIF. DMTF- \| System Ressource UNQ Info \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="0660b-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="0660b-216">Art der Unterbrechung, die auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="0660b-216">Type of interruption that can occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0660b-217">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="0660b-217">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0660b-218">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="0660b-218">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="0660b-219">**Ebene** (3)</span><span class="sxs-lookup"><span data-stu-id="0660b-219">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="0660b-220">**Edge** (4)</span><span class="sxs-lookup"><span data-stu-id="0660b-220">**Edge** (4)</span></span>


<span data-ttu-id="0660b-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0660b-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="0660b-222">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0660b-222">Remarks</span></span>

<span data-ttu-id="0660b-223">Die CIM-Klasse " **\_ iriq** " wird von [**CIM \_ Systemresource**](cim-systemresource.md)abgeleitet. Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0660b-223">The **CIM\_IRQ** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).WMI does not implement this class.</span></span> <span data-ttu-id="0660b-224">Siehe [Win32-Klassen](win32-provider.md) für Klassen, die von **CIM \_ UNQ** abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0660b-224">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_IRQ**.</span></span>

<span data-ttu-id="0660b-225">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0660b-225">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0660b-226">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0660b-226">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0660b-227">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0660b-227">Requirements</span></span>



| <span data-ttu-id="0660b-228">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0660b-228">Requirement</span></span> | <span data-ttu-id="0660b-229">Wert</span><span class="sxs-lookup"><span data-stu-id="0660b-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0660b-230">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0660b-230">Minimum supported client</span></span><br/> | <span data-ttu-id="0660b-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0660b-231">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0660b-232">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0660b-232">Minimum supported server</span></span><br/> | <span data-ttu-id="0660b-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0660b-233">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0660b-234">Namespace</span><span class="sxs-lookup"><span data-stu-id="0660b-234">Namespace</span></span><br/>                | <span data-ttu-id="0660b-235">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0660b-235">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0660b-236">MOF</span><span class="sxs-lookup"><span data-stu-id="0660b-236">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0660b-237"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0660b-237"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0660b-238">DLL</span><span class="sxs-lookup"><span data-stu-id="0660b-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0660b-239"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0660b-239"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0660b-240">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0660b-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0660b-241">**CIM- \_ Systemresource**</span><span class="sxs-lookup"><span data-stu-id="0660b-241">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

