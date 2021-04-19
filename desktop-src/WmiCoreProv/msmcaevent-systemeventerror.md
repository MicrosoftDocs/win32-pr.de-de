---
description: Gibt an, dass ein Intelligent Platform Management Interface (IPMI)-System Ereignis aufgetreten ist. Der Fehler wird in das SMBIOS-System Ereignisprotokoll (SEL) geschrieben. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 1964f850-ac55-4639-9205-2eb0996dbaae
title: MSMCAEvent_SystemEventError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SystemEventError
- MSMCAEvent_SystemEventError.Active
- MSMCAEvent_SystemEventError.AdditionalErrors
- MSMCAEvent_SystemEventError.Cpu
- MSMCAEvent_SystemEventError.ErrorSeverity
- MSMCAEvent_SystemEventError.InstanceName
- MSMCAEvent_SystemEventError.RawRecord
- MSMCAEvent_SystemEventError.RecordId
- MSMCAEvent_SystemEventError.SEL_DATA1
- MSMCAEvent_SystemEventError.SEL_DATA2
- MSMCAEvent_SystemEventError.SEL_DATA3
- MSMCAEvent_SystemEventError.SEL_EVENT_DIR_TYPE
- MSMCAEvent_SystemEventError.SEL_EVM_REV
- MSMCAEvent_SystemEventError.SEL_GENERATOR_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_TYPE
- MSMCAEvent_SystemEventError.SEL_SENSOR_NUM
- MSMCAEvent_SystemEventError.SEL_SENSOR_TYPE
- MSMCAEvent_SystemEventError.SEL_TIME_STAMP
- MSMCAEvent_SystemEventError.Size
- MSMCAEvent_SystemEventError.Type
- MSMCAEvent_SystemEventError.VALIDATION_BITS
- MSMCAEvent_SystemEventError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f20f95fb5e1b1bf07b0f70c25d54122642b13569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362629"
---
# <a name="msmcaevent_systemeventerror-class"></a><span data-ttu-id="71ad1-105">Msmcaevent \_ systemeventerror-Klasse</span><span class="sxs-lookup"><span data-stu-id="71ad1-105">MSMCAEvent\_SystemEventError class</span></span>

<span data-ttu-id="71ad1-106">Die **msmcaevent \_ systemeventerror** -Klasse gibt an, dass ein Management Interface (IPMI)-System Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="71ad1-106">The **MSMCAEvent\_SystemEventError** class indicates that an Intelligent Platform Management Interface (IPMI) system event has occurred.</span></span> <span data-ttu-id="71ad1-107">Der Fehler wird in das SMBIOS-System Ereignisprotokoll (SEL) geschrieben.</span><span class="sxs-lookup"><span data-stu-id="71ad1-107">The error is written to the SMBIOS System Event Log (SEL).</span></span> <span data-ttu-id="71ad1-108">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="71ad1-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="71ad1-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="71ad1-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="71ad1-110">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="71ad1-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ad1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="71ad1-111">Syntax</span></span>

