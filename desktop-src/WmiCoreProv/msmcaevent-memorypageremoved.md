---
description: Gibt an, dass eine Speicherseite aufgrund übermäßiger Fehler bei der Hardwarefehler Überprüfung und-Korrektur (ECC) aus der System Verwendung entfernt wurde. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 364a2520-8d7c-44f2-95f6-eea9a5531975
title: MSMCAEvent_MemoryPageRemoved-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryPageRemoved
- MSMCAEvent_MemoryPageRemoved.Active
- MSMCAEvent_MemoryPageRemoved.InstanceName
- MSMCAEvent_MemoryPageRemoved.PhysicalAddress
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dc29c5b51531e204ab50f062dd08ef8d5abf1bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350841"
---
# <a name="msmcaevent_memorypageremoved-class"></a><span data-ttu-id="7ff6c-104">Msmcaevent \_ memorypageremoved-Klasse</span><span class="sxs-lookup"><span data-stu-id="7ff6c-104">MSMCAEvent\_MemoryPageRemoved class</span></span>

<span data-ttu-id="7ff6c-105">Die Klasse " **msmcaevent \_ memorypageremoved** " gibt an, dass eine Speicherseite aufgrund übermäßiger Fehler bei der Überprüfung und Korrektur von Hardwarefehlern aus der Verwendung des Systems entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ff6c-105">The **MSMCAEvent\_MemoryPageRemoved** class indicates that a memory page has been removed from system use due to excessive hardware Error Checking and Correcting (ECC) errors.</span></span> <span data-ttu-id="7ff6c-106">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7ff6c-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="7ff6c-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ff6c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7ff6c-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="7ff6c-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff6c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ff6c-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryPageRemoved : WmiEvent
{
  boolean Active;
  string  InstanceName;
  uint64  PhysicalAddress;
};
```

## <a name="members"></a><span data-ttu-id="7ff6c-110">Member</span><span class="sxs-lookup"><span data-stu-id="7ff6c-110">Members</span></span>

<span data-ttu-id="7ff6c-111">Die Klasse " **msmcaevent \_ memorypageremoved** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7ff6c-111">The **MSMCAEvent\_MemoryPageRemoved** class has these types of members:</span></span>

-   [<span data-ttu-id="7ff6c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7ff6c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ff6c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7ff6c-113">Properties</span></span>

<span data-ttu-id="7ff6c-114">Die Klasse " **msmcaevent \_ memorypageremoved** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ff6c-114">The **MSMCAEvent\_MemoryPageRemoved** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ff6c-115">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="7ff6c-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ff6c-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7ff6c-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ff6c-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ff6c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ff6c-118">**True**, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="7ff6c-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7ff6c-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="7ff6c-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ff6c-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ff6c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ff6c-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ff6c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ff6c-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7ff6c-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7ff6c-123">Eindeutiger Bezeichner für diese Instanz der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="7ff6c-123">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="7ff6c-124">**PhysicalAddress**</span><span class="sxs-lookup"><span data-stu-id="7ff6c-124">**PhysicalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ff6c-125">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7ff6c-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7ff6c-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ff6c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ff6c-127">Die Adresse der Arbeitsspeicher Seite, die entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ff6c-127">Address of the page of memory that has been removed.</span></span>

<span data-ttu-id="7ff6c-128">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7ff6c-128">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ff6c-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ff6c-129">Remarks</span></span>

<span data-ttu-id="7ff6c-130">Die Klasse " **msmcaevent \_ memorypageremoved** " wird von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7ff6c-130">The **MSMCAEvent\_MemoryPageRemoved** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff6c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ff6c-131">Requirements</span></span>



| <span data-ttu-id="7ff6c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ff6c-132">Requirement</span></span> | <span data-ttu-id="7ff6c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7ff6c-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff6c-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ff6c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff6c-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7ff6c-135">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="7ff6c-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ff6c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff6c-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7ff6c-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="7ff6c-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ff6c-138">Namespace</span></span><br/>                | <span data-ttu-id="7ff6c-139">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="7ff6c-139">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="7ff6c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7ff6c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ff6c-141"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7ff6c-141"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ff6c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7ff6c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ff6c-143"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ff6c-143"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ff6c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ff6c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff6c-145">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="7ff6c-145">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="7ff6c-146">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="7ff6c-146">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

