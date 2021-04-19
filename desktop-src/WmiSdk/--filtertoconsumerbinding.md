---
description: Wird bei der Registrierung von permanenten Ereignisconsumern verwendet, um eine Instanz von \_ \_ eventconsumer mit einer Instanz von \_ \_ EventFilter zu verknüpfen.
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: __FilterToConsumerBinding-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
- All
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
ms.openlocfilehash: 0fd9b7f3cf60d14d27fdf5b5014b57e6f599d67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355366"
---
# <a name="__filtertoconsumerbinding-class"></a><span data-ttu-id="189f0-103">\_\_Filtertoconsumerbinding-Klasse</span><span class="sxs-lookup"><span data-stu-id="189f0-103">\_\_FilterToConsumerBinding class</span></span>

<span data-ttu-id="189f0-104">Die System Klasse **\_ \_ filtertoconsumerbinding** wird bei der Registrierung von permanenten Ereignisconsumer verwendet, um eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) mit einer Instanz von [**\_ \_ EventFilter**](--eventfilter.md)zu verknüpfen.**\_ \_ "Filtertoconsumerbinding** " ist eine Association-Klasse.</span><span class="sxs-lookup"><span data-stu-id="189f0-104">The **\_\_FilterToConsumerBinding** system class is used in the registration of permanent event consumers to relate an instance of the [**\_\_EventConsumer**](--eventconsumer.md) to an instance of [**\_\_EventFilter**](--eventfilter.md).**\_\_FilterToConsumerBinding** is an association class.</span></span>

<span data-ttu-id="189f0-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="189f0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="189f0-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="189f0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="189f0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="189f0-107">Syntax</span></span>

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a><span data-ttu-id="189f0-108">Member</span><span class="sxs-lookup"><span data-stu-id="189f0-108">Members</span></span>

<span data-ttu-id="189f0-109">Die **\_ \_ filtertoconsumerbinding** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="189f0-109">The **\_\_FilterToConsumerBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="189f0-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="189f0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="189f0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="189f0-111">Properties</span></span>

<span data-ttu-id="189f0-112">Die **\_ \_ filtertoconsumerbinding** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="189f0-112">The **\_\_FilterToConsumerBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="189f0-113">**Consumer**</span><span class="sxs-lookup"><span data-stu-id="189f0-113">**Consumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="189f0-114">Datentyp: **\_ \_ eventconsumer**</span><span class="sxs-lookup"><span data-stu-id="189f0-114">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="189f0-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="189f0-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="189f0-116">Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="189f0-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="189f0-117">Verweis auf eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) , die den Objekt Pfad zu einem logischen Consumer, den Empfänger eines Ereignisses, darstellt.</span><span class="sxs-lookup"><span data-stu-id="189f0-117">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the object path to a logical consumer, the recipient of an event.</span></span> <span data-ttu-id="189f0-118">Ein logischer Consumer ist eine Instanz einer Klasse, die von **\_ \_ eventconsumer** abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="189f0-118">A logical consumer is an instance of a class derived from **\_\_EventConsumer**.</span></span>

</dd> <dt>

<span data-ttu-id="189f0-119">**"Kreatorsid"**</span><span class="sxs-lookup"><span data-stu-id="189f0-119">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="189f0-120">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="189f0-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="189f0-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="189f0-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="189f0-122">Sicherheits-ID (SID), die den Benutzer eindeutig identifiziert, der die Bindung erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="189f0-122">Security identifier (SID) that uniquely identifies the user who created the binding.</span></span> <span data-ttu-id="189f0-123">Abhängig vom Betriebssystem speichert WMI die Administrator-SID oder die SID des Benutzers, der eine Instanz von " **\_ \_ filtertoconsumerbinding**" erstellt.</span><span class="sxs-lookup"><span data-stu-id="189f0-123">Depending on the operating system, WMI stores the Administrator SID or the SID of the user that creates an instance of **\_\_FilterToConsumerBinding**.</span></span> <span data-ttu-id="189f0-124">Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="189f0-124">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="189f0-125">**Deliversynchron**</span><span class="sxs-lookup"><span data-stu-id="189f0-125">**DeliverSynchronously**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="189f0-126">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="189f0-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="189f0-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="189f0-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="189f0-128">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="189f0-128">Obsolete.</span></span> <span data-ttu-id="189f0-129">Verwenden Sie stattdessen die Eigenschaft **deliveryqos** anstelle dieser Eigenschaft, denn wenn **deliversynchron** auf **true** festgelegt ist, überschreibt es die Einstellung der **deliveryqos** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="189f0-129">Instead use the **DeliveryQoS** property in place of this property, because if **DeliverSynchronously** is set to **True** it overrides the setting of the **DeliveryQoS** property.</span></span>

