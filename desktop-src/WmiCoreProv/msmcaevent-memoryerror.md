---
description: Stellt ein MCA-Speicherfehler Ereignis dar. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 0db1d526-e2c3-4e48-90c8-cbcd9121040e
title: MSMCAEvent_MemoryError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryError
- MSMCAEvent_MemoryError.Active
- MSMCAEvent_MemoryError.AdditionalErrors
- MSMCAEvent_MemoryError.BUS_SPECIFIC_DATA
- MSMCAEvent_MemoryError.Cpu
- MSMCAEvent_MemoryError.ErrorSeverity
- MSMCAEvent_MemoryError.InstanceName
- MSMCAEvent_MemoryError.MEM_BANK
- MSMCAEvent_MemoryError.MEM_BIT_POSITION
- MSMCAEvent_MemoryError.MEM_CARD
- MSMCAEvent_MemoryError.MEM_COLUMN
- MSMCAEvent_MemoryError.MEM_ERROR_STATUS
- MSMCAEvent_MemoryError.MEM_MODULE
- MSMCAEvent_MemoryError.MEM_NODE
- MSMCAEvent_MemoryError.MEM_PHYSICAL_ADDR
- MSMCAEvent_MemoryError.MEM_PHYSICAL_MASK
- MSMCAEvent_MemoryError.MEM_ROW
- MSMCAEvent_MemoryError.RawRecord
- MSMCAEvent_MemoryError.RecordId
- MSMCAEvent_MemoryError.REQUESTOR_ID
- MSMCAEvent_MemoryError.RESPONDER_ID
- MSMCAEvent_MemoryError.Size
- MSMCAEvent_MemoryError.TARGET_ID
- MSMCAEvent_MemoryError.Type
- MSMCAEvent_MemoryError.VALIDATION_BITS
- MSMCAEvent_MemoryError.MEM_DEVICE
- MSMCAEvent_MemoryError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8dce82b8fa7a87676c34a9c6f26f43e4db10e227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353884"
---
# <a name="msmcaevent_memoryerror-class"></a><span data-ttu-id="1173d-104">Msmcaevent \_ MemoryError-Klasse</span><span class="sxs-lookup"><span data-stu-id="1173d-104">MSMCAEvent\_MemoryError class</span></span>

<span data-ttu-id="1173d-105">Die **msmcaevent \_ MemoryError** -Klasse stellt ein MCA-Speicherfehler Ereignis dar.</span><span class="sxs-lookup"><span data-stu-id="1173d-105">The **MSMCAEvent\_MemoryError** class represents a Machine Check Architecture (MCA) memory error event.</span></span> <span data-ttu-id="1173d-106">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1173d-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="1173d-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1173d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1173d-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="1173d-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1173d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1173d-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint64  BUS_SPECIFIC_DATA;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint16  MEM_BANK;
  uint16  MEM_BIT_POSITION;
  uint16  MEM_CARD;
  uint16  MEM_COLUMN;
  uint64  MEM_ERROR_STATUS;
  uint16  MEM_MODULE;
  uint16  MEM_NODE;
  uint64  MEM_PHYSICAL_ADDR;
  uint64  MEM_PHYSICAL_MASK;
  uint16  MEM_ROW;
  uint8   RawRecord[];
  uint64  RecordId;
  uint64  REQUESTOR_ID;
  uint64  RESPONDER_ID;
  uint32  Size;
  uint64  TARGET_ID;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint16  MEM_DEVICE;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="1173d-110">Member</span><span class="sxs-lookup"><span data-stu-id="1173d-110">Members</span></span>

<span data-ttu-id="1173d-111">Die **msmcaevent \_ MemoryError** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1173d-111">The **MSMCAEvent\_MemoryError** class has these types of members:</span></span>

