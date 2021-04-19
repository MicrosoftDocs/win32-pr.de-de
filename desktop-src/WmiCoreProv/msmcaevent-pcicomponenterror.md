---
description: Gibt eine MCA-PCI-Komponenten Fehler (Machine Check Architecture) an. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 2b241333-2ea5-42cb-bdd3-27a10df51f3e
title: MSMCAEvent_PCIComponentError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIComponentError
- MSMCAEvent_PCIComponentError.Active
- MSMCAEvent_PCIComponentError.AdditionalErrors
- MSMCAEvent_PCIComponentError.Cpu
- MSMCAEvent_PCIComponentError.ErrorSeverity
- MSMCAEvent_PCIComponentError.InstanceName
- MSMCAEvent_PCIComponentError.PCI_COMP_ERROR_STATUS
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_BusNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeBaseClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeInterface
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeSubClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceId
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_FunctionNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_SegmentNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_VendorId
- MSMCAEvent_PCIComponentError.RawRecord
- MSMCAEvent_PCIComponentError.RecordId
- MSMCAEvent_PCIComponentError.Size
- MSMCAEvent_PCIComponentError.Type
- MSMCAEvent_PCIComponentError.VALIDATION_BITS
- MSMCAEvent_PCIComponentError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cbcf3ee13e822fd59cdcdd30538d5e369d798aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373241"
---
# <a name="msmcaevent_pcicomponenterror-class"></a><span data-ttu-id="069fd-104">Msmcaevent \_ pcicomponerterror-Klasse</span><span class="sxs-lookup"><span data-stu-id="069fd-104">MSMCAEvent\_PCIComponentError class</span></span>

<span data-ttu-id="069fd-105">Die " **msmcaevent \_ pcicomponeinterror** "-Klasse zeigt eine MCA-PCI-Komponenten Fehler (Machine Check Architecture) an.</span><span class="sxs-lookup"><span data-stu-id="069fd-105">The **MSMCAEvent\_PCIComponentError** class indicates an Machine Check Architecture (MCA) PCI component error.</span></span> <span data-ttu-id="069fd-106">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="069fd-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="069fd-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="069fd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="069fd-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="069fd-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="069fd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="069fd-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIComponentError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_COMP_ERROR_STATUS;
  uint8   PCI_COMP_INFO_BusNumber;
  uint8   PCI_COMP_INFO_ClassCodeBaseClass;
  uint8   PCI_COMP_INFO_ClassCodeInterface;
  uint8   PCI_COMP_INFO_ClassCodeSubClass;
  uint16  PCI_COMP_INFO_DeviceId;
  uint8   PCI_COMP_INFO_DeviceNumber;
  uint8   PCI_COMP_INFO_FunctionNumber;
  uint8   PCI_COMP_INFO_SegmentNumber;
  uint16  PCI_COMP_INFO_VendorId;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="069fd-110">Member</span><span class="sxs-lookup"><span data-stu-id="069fd-110">Members</span></span>

<span data-ttu-id="069fd-111">Die **msmcaevent \_ pcicomponenterror** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="069fd-111">The **MSMCAEvent\_PCIComponentError** class has these types of members:</span></span>