</dd> <dt>

<span data-ttu-id="189f0-130">**Deliveryqos**</span><span class="sxs-lookup"><span data-stu-id="189f0-130">**DeliveryQoS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="189f0-131">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="189f0-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="189f0-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="189f0-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="189f0-133">Quality of Service für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="189f0-133">Quality of service for a subscription.</span></span> <span data-ttu-id="189f0-134">Wenn die **deliversynchron** -Eigenschaft auf **true** festgelegt ist, überschreibt Sie die-Einstellung der **deliveryqos** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="189f0-134">If the **DeliverSynchronously** property is set to **True**, it overrides the setting of the **DeliveryQoS** property.</span></span>

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span data-ttu-id="189f0-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**Wmimsg \_ \_QoS \_ synchron markieren** (0)</span><span class="sxs-lookup"><span data-stu-id="189f0-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG\_FLAG\_QOS\_SYNCHRONOUS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="189f0-136">Synchrone Übermittlung</span><span class="sxs-lookup"><span data-stu-id="189f0-136">Synchronous delivery</span></span>

<span data-ttu-id="189f0-137">**False**.</span><span class="sxs-lookup"><span data-stu-id="189f0-137">**False**.</span></span> <span data-ttu-id="189f0-138">Das Ereignis wird synchron an den logischen Consumer übermittelt.</span><span class="sxs-lookup"><span data-stu-id="189f0-138">The event is delivered to the logical consumer synchronously.</span></span>

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span data-ttu-id="189f0-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**Wmimsg \_ Flag \_ QoS \_ Express** (1)</span><span class="sxs-lookup"><span data-stu-id="189f0-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG\_FLAG\_QOS\_EXPRESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="189f0-140">Express-Übermittlung</span><span class="sxs-lookup"><span data-stu-id="189f0-140">Express delivery</span></span>

<span data-ttu-id="189f0-141">**True**.</span><span class="sxs-lookup"><span data-stu-id="189f0-141">**True**.</span></span> <span data-ttu-id="189f0-142">Das Ereignis wird asynchron an den logischen Consumer übermittelt.</span><span class="sxs-lookup"><span data-stu-id="189f0-142">The event is delivered to the logical consumer asynchronously.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="189f0-143">**Filter**</span><span class="sxs-lookup"><span data-stu-id="189f0-143">**Filter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="189f0-144">Datentyp: **\_ \_ EventFilter**</span><span class="sxs-lookup"><span data-stu-id="189f0-144">Data type: **\_\_EventFilter**</span></span>
</dt> <dt>

<span data-ttu-id="189f0-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="189f0-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="189f0-146">Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="189f0-146">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="189f0-147">Verweis auf eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md) , die den Objekt Pfad zu einem Ereignis Filter darstellt, bei dem es sich um eine Abfrage handelt, die den Ereignistyp angibt, der empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="189f0-147">Reference to an instance of [**\_\_EventFilter**](--eventfilter.md) that represents the object path to an event filter which is a query that specifies the type of event to be received.</span></span>

</dd> <dt>

<span data-ttu-id="189f0-148">**Wart SecurityContext**</span><span class="sxs-lookup"><span data-stu-id="189f0-148">**MaintainSecurityContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="189f0-149">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="189f0-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="189f0-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="189f0-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="189f0-151">**True** gibt an, dass die Ereignisse im gleichen Sicherheitskontext übermittelt werden, in dem sich der Anbieter bei der Bereitstellung befunden hat.</span><span class="sxs-lookup"><span data-stu-id="189f0-151">If **True**, the events are delivered in the same security context that the provider was in when it provided them.</span></span>

