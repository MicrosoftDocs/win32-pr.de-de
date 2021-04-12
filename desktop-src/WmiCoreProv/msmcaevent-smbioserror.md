---
description: Gibt einen MCA-System-BIOS-Fehler (Machine Check Architecture) an. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: MSMCAEvent_SMBIOSError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 709d480e8865c5d5bde2a9f5e8de45f138e66548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217611"
---
# <a name="msmcaevent_smbioserror-class"></a><span data-ttu-id="857c3-104">Msmcaevent \_ smbioserror-Klasse</span><span class="sxs-lookup"><span data-stu-id="857c3-104">MSMCAEvent\_SMBIOSError class</span></span>

<span data-ttu-id="857c3-105">Die **msmcaevent \_ smbioserror** -Klasse gibt einen MCA-System-BIOS-Fehler (Machine Check Architecture) an.</span><span class="sxs-lookup"><span data-stu-id="857c3-105">The **MSMCAEvent\_SMBIOSError** class indicates a Machine Check Architecture (MCA) system BIOS error.</span></span> <span data-ttu-id="857c3-106">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="857c3-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="857c3-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="857c3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="857c3-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="857c3-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="857c3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="857c3-109">Syntax</span></span>

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="857c3-110">Member</span><span class="sxs-lookup"><span data-stu-id="857c3-110">Members</span></span>

<span data-ttu-id="857c3-111">Die **msmcaevent \_ smbioserror** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="857c3-111">The **MSMCAEvent\_SMBIOSError** class has these types of members:</span></span>

