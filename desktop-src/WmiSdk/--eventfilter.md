---
description: Die Registrierung eines permanenten Ereignisconsumers erfordert eine Instanz der \_ \_ EventFilter-System Klasse.
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: __EventFilter-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349520"
---
# <a name="__eventfilter-class"></a><span data-ttu-id="4786b-103">\_\_EventFilter-Klasse</span><span class="sxs-lookup"><span data-stu-id="4786b-103">\_\_EventFilter class</span></span>

<span data-ttu-id="4786b-104">Die Registrierung eines permanenten **\_ \_ Ereignisconsumers** erfordert eine Instanz der EventFilter-System Klasse.</span><span class="sxs-lookup"><span data-stu-id="4786b-104">The registration of a permanent event consumer requires an instance of the **\_\_EventFilter** system class.</span></span>

<span data-ttu-id="4786b-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="4786b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4786b-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4786b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4786b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4786b-107">Syntax</span></span>

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a><span data-ttu-id="4786b-108">Member</span><span class="sxs-lookup"><span data-stu-id="4786b-108">Members</span></span>

<span data-ttu-id="4786b-109">Die **\_ \_ EventFilter** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4786b-109">The **\_\_EventFilter** class has these types of members:</span></span>

-   [<span data-ttu-id="4786b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4786b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4786b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4786b-111">Properties</span></span>

<span data-ttu-id="4786b-112">Die **\_ \_ EventFilter** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4786b-112">The **\_\_EventFilter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4786b-113">**"Kreatorsid"**</span><span class="sxs-lookup"><span data-stu-id="4786b-113">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4786b-114">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="4786b-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4786b-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4786b-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4786b-116">Sicherheits-ID (SID), die den Benutzer, der diesen Filter erstellt, eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4786b-116">Security identifier (SID) that uniquely identifies the user who creates this filter.</span></span> <span data-ttu-id="4786b-117">Windows-Verwaltungsinstrumentation (WMI) speichert die SID des Benutzers, der eine Instanz von **\_ \_ EventFilter** oder die Administrator-SID erstellt, je nach Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="4786b-117">Windows Management Instrumentation (WMI) stores the SID of the user that creates an instance of **\_\_EventFilter** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="4786b-118">Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="4786b-118">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="4786b-119">**Eventaccess**</span><span class="sxs-lookup"><span data-stu-id="4786b-119">**EventAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4786b-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4786b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4786b-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4786b-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4786b-122">Sicherheits Beschreibung (SD) in Security Deskriptor Definition Language (SDDL), die den Zugriff auf Ereignisse steuert, die an den Filter übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="4786b-122">Security descriptor (SD) in Security Descriptor Definition Language (SDDL) that controls access for events delivered to the filter.</span></span> <span data-ttu-id="4786b-123">Verwenden Sie diese Eigenschaft, um anzugeben, dass nur Ereignisse im Sicherheitskontext bestimmter Konten an diesen Filter übermittelt werden können.</span><span class="sxs-lookup"><span data-stu-id="4786b-123">Use this property to specify that only events in the security context of specific accounts can be delivered to this filter.</span></span> <span data-ttu-id="4786b-124">Beispielsweise kann ein dauerhafter Ereignisconsumer die Sicherheitsprotokolle nur dann löschen, wenn ein bestimmtes Ereignis von einem bestimmten Benutzer generiert wird.</span><span class="sxs-lookup"><span data-stu-id="4786b-124">For example, a permanent event consumer may clear the security logs only when a specific event is generated by a specific user.</span></span> <span data-ttu-id="4786b-125">Um anzugeben, wer Ereignisse in diesem Filter veröffentlichen kann, verwenden Sie die **WBEM \_ right- \_ Veröffentlichungs** Maske im Access Control Entry (ACE) für die [**\_ sicherheitsbeschreibungenschaft**](--event.md) .</span><span class="sxs-lookup"><span data-stu-id="4786b-125">To specify who can publish events to this filter, use the **WBEM\_RIGHT\_PUBLISH** mask in the Access Control Entry (ACE) for the [**SECURITY\_DESCRIPTOR**](--event.md) property.</span></span> <span data-ttu-id="4786b-126">Weitere Informationen finden Sie unter [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span><span class="sxs-lookup"><span data-stu-id="4786b-126">For more information, see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span> <span data-ttu-id="4786b-127">Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4786b-127">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span> <span data-ttu-id="4786b-128">Weitere Informationen und Beispiele finden Sie unter ersetzen:[sicheres empfangen von Ereignissen](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="4786b-128">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="4786b-129">Sie können einen Sicherheits Deskriptor für den Ereignis Zugriff konfigurieren, um zuzulassen, dass ein Ereignis nur dann übermittelt wird, wenn das lokale Systemkonto das Ereignis generiert.</span><span class="sxs-lookup"><span data-stu-id="4786b-129">You can configure an event access security descriptor to allow an event to be delivered only when the local system account generates the event.</span></span> <span data-ttu-id="4786b-130">Weitere Informationen zum Erstellen einer Sicherheits Beschreibung und zum Autorisierungs Zugriff finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="4786b-130">For more information about creating security descriptor and authorizing access, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="4786b-131">Beispiel: mit der folgenden SDDL-Zeichenfolge können nur Administratoren Ereignisse für den Filter bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4786b-131">Example: The following SDDL string allows only administrators to provide events to the filter.</span></span> <span data-ttu-id="4786b-132">Die zum Bereitstellen von Ereignissen erforderliche Berechtigung ist **WBEM \_ right \_ Publish** (x80).</span><span class="sxs-lookup"><span data-stu-id="4786b-132">The right required to provide events is **WBEM\_RIGHT\_PUBLISH** (x80).</span></span>


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

<span data-ttu-id="4786b-133">**Eventnamespace**</span><span class="sxs-lookup"><span data-stu-id="4786b-133">**EventNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4786b-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4786b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4786b-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4786b-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4786b-136">Namespace der Ereignis Instanz, die für Namespace übergreifende Abonnements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4786b-136">Namespace of the event instance used for cross-namespace subscriptions.</span></span>

</dd> <dt>

<span data-ttu-id="4786b-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="4786b-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4786b-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4786b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4786b-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4786b-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4786b-140">Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="4786b-140">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="4786b-141">Eindeutiger Bezeichner eines Ereignis Filters.</span><span class="sxs-lookup"><span data-stu-id="4786b-141">Unique identifier of an event filter.</span></span> <span data-ttu-id="4786b-142">Da ein Ereignis Filter nur intern von WMI verwendet wird, empfiehlt es sich, diese Eigenschaft auf eine in eine Zeichenfolge konvertierte Globally Unique Identifier (**GUID**) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4786b-142">Because an event filter is only used internally by WMI, it is recommended that you set this property to a globally unique identifier (**GUID**) converted to a string.</span></span> <span data-ttu-id="4786b-143">Consumer können jedoch ein beliebiges privates Schema für einen Filternamen verwenden, solange kein Konflikt mit anderen Filtern vorliegt.</span><span class="sxs-lookup"><span data-stu-id="4786b-143">However, consumers can use any private scheme for a filter name as long as there is not a conflict with other filters.</span></span>

</dd> <dt>

<span data-ttu-id="4786b-144">**Abfrage**</span><span class="sxs-lookup"><span data-stu-id="4786b-144">**Query**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4786b-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4786b-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4786b-146">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4786b-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4786b-147">Die WQL-Ereignis Abfrage (Windows-Verwaltungsinstrumentation Query Language), die den Satz von Ereignissen für die Consumer-Benachrichtigung angibt, sowie die spezifischen Benachrichtigungs Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="4786b-147">Windows Management Instrumentation Query Language (WQL) event query that specifies the set of events for consumer notification, and the specific conditions for notification.</span></span>

</dd> <dt>

<span data-ttu-id="4786b-148">**QueryLanguage**</span><span class="sxs-lookup"><span data-stu-id="4786b-148">**QueryLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4786b-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4786b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4786b-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4786b-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4786b-151">Sprache, die für die Abfrage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4786b-151">Language used for the query.</span></span> <span data-ttu-id="4786b-152">Da WMI derzeit nur WMI Query Language (WQL) als Abfragesprache unterstützt, muss diese Eigenschaft auf "WQL" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4786b-152">Because WMI currently supports only WMI Query Language (WQL) as a query language, this property must be set to "WQL".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4786b-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4786b-153">Remarks</span></span>

<span data-ttu-id="4786b-154">Die **\_ \_ EventFilter** -Klasse wird von " [**\_ \_ bezeichationrelated**](--indicationrelated.md)" abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4786b-154">The **\_\_EventFilter** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4786b-155">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4786b-155">Examples</span></span>

<span data-ttu-id="4786b-156">Das PowerShell-Beispiel zum [Erstellen einer permanenten WMI-Ereignis Registrierung zum Überwachen von Dateien](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) in der TechNet Gallery verwendet **\_ \_ EventFilter** als Teil eines komplexen Skripts, um eine permanente WMI-Ereignis Registrierung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="4786b-156">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_EventFilter** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="4786b-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4786b-157">Requirements</span></span>



| <span data-ttu-id="4786b-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4786b-158">Requirement</span></span> | <span data-ttu-id="4786b-159">Wert</span><span class="sxs-lookup"><span data-stu-id="4786b-159">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4786b-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4786b-160">Minimum supported client</span></span><br/> | <span data-ttu-id="4786b-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4786b-161">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4786b-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4786b-162">Minimum supported server</span></span><br/> | <span data-ttu-id="4786b-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4786b-163">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4786b-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="4786b-164">Namespace</span></span><br/>                | <span data-ttu-id="4786b-165">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="4786b-165">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4786b-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4786b-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4786b-167">**\_\_Indicationrelated**</span><span class="sxs-lookup"><span data-stu-id="4786b-167">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="4786b-168">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="4786b-168">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4786b-169">Erstellen eines Ereignis Filters</span><span class="sxs-lookup"><span data-stu-id="4786b-169">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="4786b-170">Empfangen von Ereignissen zu allen Zeitpunkten</span><span class="sxs-lookup"><span data-stu-id="4786b-170">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="4786b-171">Überwachen von und reagieren auf Ereignisse mit Standard Consumern</span><span class="sxs-lookup"><span data-stu-id="4786b-171">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="4786b-172">Überwachen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="4786b-172">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="4786b-173">Standard Consumer-Klassen</span><span class="sxs-lookup"><span data-stu-id="4786b-173">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="4786b-174">Sichern von WMI-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="4786b-174">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