-   [<span data-ttu-id="069fd-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="069fd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="069fd-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="069fd-113">Properties</span></span>

<span data-ttu-id="069fd-114">Die **msmcaevent \_ pcicomponenterror** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="069fd-114">The **MSMCAEvent\_PCIComponentError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="069fd-115">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="069fd-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="069fd-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-118">**True**, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="069fd-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-119">**Additionalerrors**</span><span class="sxs-lookup"><span data-stu-id="069fd-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="069fd-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-122">Anzahl zusätzlicher Fehler im Datensatz.</span><span class="sxs-lookup"><span data-stu-id="069fd-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="069fd-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="069fd-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-126">CPU, die den Fehler gemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="069fd-126">CPU that reported the error.</span></span> <span data-ttu-id="069fd-127">Diese Eigenschaft gilt nur für ein Multiprozessorsystem, dem dem ersten Prozessor die Zahl 0 zugewiesen ist, dem zweiten Prozessor die Zahl 1 zugewiesen wird usw.</span><span class="sxs-lookup"><span data-stu-id="069fd-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-128">**Errorschwere Grad**</span><span class="sxs-lookup"><span data-stu-id="069fd-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-129">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="069fd-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-131">Der Schweregrad des gemeldeten Fehlers.</span><span class="sxs-lookup"><span data-stu-id="069fd-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="069fd-132">Wert</span><span class="sxs-lookup"><span data-stu-id="069fd-132">Value</span></span>                                                                                                | <span data-ttu-id="069fd-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="069fd-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="069fd-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="069fd-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="069fd-135">Wiederherstellbar</span><span class="sxs-lookup"><span data-stu-id="069fd-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="069fd-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="069fd-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="069fd-137">FAT</span><span class="sxs-lookup"><span data-stu-id="069fd-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="069fd-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="069fd-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="069fd-139">KORRIGIER barer</span><span class="sxs-lookup"><span data-stu-id="069fd-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="069fd-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="069fd-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="069fd-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069fd-143">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="069fd-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="069fd-144">Eindeutiger Bezeichner dieser Instanz der Klasse.</span><span class="sxs-lookup"><span data-stu-id="069fd-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-145">**Logtoeventlog**</span><span class="sxs-lookup"><span data-stu-id="069fd-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="069fd-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-148">Wenn 0 (null) ist, wird dieses Ereignis nicht im System Ereignisprotokoll protokolliert.</span><span class="sxs-lookup"><span data-stu-id="069fd-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-149">**PCI- \_ Comp- \_ Fehler \_ Status**</span><span class="sxs-lookup"><span data-stu-id="069fd-149">**PCI\_COMP\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-150">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="069fd-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-152">Interner Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="069fd-152">Internal error code.</span></span>

<span data-ttu-id="069fd-153">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="069fd-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="069fd-154">**PCI- \_ Comp- \_ Info- \_ Busnummer**</span><span class="sxs-lookup"><span data-stu-id="069fd-154">**PCI\_COMP\_INFO\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-155">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="069fd-155">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-157">Busnummer der PCI-Komponente.</span><span class="sxs-lookup"><span data-stu-id="069fd-157">Bus number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-158">**PCI- \_ Comp- \_ Info \_ classcodebaseclass**</span><span class="sxs-lookup"><span data-stu-id="069fd-158">**PCI\_COMP\_INFO\_ClassCodeBaseClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-159">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="069fd-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-161">Klassen Code der Basisklasse der PCI-Komponente.</span><span class="sxs-lookup"><span data-stu-id="069fd-161">Class code of the base class of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-162">**PCI- \_ Comp- \_ Info \_ classcodeinterface**</span><span class="sxs-lookup"><span data-stu-id="069fd-162">**PCI\_COMP\_INFO\_ClassCodeInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-163">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="069fd-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-165">Klassen Code Schnittstelle der PCI-Komponente.</span><span class="sxs-lookup"><span data-stu-id="069fd-165">Class code interface of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-166">**PCI- \_ Comp- \_ Info \_ classcodesubclass**</span><span class="sxs-lookup"><span data-stu-id="069fd-166">**PCI\_COMP\_INFO\_ClassCodeSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-167">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="069fd-167">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-169">Klassen Code-Unterklasse der PCI-Komponente.</span><span class="sxs-lookup"><span data-stu-id="069fd-169">Class code subclass of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-170">**PCI- \_ Comp- \_ Info- \_ DeviceID**</span><span class="sxs-lookup"><span data-stu-id="069fd-170">**PCI\_COMP\_INFO\_DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-171">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="069fd-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-173">Geräte Bezeichner der PCI-Komponente.</span><span class="sxs-lookup"><span data-stu-id="069fd-173">Device identifier of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-174">**PCI- \_ Comp- \_ Info- \_ devicennummer**</span><span class="sxs-lookup"><span data-stu-id="069fd-174">**PCI\_COMP\_INFO\_DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-175">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="069fd-175">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-177">Gerätenummer der PCI-Komponente.</span><span class="sxs-lookup"><span data-stu-id="069fd-177">Device number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-178">**PCI- \_ Comp- \_ Info \_ functionnumber**</span><span class="sxs-lookup"><span data-stu-id="069fd-178">**PCI\_COMP\_INFO\_FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-179">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="069fd-179">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-181">Funktions Nummer der PCI-Komponente.</span><span class="sxs-lookup"><span data-stu-id="069fd-181">Function number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-182">**PCI- \_ Comp- \_ Info \_ segmentnumber**</span><span class="sxs-lookup"><span data-stu-id="069fd-182">**PCI\_COMP\_INFO\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-183">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="069fd-183">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-185">Segment Nummer der PCI-Komponente.</span><span class="sxs-lookup"><span data-stu-id="069fd-185">Segment number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-186">**PCI \_ - \_ Comp \_ -Info-VendorID**</span><span class="sxs-lookup"><span data-stu-id="069fd-186">**PCI\_COMP\_INFO\_VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-187">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="069fd-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-189">Hersteller Bezeichner der PCI-Komponente.</span><span class="sxs-lookup"><span data-stu-id="069fd-189">Vendor identifier of the PCI Component.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-190">**Rawrecord**</span><span class="sxs-lookup"><span data-stu-id="069fd-190">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-191">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="069fd-191">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="069fd-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-193">Ein Bytearray, das den unformatierten Fehler Daten Satz enthält.</span><span class="sxs-lookup"><span data-stu-id="069fd-193">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="069fd-194">Die Anzahl von Elementen im Array, die von der **size** -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="069fd-194">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-195">**Datensatz**</span><span class="sxs-lookup"><span data-stu-id="069fd-195">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-196">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="069fd-196">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-198">Datensatz-ID des Fehler Datensatzes für diesen Fehler.</span><span class="sxs-lookup"><span data-stu-id="069fd-198">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="069fd-199">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="069fd-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="069fd-200">**Größe**</span><span class="sxs-lookup"><span data-stu-id="069fd-200">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-201">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="069fd-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-203">Größe des unformatierten Fehler Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="069fd-203">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-204">**Type**</span><span class="sxs-lookup"><span data-stu-id="069fd-204">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-205">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="069fd-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-207">Der Typ der Ereignisprotokoll Meldung.</span><span class="sxs-lookup"><span data-stu-id="069fd-207">Type of event log message.</span></span> <span data-ttu-id="069fd-208">Diese Meldungen entsprechen den Ereignisprotokoll-Nachrichten Codes, die zum Einfügen von Ereignisprotokoll Meldungen vom Windows-Ereignisprotokoll-Consumeranbieter verwendet werden, wenn ein Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="069fd-208">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="069fd-209">**Validierungs \_ Bits**</span><span class="sxs-lookup"><span data-stu-id="069fd-209">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069fd-210">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="069fd-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="069fd-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="069fd-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069fd-212">Validierungs Bits zum Angeben der Gültigkeit der nachfolgenden Felder.</span><span class="sxs-lookup"><span data-stu-id="069fd-212">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="069fd-213">Werte</span><span class="sxs-lookup"><span data-stu-id="069fd-213">Values</span></span>                                                                               | <span data-ttu-id="069fd-214">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="069fd-214">Meaning</span></span>                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="069fd-215"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="069fd-215"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="069fd-216">Der PCI- \_ Comp- \_ Fehler \_ Status ist gültig.</span><span class="sxs-lookup"><span data-stu-id="069fd-216">PCI\_COMP\_ERROR\_STATUS is valid.</span></span><br/>    |
| <dl> <span data-ttu-id="069fd-217"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="069fd-217"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="069fd-218">PCI- \_ Comp- \_ Informationen sind gültig.</span><span class="sxs-lookup"><span data-stu-id="069fd-218">PCI\_COMP\_INFO is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="069fd-219"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="069fd-219"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="069fd-220">PCI \_ Comp Comp- \_ \_ num ist gültig.</span><span class="sxs-lookup"><span data-stu-id="069fd-220">PCI\_COMP\_MEM\_NUM is valid.</span></span><br/>         |
| <dl> <span data-ttu-id="069fd-221"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="069fd-221"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="069fd-222">PCI-Comp-e/a- \_ \_ \_ num ist gültig.</span><span class="sxs-lookup"><span data-stu-id="069fd-222">PCI\_COMP\_IO\_NUM is valid.</span></span><br/>          |
| <dl> <span data-ttu-id="069fd-223"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="069fd-223"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="069fd-224">Das PCI- \_ Comp- \_ regs- \_ Daten \_ Paar ist gültig.</span><span class="sxs-lookup"><span data-stu-id="069fd-224">PCI\_COMP\_REGS\_DATA\_PAIR is valid.</span></span><br/> |



 

<span data-ttu-id="069fd-225">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="069fd-225">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="069fd-226">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="069fd-226">Remarks</span></span>

<span data-ttu-id="069fd-227">Die **msmcaevent \_ pcicomponenterror** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="069fd-227">The **MSMCAEvent\_PCIComponentError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="069fd-228">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="069fd-228">Requirements</span></span>



| <span data-ttu-id="069fd-229">Anforderung</span><span class="sxs-lookup"><span data-stu-id="069fd-229">Requirement</span></span> | <span data-ttu-id="069fd-230">Wert</span><span class="sxs-lookup"><span data-stu-id="069fd-230">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="069fd-231">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="069fd-231">Minimum supported client</span></span><br/> | <span data-ttu-id="069fd-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="069fd-232">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="069fd-233">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="069fd-233">Minimum supported server</span></span><br/> | <span data-ttu-id="069fd-234">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="069fd-234">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="069fd-235">Namespace</span><span class="sxs-lookup"><span data-stu-id="069fd-235">Namespace</span></span><br/>                | <span data-ttu-id="069fd-236">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="069fd-236">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="069fd-237">MOF</span><span class="sxs-lookup"><span data-stu-id="069fd-237">MOF</span></span><br/>                      | <dl> <span data-ttu-id="069fd-238"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="069fd-238"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="069fd-239">DLL</span><span class="sxs-lookup"><span data-stu-id="069fd-239">DLL</span></span><br/>                      | <dl> <span data-ttu-id="069fd-240"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="069fd-240"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="069fd-241">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="069fd-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="069fd-242">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="069fd-242">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="069fd-243">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="069fd-243">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

