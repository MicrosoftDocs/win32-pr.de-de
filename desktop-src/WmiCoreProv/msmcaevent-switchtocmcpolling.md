---
description: Stellt die Überprüfung der korrigierten Computer Überprüfung (CMC) dar, die vom Interrupt-Treiber zum Abrufen gewechselt werden soll. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: MSMCAEvent_SwitchToCMCPolling-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f7d0d543dc36054550d4ddf6cc1a77ce80cf1647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343448"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a><span data-ttu-id="cba3d-104">Msmcaevent \_ switchdecmcabruf-Klasse</span><span class="sxs-lookup"><span data-stu-id="cba3d-104">MSMCAEvent\_SwitchToCMCPolling class</span></span>

<span data-ttu-id="cba3d-105">Die **msmcaevent \_ switchdecmcabruf** -Klasse stellt die SMTP-Verarbeitung (korrigiert Machine Check) dar, die vom Interrupt-Treiber zum Abrufen gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cba3d-105">The **MSMCAEvent\_SwitchToCMCPolling** class represents the corrected machine check (CMC) handling to be switched from the interrupt driver to polling.</span></span> <span data-ttu-id="cba3d-106">In einigen Fällen fragt der Kernel die System Abstraktionsschicht (System Abstraktion Layer, SAL) nach einem beliebigen oder korrigierten Platt Formfehler (CPE) ab, der im vorherigen Abruf Intervall aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cba3d-106">In some cases, the kernel polls the system abstraction layer (SAL) for any CMC or corrected platform error (CPE) that occurred within the previous polling interval.</span></span> <span data-ttu-id="cba3d-107">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cba3d-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="cba3d-108">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cba3d-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cba3d-109">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="cba3d-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba3d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="cba3d-110">Syntax</span></span>

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="cba3d-111">Member</span><span class="sxs-lookup"><span data-stu-id="cba3d-111">Members</span></span>

<span data-ttu-id="cba3d-112">Die **msmcaevent \_ switchtocmcabruf** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cba3d-112">The **MSMCAEvent\_SwitchToCMCPolling** class has these types of members:</span></span>

-   [<span data-ttu-id="cba3d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cba3d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cba3d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cba3d-114">Properties</span></span>

<span data-ttu-id="cba3d-115">Die **msmcaevent \_ switchdecmcabruf** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cba3d-115">The **MSMCAEvent\_SwitchToCMCPolling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cba3d-116">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="cba3d-116">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cba3d-117">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="cba3d-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cba3d-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cba3d-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cba3d-119">**True**, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="cba3d-119">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="cba3d-120">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="cba3d-120">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cba3d-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cba3d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cba3d-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cba3d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cba3d-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cba3d-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cba3d-124">Eindeutiger Bezeichner dieser Instanz der Klasse.</span><span class="sxs-lookup"><span data-stu-id="cba3d-124">Unique identifier of this instance of the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cba3d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cba3d-125">Remarks</span></span>

<span data-ttu-id="cba3d-126">Die **msmcaevent \_ switchdecmcabruf** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="cba3d-126">The **MSMCAEvent\_SwitchToCMCPolling** class is derived from [**WMIEvent**](wmievent.md).</span></span>

<span data-ttu-id="cba3d-127">Die System Abstraktionsschicht (System Abstraktion Layer, SAL) ist der Code, der auf Rom gebrannt ist, den das Betriebssystem aufruft, um Platt Form abhängige Vorgänge</span><span class="sxs-lookup"><span data-stu-id="cba3d-127">The system abstraction layer (SAL) is code burned onto ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="cba3d-128">Sie ähnelt dem BIOS auf einer x86-Plattform.</span><span class="sxs-lookup"><span data-stu-id="cba3d-128">It is similar to the BIOS on an x86 platform.</span></span> <span data-ttu-id="cba3d-129">In Fällen, in denen die Plattform keine Interrupts für den Abruf von CMC oder CPE unterstützt, ruft das Betriebssystem jede Minute ab und überprüft, ob zuvor ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cba3d-129">In cases where the platform does not support interrupts for CMC or CPE polling, the operating system polls every minute, checking if an error occurred previously.</span></span> <span data-ttu-id="cba3d-130">Wenn die Plattform Interrupts unterstützt und das Betriebssystem innerhalb einer Minute eine benutzerdefinierte Menge an CMC-oder CPE-Abruf Vorgängen erhält, deaktiviert Sie die Unterbrechung und den Abruf Vorgang.</span><span class="sxs-lookup"><span data-stu-id="cba3d-130">If the platform does support interrupts and the operating system receives a user defined amount of CMC or CPE polls within one minute, then it disables the interrupt and poll.</span></span> <span data-ttu-id="cba3d-131">Wenn der Benutzer die Anzahl der Umfragen nicht innerhalb einer Minute definiert, legt das System einen Standardwert auf 10 Umfragen pro Minute fest.</span><span class="sxs-lookup"><span data-stu-id="cba3d-131">If the user does not define the number of polls within one minute, the system sets a default to 10 polls per minute.</span></span>

## <a name="requirements"></a><span data-ttu-id="cba3d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cba3d-132">Requirements</span></span>



| <span data-ttu-id="cba3d-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cba3d-133">Requirement</span></span> | <span data-ttu-id="cba3d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="cba3d-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cba3d-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cba3d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cba3d-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cba3d-136">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="cba3d-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cba3d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cba3d-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cba3d-138">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="cba3d-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="cba3d-139">Namespace</span></span><br/>                | <span data-ttu-id="cba3d-140">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="cba3d-140">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="cba3d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="cba3d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cba3d-142"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cba3d-142"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="cba3d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cba3d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cba3d-144"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cba3d-144"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cba3d-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cba3d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba3d-146">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="cba3d-146">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="cba3d-147">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="cba3d-147">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

