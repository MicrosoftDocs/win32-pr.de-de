---
description: Der Win32- \_ &\# 160; Die WMI-Klasse stellt eine Anzahl von Interrupt-Anforderungs Zeilen in einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: bae0c28e-2b66-40ac-9679-b2dfe9269306
ms.tgt_platform: multiple
title: Win32_IRQResource-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IRQResource
- Win32_IRQResource.Availability
- Win32_IRQResource.Caption
- Win32_IRQResource.CreationClassName
- Win32_IRQResource.CSCreationClassName
- Win32_IRQResource.CSName
- Win32_IRQResource.Description
- Win32_IRQResource.Hardware
- Win32_IRQResource.InstallDate
- Win32_IRQResource.IRQNumber
- Win32_IRQResource.Name
- Win32_IRQResource.Shareable
- Win32_IRQResource.Status
- Win32_IRQResource.TriggerLevel
- Win32_IRQResource.TriggerType
- Win32_IRQResource.Vector
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd02487fe166cd7ce55482eaca1339c8701f2b62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126254"
---
# <a name="win32_irqresource-class"></a><span data-ttu-id="a9dab-103">Win32- \_ Klasse "iriqresource"</span><span class="sxs-lookup"><span data-stu-id="a9dab-103">Win32\_IRQResource class</span></span>

<span data-ttu-id="a9dab-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für die Win32-Klasse " **\_ iriqresource**" stellt eine Anzahl von Interrupt-Anforderungs Zeilen auf einem Computersystem mit Windows dar.  </span><span class="sxs-lookup"><span data-stu-id="a9dab-104">The **Win32\_IRQResource**  [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an interrupt request line (IRQ) number on a computer system running Windows.</span></span> <span data-ttu-id="a9dab-105">Eine Interrupt-Anforderung ist ein Signal, das von einem Gerät oder Programm für zeitkritische Ereignisse an die CPU gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9dab-105">An interrupt request is a signal sent to the CPU by a device or program for time critical events.</span></span> <span data-ttu-id="a9dab-106">Bei "UNQ" kann es sich um Hardware-oder softwarebasierte Anwendungen handeln.</span><span class="sxs-lookup"><span data-stu-id="a9dab-106">IRQ can be hardware-based or software-based.</span></span>

