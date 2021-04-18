---
description: Gibt einen ungültigen MCA (Machine Check Architecture)-Fehler an. Ein ungültiger MCA-Fehler identifiziert ein Fehler Format, das nicht den Windows-Spezifikationen entspricht. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 476ea558-2e0e-480f-b4ba-8d73fdef3308
title: MSMCAEvent_InvalidError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_InvalidError
- MSMCAEvent_InvalidError.Active
- MSMCAEvent_InvalidError.AdditionalErrors
- MSMCAEvent_InvalidError.Cpu
- MSMCAEvent_InvalidError.ErrorSeverity
- MSMCAEvent_InvalidError.InstanceName
- MSMCAEvent_InvalidError.RawRecord
- MSMCAEvent_InvalidError.RecordId
- MSMCAEvent_InvalidError.Size
- MSMCAEvent_InvalidError.Type
- MSMCAEvent_InvalidError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: abd12cfa7280a1b2f6a718b47b17d4ddf121cc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368072"
---
# <a name="msmcaevent_invaliderror-class"></a><span data-ttu-id="17a3d-105">Msmcaevent \_ invaliderror-Klasse</span><span class="sxs-lookup"><span data-stu-id="17a3d-105">MSMCAEvent\_InvalidError class</span></span>

<span data-ttu-id="17a3d-106">Die **msmcaevent \_ invaliderror** -Klasse gibt einen ungültigen MCA (Machine Check Architecture)-Fehler an.</span><span class="sxs-lookup"><span data-stu-id="17a3d-106">The **MSMCAEvent\_InvalidError** class indicates a Machine Check Architecture (MCA) invalid error.</span></span> <span data-ttu-id="17a3d-107">Ein ungültiger MCA-Fehler identifiziert ein Fehler Format, das nicht den Windows-Spezifikationen entspricht.</span><span class="sxs-lookup"><span data-stu-id="17a3d-107">An invalid MCA error identifies an error format that does not conform to Windows specifications.</span></span> <span data-ttu-id="17a3d-108">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="17a3d-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="17a3d-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17a3d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="17a3d-110">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="17a3d-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a3d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="17a3d-111">Syntax</span></span>

