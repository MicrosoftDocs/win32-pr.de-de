---
description: Ist eine Basisklasse für alle systeminternen Ereignisse, die sich auf eine Klasse beziehen.
ms.assetid: 554bbabd-2639-40f5-8786-6df2188db0ec
ms.tgt_platform: multiple
title: __ClassOperationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0c7a78219cec5c014e289dad4bf1cc29f0466a06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366516"
---
# <a name="__classoperationevent-class"></a><span data-ttu-id="bde9d-103">\_\_Classoperationevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="bde9d-103">\_\_ClassOperationEvent class</span></span>

<span data-ttu-id="bde9d-104">Die **\_ \_ classoperationevent** -System Klasse ist eine Basisklasse für alle systeminternen Ereignisse, die sich auf eine Klasse beziehen.</span><span class="sxs-lookup"><span data-stu-id="bde9d-104">The **\_\_ClassOperationEvent** system class is a base class for all intrinsic events that relate to a class.</span></span>

<span data-ttu-id="bde9d-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="bde9d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bde9d-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bde9d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bde9d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bde9d-107">Syntax</span></span>

``` syntax
class __ClassOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="bde9d-108">Member</span><span class="sxs-lookup"><span data-stu-id="bde9d-108">Members</span></span>

<span data-ttu-id="bde9d-109">Die **\_ \_ classoperationevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bde9d-109">The **\_\_ClassOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="bde9d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bde9d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bde9d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bde9d-111">Properties</span></span>

<span data-ttu-id="bde9d-112">Die **\_ \_ classoperationevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bde9d-112">The **\_\_ClassOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bde9d-113">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bde9d-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bde9d-114">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="bde9d-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="bde9d-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bde9d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bde9d-116">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="bde9d-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="bde9d-117">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bde9d-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="bde9d-118">**Targetclass**</span><span class="sxs-lookup"><span data-stu-id="bde9d-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bde9d-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="bde9d-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="bde9d-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bde9d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bde9d-121">Die Klasse, auf die sich das Ereignis auswirkt.</span><span class="sxs-lookup"><span data-stu-id="bde9d-121">Class affected by the event.</span></span> <span data-ttu-id="bde9d-122">Bei Erstellungs Ereignissen handelt es sich hierbei um die neu erstellte Klasse.</span><span class="sxs-lookup"><span data-stu-id="bde9d-122">For creation events, this is the newly created class.</span></span> <span data-ttu-id="bde9d-123">Bei Änderungs Ereignissen handelt es sich hierbei um die neue Version der geänderten-Klasse.</span><span class="sxs-lookup"><span data-stu-id="bde9d-123">For modification events, this is the new version of the changed class.</span></span> <span data-ttu-id="bde9d-124">Bei Lösch Ereignissen handelt es sich hierbei um die gelöschte-Klasse.</span><span class="sxs-lookup"><span data-stu-id="bde9d-124">For deletion events, this is the deleted class.</span></span>

</dd> <dt>

<span data-ttu-id="bde9d-125">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="bde9d-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bde9d-126">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bde9d-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bde9d-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bde9d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bde9d-128">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bde9d-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="bde9d-129">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="bde9d-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="bde9d-130">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="bde9d-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="bde9d-131">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bde9d-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="bde9d-132">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="bde9d-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bde9d-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bde9d-133">Remarks</span></span>

<span data-ttu-id="bde9d-134">Die **\_ \_ classoperationevent** -Klasse wird von [**\_ \_ Event**](--event.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bde9d-134">The **\_\_ClassOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="bde9d-135">Es werden keine Instanzen von **\_ \_ classoperationevent** erstellt; es werden nur Instanzen der Unterklassen erstellt.</span><span class="sxs-lookup"><span data-stu-id="bde9d-135">Instances of **\_\_ClassOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="bde9d-136">Die folgenden Klassen werden von **\_ \_ classoperationevent** abgeleitet:</span><span class="sxs-lookup"><span data-stu-id="bde9d-136">The following classes derive from **\_\_ClassOperationEvent**:</span></span>

[<span data-ttu-id="bde9d-137">**\_\_Classcreationevent**</span><span class="sxs-lookup"><span data-stu-id="bde9d-137">**\_\_ClassCreationEvent**</span></span>](--classcreationevent.md)

[<span data-ttu-id="bde9d-138">**\_\_Classmodificationevent**</span><span class="sxs-lookup"><span data-stu-id="bde9d-138">**\_\_ClassModificationEvent**</span></span>](--classmodificationevent.md)

[<span data-ttu-id="bde9d-139">**\_\_Classdeletionevent**</span><span class="sxs-lookup"><span data-stu-id="bde9d-139">**\_\_ClassDeletionEvent**</span></span>](--classdeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="bde9d-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bde9d-140">Requirements</span></span>



| <span data-ttu-id="bde9d-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bde9d-141">Requirement</span></span> | <span data-ttu-id="bde9d-142">Wert</span><span class="sxs-lookup"><span data-stu-id="bde9d-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="bde9d-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bde9d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bde9d-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bde9d-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="bde9d-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bde9d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bde9d-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bde9d-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="bde9d-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="bde9d-147">Namespace</span></span><br/>                | <span data-ttu-id="bde9d-148">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="bde9d-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="bde9d-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bde9d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde9d-150">**\_\_Ereignis**</span><span class="sxs-lookup"><span data-stu-id="bde9d-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="bde9d-151">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="bde9d-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="bde9d-152">Bestimmen des zu empfangenden Ereignis Typs</span><span class="sxs-lookup"><span data-stu-id="bde9d-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