-   [<span data-ttu-id="857c3-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="857c3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="857c3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="857c3-113">Properties</span></span>

<span data-ttu-id="857c3-114">Die **msmcaevent \_ smbioserror** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="857c3-114">The **MSMCAEvent\_SMBIOSError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="857c3-115">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="857c3-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c3-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="857c3-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="857c3-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="857c3-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c3-118">**True**, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="857c3-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="857c3-119">**Additionalerrors**</span><span class="sxs-lookup"><span data-stu-id="857c3-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c3-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="857c3-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="857c3-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="857c3-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c3-122">Anzahl zusätzlicher Fehler im Datensatz.</span><span class="sxs-lookup"><span data-stu-id="857c3-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="857c3-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="857c3-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c3-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="857c3-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="857c3-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="857c3-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c3-126">CPU, die den Fehler gemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="857c3-126">CPU that reported the error.</span></span> <span data-ttu-id="857c3-127">Diese Eigenschaft gilt nur für ein Multiprozessorsystem, dem dem ersten Prozessor die Zahl 0 zugewiesen ist, dem zweiten Prozessor die Zahl 1 zugewiesen wird usw.</span><span class="sxs-lookup"><span data-stu-id="857c3-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="857c3-128">**Errorschwere Grad**</span><span class="sxs-lookup"><span data-stu-id="857c3-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c3-129">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="857c3-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="857c3-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="857c3-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c3-131">Der Schweregrad des gemeldeten Fehlers.</span><span class="sxs-lookup"><span data-stu-id="857c3-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="857c3-132">Wert</span><span class="sxs-lookup"><span data-stu-id="857c3-132">Value</span></span>                                                                                                | <span data-ttu-id="857c3-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="857c3-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="857c3-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="857c3-135">Wiederherstellbar</span><span class="sxs-lookup"><span data-stu-id="857c3-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="857c3-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="857c3-137">FAT</span><span class="sxs-lookup"><span data-stu-id="857c3-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="857c3-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="857c3-139">KORRIGIER barer</span><span class="sxs-lookup"><span data-stu-id="857c3-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="857c3-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="857c3-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c3-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="857c3-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c3-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="857c3-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c3-143">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="857c3-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="857c3-144">Eindeutiger Bezeichner dieser Instanz der Klasse.</span><span class="sxs-lookup"><span data-stu-id="857c3-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="857c3-145">**Logtoeventlog**</span><span class="sxs-lookup"><span data-stu-id="857c3-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c3-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="857c3-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="857c3-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="857c3-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c3-148">Wenn 0 (null) ist, wird dieses Ereignis nicht im System Ereignisprotokoll protokolliert.</span><span class="sxs-lookup"><span data-stu-id="857c3-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="857c3-149">**Rawrecord**</span><span class="sxs-lookup"><span data-stu-id="857c3-149">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c3-150">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="857c3-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="857c3-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="857c3-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c3-152">Ein Bytearray, das den unformatierten Fehler Daten Satz enthält.</span><span class="sxs-lookup"><span data-stu-id="857c3-152">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="857c3-153">Die Anzahl von Elementen im Array, die von der **size** -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="857c3-153">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="857c3-154">**Datensatz**</span><span class="sxs-lookup"><span data-stu-id="857c3-154">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c3-155">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="857c3-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="857c3-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="857c3-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c3-157">Datensatz-ID des Fehler Datensatzes für diesen Fehler.</span><span class="sxs-lookup"><span data-stu-id="857c3-157">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="857c3-158">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="857c3-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="857c3-159">**Größe**</span><span class="sxs-lookup"><span data-stu-id="857c3-159">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c3-160">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="857c3-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="857c3-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="857c3-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c3-162">Größe des unformatierten Fehler Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="857c3-162">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="857c3-163">**SMBIOS \_ - \_ Ereignistyp**</span><span class="sxs-lookup"><span data-stu-id="857c3-163">**SMBIOS\_EVENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c3-164">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="857c3-164">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="857c3-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="857c3-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c3-166">Der Ereignistyp.</span><span class="sxs-lookup"><span data-stu-id="857c3-166">Event type.</span></span>



| <span data-ttu-id="857c3-167">Wert</span><span class="sxs-lookup"><span data-stu-id="857c3-167">Value</span></span>                                                                                                  | <span data-ttu-id="857c3-168">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="857c3-168">Meaning</span></span>                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="857c3-169"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-169"><dt>**0**</dt></span></span> </dl>   | <span data-ttu-id="857c3-170">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="857c3-170">Reserved.</span></span><br/>                                                                                                        |
| <span id="1"></span><dl> <span data-ttu-id="857c3-171"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-171"><dt>**1**</dt></span></span> </dl>   | <span data-ttu-id="857c3-172">Single-Bit-ECC-Speicherfehler.</span><span class="sxs-lookup"><span data-stu-id="857c3-172">Single bit ECC memory error.</span></span><br/>                                                                                     |
| <span id="2"></span><dl> <span data-ttu-id="857c3-173"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-173"><dt>**2**</dt></span></span> </dl>   | <span data-ttu-id="857c3-174">Multibit-ECC-Speicherfehler.</span><span class="sxs-lookup"><span data-stu-id="857c3-174">Multiple bit ECC memory error.</span></span><br/>                                                                                   |
| <span id="3"></span><dl> <span data-ttu-id="857c3-175"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-175"><dt>**3**</dt></span></span> </dl>   | <span data-ttu-id="857c3-176">Fehler bei Paritäts Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="857c3-176">Parity Memory error.</span></span><br/>                                                                                             |
| <span id="4"></span><dl> <span data-ttu-id="857c3-177"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-177"><dt>**4**</dt></span></span> </dl>   | <span data-ttu-id="857c3-178">Bustimeout.</span><span class="sxs-lookup"><span data-stu-id="857c3-178">Bus time out.</span></span><br/>                                                                                                    |
| <span id="5"></span><dl> <span data-ttu-id="857c3-179"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-179"><dt>**5**</dt></span></span> </dl>   | <span data-ttu-id="857c3-180">Überprüfung des e/a-Kanals.</span><span class="sxs-lookup"><span data-stu-id="857c3-180">I/O Channel Check.</span></span><br/>                                                                                               |
| <span id="6"></span><dl> <span data-ttu-id="857c3-181"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-181"><dt>**6**</dt></span></span> </dl>   | <span data-ttu-id="857c3-182">Software-NMI.</span><span class="sxs-lookup"><span data-stu-id="857c3-182">Software NMI.</span></span><br/>                                                                                                    |
| <span id="7"></span><dl> <span data-ttu-id="857c3-183"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-183"><dt>**7**</dt></span></span> </dl>   | <span data-ttu-id="857c3-184">Größe des Arbeitsspeichers nach dem Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="857c3-184">Post Memory Resize.</span></span><br/>                                                                                              |
| <span id="8"></span><dl> <span data-ttu-id="857c3-185"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-185"><dt>**8**</dt></span></span> </dl>   | <span data-ttu-id="857c3-186">Fehler nach dem Fehler.</span><span class="sxs-lookup"><span data-stu-id="857c3-186">POST Error.</span></span><br/>                                                                                                      |
| <span id="9"></span><dl> <span data-ttu-id="857c3-187"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-187"><dt>**9**</dt></span></span> </dl>   | <span data-ttu-id="857c3-188">PCI-Paritätsfehler.</span><span class="sxs-lookup"><span data-stu-id="857c3-188">PCI Parity Error.</span></span><br/>                                                                                                |
| <span id="10"></span><dl> <span data-ttu-id="857c3-189"><dt>**10**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-189"><dt>**10**</dt></span></span> </dl> | <span data-ttu-id="857c3-190">PCI-System Fehler.</span><span class="sxs-lookup"><span data-stu-id="857c3-190">PCI System Error.</span></span><br/>                                                                                                |
| <span id="11"></span><dl> <span data-ttu-id="857c3-191"><dt>**11:**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-191"><dt>**11**</dt></span></span> </dl> | <span data-ttu-id="857c3-192">CPU-Fehler.</span><span class="sxs-lookup"><span data-stu-id="857c3-192">CPU Failure.</span></span><br/>                                                                                                     |
| <span id="12"></span><dl> <span data-ttu-id="857c3-193"><dt>**12.12.2016**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-193"><dt>**12**</dt></span></span> </dl> | <span data-ttu-id="857c3-194">Timeout des EISA-Failsafe-Timers.</span><span class="sxs-lookup"><span data-stu-id="857c3-194">EISA Failsafe Timer time out.</span></span><br/>                                                                                    |
| <span id="13"></span><dl> <span data-ttu-id="857c3-195"><dt>**13**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-195"><dt>**13**</dt></span></span> </dl> | <span data-ttu-id="857c3-196">Das korrigierbare Speicher Protokoll ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="857c3-196">Correctable memory log disabled.</span></span><br/>                                                                                 |
| <span id="14"></span><dl> <span data-ttu-id="857c3-197"><dt>**14**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-197"><dt>**14**</dt></span></span> </dl> | <span data-ttu-id="857c3-198">Die Protokollierung für einen bestimmten Ereignistyp ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="857c3-198">Logging disabled for a specific event type.</span></span> <span data-ttu-id="857c3-199">In kurzer Zeit wurden zu viele Fehler desselben Typs empfangen.</span><span class="sxs-lookup"><span data-stu-id="857c3-199">Too many errors of the same type received in a short amount of time.</span></span><br/> |
| <span id="15"></span><dl> <span data-ttu-id="857c3-200"><dt>**17.15**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-200"><dt>**15**</dt></span></span> </dl> | <span data-ttu-id="857c3-201">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="857c3-201">Reserved.</span></span><br/>                                                                                                        |
| <span id="16"></span><dl> <span data-ttu-id="857c3-202"><dt>**Uhr**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-202"><dt>**16**</dt></span></span> </dl> | <span data-ttu-id="857c3-203">Das System Limit wurde überschritten (z. b. Spannung oder Temperaturschwellen Wert überschritten).</span><span class="sxs-lookup"><span data-stu-id="857c3-203">System limit exceeded (for example, voltage or temperature threshold exceeded).</span></span><br/>                                  |
| <span id="17"></span><dl> <span data-ttu-id="857c3-204"><dt>**Uhr**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-204"><dt>**17**</dt></span></span> </dl> | <span data-ttu-id="857c3-205">Der asynchrone Hardware-Timer ist abgelaufen und hat eine System Zurücksetzung ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="857c3-205">Asynchronous hardware timer expired and issued a system reset.</span></span><br/>                                                   |
| <span id="18"></span><dl> <span data-ttu-id="857c3-206"><dt>**Jahren**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-206"><dt>**18**</dt></span></span> </dl> | <span data-ttu-id="857c3-207">System Konfigurationsinformationen.</span><span class="sxs-lookup"><span data-stu-id="857c3-207">System configuration information.</span></span><br/>                                                                                |
| <span id="19"></span><dl> <span data-ttu-id="857c3-208"><dt>**19.07.2016**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-208"><dt>**19**</dt></span></span> </dl> | <span data-ttu-id="857c3-209">Festplatten Informationen.</span><span class="sxs-lookup"><span data-stu-id="857c3-209">Hard disk information.</span></span><br/>                                                                                           |
| <span id="20"></span><dl> <span data-ttu-id="857c3-210"><dt>**20**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-210"><dt>**20**</dt></span></span> </dl> | <span data-ttu-id="857c3-211">Das System wurde neu konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="857c3-211">System reconfigured.</span></span><br/>                                                                                             |
| <span id="21"></span><dl> <span data-ttu-id="857c3-212"><dt>**21**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-212"><dt>**21**</dt></span></span> </dl> | <span data-ttu-id="857c3-213">Nicht korrigierbare CPU-komplexer Fehler.</span><span class="sxs-lookup"><span data-stu-id="857c3-213">Uncorrectable CPU-complex error.</span></span><br/>                                                                                 |
| <span id="22"></span><dl> <span data-ttu-id="857c3-214"><dt>**22**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-214"><dt>**22**</dt></span></span> </dl> | <span data-ttu-id="857c3-215">Der Protokollbereich wurde zurückgesetzt oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="857c3-215">Log Area Reset or Cleared.</span></span><br/>                                                                                       |
| <span id="23"></span><dl> <span data-ttu-id="857c3-216"><dt>**23**</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-216"><dt>**23**</dt></span></span> </dl> | <span data-ttu-id="857c3-217">System Start.</span><span class="sxs-lookup"><span data-stu-id="857c3-217">System boot.</span></span> <span data-ttu-id="857c3-218">Bei Implementierung ist dieser Protokolleintrag garantiert der erste, der bei jedem Systemstart geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="857c3-218">If implemented, this log entry is guaranteed to be the first one written on any system boot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="857c3-219">**Type**</span><span class="sxs-lookup"><span data-stu-id="857c3-219">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c3-220">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="857c3-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="857c3-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="857c3-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c3-222">Der Typ der Ereignisprotokoll Meldung.</span><span class="sxs-lookup"><span data-stu-id="857c3-222">Type of event log message.</span></span> <span data-ttu-id="857c3-223">Diese Meldungen entsprechen den Ereignisprotokoll-Nachrichten Codes, die zum Einfügen von Ereignisprotokoll Meldungen vom Windows-Ereignisprotokoll-Consumeranbieter verwendet werden, wenn ein Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="857c3-223">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="857c3-224">**Validierungs \_ Bits**</span><span class="sxs-lookup"><span data-stu-id="857c3-224">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c3-225">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="857c3-225">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="857c3-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="857c3-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c3-227">Validierungs Bits zum Angeben der Gültigkeit der nachfolgenden Felder.</span><span class="sxs-lookup"><span data-stu-id="857c3-227">Validation bits used to indicate the validity of the subsequent fields.</span></span> <span data-ttu-id="857c3-228">Der Wert 1 (0x1) bedeutet, dass das **SMBIOS- \_ Ereignis** gültig ist.</span><span class="sxs-lookup"><span data-stu-id="857c3-228">A value of 1 (0x1) means that the **SMBIOS\_EVENT** is valid.</span></span>

<span data-ttu-id="857c3-229">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="857c3-229">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="857c3-230">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="857c3-230">Remarks</span></span>

<span data-ttu-id="857c3-231">Die **msmcaevent \_ smbioserror** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="857c3-231">The **MSMCAEvent\_SMBIOSError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="857c3-232">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="857c3-232">Requirements</span></span>



| <span data-ttu-id="857c3-233">Anforderung</span><span class="sxs-lookup"><span data-stu-id="857c3-233">Requirement</span></span> | <span data-ttu-id="857c3-234">Wert</span><span class="sxs-lookup"><span data-stu-id="857c3-234">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="857c3-235">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="857c3-235">Minimum supported client</span></span><br/> | <span data-ttu-id="857c3-236">Windows XP</span><span class="sxs-lookup"><span data-stu-id="857c3-236">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="857c3-237">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="857c3-237">Minimum supported server</span></span><br/> | <span data-ttu-id="857c3-238">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="857c3-238">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="857c3-239">Namespace</span><span class="sxs-lookup"><span data-stu-id="857c3-239">Namespace</span></span><br/>                | <span data-ttu-id="857c3-240">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="857c3-240">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="857c3-241">MOF</span><span class="sxs-lookup"><span data-stu-id="857c3-241">MOF</span></span><br/>                      | <dl> <span data-ttu-id="857c3-242"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-242"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="857c3-243">DLL</span><span class="sxs-lookup"><span data-stu-id="857c3-243">DLL</span></span><br/>                      | <dl> <span data-ttu-id="857c3-244"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="857c3-244"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="857c3-245">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="857c3-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="857c3-246">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="857c3-246">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="857c3-247">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="857c3-247">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

