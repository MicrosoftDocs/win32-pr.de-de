---
description: Gibt einen plattformspezifischen Fehler in der Machine Check-Architektur (MCA) an. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 409641d5-3451-4d26-88d1-bfd0e55db257
title: MSMCAEvent_PlatformSpecificError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PlatformSpecificError
- MSMCAEvent_PlatformSpecificError.Active
- MSMCAEvent_PlatformSpecificError.AdditionalErrors
- MSMCAEvent_PlatformSpecificError.Cpu
- MSMCAEvent_PlatformSpecificError.ErrorSeverity
- MSMCAEvent_PlatformSpecificError.InstanceName
- MSMCAEvent_PlatformSpecificError.OEM_COMPONENT_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_BUS_SPECIFIC_DATA
- MSMCAEvent_PlatformSpecificError.PLATFORM_ERROR_STATUS
- MSMCAEvent_PlatformSpecificError.PLATFORM_REQUESTOR_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_RESPONDER_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_TARGET_ID
- MSMCAEvent_PlatformSpecificError.RawRecord
- MSMCAEvent_PlatformSpecificError.RecordId
- MSMCAEvent_PlatformSpecificError.Size
- MSMCAEvent_PlatformSpecificError.Type
- MSMCAEvent_PlatformSpecificError.VALIDATION_BITS
- MSMCAEvent_PlatformSpecificError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 51993c8c41206dac8f4c944d24fa59ae7b689f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484910"
---
# <a name="msmcaevent_platformspecificerror-class"></a><span data-ttu-id="240a9-104">Msmcaevent \_ platformspecificerror-Klasse</span><span class="sxs-lookup"><span data-stu-id="240a9-104">MSMCAEvent\_PlatformSpecificError class</span></span>

<span data-ttu-id="240a9-105">Die Klasse " **msmcaevent \_ platformspecificerror** " zeigt einen plattformspezifischen Fehler in der Machine Check-Architektur (MCA) an.</span><span class="sxs-lookup"><span data-stu-id="240a9-105">The **MSMCAEvent\_PlatformSpecificError** class indicates a Machine Check Architecture (MCA) platform-specific error.</span></span> <span data-ttu-id="240a9-106">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="240a9-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="240a9-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="240a9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="240a9-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="240a9-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="240a9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="240a9-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PlatformSpecificError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   OEM_COMPONENT_ID;
  uint64  PLATFORM_BUS_SPECIFIC_DATA;
  uint64  PLATFORM_ERROR_STATUS;
  uint64  PLATFORM_REQUESTOR_ID;
  uint64  PLATFORM_RESPONDER_ID;
  uint64  PLATFORM_TARGET_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="240a9-110">Member</span><span class="sxs-lookup"><span data-stu-id="240a9-110">Members</span></span>

<span data-ttu-id="240a9-111">Die Klasse " **msmcaevent \_ platformspecificerror** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="240a9-111">The **MSMCAEvent\_PlatformSpecificError** class has these types of members:</span></span>