``` syntax
class MSMCAEvent_InvalidError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="17a3d-112">Member</span><span class="sxs-lookup"><span data-stu-id="17a3d-112">Members</span></span>

<span data-ttu-id="17a3d-113">Die **msmcaevent \_ invaliderror** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="17a3d-113">The **MSMCAEvent\_InvalidError** class has these types of members:</span></span>

-   [<span data-ttu-id="17a3d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17a3d-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17a3d-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17a3d-115">Properties</span></span>

<span data-ttu-id="17a3d-116">Die **msmcaevent \_ invaliderror** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17a3d-116">The **MSMCAEvent\_InvalidError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17a3d-117">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="17a3d-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a3d-118">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="17a3d-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="17a3d-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17a3d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17a3d-120">**True**, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="17a3d-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="17a3d-121">**Additionalerrors**</span><span class="sxs-lookup"><span data-stu-id="17a3d-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a3d-122">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17a3d-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17a3d-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17a3d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17a3d-124">Anzahl zusätzlicher Fehler im MCA-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="17a3d-124">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="17a3d-125">**CPU**</span><span class="sxs-lookup"><span data-stu-id="17a3d-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a3d-126">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17a3d-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17a3d-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17a3d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17a3d-128">CPU, die den Fehler gemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="17a3d-128">CPU that reported the error.</span></span> <span data-ttu-id="17a3d-129">Diese Eigenschaft gilt nur für ein Multiprozessorsystem, dem dem ersten Prozessor die Zahl 0 zugewiesen ist, dem zweiten Prozessor die Zahl 1 zugewiesen wird usw.</span><span class="sxs-lookup"><span data-stu-id="17a3d-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="17a3d-130">**Errorschwere Grad**</span><span class="sxs-lookup"><span data-stu-id="17a3d-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a3d-131">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="17a3d-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="17a3d-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17a3d-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17a3d-133">Der Schweregrad des gemeldeten Fehlers.</span><span class="sxs-lookup"><span data-stu-id="17a3d-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="17a3d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="17a3d-134">Value</span></span>                                                                                                | <span data-ttu-id="17a3d-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="17a3d-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="17a3d-136"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="17a3d-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="17a3d-137">Wiederherstellbar</span><span class="sxs-lookup"><span data-stu-id="17a3d-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="17a3d-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="17a3d-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="17a3d-139">FAT</span><span class="sxs-lookup"><span data-stu-id="17a3d-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="17a3d-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="17a3d-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="17a3d-141">KORRIGIER barer</span><span class="sxs-lookup"><span data-stu-id="17a3d-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="17a3d-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="17a3d-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a3d-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="17a3d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17a3d-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17a3d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17a3d-145">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="17a3d-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="17a3d-146">Eindeutiger Bezeichner dieser Instanz der Klasse.</span><span class="sxs-lookup"><span data-stu-id="17a3d-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="17a3d-147">**Logtoeventlog**</span><span class="sxs-lookup"><span data-stu-id="17a3d-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a3d-148">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17a3d-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17a3d-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17a3d-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17a3d-150">Wenn 0 (null) ist, wird dieses Ereignis nicht im System Ereignisprotokoll protokolliert.</span><span class="sxs-lookup"><span data-stu-id="17a3d-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="17a3d-151">**Rawrecord**</span><span class="sxs-lookup"><span data-stu-id="17a3d-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a3d-152">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="17a3d-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="17a3d-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17a3d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17a3d-154">Ein Bytearray, das den unformatierten Fehler Daten Satz enthält, wie Windows von der System Abstraktion Layer (SAL) dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="17a3d-154">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="17a3d-155">Die Anzahl der Elemente im Array wird durch die **size** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="17a3d-155">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="17a3d-156">**Datensatz**</span><span class="sxs-lookup"><span data-stu-id="17a3d-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a3d-157">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="17a3d-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="17a3d-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17a3d-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17a3d-159">Datensatz-ID des Fehler Datensatzes für diesen Fehler.</span><span class="sxs-lookup"><span data-stu-id="17a3d-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="17a3d-160">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17a3d-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="17a3d-161">**Größe**</span><span class="sxs-lookup"><span data-stu-id="17a3d-161">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a3d-162">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17a3d-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17a3d-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17a3d-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17a3d-164">Größe des unformatierten Fehler Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="17a3d-164">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="17a3d-165">**Type**</span><span class="sxs-lookup"><span data-stu-id="17a3d-165">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17a3d-166">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17a3d-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17a3d-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="17a3d-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17a3d-168">Der Typ der Ereignisprotokoll Meldung.</span><span class="sxs-lookup"><span data-stu-id="17a3d-168">Type of event log message.</span></span> <span data-ttu-id="17a3d-169">Diese Meldungen entsprechen den Ereignisprotokoll-Nachrichten Codes, die zum Einfügen von Ereignisprotokoll Meldungen vom Windows-Ereignisprotokoll-Consumeranbieter verwendet werden, wenn ein Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="17a3d-169">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17a3d-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17a3d-170">Remarks</span></span>

<span data-ttu-id="17a3d-171">Die **msmcaevent \_ invaliderror** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="17a3d-171">The **MSMCAEvent\_InvalidError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17a3d-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17a3d-172">Requirements</span></span>



| <span data-ttu-id="17a3d-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17a3d-173">Requirement</span></span> | <span data-ttu-id="17a3d-174">Wert</span><span class="sxs-lookup"><span data-stu-id="17a3d-174">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17a3d-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17a3d-175">Minimum supported client</span></span><br/> | <span data-ttu-id="17a3d-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="17a3d-176">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="17a3d-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17a3d-177">Minimum supported server</span></span><br/> | <span data-ttu-id="17a3d-178">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17a3d-178">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="17a3d-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="17a3d-179">Namespace</span></span><br/>                | <span data-ttu-id="17a3d-180">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="17a3d-180">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="17a3d-181">MOF</span><span class="sxs-lookup"><span data-stu-id="17a3d-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17a3d-182"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="17a3d-182"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="17a3d-183">DLL</span><span class="sxs-lookup"><span data-stu-id="17a3d-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17a3d-184"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17a3d-184"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17a3d-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17a3d-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a3d-186">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="17a3d-186">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="17a3d-187">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="17a3d-187">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

