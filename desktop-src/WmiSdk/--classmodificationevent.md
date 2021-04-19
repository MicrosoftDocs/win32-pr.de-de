---
description: Stellt ein Klassen Änderungs Ereignis dar, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das generiert wird, wenn eine Klasse im Namespace geändert wird.
ms.assetid: 77e8e025-d584-495d-98f8-71e7fb2c9698
ms.tgt_platform: multiple
title: __ClassModificationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 3634b632fa9ab66f0da3e48bf77fab5875daf12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358953"
---
# <a name="__classmodificationevent-class"></a><span data-ttu-id="e64e5-103">\_\_Classmodificationevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="e64e5-103">\_\_ClassModificationEvent class</span></span>

<span data-ttu-id="e64e5-104">Die **\_ \_ classmodificationevent** -System Klasse stellt ein Klassen Änderungs Ereignis dar, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das generiert wird, wenn eine Klasse im-Namespace geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e64e5-104">The **\_\_ClassModificationEvent** system class represents a class modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a class is changed in the namespace.</span></span>

<span data-ttu-id="e64e5-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e64e5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e64e5-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e64e5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e64e5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e64e5-107">Syntax</span></span>

``` syntax
class __ClassModificationEvent : __ClassOperationEvent
{
  object PreviousClass;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="e64e5-108">Member</span><span class="sxs-lookup"><span data-stu-id="e64e5-108">Members</span></span>

<span data-ttu-id="e64e5-109">Die **\_ \_ classmodificationevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e64e5-109">The **\_\_ClassModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="e64e5-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e64e5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e64e5-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e64e5-111">Properties</span></span>

<span data-ttu-id="e64e5-112">Die **\_ \_ classmodificationevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e64e5-112">The **\_\_ClassModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e64e5-113">**Previousclass**</span><span class="sxs-lookup"><span data-stu-id="e64e5-113">**PreviousClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e64e5-114">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="e64e5-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e64e5-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e64e5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e64e5-116">Kopie der ursprünglichen Version der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="e64e5-116">Copy of the original version of the class.</span></span>

</dd> <dt>

<span data-ttu-id="e64e5-117">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e64e5-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e64e5-118">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="e64e5-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e64e5-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e64e5-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e64e5-120">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="e64e5-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="e64e5-121">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e64e5-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="e64e5-122">**Targetclass**</span><span class="sxs-lookup"><span data-stu-id="e64e5-122">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e64e5-123">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="e64e5-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e64e5-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e64e5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e64e5-125">Kopie der neu geänderten Klasse, die vom Klassen Änderungs Ereignis gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="e64e5-125">Copy of the newly modified class reported by the class modification event.</span></span> <span data-ttu-id="e64e5-126">Diese Eigenschaft wird von [**\_ \_ classoperationevent**](--classoperationevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e64e5-126">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e64e5-127">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="e64e5-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e64e5-128">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e64e5-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e64e5-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e64e5-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e64e5-130">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e64e5-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="e64e5-131">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="e64e5-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="e64e5-132">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="e64e5-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="e64e5-133">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e64e5-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="e64e5-134">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e64e5-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e64e5-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e64e5-135">Remarks</span></span>

<span data-ttu-id="e64e5-136">Die **\_ \_ classmodificationevent** -Klasse wird von [**\_ \_ classoperationevent**](--classoperationevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e64e5-136">The **\_\_ClassModificationEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="e64e5-137">Das Ereignis meldet sowohl die neue als auch die alte Version der Klassendefinition.</span><span class="sxs-lookup"><span data-stu-id="e64e5-137">The event reports both the new and old versions of the class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="e64e5-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e64e5-138">Requirements</span></span>



| <span data-ttu-id="e64e5-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e64e5-139">Requirement</span></span> | <span data-ttu-id="e64e5-140">Wert</span><span class="sxs-lookup"><span data-stu-id="e64e5-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e64e5-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e64e5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e64e5-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e64e5-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e64e5-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e64e5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e64e5-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e64e5-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e64e5-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="e64e5-145">Namespace</span></span><br/>                | <span data-ttu-id="e64e5-146">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="e64e5-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e64e5-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e64e5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e64e5-148">**\_\_Classoperationevent**</span><span class="sxs-lookup"><span data-stu-id="e64e5-148">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="e64e5-149">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="e64e5-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

