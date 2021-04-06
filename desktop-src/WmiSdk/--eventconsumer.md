---
description: Eine abstrakte Basisklasse, die bei der Registrierung eines permanenten Ereignisconsumers verwendet wird.
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: __EventConsumer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b8478b76aebf293d562129d047330f33e52706b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960896"
---
# <a name="__eventconsumer-class"></a><span data-ttu-id="bbbe5-103">\_\_Eventconsumer-Klasse</span><span class="sxs-lookup"><span data-stu-id="bbbe5-103">\_\_EventConsumer class</span></span>

<span data-ttu-id="bbbe5-104">Die eventconsumer-System Klasse ist eine abstrakte Basisklasse, die bei der Registrierung eines permanenten **\_ \_ Ereignisconsumers** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-104">The **\_\_EventConsumer** system class is an abstract base class that is used in the registration of a permanent event consumer.</span></span> <span data-ttu-id="bbbe5-105">Sie können eine neue **\_ \_ ereignisconsumerklasse von eventconsumer** ableiten.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-105">You can derive a new event consumer class from **\_\_EventConsumer**.</span></span>

<span data-ttu-id="bbbe5-106">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bbbe5-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbbe5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbbe5-108">Syntax</span></span>

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a><span data-ttu-id="bbbe5-109">Member</span><span class="sxs-lookup"><span data-stu-id="bbbe5-109">Members</span></span>

<span data-ttu-id="bbbe5-110">Die **\_ \_ eventconsumer** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bbbe5-110">The **\_\_EventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="bbbe5-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bbbe5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bbbe5-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bbbe5-112">Properties</span></span>

<span data-ttu-id="bbbe5-113">Die **\_ \_ eventconsumer** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-113">The **\_\_EventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bbbe5-114">**"Kreatorsid"**</span><span class="sxs-lookup"><span data-stu-id="bbbe5-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbbe5-115">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="bbbe5-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="bbbe5-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbbe5-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbbe5-117">Sicherheits-ID (SID), die den Benutzer, der einen Filter erstellt, eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="bbbe5-118">WMI speichert die SID des Benutzers, der eine Instanz von **\_ \_ eventconsumer** oder die Administrator-SID erstellt, je nach Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-118">WMI stores the SID of the user who creates an instance of **\_\_EventConsumer** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="bbbe5-119">Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbbe5-120">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="bbbe5-120">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbbe5-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbbe5-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbbe5-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbbe5-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbbe5-123">Der Name des Computers, an den Windows-Verwaltungsinstrumentation (WMI) Ereignisse sendet.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-123">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

</dd> <dt>

<span data-ttu-id="bbbe5-124">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="bbbe5-124">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbbe5-125">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbbe5-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbbe5-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbbe5-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbbe5-127">Maximale Warteschlange für einen bestimmten Consumer in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-127">Maximum queue for a specific consumer, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bbbe5-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbbe5-128">Remarks</span></span>

<span data-ttu-id="bbbe5-129">Die **\_ \_ eventconsumer** -Klasse wird von " [**\_ \_ indicationrelated**](--indicationrelated.md)" abgeleitet, die keine Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-129">The **\_\_EventConsumer** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which does not have properties.</span></span>

<span data-ttu-id="bbbe5-130">Permanente Consumer definieren neue Consumerklassen, um eine Aktion zu beschreiben, die ausgeführt werden soll, und Daten, die verarbeitet werden sollen, wenn Consumer Ereignis Benachrichtigungen empfangen.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-130">Permanent consumers define new consumer classes to describe an action to take and data to be processed when consumers receive event notifications.</span></span> <span data-ttu-id="bbbe5-131">Permanente Consumer haben besondere Sicherheitsbedenken.</span><span class="sxs-lookup"><span data-stu-id="bbbe5-131">Permanent consumers have special security concerns.</span></span> <span data-ttu-id="bbbe5-132">Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="bbbe5-132">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbbe5-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbbe5-133">Requirements</span></span>



| <span data-ttu-id="bbbe5-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbbe5-134">Requirement</span></span> | <span data-ttu-id="bbbe5-135">Wert</span><span class="sxs-lookup"><span data-stu-id="bbbe5-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="bbbe5-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbbe5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bbbe5-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbbe5-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="bbbe5-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbbe5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bbbe5-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbbe5-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="bbbe5-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="bbbe5-140">Namespace</span></span><br/>                | <span data-ttu-id="bbbe5-141">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="bbbe5-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="bbbe5-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbbe5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbbe5-143">**\_\_Indicationrelated**</span><span class="sxs-lookup"><span data-stu-id="bbbe5-143">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="bbbe5-144">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="bbbe5-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="bbbe5-145">Empfangen von Ereignissen zu allen Zeitpunkten</span><span class="sxs-lookup"><span data-stu-id="bbbe5-145">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="bbbe5-146">Erstellen einer neuen permanenten ereignisconsumerklasse</span><span class="sxs-lookup"><span data-stu-id="bbbe5-146">Creating a New Permanent Event Consumer Class</span></span>](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[<span data-ttu-id="bbbe5-147">Erstellen eines logischen Consumers</span><span class="sxs-lookup"><span data-stu-id="bbbe5-147">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="bbbe5-148">Sichern von WMI-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="bbbe5-148">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