-   [<span data-ttu-id="1173d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1173d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1173d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1173d-113">Properties</span></span>

<span data-ttu-id="1173d-114">Die **msmcaevent \_ MemoryError** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1173d-114">The **MSMCAEvent\_MemoryError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1173d-115">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="1173d-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1173d-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-118">**True**, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="1173d-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-119">**Additionalerrors**</span><span class="sxs-lookup"><span data-stu-id="1173d-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1173d-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-122">Anzahl zusätzlicher Fehler im MCA-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="1173d-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-123">**\_Busspezifische \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="1173d-123">**BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-124">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1173d-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-126">OEM-spezifische, Bus abhängige Daten.</span><span class="sxs-lookup"><span data-stu-id="1173d-126">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="1173d-127">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1173d-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1173d-128">**CPU**</span><span class="sxs-lookup"><span data-stu-id="1173d-128">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1173d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-131">CPU, die den Fehler gemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="1173d-131">CPU that reported the error.</span></span> <span data-ttu-id="1173d-132">Diese Eigenschaft gilt nur für ein Multiprozessorsystem, dem dem ersten Prozessor die Zahl 0 zugewiesen ist, dem zweiten Prozessor die Zahl 1 zugewiesen wird usw.</span><span class="sxs-lookup"><span data-stu-id="1173d-132">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-133">**Errorschwere Grad**</span><span class="sxs-lookup"><span data-stu-id="1173d-133">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-134">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1173d-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-136">Der Schweregrad des gemeldeten Fehlers.</span><span class="sxs-lookup"><span data-stu-id="1173d-136">Severity level of the error reported.</span></span>



| <span data-ttu-id="1173d-137">Wert</span><span class="sxs-lookup"><span data-stu-id="1173d-137">Value</span></span>                                                                                                | <span data-ttu-id="1173d-138">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1173d-138">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="1173d-139"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-139"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="1173d-140">Wiederherstellbar</span><span class="sxs-lookup"><span data-stu-id="1173d-140">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="1173d-141"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-141"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="1173d-142">FAT</span><span class="sxs-lookup"><span data-stu-id="1173d-142">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="1173d-143"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-143"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="1173d-144">KORRIGIER barer</span><span class="sxs-lookup"><span data-stu-id="1173d-144">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1173d-145">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="1173d-145">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1173d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1173d-148">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1173d-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1173d-149">Eindeutiger Bezeichner dieser Instanz der Klasse.</span><span class="sxs-lookup"><span data-stu-id="1173d-149">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-150">**Logtoeventlog**</span><span class="sxs-lookup"><span data-stu-id="1173d-150">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1173d-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-153">Wenn der Wert NULL ist, wird dieses Ereignis nicht im System Ereignisprotokoll protokolliert.</span><span class="sxs-lookup"><span data-stu-id="1173d-153">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-154">**Arbeitsspeicher- \_ Bank**</span><span class="sxs-lookup"><span data-stu-id="1173d-154">**MEM\_BANK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-155">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1173d-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-157">Das Modul oder die Rang Nummer des Speicherfehler Speicher Orts.</span><span class="sxs-lookup"><span data-stu-id="1173d-157">The Module or RANK number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-158">**Arbeitsspeicher- \_ \_ Bitposition**</span><span class="sxs-lookup"><span data-stu-id="1173d-158">**MEM\_BIT\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-159">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1173d-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-161">Bitposition im Arbeitsspeicher Wort, die den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="1173d-161">Bit position in the memory word that contains the error.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-162">**Arbeitsspeicher \_ Karte**</span><span class="sxs-lookup"><span data-stu-id="1173d-162">**MEM\_CARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-163">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1173d-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-165">Die Kartennummer des Speicherfehler Speicher Orts.</span><span class="sxs-lookup"><span data-stu-id="1173d-165">Card number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-166">**Arbeitsspeicher \_ Spalte**</span><span class="sxs-lookup"><span data-stu-id="1173d-166">**MEM\_COLUMN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1173d-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-169">Die Spaltennummer des Speicherfehler Speicher Orts.</span><span class="sxs-lookup"><span data-stu-id="1173d-169">Column number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-170">**Arbeits \_ Speichergerät**</span><span class="sxs-lookup"><span data-stu-id="1173d-170">**MEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-171">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1173d-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-173">Gerätenummer des Speicherfehler Speicher Orts.</span><span class="sxs-lookup"><span data-stu-id="1173d-173">Device number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-174">**Status des Arbeitsspeicher \_ Fehlers \_**</span><span class="sxs-lookup"><span data-stu-id="1173d-174">**MEM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-175">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1173d-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-177">Fehlerstatus des Speichers.</span><span class="sxs-lookup"><span data-stu-id="1173d-177">Memory error status.</span></span>

<span data-ttu-id="1173d-178">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1173d-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1173d-179">**Arbeitsspeicher \_ Modul**</span><span class="sxs-lookup"><span data-stu-id="1173d-179">**MEM\_MODULE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-180">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1173d-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-182">Modul oder Rang Nummer des Speicherfehler Speicher Orts.</span><span class="sxs-lookup"><span data-stu-id="1173d-182">Module or rank number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-183">**\_Knoten "Knoten"**</span><span class="sxs-lookup"><span data-stu-id="1173d-183">**MEM\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-184">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1173d-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-186">Knoten, der den Arbeitsspeicher Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="1173d-186">Node that contains the memory error.</span></span> <span data-ttu-id="1173d-187">Diese Eigenschaft ist nur in einem System mit mehreren Knoten anwendbar.</span><span class="sxs-lookup"><span data-stu-id="1173d-187">This property applies only in a multi-node system.</span></span> <span data-ttu-id="1173d-188">Diese Eigenschaft ist Anbieter spezifisch.</span><span class="sxs-lookup"><span data-stu-id="1173d-188">This property is vendor-specific.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-189">**physische Arbeitsspeicher- \_ \_ addr**</span><span class="sxs-lookup"><span data-stu-id="1173d-189">**MEM\_PHYSICAL\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-190">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1173d-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-192">Die physische Adresse des Arbeitsspeicher Fehlers.</span><span class="sxs-lookup"><span data-stu-id="1173d-192">Physical address of the memory error.</span></span>

<span data-ttu-id="1173d-193">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1173d-193">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1173d-194">**physische Arbeitsspeicher \_ \_ Maske**</span><span class="sxs-lookup"><span data-stu-id="1173d-194">**MEM\_PHYSICAL\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-195">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1173d-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-197">Gültige Adress Bits in der physischen 64-Bit-Adresse des Arbeitsspeicher Fehlers.</span><span class="sxs-lookup"><span data-stu-id="1173d-197">Valid address bits in the 64-bit physical address of the memory error.</span></span>

> [!Note]  
> <span data-ttu-id="1173d-198">Die physische Maske gibt die Granularität der physischen Adresse an.</span><span class="sxs-lookup"><span data-stu-id="1173d-198">The physical mask specifies the granularity of the physical address.</span></span> <span data-ttu-id="1173d-199">Die physische Adresse des Arbeitsspeicher Fehlers hängt von den Hardware Implementierungs Faktoren ab.</span><span class="sxs-lookup"><span data-stu-id="1173d-199">The physical address of the memory error is dependent on hardware implementation factors.</span></span>

 

<span data-ttu-id="1173d-200">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1173d-200">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1173d-201">**Arbeitsspeicher \_ Zeile**</span><span class="sxs-lookup"><span data-stu-id="1173d-201">**MEM\_ROW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-202">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1173d-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-204">Die Zeilennummer des Speicherfehler Speicher Orts.</span><span class="sxs-lookup"><span data-stu-id="1173d-204">Row number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-205">**Rawrecord**</span><span class="sxs-lookup"><span data-stu-id="1173d-205">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-206">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="1173d-206">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1173d-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-208">Ein Bytearray, das den unformatierten Fehler Daten Satz enthält, wie Windows von der System Abstraktion Layer (SAL) dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1173d-208">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="1173d-209">Die Anzahl der Elemente im Array wird durch die **size** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="1173d-209">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-210">**Datensatz**</span><span class="sxs-lookup"><span data-stu-id="1173d-210">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-211">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1173d-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-213">Datensatz-ID des Fehler Datensatzes für diesen Fehler.</span><span class="sxs-lookup"><span data-stu-id="1173d-213">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="1173d-214">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1173d-214">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1173d-215">**\_RequestId-ID**</span><span class="sxs-lookup"><span data-stu-id="1173d-215">**REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-216">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1173d-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-218">Die Hardware Adresse des Geräts oder der Komponente, von der die Transaktion initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="1173d-218">Hardware address of the device or component that initiates the transaction.</span></span>

<span data-ttu-id="1173d-219">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1173d-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1173d-220">**Responder- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="1173d-220">**RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-221">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1173d-221">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-223">Die Hardware Adresse des Responders für die Transaktion.</span><span class="sxs-lookup"><span data-stu-id="1173d-223">Hardware address of the responder to the transaction.</span></span>

<span data-ttu-id="1173d-224">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1173d-224">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1173d-225">**Größe**</span><span class="sxs-lookup"><span data-stu-id="1173d-225">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-226">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1173d-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-227">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-228">Größe des unformatierten Fehler Datensatzes in Byte.</span><span class="sxs-lookup"><span data-stu-id="1173d-228">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-229">**Ziel- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="1173d-229">**TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-230">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1173d-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-232">Die Hardware Adresse des beabsichtigten Ziels der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="1173d-232">Hardware address of the intended target of the transaction.</span></span>

<span data-ttu-id="1173d-233">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1173d-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1173d-234">**Type**</span><span class="sxs-lookup"><span data-stu-id="1173d-234">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-235">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1173d-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-237">Der Typ der Ereignisprotokoll Meldung.</span><span class="sxs-lookup"><span data-stu-id="1173d-237">Type of event log message.</span></span> <span data-ttu-id="1173d-238">Diese Meldungen entsprechen den Ereignisprotokoll-Nachrichten Codes, die zum Einfügen von Ereignisprotokoll Meldungen vom Windows-Ereignisprotokoll-Consumeranbieter verwendet werden, wenn ein Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="1173d-238">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="1173d-239">**Validierungs \_ Bits**</span><span class="sxs-lookup"><span data-stu-id="1173d-239">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1173d-240">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1173d-240">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1173d-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1173d-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1173d-242">Validierungs Bits zum Angeben der Gültigkeit der nachfolgenden Felder.</span><span class="sxs-lookup"><span data-stu-id="1173d-242">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="1173d-243">Werte</span><span class="sxs-lookup"><span data-stu-id="1173d-243">Values</span></span>                                                                                     | <span data-ttu-id="1173d-244">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1173d-244">Meaning</span></span>                                                 |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="1173d-245"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-245"><dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="1173d-246">Der Status des Arbeitsspeicher \_ Fehlers \_ ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-246">MEM\_ERROR\_STATUS is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="1173d-247"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-247"><dt>2 (0x2)</dt></span></span> </dl>         | <span data-ttu-id="1173d-248">Die physische Arbeitsspeicher- \_ \_ addr ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-248">MEM\_PHYSICAL\_ADDR is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="1173d-249"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-249"><dt>4 (0x4)</dt></span></span> </dl>         | <span data-ttu-id="1173d-250">Die "Mem \_ addr \_ Mask" ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-250">MEM\_ADDR\_MASK is valid.</span></span><br/>                    |
| <dl> <span data-ttu-id="1173d-251"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-251"><dt>8 (0x8)</dt></span></span> </dl>         | <span data-ttu-id="1173d-252">Der Arbeitsspeicher \_ Knoten ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-252">MEM\_NODE is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="1173d-253"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-253"><dt>16 (0x10)</dt></span></span> </dl>       | <span data-ttu-id="1173d-254">Die Arbeitsspeicher \_ Karte ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-254">MEM\_CARD is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="1173d-255"><dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-255"><dt>32 (0x20)</dt></span></span> </dl>       | <span data-ttu-id="1173d-256">Das Speicher \_ Modul ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-256">MEM\_MODULE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="1173d-257"><dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-257"><dt>64 (0x40)</dt></span></span> </dl>       | <span data-ttu-id="1173d-258">Die Arbeitsspeicher- \_ Bank ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-258">MEM\_BANK is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="1173d-259"><dt>128 (0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-259"><dt>128 (0x80)</dt></span></span> </dl>      | <span data-ttu-id="1173d-260">Das Arbeits \_ Speichergerät ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-260">MEM\_DEVICE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="1173d-261"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-261"><dt>256 (0x100)</dt></span></span> </dl>     | <span data-ttu-id="1173d-262">Die Arbeitsspeicher \_ Zeile ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-262">MEM\_ROW is valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="1173d-263"><dt>512 (0x200)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-263"><dt>512 (0x200)</dt></span></span> </dl>     | <span data-ttu-id="1173d-264">Die Arbeitsspeicher \_ Spalte ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-264">MEM\_COLUMN is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="1173d-265"><dt>1024 (0x400)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-265"><dt>1024 (0x400)</dt></span></span> </dl>    | <span data-ttu-id="1173d-266">Die Arbeitsspeicher- \_ \_ Bitposition ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-266">MEM\_BIT\_POSITION is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="1173d-267"><dt>2048 (0x800)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-267"><dt>2048 (0x800)</dt></span></span> </dl>    | <span data-ttu-id="1173d-268">Die ID der Arbeitsspeicher \_ Plattform \_ \_ ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-268">MEM\_PLATFORM\_REQUESTOR\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="1173d-269"><dt>4096 (0x1000)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-269"><dt>4096 (0x1000)</dt></span></span> </dl>   | <span data-ttu-id="1173d-270">Die \_ Antwort-ID der Arbeitsspeicher Plattform \_ \_ ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-270">MEM\_PLATFORM\_RESPONDER\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="1173d-271"><dt>8192 (0x2000)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-271"><dt>8192 (0x2000)</dt></span></span> </dl>   | <span data-ttu-id="1173d-272">Das Ziel der G4- \_ Plattform \_ ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-272">MEM\_PLATFORM\_TARGET is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="1173d-273"><dt>16384 (0x4000)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-273"><dt>16384 (0x4000)</dt></span></span> </dl>  | <span data-ttu-id="1173d-274">Die \_ spezifischen Daten des G4-Platt Form \_ Busses \_ \_ sind gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-274">MEM\_PLATFORM\_BUS\_SPECIFIC\_DATA is valid.</span></span><br/> |
| <dl> <span data-ttu-id="1173d-275"><dt>32768 (0X8000)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-275"><dt>32768 (0x8000)</dt></span></span> </dl>  | <span data-ttu-id="1173d-276">Die OEM-ID der Arbeitsspeicher \_ Plattform \_ \_ ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-276">MEM\_PLATFORM\_OEM\_ID is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="1173d-277"><dt>65536 (0x10000)</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-277"><dt>65536 (0x10000)</dt></span></span> </dl> | <span data-ttu-id="1173d-278">Die \_ OEM-Datenstruktur der Arbeitsspeicher Plattform \_ \_ \_ ist gültig.</span><span class="sxs-lookup"><span data-stu-id="1173d-278">MEM\_PLATFORM\_OEM\_DATA\_STRUCT is valid.</span></span><br/>   |



 

<span data-ttu-id="1173d-279">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1173d-279">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1173d-280">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1173d-280">Remarks</span></span>

<span data-ttu-id="1173d-281">Die **msmcaevent \_ MemoryError** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1173d-281">The **MSMCAEvent\_MemoryError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1173d-282">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1173d-282">Requirements</span></span>



| <span data-ttu-id="1173d-283">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1173d-283">Requirement</span></span> | <span data-ttu-id="1173d-284">Wert</span><span class="sxs-lookup"><span data-stu-id="1173d-284">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1173d-285">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1173d-285">Minimum supported client</span></span><br/> | <span data-ttu-id="1173d-286">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1173d-286">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="1173d-287">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1173d-287">Minimum supported server</span></span><br/> | <span data-ttu-id="1173d-288">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1173d-288">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="1173d-289">Namespace</span><span class="sxs-lookup"><span data-stu-id="1173d-289">Namespace</span></span><br/>                | <span data-ttu-id="1173d-290">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="1173d-290">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1173d-291">MOF</span><span class="sxs-lookup"><span data-stu-id="1173d-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1173d-292"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-292"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1173d-293">DLL</span><span class="sxs-lookup"><span data-stu-id="1173d-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1173d-294"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1173d-294"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1173d-295">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1173d-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1173d-296">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="1173d-296">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="1173d-297">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="1173d-297">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

