---
description: Meldet ein instanzänderungsereignis, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das beim Ändern einer Instanz im Namespace generiert wird.
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: __InstanceModificationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866904"
---
# <a name="__instancemodificationevent-class"></a><span data-ttu-id="e2561-103">\_\_Instancemodificationevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2561-103">\_\_InstanceModificationEvent class</span></span>

<span data-ttu-id="e2561-104">Die **\_ \_ instancemodificationevent** -System Klasse meldet ein instanzänderungsereignis, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das beim Ändern einer Instanz im-Namespace generiert wird.</span><span class="sxs-lookup"><span data-stu-id="e2561-104">The **\_\_InstanceModificationEvent** system class reports an instance modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance changes in the namespace.</span></span>

<span data-ttu-id="e2561-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e2561-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e2561-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e2561-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2561-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2561-107">Syntax</span></span>

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="e2561-108">Member</span><span class="sxs-lookup"><span data-stu-id="e2561-108">Members</span></span>

<span data-ttu-id="e2561-109">Die **\_ \_ instancemodificationevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e2561-109">The **\_\_InstanceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="e2561-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2561-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2561-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2561-111">Properties</span></span>

<span data-ttu-id="e2561-112">Die **\_ \_ instancemodificationevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e2561-112">The **\_\_InstanceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2561-113">**PreviousInstance**</span><span class="sxs-lookup"><span data-stu-id="e2561-113">**PreviousInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2561-114">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="e2561-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e2561-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2561-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2561-116">Kopie der Instanz vor der Änderung.</span><span class="sxs-lookup"><span data-stu-id="e2561-116">Copy of the instance prior to modification.</span></span>

</dd> <dt>

<span data-ttu-id="e2561-117">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2561-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2561-118">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="e2561-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e2561-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2561-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2561-120">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="e2561-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="e2561-121">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2561-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2561-122">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="e2561-122">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2561-123">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="e2561-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e2561-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2561-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2561-125">Neue Version der geänderten Instanz.</span><span class="sxs-lookup"><span data-stu-id="e2561-125">New version of the changed instance.</span></span> <span data-ttu-id="e2561-126">Diese Eigenschaft wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2561-126">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2561-127">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="e2561-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2561-128">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2561-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2561-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2561-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2561-130">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e2561-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="e2561-131">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2561-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="e2561-132">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="e2561-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="e2561-133">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2561-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="e2561-134">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e2561-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2561-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2561-135">Remarks</span></span>

<span data-ttu-id="e2561-136">Die **\_ \_ instancemodificationevent** -Klasse wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e2561-136">The **\_\_InstanceModificationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="e2561-137">**Änderung einer Ressource: \_ \_ instancemodificationevent**</span><span class="sxs-lookup"><span data-stu-id="e2561-137">**Modification of a resource: \_\_InstanceModificationEvent**</span></span>

<span data-ttu-id="e2561-138">Angenommen, Sie vermuten, dass eine von Ihnen verwendete Verwaltungs Anwendung fälschlicherweise den Starttyp eines Diensts auf einem der Server ändert.</span><span class="sxs-lookup"><span data-stu-id="e2561-138">Suppose you suspect that a management application you are using is erroneously changing the startup type of a service on one of your servers.</span></span> <span data-ttu-id="e2561-139">Sie möchten ein WMI-Skript schreiben, um Änderungen zu überwachen, die an der Konfiguration des Dienstanbieter vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="e2561-139">You want to write a WMI script to monitor any modifications made to the configuration of the service.</span></span> <span data-ttu-id="e2561-140">Sobald eine Änderung an einem Dienst vorgenommen wird, spiegelt die zugehörige TargetInstance die Änderung wider.</span><span class="sxs-lookup"><span data-stu-id="e2561-140">As soon as a modification is made to a service, its corresponding TargetInstance reflects the modification.</span></span>

<span data-ttu-id="e2561-141">Wenn Sie Ihr Interesse bei diesem Ereignis registrieren, führt eine Änderung an der Konfiguration des dienstantrags zur Erstellung einer Instanz der **\_ \_ instancemodificationevent** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="e2561-141">If you register your interest in this event, a modification to the configuration of the service results in the creation of an instance of the **\_\_InstanceModificationEvent** class.</span></span>

<span data-ttu-id="e2561-142">Benachrichtigungs Abfragen, die eine Benachrichtigung über die Änderung einer Ressource anfordern und intrinsische Ereignisse verwenden, verwenden alle eine Syntax, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="e2561-142">Notification queries that request notification of the modification of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a><span data-ttu-id="e2561-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2561-143">Examples</span></span>

<span data-ttu-id="e2561-144">Das Beispiel [Monitor Process modificationevent](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) VBScript in der TechNet Gallery verwendet **\_ \_ instancemodificationevent** , um das erste Vorkommen eines WMI-instanzänderungsereignisses für den [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process)zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="e2561-144">The [Monitor process modification event](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) VBScript sample on TechNet Gallery uses **\_\_InstanceModificationEvent** to monitor the first occurrence of a WMI instance modification event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2561-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2561-145">Requirements</span></span>



| <span data-ttu-id="e2561-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2561-146">Requirement</span></span> | <span data-ttu-id="e2561-147">Wert</span><span class="sxs-lookup"><span data-stu-id="e2561-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e2561-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2561-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e2561-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2561-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e2561-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2561-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e2561-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2561-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e2561-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2561-152">Namespace</span></span><br/>                | <span data-ttu-id="e2561-153">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="e2561-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e2561-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2561-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2561-155">**\_\_Instanceoperationevent**</span><span class="sxs-lookup"><span data-stu-id="e2561-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="e2561-156">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="e2561-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