<span data-ttu-id="a9dab-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a9dab-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a9dab-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a9dab-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9dab-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9dab-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_IRQResource : CIM_IRQ
{
  uint16   Availability;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  boolean  Hardware;
  datetime InstallDate;
  uint32   IRQNumber;
  string   Name;
  boolean  Shareable;
  string   Status;
  uint16   TriggerLevel;
  uint16   TriggerType;
  uint32   Vector;
};
```

## <a name="members"></a><span data-ttu-id="a9dab-110">Member</span><span class="sxs-lookup"><span data-stu-id="a9dab-110">Members</span></span>

<span data-ttu-id="a9dab-111">Die Win32-Klasse " **\_ iriqresource** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a9dab-111">The **Win32\_IRQResource** class has these types of members:</span></span>

-   [<span data-ttu-id="a9dab-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9dab-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9dab-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9dab-113">Properties</span></span>

<span data-ttu-id="a9dab-114">Die Win32-Klasse " **\_ iriqresource** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a9dab-114">The **Win32\_IRQResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9dab-115">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="a9dab-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9dab-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-118">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| UNQ \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="a9dab-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-119">Verfügbarkeit von "UNQ".</span><span class="sxs-lookup"><span data-stu-id="a9dab-119">Availability of the IRQ.</span></span>

<span data-ttu-id="a9dab-120">Diese Eigenschaft wird von [**CIM \_ UNQ**](cim-irq.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-120">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a9dab-121"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="a9dab-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a9dab-122">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="a9dab-122">Other</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a9dab-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a9dab-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a9dab-124">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="a9dab-124">Unknown</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9dab-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a9dab-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a9dab-126">Verfügbar</span><span class="sxs-lookup"><span data-stu-id="a9dab-126">Available</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="a9dab-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Verfügbar** (3)</span><span class="sxs-lookup"><span data-stu-id="a9dab-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a9dab-128">In Verwendung oder nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a9dab-128">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="a9dab-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Gebrauch/nicht verfügbar** (4)</span><span class="sxs-lookup"><span data-stu-id="a9dab-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a9dab-130">In Verwendung und verfügbar oder Sharable</span><span class="sxs-lookup"><span data-stu-id="a9dab-130">In Use and Available or Sharable</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="a9dab-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Verwendung und verfügbar/frei stellbar** (5)</span><span class="sxs-lookup"><span data-stu-id="a9dab-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a9dab-132">In Verwendung und verfügbar/Sharable</span><span class="sxs-lookup"><span data-stu-id="a9dab-132">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a9dab-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a9dab-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a9dab-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-136">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a9dab-136">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-137">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a9dab-137">Short description of the object a one-line string.</span></span>

<span data-ttu-id="a9dab-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9dab-139">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="a9dab-139">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a9dab-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-142">Qualifizierer: [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a9dab-142">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-143">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9dab-143">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a9dab-144">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="a9dab-144">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a9dab-145">Diese Eigenschaft wird von [**CIM \_ UNQ**](cim-irq.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-145">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9dab-146">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a9dab-146">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a9dab-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-149">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a9dab-149">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-150">Name der System Erstellungs Klasse des Bereichs bezogenen Computers.</span><span class="sxs-lookup"><span data-stu-id="a9dab-150">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="a9dab-151">Diese Eigenschaft wird von [**CIM \_ UNQ**](cim-irq.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-151">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9dab-152">**CSName**</span><span class="sxs-lookup"><span data-stu-id="a9dab-152">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a9dab-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-155">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a9dab-155">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-156">Name des Bereichs Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="a9dab-156">Name of the scoping computer system.</span></span>

<span data-ttu-id="a9dab-157">Diese Eigenschaft wird von [**CIM \_ UNQ**](cim-irq.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-157">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9dab-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9dab-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a9dab-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-161">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a9dab-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-162">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a9dab-162">Textual description of the object.</span></span>

<span data-ttu-id="a9dab-163">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9dab-164">**Hardware**</span><span class="sxs-lookup"><span data-stu-id="a9dab-164">**Hardware**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-165">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a9dab-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-167">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Structures \| Ressourcen \_ Deskriptor \| interfaketype")</span><span class="sxs-lookup"><span data-stu-id="a9dab-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|RESOURCE\_DESCRIPTOR\|InterfaceType")</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-168">**True** gibt an, dass die Unterbrechung Hardware-oder Software basiert ist.</span><span class="sxs-lookup"><span data-stu-id="a9dab-168">If **TRUE**, the interrupt is hardware or software based.</span></span> <span data-ttu-id="a9dab-169">Bei einer Hardware-UNQ handelt es sich um ein physisches Netzwerk, das von der Peripherie auf den Chip des programmierbaren interruptcontrollers (PIC) gesendet wird, über den die CPU über zeitkritische Ereignisse benachrichtigt werden kann</span><span class="sxs-lookup"><span data-stu-id="a9dab-169">A hardware IRQ is a physical wire from the peripheral to the programmable interrupt controller (PIC) chip through which the CPU can be notified of time-critical events.</span></span> <span data-ttu-id="a9dab-170">Einige UNQ-Zeilen sind für Standardgeräte reserviert, z. b. die Tastatur, Diskettenlaufwerke und die Systemuhr.</span><span class="sxs-lookup"><span data-stu-id="a9dab-170">Some IRQ lines are reserved for standard devices, such as the keyboard, floppy disk drives, and the system clock.</span></span> <span data-ttu-id="a9dab-171">Ein Software Interrupt ermöglicht Anwendungen, die Aufmerksamkeit des Prozessors zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a9dab-171">A software interrupt allows applications to get the attention of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="a9dab-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a9dab-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-173">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9dab-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-175">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="a9dab-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-176">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a9dab-176">Date and time the object was installed.</span></span> <span data-ttu-id="a9dab-177">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a9dab-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a9dab-178">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9dab-179">**"Unqnumber"**</span><span class="sxs-lookup"><span data-stu-id="a9dab-179">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-180">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9dab-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-182">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| UNQ \| 001,1 "), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a9dab-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-183">Teil des Schlüssel Werts des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a9dab-183">Part of the object's key value.</span></span>

<span data-ttu-id="a9dab-184">Diese Eigenschaft wird von [**CIM \_ UNQ**](cim-irq.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-184">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9dab-185">**Name**</span><span class="sxs-lookup"><span data-stu-id="a9dab-185">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a9dab-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-188">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a9dab-188">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-189">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a9dab-189">Label by which the object is known.</span></span> <span data-ttu-id="a9dab-190">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a9dab-190">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a9dab-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9dab-192">**Freigegeben**</span><span class="sxs-lookup"><span data-stu-id="a9dab-192">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-193">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="a9dab-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-195">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| UNQ \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="a9dab-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-196">**True** gibt an, dass die UNQ freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a9dab-196">If **TRUE**, the IRQ can be shared.</span></span>

<span data-ttu-id="a9dab-197">Diese Eigenschaft wird von [**CIM \_ UNQ**](cim-irq.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-197">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9dab-198">**Status**</span><span class="sxs-lookup"><span data-stu-id="a9dab-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a9dab-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-201">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a9dab-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-202">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a9dab-202">Current status of the object.</span></span> <span data-ttu-id="a9dab-203">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9dab-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a9dab-204">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="a9dab-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a9dab-205">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="a9dab-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a9dab-206">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9dab-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a9dab-207">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="a9dab-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a9dab-208">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a9dab-209">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="a9dab-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a9dab-210">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a9dab-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a9dab-211">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="a9dab-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a9dab-212">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="a9dab-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9dab-213">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="a9dab-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a9dab-214">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a9dab-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a9dab-215">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="a9dab-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a9dab-216">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="a9dab-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a9dab-217">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="a9dab-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a9dab-218">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="a9dab-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a9dab-219">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="a9dab-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a9dab-220">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="a9dab-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a9dab-221">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="a9dab-221">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9dab-222">**Triggerlevel**</span><span class="sxs-lookup"><span data-stu-id="a9dab-222">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-223">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9dab-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-225">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource UNQ Info \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="a9dab-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-226">Die Ebene der UNQ-Trigger, die angibt, ob die Unterbrechung durch das Hardware Signal ausgelöst wird, das hoch (4) oder niedrig (3) ist.</span><span class="sxs-lookup"><span data-stu-id="a9dab-226">IRQ trigger level indicating whether the interrupt is triggered by the hardware signal going high (4) or low (3).</span></span>

<span data-ttu-id="a9dab-227">Diese Eigenschaft wird von [**CIM \_ UNQ**](cim-irq.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-227">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a9dab-228">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a9dab-228">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9dab-229">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a9dab-229">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="a9dab-230">**Aktiv, niedrig** (3)</span><span class="sxs-lookup"><span data-stu-id="a9dab-230">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="a9dab-231">**Aktiv hoch** (4)</span><span class="sxs-lookup"><span data-stu-id="a9dab-231">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9dab-232">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="a9dab-232">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-233">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9dab-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-235">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| UNQ \| 001,3 "," MIF. DMTF- \| System Ressource UNQ Info \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="a9dab-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-236">Der Typ "UNQ-Trigger" gibt an, ob durch Edge ausgelöste (4) oder auf der Ebene ausgelöste (3) Interrupts auftreten.</span><span class="sxs-lookup"><span data-stu-id="a9dab-236">IRQ trigger type indicating whether edge-triggered (4) or level-triggered (3) interrupts occur.</span></span>

<span data-ttu-id="a9dab-237">Diese Eigenschaft wird von [**CIM \_ UNQ**](cim-irq.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="a9dab-237">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a9dab-238">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="a9dab-238">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9dab-239">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="a9dab-239">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="a9dab-240">**Ebene** (3)</span><span class="sxs-lookup"><span data-stu-id="a9dab-240">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="a9dab-241">**Edge** (4)</span><span class="sxs-lookup"><span data-stu-id="a9dab-241">**Edge** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9dab-242">**Vektor**</span><span class="sxs-lookup"><span data-stu-id="a9dab-242">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dab-243">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9dab-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a9dab-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9dab-245">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Structures \| [**cm \_ partiellen \_ Ressourcen \_ Deskriptor**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor) \| \| Interruptebene")</span><span class="sxs-lookup"><span data-stu-id="a9dab-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Interrupt\|Level")</span></span>
</dt> </dl>

<span data-ttu-id="a9dab-246">Vektor der Windows-Ressource "UNQ".</span><span class="sxs-lookup"><span data-stu-id="a9dab-246">Vector of the Windows IRQ resource.</span></span> <span data-ttu-id="a9dab-247">Ein Vektor enthält die Speicheradresse der Funktion, die ausgeführt wird, sobald die Interruptanforderung von der CPU bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="a9dab-247">A vector contains the memory address to the function that will execute once the interrupt request is acknowledged by the CPU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9dab-248">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9dab-248">Remarks</span></span>

<span data-ttu-id="a9dab-249">Die Win32-Klasse " **\_ iriqresource** " wird von [**CIM \_ UNQ**](cim-irq.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a9dab-249">The **Win32\_IRQResource** class is derived from [**CIM\_IRQ**](cim-irq.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9dab-250">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9dab-250">Requirements</span></span>



| <span data-ttu-id="a9dab-251">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9dab-251">Requirement</span></span> | <span data-ttu-id="a9dab-252">Wert</span><span class="sxs-lookup"><span data-stu-id="a9dab-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9dab-253">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9dab-253">Minimum supported client</span></span><br/> | <span data-ttu-id="a9dab-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9dab-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9dab-255">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9dab-255">Minimum supported server</span></span><br/> | <span data-ttu-id="a9dab-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9dab-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9dab-257">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9dab-257">Namespace</span></span><br/>                | <span data-ttu-id="a9dab-258">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a9dab-258">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a9dab-259">MOF</span><span class="sxs-lookup"><span data-stu-id="a9dab-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9dab-260"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a9dab-260"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9dab-261">DLL</span><span class="sxs-lookup"><span data-stu-id="a9dab-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9dab-262"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9dab-262"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9dab-263">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9dab-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9dab-264">**CIM \_ -Antwort**</span><span class="sxs-lookup"><span data-stu-id="a9dab-264">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dt>

[<span data-ttu-id="a9dab-265">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="a9dab-265">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

