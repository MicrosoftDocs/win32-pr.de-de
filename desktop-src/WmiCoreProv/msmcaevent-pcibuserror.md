---
description: Stellt einen PCI-Busfehler (Machine Check Architecture, MCA) dar. Diese Klasse ist nur für Computer verfügbar, die auf einem 64-Bit-Windows-Betriebssystem ausgeführt werden.
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: MSMCAEvent_PCIBusError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 7f2b800a07c0b979468a5df5a8be67e6adee39de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751384"
---
# <a name="msmcaevent_pcibuserror-class"></a><span data-ttu-id="58d7f-104">Msmcaevent \_ pcibuserror-Klasse</span><span class="sxs-lookup"><span data-stu-id="58d7f-104">MSMCAEvent\_PCIBusError class</span></span>

<span data-ttu-id="58d7f-105">Die **msmcaevent \_ pcibuserror** -Klasse stellt eine MCA-PCI-Busfehler (Machine Check Architecture) dar.</span><span class="sxs-lookup"><span data-stu-id="58d7f-105">The **MSMCAEvent\_PCIBusError** class represents a Machine Check Architecture (MCA) PCI bus error.</span></span> <span data-ttu-id="58d7f-106">Diese Klasse ist nur für Computer verfügbar, die auf einem 64-Bit-Windows-Betriebssystem ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="58d7f-106">This class is available only for computers running on a 64-bit Windows operating system.</span></span>

<span data-ttu-id="58d7f-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="58d7f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="58d7f-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="58d7f-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="58d7f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="58d7f-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="58d7f-110">Member</span><span class="sxs-lookup"><span data-stu-id="58d7f-110">Members</span></span>

<span data-ttu-id="58d7f-111">Die **msmcaevent \_ pcibuserror** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="58d7f-111">The **MSMCAEvent\_PCIBusError** class has these types of members:</span></span>

