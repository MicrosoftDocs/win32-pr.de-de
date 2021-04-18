---
description: Stellt den allgemeinen Header dar, der von allen msmcaevent-Klassen verwendet wird. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: MSMCAEvent_Header-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_Header
- MSMCAEvent_Header.AdditionalErrors
- MSMCAEvent_Header.Cpu
- MSMCAEvent_Header.ErrorSeverity
- MSMCAEvent_Header.RecordId
- MSMCAEvent_Header.Type
- MSMCAEvent_Header.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 426f943014f3b6cfbdba5a25d331c0ea621048cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352228"
---
# <a name="msmcaevent_header-class"></a><span data-ttu-id="9803b-104">Msmcaevent- \_ Header Klasse</span><span class="sxs-lookup"><span data-stu-id="9803b-104">MSMCAEvent\_Header class</span></span>

<span data-ttu-id="9803b-105">Die **msmcaevent- \_ Header** Klasse stellt den allgemeinen Header dar, der von allen [MSMCA-Klassen](msmca-classes.md) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9803b-105">The **MSMCAEvent\_Header** class represents the common header that all [MSMCA classes](msmca-classes.md) use.</span></span> <span data-ttu-id="9803b-106">Die Header Dateien werden verwendet, sodass C-und C++-Code über eine Datenstruktur verfügen können, die den allgemeinen Header für alle Ereignisse beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9803b-106">The header files are used so that C and C++ code can have a data structure that describes the common header for all events.</span></span> <span data-ttu-id="9803b-107">Diese Klasse ist für die interne Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9803b-107">This class is reserved for internal use.</span></span> <span data-ttu-id="9803b-108">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9803b-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="9803b-109">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9803b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9803b-110">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="9803b-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9803b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9803b-111">Syntax</span></span>

``` syntax
class MSMCAEvent_Header
{
  uint32 AdditionalErrors;
  uint32 Cpu;
  uint8  ErrorSeverity;
  uint64 RecordId;
  uint32 Type;
  uint32 LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="9803b-112">Member</span><span class="sxs-lookup"><span data-stu-id="9803b-112">Members</span></span>

<span data-ttu-id="9803b-113">Die **msmcaevent- \_ Header** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9803b-113">The **MSMCAEvent\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="9803b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9803b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9803b-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9803b-115">Properties</span></span>

<span data-ttu-id="9803b-116">Die **msmcaevent- \_ Header** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9803b-116">The **MSMCAEvent\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9803b-117">**Additionalerrors**</span><span class="sxs-lookup"><span data-stu-id="9803b-117">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9803b-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9803b-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9803b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9803b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9803b-120">Anzahl zusätzlicher Fehler im MCA-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="9803b-120">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="9803b-121">**CPU**</span><span class="sxs-lookup"><span data-stu-id="9803b-121">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9803b-122">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9803b-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9803b-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9803b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9803b-124">CPU, die den Fehler meldet.</span><span class="sxs-lookup"><span data-stu-id="9803b-124">CPU that reports the error.</span></span> <span data-ttu-id="9803b-125">Diese Eigenschaft gilt nur für ein Multiprozessorsystem, dem dem ersten Prozessor die Zahl 0 zugewiesen ist, dem zweiten Prozessor die Zahl 1 zugewiesen wird usw.</span><span class="sxs-lookup"><span data-stu-id="9803b-125">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="9803b-126">**Errorschwere Grad**</span><span class="sxs-lookup"><span data-stu-id="9803b-126">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9803b-127">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9803b-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9803b-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9803b-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9803b-129">Der Schweregrad des gemeldeten Fehlers.</span><span class="sxs-lookup"><span data-stu-id="9803b-129">Severity level of the error reported.</span></span>



| <span data-ttu-id="9803b-130">Wert</span><span class="sxs-lookup"><span data-stu-id="9803b-130">Value</span></span>                                                                                                | <span data-ttu-id="9803b-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9803b-131">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="9803b-132"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="9803b-132"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="9803b-133">Wiederherstellbar</span><span class="sxs-lookup"><span data-stu-id="9803b-133">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="9803b-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9803b-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9803b-135">FAT</span><span class="sxs-lookup"><span data-stu-id="9803b-135">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="9803b-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9803b-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9803b-137">KORRIGIER barer</span><span class="sxs-lookup"><span data-stu-id="9803b-137">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9803b-138">**Logtoeventlog**</span><span class="sxs-lookup"><span data-stu-id="9803b-138">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9803b-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9803b-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9803b-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9803b-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9803b-141">Wenn 0 (null) ist, wird dieses Ereignis nicht im System Ereignisprotokoll protokolliert.</span><span class="sxs-lookup"><span data-stu-id="9803b-141">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="9803b-142">**Datensatz**</span><span class="sxs-lookup"><span data-stu-id="9803b-142">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9803b-143">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9803b-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9803b-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9803b-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9803b-145">Datensatz-ID des Fehler Datensatzes für diesen Fehler.</span><span class="sxs-lookup"><span data-stu-id="9803b-145">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="9803b-146">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9803b-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9803b-147">**Type**</span><span class="sxs-lookup"><span data-stu-id="9803b-147">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9803b-148">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9803b-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9803b-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9803b-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9803b-150">Der Typ der Ereignisprotokoll Meldung.</span><span class="sxs-lookup"><span data-stu-id="9803b-150">Type of event log message.</span></span> <span data-ttu-id="9803b-151">Diese Meldungen entsprechen den Ereignisprotokoll-Nachrichten Codes, die zum Einfügen von Ereignisprotokoll Meldungen vom Windows-Ereignisprotokoll-Consumeranbieter verwendet werden, wenn ein Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="9803b-151">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9803b-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9803b-152">Requirements</span></span>



| <span data-ttu-id="9803b-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9803b-153">Requirement</span></span> | <span data-ttu-id="9803b-154">Wert</span><span class="sxs-lookup"><span data-stu-id="9803b-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9803b-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9803b-155">Minimum supported client</span></span><br/> | <span data-ttu-id="9803b-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9803b-156">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="9803b-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9803b-157">Minimum supported server</span></span><br/> | <span data-ttu-id="9803b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9803b-158">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="9803b-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="9803b-159">Namespace</span></span><br/>                | <span data-ttu-id="9803b-160">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="9803b-160">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="9803b-161">MOF</span><span class="sxs-lookup"><span data-stu-id="9803b-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9803b-162"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9803b-162"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9803b-163">DLL</span><span class="sxs-lookup"><span data-stu-id="9803b-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9803b-164"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9803b-164"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9803b-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9803b-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9803b-166">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="9803b-166">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="9803b-167">WMI-C++-Klassen</span><span class="sxs-lookup"><span data-stu-id="9803b-167">WMI C++ Classes</span></span>](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