``` syntax
class MSMCAEvent_SystemEventError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint8   SEL_DATA1;
  uint8   SEL_DATA2;
  uint8   SEL_DATA3;
  uint8   SEL_EVENT_DIR_TYPE;
  uint8   SEL_EVM_REV;
  uint16  SEL_GENERATOR_ID;
  uint16  SEL_RECORD_ID;
  uint8   SEL_RECORD_TYPE;
  uint8   SEL_SENSOR_NUM;
  uint8   SEL_SENSOR_TYPE;
  uint64  SEL_TIME_STAMP;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="71ad1-112">Member</span><span class="sxs-lookup"><span data-stu-id="71ad1-112">Members</span></span>

<span data-ttu-id="71ad1-113">Die **msmcaevent \_ systemeventerror** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="71ad1-113">The **MSMCAEvent\_SystemEventError** class has these types of members:</span></span>

-   [<span data-ttu-id="71ad1-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71ad1-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71ad1-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71ad1-115">Properties</span></span>

<span data-ttu-id="71ad1-116">Die **msmcaevent \_ systemeventerror** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="71ad1-116">The **MSMCAEvent\_SystemEventError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71ad1-117">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="71ad1-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-118">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="71ad1-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-120">**True**, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="71ad1-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-121">**Additionalerrors**</span><span class="sxs-lookup"><span data-stu-id="71ad1-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-122">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71ad1-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-124">Anzahl zusätzlicher Fehler im Datensatz.</span><span class="sxs-lookup"><span data-stu-id="71ad1-124">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-125">**CPU**</span><span class="sxs-lookup"><span data-stu-id="71ad1-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-126">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71ad1-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-128">CPU, die den Fehler gemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="71ad1-128">CPU that reported the error.</span></span> <span data-ttu-id="71ad1-129">Diese Eigenschaft gilt nur für ein Multiprozessorsystem, dem dem ersten Prozessor die Zahl 0 zugewiesen ist, dem zweiten Prozessor die Zahl 1 zugewiesen wird usw.</span><span class="sxs-lookup"><span data-stu-id="71ad1-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-130">**Errorschwere Grad**</span><span class="sxs-lookup"><span data-stu-id="71ad1-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-131">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71ad1-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-133">Der Schweregrad des gemeldeten Fehlers.</span><span class="sxs-lookup"><span data-stu-id="71ad1-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="71ad1-134">Wert</span><span class="sxs-lookup"><span data-stu-id="71ad1-134">Value</span></span>                                                                                                | <span data-ttu-id="71ad1-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="71ad1-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="71ad1-136"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="71ad1-137">Wiederherstellbar</span><span class="sxs-lookup"><span data-stu-id="71ad1-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="71ad1-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="71ad1-139">FAT</span><span class="sxs-lookup"><span data-stu-id="71ad1-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="71ad1-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="71ad1-141">KORRIGIER barer</span><span class="sxs-lookup"><span data-stu-id="71ad1-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="71ad1-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="71ad1-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="71ad1-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-145">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="71ad1-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-146">Eindeutiger Bezeichner dieser Instanz der Klasse.</span><span class="sxs-lookup"><span data-stu-id="71ad1-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-147">**Logtoeventlog**</span><span class="sxs-lookup"><span data-stu-id="71ad1-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-148">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71ad1-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-150">Wenn 0 (null) ist, wird dieses Ereignis nicht im System Ereignisprotokoll protokolliert.</span><span class="sxs-lookup"><span data-stu-id="71ad1-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-151">**Rawrecord**</span><span class="sxs-lookup"><span data-stu-id="71ad1-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-152">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="71ad1-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-154">Ein Bytearray, das den unformatierten Fehler Daten Satz enthält.</span><span class="sxs-lookup"><span data-stu-id="71ad1-154">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="71ad1-155">Die Anzahl von Elementen im Array, die von der **size** -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="71ad1-155">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-156">**Datensatz**</span><span class="sxs-lookup"><span data-stu-id="71ad1-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-157">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71ad1-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-159">Datensatz-ID des Fehler Datensatzes für diesen Fehler.</span><span class="sxs-lookup"><span data-stu-id="71ad1-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="71ad1-160">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71ad1-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-161">**SEL \_ data1**</span><span class="sxs-lookup"><span data-stu-id="71ad1-161">**SEL\_DATA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-162">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71ad1-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-164">Ereignisdaten Feld 1.</span><span class="sxs-lookup"><span data-stu-id="71ad1-164">Event data field 1.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-165">**SEL \_ data2**</span><span class="sxs-lookup"><span data-stu-id="71ad1-165">**SEL\_DATA2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-166">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71ad1-166">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-168">Ereignisdaten Feld 2.</span><span class="sxs-lookup"><span data-stu-id="71ad1-168">Event data field 2.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-169">**SEL \_ data3**</span><span class="sxs-lookup"><span data-stu-id="71ad1-169">**SEL\_DATA3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-170">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71ad1-170">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-172">Ereignisdaten Feld 3.</span><span class="sxs-lookup"><span data-stu-id="71ad1-172">Event data field 3.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-173">**SEL- \_ Ereignis \_ dir- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="71ad1-173">**SEL\_EVENT\_DIR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-174">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71ad1-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-176">Der Ereignis Verzeichnistyp.</span><span class="sxs-lookup"><span data-stu-id="71ad1-176">Event directory type.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-177">**SEL \_ EVM \_ Rev**</span><span class="sxs-lookup"><span data-stu-id="71ad1-177">**SEL\_EVM\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-178">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71ad1-178">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-180">Format Version der Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="71ad1-180">Format version of the error message.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-181">**SEL \_ Generator- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="71ad1-181">**SEL\_GENERATOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-182">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71ad1-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-184">Software Bezeichner, wenn das Ereignis Software generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="71ad1-184">Software identifier, if the event was software-generated.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-185">**SEL- \_ Datensatz- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="71ad1-185">**SEL\_RECORD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-186">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71ad1-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-188">Datensatz-ID für den Zugriff auf das SMBIOS-System Ereignisprotokoll (SEL).</span><span class="sxs-lookup"><span data-stu-id="71ad1-188">Record identifier used for SMBIOS system event log (SEL) access.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-189">**SEL- \_ Daten Satz \_ Typen**</span><span class="sxs-lookup"><span data-stu-id="71ad1-189">**SEL\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-190">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71ad1-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-192">Der Datensatztyp.</span><span class="sxs-lookup"><span data-stu-id="71ad1-192">Record type.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-193">**SEL- \_ Sensor \_ NUM**</span><span class="sxs-lookup"><span data-stu-id="71ad1-193">**SEL\_SENSOR\_NUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-194">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71ad1-194">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-196">Die Sensor Nummer, die das Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="71ad1-196">Sensor number that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-197">**SEL \_ - \_ Sensortyp**</span><span class="sxs-lookup"><span data-stu-id="71ad1-197">**SEL\_SENSOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-198">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="71ad1-198">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-200">Der Sensortyp Code des Sensors, der das Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="71ad1-200">Sensor type code of the sensor that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-201">**SEL- \_ Zeit \_ Stempel**</span><span class="sxs-lookup"><span data-stu-id="71ad1-201">**SEL\_TIME\_STAMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-202">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71ad1-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-204">Der Zeitstempel des Ereignis Protokolls.</span><span class="sxs-lookup"><span data-stu-id="71ad1-204">Timestamp of the event log.</span></span>

<span data-ttu-id="71ad1-205">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71ad1-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-206">**Größe**</span><span class="sxs-lookup"><span data-stu-id="71ad1-206">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-207">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71ad1-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-209">Größe des unformatierten Fehler Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="71ad1-209">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-210">**Type**</span><span class="sxs-lookup"><span data-stu-id="71ad1-210">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-211">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71ad1-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-213">Der Typ der Ereignisprotokoll Meldung.</span><span class="sxs-lookup"><span data-stu-id="71ad1-213">Type of event log message.</span></span> <span data-ttu-id="71ad1-214">Diese Meldungen entsprechen den Ereignisprotokoll-Nachrichten Codes, die zum Einfügen von Ereignisprotokoll Meldungen vom Windows-Ereignisprotokoll-Consumeranbieter verwendet werden, wenn ein Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="71ad1-214">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="71ad1-215">**Validierungs \_ Bits**</span><span class="sxs-lookup"><span data-stu-id="71ad1-215">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71ad1-216">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71ad1-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71ad1-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="71ad1-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71ad1-218">Validierungs Bits zum Angeben der Gültigkeit der nachfolgenden Felder.</span><span class="sxs-lookup"><span data-stu-id="71ad1-218">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="71ad1-219">Wert</span><span class="sxs-lookup"><span data-stu-id="71ad1-219">Value</span></span>                                                                                                                                            | <span data-ttu-id="71ad1-220">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="71ad1-220">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="71ad1-221"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-221"><dt>**1 0x1**</dt></span></span> </dl>             | <span data-ttu-id="71ad1-222">**SEL \_ Die Datensatz- \_ ID** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="71ad1-222">**SEL\_RECORD\_ID** is valid.</span></span><br/>    |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="71ad1-223"><dt>**2 0x2**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-223"><dt>**2 0x2**</dt></span></span> </dl>             | <span data-ttu-id="71ad1-224">**SEL \_ Der \_ Typ des Datensatzes** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="71ad1-224">**SEL\_RECORD\_TYPE** is valid.</span></span><br/>  |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="71ad1-225"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-225"><dt>**4 0x4**</dt></span></span> </dl>             | <span data-ttu-id="71ad1-226">**SEL \_ Die Generator- \_ ID** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="71ad1-226">**SEL\_GENERATOR\_ID** is valid.</span></span><br/> |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="71ad1-227"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-227"><dt>**8 0x8**</dt></span></span> </dl>             | <span data-ttu-id="71ad1-228">**SEL \_ EVM- \_ Rev** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="71ad1-228">**SEL\_EVM\_REV** is valid.</span></span><br/>      |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="71ad1-229"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-229"><dt>**16 0x10**</dt></span></span> </dl>       | <span data-ttu-id="71ad1-230">**SEL \_ Der \_ Sensortyp** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="71ad1-230">**SEL\_SENSOR\_TYPE** is valid.</span></span><br/>  |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="71ad1-231"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-231"><dt>**32 0x20**</dt></span></span> </dl>       | <span data-ttu-id="71ad1-232">**SEL \_ Der Sensor " \_ NUM** " ist gültig.</span><span class="sxs-lookup"><span data-stu-id="71ad1-232">**SEL\_SENSOR\_NUM** is valid.</span></span><br/>   |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="71ad1-233"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-233"><dt>**64 0x40**</dt></span></span> </dl>       | <span data-ttu-id="71ad1-234">**SEL \_ Das \_ Ereignis** Verzeichnis ist gültig.</span><span class="sxs-lookup"><span data-stu-id="71ad1-234">**SEL\_EVENT\_DIR** is valid.</span></span><br/>    |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="71ad1-235"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-235"><dt>**128 0x80**</dt></span></span> </dl>    | <span data-ttu-id="71ad1-236">**SEL \_ Das Ereignis \_ data1** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="71ad1-236">**SEL\_EVENT\_DATA1** is valid.</span></span><br/>  |
| <span id="256_0x100"></span><span id="256_0X100"></span><dl> <span data-ttu-id="71ad1-237"><dt>**256 0x100**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-237"><dt>**256 0x100**</dt></span></span> </dl> | <span data-ttu-id="71ad1-238">**SEL \_ Das Ereignis \_ data2** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="71ad1-238">**SEL\_EVENT\_DATA2** is valid.</span></span><br/>  |
| <span id="512_0x200"></span><span id="512_0X200"></span><dl> <span data-ttu-id="71ad1-239"><dt>**512 0x200**</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-239"><dt>**512 0x200**</dt></span></span> </dl> | <span data-ttu-id="71ad1-240">**SEL \_ Das Ereignis \_ data3** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="71ad1-240">**SEL\_EVENT\_DATA3** is valid.</span></span><br/>  |



 

<span data-ttu-id="71ad1-241">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71ad1-241">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71ad1-242">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71ad1-242">Remarks</span></span>

<span data-ttu-id="71ad1-243">Die **msmcaevent \_ systemeventerror** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="71ad1-243">The **MSMCAEvent\_SystemEventError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71ad1-244">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71ad1-244">Requirements</span></span>



| <span data-ttu-id="71ad1-245">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71ad1-245">Requirement</span></span> | <span data-ttu-id="71ad1-246">Wert</span><span class="sxs-lookup"><span data-stu-id="71ad1-246">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71ad1-247">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71ad1-247">Minimum supported client</span></span><br/> | <span data-ttu-id="71ad1-248">Windows XP</span><span class="sxs-lookup"><span data-stu-id="71ad1-248">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="71ad1-249">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71ad1-249">Minimum supported server</span></span><br/> | <span data-ttu-id="71ad1-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="71ad1-250">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="71ad1-251">Namespace</span><span class="sxs-lookup"><span data-stu-id="71ad1-251">Namespace</span></span><br/>                | <span data-ttu-id="71ad1-252">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="71ad1-252">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="71ad1-253">MOF</span><span class="sxs-lookup"><span data-stu-id="71ad1-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71ad1-254"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-254"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="71ad1-255">DLL</span><span class="sxs-lookup"><span data-stu-id="71ad1-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71ad1-256"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71ad1-256"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ad1-257">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71ad1-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ad1-258">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="71ad1-258">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="71ad1-259">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="71ad1-259">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