-   [<span data-ttu-id="58d7f-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58d7f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58d7f-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58d7f-113">Properties</span></span>

<span data-ttu-id="58d7f-114">Die **msmcaevent \_ pcibuserror** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="58d7f-114">The **MSMCAEvent\_PCIBusError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58d7f-115">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="58d7f-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="58d7f-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-118">**True**, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="58d7f-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-119">**Additionalerrors**</span><span class="sxs-lookup"><span data-stu-id="58d7f-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58d7f-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-122">Anzahl zusätzlicher Fehler im Datensatz.</span><span class="sxs-lookup"><span data-stu-id="58d7f-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-123">**CPU**</span><span class="sxs-lookup"><span data-stu-id="58d7f-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58d7f-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-126">CPU, die den Fehler gemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="58d7f-126">CPU that reported the error.</span></span> <span data-ttu-id="58d7f-127">Diese Eigenschaft gilt nur für ein Multiprozessorsystem, dem dem ersten Prozessor die Zahl 0 zugewiesen ist, dem zweiten Prozessor die Zahl 1 zugewiesen wird usw.</span><span class="sxs-lookup"><span data-stu-id="58d7f-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-128">**Errorschwere Grad**</span><span class="sxs-lookup"><span data-stu-id="58d7f-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-129">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="58d7f-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-131">Der Schweregrad des gemeldeten Fehlers.</span><span class="sxs-lookup"><span data-stu-id="58d7f-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="58d7f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="58d7f-132">Value</span></span>                                                                                                | <span data-ttu-id="58d7f-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="58d7f-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="58d7f-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="58d7f-135">Wiederherstellbar</span><span class="sxs-lookup"><span data-stu-id="58d7f-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="58d7f-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="58d7f-137">FAT</span><span class="sxs-lookup"><span data-stu-id="58d7f-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="58d7f-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="58d7f-139">KORRIGIER barer</span><span class="sxs-lookup"><span data-stu-id="58d7f-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="58d7f-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="58d7f-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58d7f-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-143">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="58d7f-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-144">Eindeutiger Bezeichner dieser Instanz der Klasse.</span><span class="sxs-lookup"><span data-stu-id="58d7f-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-145">**Logtoeventlog**</span><span class="sxs-lookup"><span data-stu-id="58d7f-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58d7f-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-148">Wenn 0 (null) ist, wird dieses Ereignis nicht im System Ereignisprotokoll protokolliert.</span><span class="sxs-lookup"><span data-stu-id="58d7f-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-149">**PCI \_ - \_ Busadresse**</span><span class="sxs-lookup"><span data-stu-id="58d7f-149">**PCI\_BUS\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-150">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58d7f-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-152">Arbeitsspeicher oder e/a-Adresse auf dem PCI-Bus zum Zeitpunkt des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="58d7f-152">Memory or I/O address on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="58d7f-153">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58d7f-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-154">**PCI- \_ Bus- \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="58d7f-154">**PCI\_BUS\_CMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-155">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58d7f-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-157">Bus Befehl oder-Vorgang zum Zeitpunkt des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="58d7f-157">Bus command or operation at the time of the event.</span></span>

<span data-ttu-id="58d7f-158">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58d7f-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-159">**PCI \_ - \_ Busdaten**</span><span class="sxs-lookup"><span data-stu-id="58d7f-159">**PCI\_BUS\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-160">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58d7f-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-162">Daten auf dem PCI-Bus zum Zeitpunkt des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="58d7f-162">Data on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="58d7f-163">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58d7f-163">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-164">**PCI \_ - \_ \_ busfehlerstatus**</span><span class="sxs-lookup"><span data-stu-id="58d7f-164">**PCI\_BUS\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-165">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58d7f-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-167">Busstatus zum Zeitpunkt des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="58d7f-167">Bus status at the time of the error.</span></span>

<span data-ttu-id="58d7f-168">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58d7f-168">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-169">**PCI \_ - \_ \_ busfehlertyp**</span><span class="sxs-lookup"><span data-stu-id="58d7f-169">**PCI\_BUS\_ERROR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-170">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58d7f-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-172">Typ des PCI-Busfehlers.</span><span class="sxs-lookup"><span data-stu-id="58d7f-172">Type of PCI bus error.</span></span>



| <span data-ttu-id="58d7f-173">Wert</span><span class="sxs-lookup"><span data-stu-id="58d7f-173">Value</span></span>                                                                                                | <span data-ttu-id="58d7f-174">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="58d7f-174">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="58d7f-175"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-175"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="58d7f-176">Unbekannter oder OEM-System spezifischer Fehler.</span><span class="sxs-lookup"><span data-stu-id="58d7f-176">Unknown or OEM System Specific Error.</span></span><br/>            |
| <span id="1"></span><dl> <span data-ttu-id="58d7f-177"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-177"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="58d7f-178">Daten Paritätsfehler.</span><span class="sxs-lookup"><span data-stu-id="58d7f-178">Data Parity Error.</span></span><br/>                               |
| <span id="2"></span><dl> <span data-ttu-id="58d7f-179"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-179"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="58d7f-180">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="58d7f-180">System Error.</span></span><br/>                                    |
| <span id="3"></span><dl> <span data-ttu-id="58d7f-181"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-181"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="58d7f-182">Master Abbruch.</span><span class="sxs-lookup"><span data-stu-id="58d7f-182">Master Abort.</span></span><br/>                                    |
| <span id="4"></span><dl> <span data-ttu-id="58d7f-183"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-183"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="58d7f-184">Bustimeout oder kein Gerät vorhanden (keine devsel \# ).</span><span class="sxs-lookup"><span data-stu-id="58d7f-184">Bus Time Out or No Device Present (NO DEVSEL\#).</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="58d7f-185"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-185"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="58d7f-186">Fehler bei der Master Daten Parität.</span><span class="sxs-lookup"><span data-stu-id="58d7f-186">Master Data Parity Error.</span></span><br/>                        |
| <span id="6"></span><dl> <span data-ttu-id="58d7f-187"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-187"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="58d7f-188">Adress Paritätsfehler.</span><span class="sxs-lookup"><span data-stu-id="58d7f-188">Address Parity Error.</span></span><br/>                            |
| <span id="7"></span><dl> <span data-ttu-id="58d7f-189"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-189"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="58d7f-190">Befehls Paritätsfehler.</span><span class="sxs-lookup"><span data-stu-id="58d7f-190">Command Parity Error.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="58d7f-191">**PCI- \_ Bus- \_ ID \_ Busnummer**</span><span class="sxs-lookup"><span data-stu-id="58d7f-191">**PCI\_BUS\_ID\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-192">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="58d7f-192">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-194">Der angegebene Bezeichner für den PCI-Bus, der den Fehler gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="58d7f-194">Designated identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-195">**PCI- \_ Bus- \_ ID \_ segmentnumber**</span><span class="sxs-lookup"><span data-stu-id="58d7f-195">**PCI\_BUS\_ID\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-196">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="58d7f-196">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-198">Der angegebene Segment Bezeichner für den PCI-Bus, der den Fehler festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="58d7f-198">Designated segment identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-199">**PCI- \_ Bus- \_ \_ RequestId-ID**</span><span class="sxs-lookup"><span data-stu-id="58d7f-199">**PCI\_BUS\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-200">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58d7f-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-202">Der PCI-Bus-Anforderer Bezeichner zum Zeitpunkt des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="58d7f-202">PCI Bus requestor identifier at the time of the event.</span></span>

<span data-ttu-id="58d7f-203">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58d7f-203">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-204">**PCI- \_ Bus- \_ Responder- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="58d7f-204">**PCI\_BUS\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-205">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58d7f-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-207">Der PCI-Bus-Responder-Bezeichner zum Zeitpunkt des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="58d7f-207">PCI Bus Responder identifier at the time of the event.</span></span>

<span data-ttu-id="58d7f-208">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58d7f-208">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-209">**Rawrecord**</span><span class="sxs-lookup"><span data-stu-id="58d7f-209">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-210">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="58d7f-210">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-212">Ein Bytearray, das den unformatierten Fehler Daten Satz enthält, wie Windows von der System Abstraktion Layer (SAL) dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="58d7f-212">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="58d7f-213">Die Anzahl der Elemente im Array wird durch die **size** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="58d7f-213">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-214">**Datensatz**</span><span class="sxs-lookup"><span data-stu-id="58d7f-214">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-215">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58d7f-215">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-217">Datensatz-ID des Fehler Datensatzes für diesen Fehler.</span><span class="sxs-lookup"><span data-stu-id="58d7f-217">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="58d7f-218">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58d7f-218">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-219">**Größe**</span><span class="sxs-lookup"><span data-stu-id="58d7f-219">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-220">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58d7f-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-222">Größe des unformatierten Fehler Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="58d7f-222">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-223">**Type**</span><span class="sxs-lookup"><span data-stu-id="58d7f-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-224">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58d7f-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-226">Der Typ der Ereignisprotokoll Meldung.</span><span class="sxs-lookup"><span data-stu-id="58d7f-226">Type of event log message.</span></span> <span data-ttu-id="58d7f-227">Diese Meldungen entsprechen den Ereignisprotokoll-Nachrichten Codes, die zum Einfügen von Ereignisprotokoll Meldungen vom Windows-Ereignisprotokoll-Consumeranbieter verwendet werden, wenn ein Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="58d7f-227">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="58d7f-228">**Validierungs \_ Bits**</span><span class="sxs-lookup"><span data-stu-id="58d7f-228">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58d7f-229">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58d7f-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58d7f-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58d7f-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58d7f-231">Validierungs Bits zum Angeben der Gültigkeit der nachfolgenden Felder.</span><span class="sxs-lookup"><span data-stu-id="58d7f-231">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="58d7f-232">Werte</span><span class="sxs-lookup"><span data-stu-id="58d7f-232">Values</span></span>                                                                                  | <span data-ttu-id="58d7f-233">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="58d7f-233">Meaning</span></span>                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="58d7f-234"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-234"><dt>1 (0x1)</dt></span></span> </dl>      | <span data-ttu-id="58d7f-235">Der Status des PCI- \_ \_ Busfehlers \_ ist gültig.</span><span class="sxs-lookup"><span data-stu-id="58d7f-235">PCI\_BUS\_ERROR\_STATUS is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="58d7f-236"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-236"><dt>2 (0x2)</dt></span></span> </dl>      | <span data-ttu-id="58d7f-237">Der PCI- \_ \_ \_ busfehlertyp ist gültig.</span><span class="sxs-lookup"><span data-stu-id="58d7f-237">PCI\_BUS\_ERROR\_TYPE is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="58d7f-238"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-238"><dt>4 (0x4)</dt></span></span> </dl>      | <span data-ttu-id="58d7f-239">Die PCI- \_ Bus- \_ ID ist gültig.</span><span class="sxs-lookup"><span data-stu-id="58d7f-239">PCI\_BUS\_ID is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="58d7f-240"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-240"><dt>8 (0x8)</dt></span></span> </dl>      | <span data-ttu-id="58d7f-241">Die PCI- \_ \_ Busadresse ist gültig.</span><span class="sxs-lookup"><span data-stu-id="58d7f-241">PCI\_BUS\_ADDRESS is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="58d7f-242"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-242"><dt>16 (0x10)</dt></span></span> </dl>    | <span data-ttu-id="58d7f-243">PCI \_ - \_ Busdaten sind gültig.</span><span class="sxs-lookup"><span data-stu-id="58d7f-243">PCI\_BUS\_DATA is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="58d7f-244"><dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-244"><dt>32 (0x20)</dt></span></span> </dl>    | <span data-ttu-id="58d7f-245">Der PCI- \_ Bus- \_ cmd ist gültig.</span><span class="sxs-lookup"><span data-stu-id="58d7f-245">PCI\_BUS\_CMD is valid.</span></span><br/>               |
| <dl> <span data-ttu-id="58d7f-246"><dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-246"><dt>64 (0x40)</dt></span></span> </dl>    | <span data-ttu-id="58d7f-247">Die PCI- \_ \_ busrequestid \_ ist gültig.</span><span class="sxs-lookup"><span data-stu-id="58d7f-247">PCI\_BUS\_REQUESTOR\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="58d7f-248"><dt>128 (0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-248"><dt>128 (0x80)</dt></span></span> </dl>   | <span data-ttu-id="58d7f-249">Die PCI- \_ Bus- \_ Responder- \_ ID ist gültig.</span><span class="sxs-lookup"><span data-stu-id="58d7f-249">PCI\_BUS\_RESPONDER\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="58d7f-250"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-250"><dt>256 (0x100)</dt></span></span> </dl>  | <span data-ttu-id="58d7f-251">Die PCI- \_ \_ busziel- \_ ID ist gültig.</span><span class="sxs-lookup"><span data-stu-id="58d7f-251">PCI\_BUS\_TARGET\_ID is valid.</span></span><br/>        |
| <dl> <span data-ttu-id="58d7f-252"><dt>512 (0x200)</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-252"><dt>512 (0x200)</dt></span></span> </dl>  | <span data-ttu-id="58d7f-253">Die OEM-ID des PCI- \_ Busses \_ \_ ist gültig.</span><span class="sxs-lookup"><span data-stu-id="58d7f-253">PCI\_BUS\_OEM\_ID is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="58d7f-254"><dt>1024 (0x400)</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-254"><dt>1024 (0x400)</dt></span></span> </dl> | <span data-ttu-id="58d7f-255">Die \_ OEM-Datenstruktur des PCI-Busses \_ \_ \_ ist gültig.</span><span class="sxs-lookup"><span data-stu-id="58d7f-255">PCI\_BUS\_OEM\_DATA\_STRUCT is valid.</span></span><br/> |



 

<span data-ttu-id="58d7f-256">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58d7f-256">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58d7f-257">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58d7f-257">Remarks</span></span>

<span data-ttu-id="58d7f-258">Die **msmcaevent \_ pcibuserror** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="58d7f-258">The **MSMCAEvent\_PCIBusError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58d7f-259">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58d7f-259">Requirements</span></span>



| <span data-ttu-id="58d7f-260">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58d7f-260">Requirement</span></span> | <span data-ttu-id="58d7f-261">Wert</span><span class="sxs-lookup"><span data-stu-id="58d7f-261">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58d7f-262">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58d7f-262">Minimum supported client</span></span><br/> | <span data-ttu-id="58d7f-263">Windows XP</span><span class="sxs-lookup"><span data-stu-id="58d7f-263">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="58d7f-264">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58d7f-264">Minimum supported server</span></span><br/> | <span data-ttu-id="58d7f-265">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="58d7f-265">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="58d7f-266">Namespace</span><span class="sxs-lookup"><span data-stu-id="58d7f-266">Namespace</span></span><br/>                | <span data-ttu-id="58d7f-267">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="58d7f-267">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="58d7f-268">MOF</span><span class="sxs-lookup"><span data-stu-id="58d7f-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58d7f-269"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-269"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="58d7f-270">DLL</span><span class="sxs-lookup"><span data-stu-id="58d7f-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58d7f-271"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58d7f-271"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58d7f-272">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58d7f-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d7f-273">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="58d7f-273">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="58d7f-274">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="58d7f-274">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

