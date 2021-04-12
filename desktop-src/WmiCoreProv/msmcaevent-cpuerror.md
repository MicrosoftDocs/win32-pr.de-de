---
description: Stellt ein CPU-Fehler Ereignis dar. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 4ee4aa51-a965-4569-b53c-0ba21bf42752
title: MSMCAEvent_CPUError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_CPUError
- MSMCAEvent_CPUError.Active
- MSMCAEvent_CPUError.AdditionalErrors
- MSMCAEvent_CPUError.Cpu
- MSMCAEvent_CPUError.ErrorSeverity
- MSMCAEvent_CPUError.InstanceName
- MSMCAEvent_CPUError.Level
- MSMCAEvent_CPUError.RawRecord
- MSMCAEvent_CPUError.RecordId
- MSMCAEvent_CPUError.Size
- MSMCAEvent_CPUError.Type
- MSMCAEvent_CPUError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dff990b46d730a1e8b54ef99a24a686745e3dacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526108"
---
# <a name="msmcaevent_cpuerror-class"></a><span data-ttu-id="c2bcc-104">Msmcaevent \_ cpuerror-Klasse</span><span class="sxs-lookup"><span data-stu-id="c2bcc-104">MSMCAEvent\_CPUError class</span></span>

<span data-ttu-id="c2bcc-105">Die **msmcaevent \_ cpuerror** -Klasse stellt ein CPU-Fehler Ereignis dar.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-105">The **MSMCAEvent\_CPUError** class represents a CPU error event.</span></span> <span data-ttu-id="c2bcc-106">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="c2bcc-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c2bcc-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2bcc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2bcc-109">Syntax</span></span>

``` syntax
class MSMCAEvent_CPUError : WmiEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint32  Level;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="c2bcc-110">Member</span><span class="sxs-lookup"><span data-stu-id="c2bcc-110">Members</span></span>

<span data-ttu-id="c2bcc-111">Die **msmcaevent \_ cpuerror** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c2bcc-111">The **MSMCAEvent\_CPUError** class has these types of members:</span></span>

-   [<span data-ttu-id="c2bcc-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2bcc-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2bcc-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2bcc-113">Properties</span></span>

<span data-ttu-id="c2bcc-114">Die **msmcaevent \_ cpuerror** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-114">The **MSMCAEvent\_CPUError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2bcc-115">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2bcc-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c2bcc-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2bcc-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2bcc-118">**True**, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="c2bcc-119">**Additionalerrors**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2bcc-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2bcc-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2bcc-122">Anzahl zusätzlicher Fehler im MCA-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="c2bcc-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2bcc-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2bcc-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2bcc-126">CPU, die den Fehler gemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-126">CPU that reported the error.</span></span> <span data-ttu-id="c2bcc-127">Diese Eigenschaft gilt nur für ein Multiprozessorsystem, dem dem ersten Prozessor die Zahl 0 zugewiesen ist, dem zweiten Prozessor die Zahl 1 zugewiesen wird usw.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="c2bcc-128">**Errorschwere Grad**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2bcc-129">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2bcc-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2bcc-131">Der Schweregrad des gemeldeten Fehlers.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="c2bcc-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c2bcc-132">Value</span></span>                                                                                                | <span data-ttu-id="c2bcc-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c2bcc-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="c2bcc-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="c2bcc-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="c2bcc-135">Wiederherstellbar</span><span class="sxs-lookup"><span data-stu-id="c2bcc-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="c2bcc-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c2bcc-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c2bcc-137">FAT</span><span class="sxs-lookup"><span data-stu-id="c2bcc-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="c2bcc-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c2bcc-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c2bcc-139">KORRIGIER barer</span><span class="sxs-lookup"><span data-stu-id="c2bcc-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c2bcc-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2bcc-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2bcc-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-143">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c2bcc-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c2bcc-144">Eindeutiger Bezeichner für diese Instanz der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-144">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="c2bcc-145">**Level**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-145">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2bcc-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2bcc-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-148">Qualifizierer: **wmimissingdata** (-1)</span><span class="sxs-lookup"><span data-stu-id="c2bcc-148">Qualifiers: **WmiMissingData** (-1)</span></span>
</dt> </dl>

<span data-ttu-id="c2bcc-149">Cache Ebene, Übersetzungs Puffer (TLB) oder Struktur der Mikroarchitektur, in der der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-149">Level of cache, translation buffer (TLB), or micro-architectural structure where the error occurred.</span></span> <span data-ttu-id="c2bcc-150">Der Wert 0 (null) gibt die erste Ebene an.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-150">A value of 0 (zero) indicates the first level.</span></span>

</dd> <dt>

<span data-ttu-id="c2bcc-151">**Logtoeventlog**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-151">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2bcc-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2bcc-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2bcc-154">Wenn der Wert NULL ist, wird dieses Ereignis nicht im System Ereignisprotokoll protokolliert.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-154">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="c2bcc-155">**Rawrecord**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-155">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2bcc-156">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="c2bcc-156">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2bcc-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2bcc-158">Ein Bytearray, das den unformatierten Fehler Daten Satz enthält.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-158">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="c2bcc-159">Die Anzahl von Elementen im Array, die von der **size** -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-159">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="c2bcc-160">**Datensatz**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-160">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2bcc-161">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2bcc-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2bcc-163">Datensatz-ID des Fehler Datensatzes für diesen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-163">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="c2bcc-164">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c2bcc-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c2bcc-165">**Größe**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-165">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2bcc-166">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2bcc-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2bcc-168">Größe des unformatierten Fehler Datensatzes in Byte.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-168">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c2bcc-169">**Type**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-169">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2bcc-170">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2bcc-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2bcc-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2bcc-172">Der Typ der Ereignisprotokoll Meldung.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-172">Type of event log message.</span></span> <span data-ttu-id="c2bcc-173">Diese Meldungen entsprechen den Ereignisprotokoll-Nachrichten Codes, die zum Einfügen von Ereignisprotokoll Meldungen vom Windows-Ereignisprotokoll-Consumeranbieter verwendet werden, wenn ein Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-173">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2bcc-174">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2bcc-174">Remarks</span></span>

<span data-ttu-id="c2bcc-175">Die **msmcaevent \_ cpuerror** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-175">The **MSMCAEvent\_CPUError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2bcc-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2bcc-176">Requirements</span></span>



| <span data-ttu-id="c2bcc-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2bcc-177">Requirement</span></span> | <span data-ttu-id="c2bcc-178">Wert</span><span class="sxs-lookup"><span data-stu-id="c2bcc-178">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2bcc-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2bcc-179">Minimum supported client</span></span><br/> | <span data-ttu-id="c2bcc-180">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c2bcc-180">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="c2bcc-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2bcc-181">Minimum supported server</span></span><br/> | <span data-ttu-id="c2bcc-182">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c2bcc-182">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="c2bcc-183">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2bcc-183">Namespace</span></span><br/>                | <span data-ttu-id="c2bcc-184">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="c2bcc-184">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="c2bcc-185">MOF</span><span class="sxs-lookup"><span data-stu-id="c2bcc-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2bcc-186"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c2bcc-186"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2bcc-187">DLL</span><span class="sxs-lookup"><span data-stu-id="c2bcc-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2bcc-188"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2bcc-188"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2bcc-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2bcc-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2bcc-190">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="c2bcc-190">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="c2bcc-191">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="c2bcc-191">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

