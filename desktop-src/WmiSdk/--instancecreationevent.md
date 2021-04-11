---
description: Meldet ein instanzerstellungs-Ereignis, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das generiert wird, wenn dem Namespace eine neue Instanz hinzugefügt wird.
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: __InstanceCreationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217975"
---
# <a name="__instancecreationevent-class"></a><span data-ttu-id="ffc43-103">\_\_Instancecreationevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="ffc43-103">\_\_InstanceCreationEvent class</span></span>

<span data-ttu-id="ffc43-104">Die **\_ \_ instancecreationevent** -System Klasse meldet ein instanzerstellungs Ereignis, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das generiert wird, wenn dem Namespace eine neue Instanz hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ffc43-104">The **\_\_InstanceCreationEvent** system class reports an instance creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a new instance is added to the namespace.</span></span>

<span data-ttu-id="ffc43-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ffc43-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ffc43-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ffc43-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc43-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffc43-107">Syntax</span></span>

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="ffc43-108">Member</span><span class="sxs-lookup"><span data-stu-id="ffc43-108">Members</span></span>

<span data-ttu-id="ffc43-109">Die **\_ \_ instancecreationevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ffc43-109">The **\_\_InstanceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ffc43-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ffc43-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffc43-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ffc43-111">Properties</span></span>

<span data-ttu-id="ffc43-112">Die **\_ \_ instancecreationevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ffc43-112">The **\_\_InstanceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ffc43-113">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffc43-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc43-114">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="ffc43-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ffc43-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ffc43-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffc43-116">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="ffc43-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="ffc43-117">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ffc43-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffc43-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="ffc43-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc43-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="ffc43-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ffc43-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ffc43-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffc43-121">Kopie der erstellten Instanz.</span><span class="sxs-lookup"><span data-stu-id="ffc43-121">Copy of the instance that was created.</span></span> <span data-ttu-id="ffc43-122">Diese Eigenschaft wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ffc43-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffc43-123">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="ffc43-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffc43-124">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ffc43-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ffc43-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ffc43-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffc43-126">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ffc43-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="ffc43-127">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="ffc43-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="ffc43-128">Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor.</span><span class="sxs-lookup"><span data-stu-id="ffc43-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="ffc43-129">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ffc43-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="ffc43-130">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ffc43-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffc43-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffc43-131">Remarks</span></span>

<span data-ttu-id="ffc43-132">Die **\_ \_ instancecreationevent** -Klasse wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ffc43-132">The **\_\_InstanceCreationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="ffc43-133">**Erstellung einer Ressource: \_ \_ instancecreationevent**</span><span class="sxs-lookup"><span data-stu-id="ffc43-133">**Creation of a resource: \_\_InstanceCreationEvent**</span></span>

<span data-ttu-id="ffc43-134">Angenommen, Sie möchten eine Benachrichtigung erhalten, wenn Notepad auf einem bestimmten Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffc43-134">Suppose you are interested in receiving a notification if Notepad is run on a certain computer.</span></span> <span data-ttu-id="ffc43-135">Wenn Notepad ausgeführt wird, wird ein entsprechender Prozess erstellt.</span><span class="sxs-lookup"><span data-stu-id="ffc43-135">When Notepad runs, a corresponding process is created.</span></span> <span data-ttu-id="ffc43-136">Prozesse können mithilfe von WMI verwaltet werden und werden durch die Win32- \_ Prozess Klasse dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ffc43-136">Processes can be managed by using WMI and are represented by the Win32\_Process class.</span></span> <span data-ttu-id="ffc43-137">Wenn Notepad gestartet wird, wird eine entsprechende Instanz der Win32- \_ Prozess Klasse über WMI verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ffc43-137">When Notepad starts running, a corresponding instance of the Win32\_Process class becomes available through WMI.</span></span> <span data-ttu-id="ffc43-138">Wenn Sie Ihr Interesse an diesem Ereignis registriert haben (indem Sie die entsprechende Ereignis Benachrichtigungs Abfrage ausgeben), führt die Verfügbarkeit dieser Instanz zur Erstellung einer Instanz der **\_ \_ instancecreationevent** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="ffc43-138">If you have registered your interest in this event (by issuing the appropriate event notification query), the availability of this instance results in the creation of an instance of the **\_\_InstanceCreationEvent** class.</span></span>

<span data-ttu-id="ffc43-139">Benachrichtigungs Abfragen, die eine Benachrichtigung über die Erstellung einer Ressource anfordern und systeminterne Ereignisse verwenden, verwenden alle eine Syntax ähnlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="ffc43-139">Notification queries that request notification of the creation of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

<span data-ttu-id="ffc43-140">Eine ausführlichere Erläuterung der Verwendung von **\_ \_ instancecreationevent** als Möglichkeit zum Überwachen von Dateisystemen finden Sie unter [WMI und Datei System Überwachung](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) für Code Project.</span><span class="sxs-lookup"><span data-stu-id="ffc43-140">For a larger discussion of using **\_\_InstanceCreationEvent** as a way to monitor file systems, see [WMI and File System Monitoring](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) on CodeProject.</span></span>

## <a name="examples"></a><span data-ttu-id="ffc43-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ffc43-141">Examples</span></span>

<span data-ttu-id="ffc43-142">Das PowerShell-Beispiel zur [Erstellung dauerhafter WMI-Ereignis Registrierung zum Überwachen von Dateien](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) in der TechNet Gallery verwendet **\_ \_ instancecreationevent** als Teil eines komplexen Skripts, um eine permanente WMI-Ereignis Registrierung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="ffc43-142">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a complex script to set up a permanent WMI event registration.</span></span>

<span data-ttu-id="ffc43-143">Das PowerShell-Beispiel PowerShell-PowerShell für [permanente Ereignisse](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) in der TechNet Gallery verwendet **\_ \_ instancecreationevent** als Teil eines Demonstrations Skripts zum Einrichten einer permanenten Ereignis Registrierung.</span><span class="sxs-lookup"><span data-stu-id="ffc43-143">The [PowerShell WMI Permanent Events](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a demonstration script for setting up a permanent event registration.</span></span>

<span data-ttu-id="ffc43-144">Im VBScript-Beispiel für das [Monitor Prozess Erstellungs Ereignis](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) auf der TechNet-Instanz wird **\_ \_ instancecreationevent** verwendet, um das erste Ereignis Erstellungs Ereignis für [**Win32- \_ Prozesse**](/windows/desktop/CIMWin32Prov/win32-process)zu überwachen</span><span class="sxs-lookup"><span data-stu-id="ffc43-144">The [Monitor process creation event](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) VBScript sample on TechNet uses **\_\_InstanceCreationEvent** to monitors the first WMI instance creation event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffc43-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffc43-145">Requirements</span></span>



| <span data-ttu-id="ffc43-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffc43-146">Requirement</span></span> | <span data-ttu-id="ffc43-147">Wert</span><span class="sxs-lookup"><span data-stu-id="ffc43-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ffc43-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ffc43-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ffc43-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffc43-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ffc43-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ffc43-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ffc43-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffc43-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ffc43-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffc43-152">Namespace</span></span><br/>                | <span data-ttu-id="ffc43-153">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="ffc43-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ffc43-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffc43-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffc43-155">**\_\_Instanceoperationevent**</span><span class="sxs-lookup"><span data-stu-id="ffc43-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="ffc43-156">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="ffc43-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