-   [<span data-ttu-id="240a9-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="240a9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="240a9-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="240a9-113">Properties</span></span>

<span data-ttu-id="240a9-114">Die Klasse " **msmcaevent \_ platformspecificerror** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="240a9-114">The **MSMCAEvent\_PlatformSpecificError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="240a9-115">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="240a9-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="240a9-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-118">**True**, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="240a9-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="240a9-119">**Additionalerrors**</span><span class="sxs-lookup"><span data-stu-id="240a9-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="240a9-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-122">Anzahl zusätzlicher Fehler im Datensatz.</span><span class="sxs-lookup"><span data-stu-id="240a9-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="240a9-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="240a9-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="240a9-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-126">CPU, die den Fehler gemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="240a9-126">CPU that reported the error.</span></span> <span data-ttu-id="240a9-127">Diese Eigenschaft gilt nur für ein Multiprozessorsystem, dem dem ersten Prozessor die Zahl 0 zugewiesen ist, dem zweiten Prozessor die Zahl 1 zugewiesen wird usw.</span><span class="sxs-lookup"><span data-stu-id="240a9-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="240a9-128">**Errorschwere Grad**</span><span class="sxs-lookup"><span data-stu-id="240a9-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-129">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="240a9-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-131">Der Schweregrad des gemeldeten Fehlers.</span><span class="sxs-lookup"><span data-stu-id="240a9-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="240a9-132">Wert</span><span class="sxs-lookup"><span data-stu-id="240a9-132">Value</span></span>                                                                                                | <span data-ttu-id="240a9-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="240a9-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="240a9-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="240a9-135">Wiederherstellbar</span><span class="sxs-lookup"><span data-stu-id="240a9-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="240a9-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="240a9-137">FAT</span><span class="sxs-lookup"><span data-stu-id="240a9-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="240a9-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="240a9-139">KORRIGIER barer</span><span class="sxs-lookup"><span data-stu-id="240a9-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="240a9-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="240a9-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="240a9-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a9-143">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="240a9-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="240a9-144">Eindeutiger Bezeichner dieser Instanz der Klasse.</span><span class="sxs-lookup"><span data-stu-id="240a9-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="240a9-145">**Logtoeventlog**</span><span class="sxs-lookup"><span data-stu-id="240a9-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="240a9-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-148">Wenn 0 (null) ist, wird dieses Ereignis nicht im System Ereignisprotokoll protokolliert.</span><span class="sxs-lookup"><span data-stu-id="240a9-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="240a9-149">**OEM- \_ Komponenten- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="240a9-149">**OEM\_COMPONENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-150">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="240a9-150">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-152">Eindeutiger Bezeichner der Komponente, die den Fehler meldet.</span><span class="sxs-lookup"><span data-stu-id="240a9-152">Unique identifier of the component that reports the error.</span></span>

</dd> <dt>

<span data-ttu-id="240a9-153">**Platt \_ Form \_ Busspezifische \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="240a9-153">**PLATFORM\_BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-154">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="240a9-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-156">OEM-spezifische, Bus abhängige Daten.</span><span class="sxs-lookup"><span data-stu-id="240a9-156">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="240a9-157">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="240a9-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="240a9-158">**Platt Form \_ Fehler \_ Status**</span><span class="sxs-lookup"><span data-stu-id="240a9-158">**PLATFORM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-159">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="240a9-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-161">Fehlerstatus der generischen Plattform.</span><span class="sxs-lookup"><span data-stu-id="240a9-161">Generic platform error status.</span></span>

<span data-ttu-id="240a9-162">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="240a9-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="240a9-163">**\_Requestor- \_ ID der Plattform**</span><span class="sxs-lookup"><span data-stu-id="240a9-163">**PLATFORM\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-164">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="240a9-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-166">Der Anforderer Bezeichner zum Zeitpunkt des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="240a9-166">Requestor identifier at the time of the event.</span></span>

<span data-ttu-id="240a9-167">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="240a9-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="240a9-168">**Plattform- \_ Responder- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="240a9-168">**PLATFORM\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-169">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="240a9-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-171">Der Responder-Bezeichner zum Zeitpunkt des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="240a9-171">Responder identifier at the time of the event.</span></span>

<span data-ttu-id="240a9-172">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="240a9-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="240a9-173">**\_Ziel- \_ ID der Plattform**</span><span class="sxs-lookup"><span data-stu-id="240a9-173">**PLATFORM\_TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-174">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="240a9-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-176">Der Ziel Bezeichner zum Zeitpunkt des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="240a9-176">Target identifier at the time of the event.</span></span>

<span data-ttu-id="240a9-177">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="240a9-177">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="240a9-178">**Rawrecord**</span><span class="sxs-lookup"><span data-stu-id="240a9-178">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-179">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="240a9-179">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="240a9-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-181">Ein Bytearray, das den unformatierten Fehler Daten Satz enthält, wie Windows von der System Abstraktion Layer (SAL) dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="240a9-181">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="240a9-182">Die Anzahl der Elemente im Array wird durch die **size** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="240a9-182">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="240a9-183">**Datensatz**</span><span class="sxs-lookup"><span data-stu-id="240a9-183">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-184">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="240a9-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-186">Datensatz-ID des Fehler Datensatzes für diesen Fehler.</span><span class="sxs-lookup"><span data-stu-id="240a9-186">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="240a9-187">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="240a9-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="240a9-188">**Größe**</span><span class="sxs-lookup"><span data-stu-id="240a9-188">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-189">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="240a9-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-191">Größe des unformatierten Fehler Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="240a9-191">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="240a9-192">**Type**</span><span class="sxs-lookup"><span data-stu-id="240a9-192">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-193">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="240a9-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-195">Der Typ der Ereignisprotokoll Meldung.</span><span class="sxs-lookup"><span data-stu-id="240a9-195">Type of event log message.</span></span> <span data-ttu-id="240a9-196">Diese Meldungen entsprechen den Ereignisprotokoll-Nachrichten Codes, die zum Einfügen von Ereignisprotokoll Meldungen vom Windows-Ereignisprotokoll-Consumeranbieter verwendet werden, wenn ein Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="240a9-196">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="240a9-197">**Validierungs \_ Bits**</span><span class="sxs-lookup"><span data-stu-id="240a9-197">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a9-198">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="240a9-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="240a9-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="240a9-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a9-200">Validierungs Bits zum Angeben der Gültigkeit der nachfolgenden Felder.</span><span class="sxs-lookup"><span data-stu-id="240a9-200">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="240a9-201">Wert</span><span class="sxs-lookup"><span data-stu-id="240a9-201">Value</span></span>                                                                                                                                         | <span data-ttu-id="240a9-202">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="240a9-202">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="240a9-203"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-203"><dt>**1 0x1**</dt></span></span> </dl>          | <span data-ttu-id="240a9-204">**Plattform \_ Der Fehler \_ Status** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="240a9-204">**PLATFORM\_ERROR\_STATUS** is valid.</span></span><br/>            |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="240a9-205"><dt>**2 0x2**</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-205"><dt>**2 0x2**</dt></span></span> </dl>          | <span data-ttu-id="240a9-206">**Plattform \_ Die \_ \_ ID des Fehler** Anforderer ist gültig.</span><span class="sxs-lookup"><span data-stu-id="240a9-206">**PLATFORM\_ERROR\_REQUESTOR\_ID** is valid.</span></span><br/>     |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="240a9-207"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-207"><dt>**4 0x4**</dt></span></span> </dl>          | <span data-ttu-id="240a9-208">**Plattform \_ Die \_ fehlerresponder- \_ ID** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="240a9-208">**PLATFORM\_ERROR\_RESPONDER\_ID** is valid.</span></span><br/>     |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="240a9-209"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-209"><dt>**8 0x8**</dt></span></span> </dl>          | <span data-ttu-id="240a9-210">**Plattform \_ Die Fehler \_ Ziel- \_ ID** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="240a9-210">**PLATFORM\_ERROR\_TARGET\_ID** is valid.</span></span><br/>        |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="240a9-211"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-211"><dt>**16 0x10**</dt></span></span> </dl>    | <span data-ttu-id="240a9-212">**Plattform \_ Fehler \_ spezifische \_ Daten** sind gültig.</span><span class="sxs-lookup"><span data-stu-id="240a9-212">**PLATFORM\_ERROR\_SPECIFIC\_DATA** is valid.</span></span><br/>    |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="240a9-213"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-213"><dt>**32 0x20**</dt></span></span> </dl>    | <span data-ttu-id="240a9-214">**Plattform \_ Fehler \_ OEM- \_ ID** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="240a9-214">**PLATFORM\_ERROR\_OEM\_ID** is valid.</span></span><br/>           |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="240a9-215"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-215"><dt>**64 0x40**</dt></span></span> </dl>    | <span data-ttu-id="240a9-216">**Plattform \_ Fehler \_ OEM- \_ Daten \_ Struktur** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="240a9-216">**PLATFORM\_ERROR\_OEM\_DATA\_STRUCT** is valid.</span></span><br/> |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="240a9-217"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-217"><dt>**128 0x80**</dt></span></span> </dl> | <span data-ttu-id="240a9-218">**Plattform \_ Fehler der \_ OEM- \_ Geräte \_ Pfad** ist gültig.</span><span class="sxs-lookup"><span data-stu-id="240a9-218">**PLATFORM\_ERROR\_OEM\_DEVICE\_PATH** is valid.</span></span><br/> |



 

<span data-ttu-id="240a9-219">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="240a9-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="240a9-220">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="240a9-220">Remarks</span></span>

<span data-ttu-id="240a9-221">Die Klasse " **msmcaevent \_ platformspecificerror** " ist von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="240a9-221">The **MSMCAEvent\_PlatformSpecificError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="240a9-222">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="240a9-222">Requirements</span></span>



| <span data-ttu-id="240a9-223">Anforderung</span><span class="sxs-lookup"><span data-stu-id="240a9-223">Requirement</span></span> | <span data-ttu-id="240a9-224">Wert</span><span class="sxs-lookup"><span data-stu-id="240a9-224">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="240a9-225">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="240a9-225">Minimum supported client</span></span><br/> | <span data-ttu-id="240a9-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="240a9-226">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="240a9-227">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="240a9-227">Minimum supported server</span></span><br/> | <span data-ttu-id="240a9-228">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="240a9-228">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="240a9-229">Namespace</span><span class="sxs-lookup"><span data-stu-id="240a9-229">Namespace</span></span><br/>                | <span data-ttu-id="240a9-230">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="240a9-230">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="240a9-231">MOF</span><span class="sxs-lookup"><span data-stu-id="240a9-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="240a9-232"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-232"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="240a9-233">DLL</span><span class="sxs-lookup"><span data-stu-id="240a9-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="240a9-234"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="240a9-234"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="240a9-235">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="240a9-235">See also</span></span>

<dl> <dt>

[<span data-ttu-id="240a9-236">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="240a9-236">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="240a9-237">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="240a9-237">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