> [!Note]  
> <span data-ttu-id="189f0-152">Nur ein Consumer, der als DLL (ein Prozess interner Consumer) implementiert ist, kann Ereignisse im Sicherheitskontext des Anbieters empfangen.</span><span class="sxs-lookup"><span data-stu-id="189f0-152">Only a consumer implemented as a DLL (an in-process consumer) can receive events in the security context of the provider.</span></span> <span data-ttu-id="189f0-153">Weitere Informationen zu Prozess internen Anbietern und zur Sicherheit finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="189f0-153">For more information about in-process providers and security, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="189f0-154">Weitere Informationen und Beispiele finden Sie unter ersetzen:[sicheres empfangen von Ereignissen](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="189f0-154">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

 

</dd> <dt>

<span data-ttu-id="189f0-155">**Slowdownproviders**</span><span class="sxs-lookup"><span data-stu-id="189f0-155">**SlowDownProviders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="189f0-156">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="189f0-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="189f0-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="189f0-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="189f0-158">**True** gibt an, dass die Anbieter verlangsamt werden, wenn dieser Consumer nicht in der Einrichtung bleiben kann.</span><span class="sxs-lookup"><span data-stu-id="189f0-158">If **True**, providers are slowed down if this consumer cannot keep up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="189f0-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="189f0-159">Remarks</span></span>

<span data-ttu-id="189f0-160">Die **\_ \_ filtertoconsumerbinding** -Klasse wird von " [**\_ \_ indicationrelated**](--indicationrelated.md)" abgeleitet, die keine Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="189f0-160">The **\_\_FilterToConsumerBinding** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="189f0-161">Permanente Ereignisconsumer verwenden die **\_ \_ filtertoconsumerbinding** -System Klasse, um Ereignis Filter an endgültige Consumer zu binden.</span><span class="sxs-lookup"><span data-stu-id="189f0-161">Permanent event consumers use the **\_\_FilterToConsumerBinding** system class to bind event filters to final consumers.</span></span> <span data-ttu-id="189f0-162">Nachdem der Filter und der Consumer zusammengebunden wurden, kann WMI Ereignisse, die mit dem Filter übereinstimmen, an den entsprechenden Consumer weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="189f0-162">After the filter and consumer are bound together, WMI can forward events that match the filter to the corresponding consumer.</span></span>

## <a name="examples"></a><span data-ttu-id="189f0-163">Beispiele</span><span class="sxs-lookup"><span data-stu-id="189f0-163">Examples</span></span>

<span data-ttu-id="189f0-164">Das PowerShell-Beispiel zur [Erstellung dauerhafter WMI-Ereignis Registrierung zum Überwachen von Dateien](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) in der TechNet Gallery verwendet **\_ \_ filtertoconsumerbinding** als Teil eines komplexen Skripts, um eine permanente WMI-Ereignis Registrierung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="189f0-164">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_FilterToConsumerBinding** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="189f0-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="189f0-165">Requirements</span></span>



| <span data-ttu-id="189f0-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="189f0-166">Requirement</span></span> | <span data-ttu-id="189f0-167">Wert</span><span class="sxs-lookup"><span data-stu-id="189f0-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="189f0-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="189f0-168">Minimum supported client</span></span><br/> | <span data-ttu-id="189f0-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="189f0-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="189f0-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="189f0-170">Minimum supported server</span></span><br/> | <span data-ttu-id="189f0-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="189f0-171">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="189f0-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="189f0-172">Namespace</span></span><br/>                | <span data-ttu-id="189f0-173">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="189f0-173">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="189f0-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="189f0-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="189f0-175">**\_\_Indicationrelated**</span><span class="sxs-lookup"><span data-stu-id="189f0-175">**\_\_IndicationRelated**</span></span>](--indicationrelated.md)
</dt> <dt>

[<span data-ttu-id="189f0-176">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="189f0-176">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="189f0-177">Überwachen von und reagieren auf Ereignisse mit Standard Consumern</span><span class="sxs-lookup"><span data-stu-id="189f0-177">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="189f0-178">Überwachen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="189f0-178">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="189f0-179">Erstellen eines Ereignis Filters</span><span class="sxs-lookup"><span data-stu-id="189f0-179">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="189f0-180">Sichern von WMI-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="189f0-180">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




