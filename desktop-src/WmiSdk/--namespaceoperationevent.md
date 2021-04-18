---
description: Eine Basisklasse für alle systeminternen Ereignisse, die sich auf einen Namespace beziehen.
ms.assetid: 168637b1-217e-4b6d-bd07-25127b9e9f6c
ms.tgt_platform: multiple
title: __NamespaceOperationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: d263af0eab5fc3899b45659bc8409a5e68776fe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352524"
---
# <a name="__namespaceoperationevent-class"></a><span data-ttu-id="b3e66-103">\_\_Namespaceoperationevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="b3e66-103">\_\_NamespaceOperationEvent class</span></span>

<span data-ttu-id="b3e66-104">Die **\_ \_ namespaceoperationevent** -System Klasse ist eine Basisklasse für alle systeminternen Ereignisse, die sich auf einen Namespace beziehen.</span><span class="sxs-lookup"><span data-stu-id="b3e66-104">The **\_\_NamespaceOperationEvent** system class is a base class for all intrinsic events that relate to a namespace.</span></span>

<span data-ttu-id="b3e66-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b3e66-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b3e66-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b3e66-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3e66-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3e66-107">Syntax</span></span>

``` syntax
class __NamespaceOperationEvent : __Event
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="b3e66-108">Member</span><span class="sxs-lookup"><span data-stu-id="b3e66-108">Members</span></span>

<span data-ttu-id="b3e66-109">Die **\_ \_ namespaceoperationevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b3e66-109">The **\_\_NamespaceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b3e66-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3e66-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3e66-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3e66-111">Properties</span></span>

<span data-ttu-id="b3e66-112">Die **\_ \_ namespaceoperationevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b3e66-112">The **\_\_NamespaceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3e66-113">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3e66-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3e66-114">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="b3e66-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b3e66-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3e66-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3e66-116">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="b3e66-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="b3e66-117">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b3e66-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3e66-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="b3e66-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3e66-119">Datentyp: **\_ \_ Namespace**</span><span class="sxs-lookup"><span data-stu-id="b3e66-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="b3e66-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3e66-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3e66-121">Vom Ereignis betroffener Namespace.</span><span class="sxs-lookup"><span data-stu-id="b3e66-121">Namespace affected by the event.</span></span> <span data-ttu-id="b3e66-122">Bei Erstellungs Ereignissen handelt es sich hierbei um den neu erstellten Namespace.</span><span class="sxs-lookup"><span data-stu-id="b3e66-122">For creation events, this is the newly created namespace.</span></span> <span data-ttu-id="b3e66-123">Bei Änderungs Ereignissen handelt es sich hierbei um den geänderten Namespace.</span><span class="sxs-lookup"><span data-stu-id="b3e66-123">For modification events, this is the changed namespace.</span></span> <span data-ttu-id="b3e66-124">Bei Lösch Ereignissen handelt es sich hierbei um den gelöschten Namespace.</span><span class="sxs-lookup"><span data-stu-id="b3e66-124">For deletion events, this is the deleted namespace.</span></span>

</dd> <dt>

<span data-ttu-id="b3e66-125">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="b3e66-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3e66-126">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b3e66-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b3e66-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3e66-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3e66-128">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b3e66-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="b3e66-129">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3e66-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="b3e66-130">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="b3e66-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="b3e66-131">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b3e66-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="b3e66-132">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b3e66-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3e66-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3e66-133">Remarks</span></span>

<span data-ttu-id="b3e66-134">Die **\_ \_ namespaceoperationevent** -Klasse wird vom [**\_ \_ Ereignis**](--event.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b3e66-134">The **\_\_NamespaceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="b3e66-135">Instanzen dieser Klasse werden nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3e66-135">Instances of this class are not created.</span></span> <span data-ttu-id="b3e66-136">WMI erstellt Instanzen von einer der folgenden Klassen, die von dieser Klasse abgeleitet werden:</span><span class="sxs-lookup"><span data-stu-id="b3e66-136">WMI creates instances of one of the following classes derived from this class:</span></span>

[<span data-ttu-id="b3e66-137">**\_\_Namespacecreationevent**</span><span class="sxs-lookup"><span data-stu-id="b3e66-137">**\_\_NamespaceCreationEvent**</span></span>](--namespacecreationevent.md)

[<span data-ttu-id="b3e66-138">**\_\_Namespacemodificationevent**</span><span class="sxs-lookup"><span data-stu-id="b3e66-138">**\_\_NamespaceModificationEvent**</span></span>](--namespacemodificationevent.md)

[<span data-ttu-id="b3e66-139">**\_\_Namespacedeletionevent**</span><span class="sxs-lookup"><span data-stu-id="b3e66-139">**\_\_NamespaceDeletionEvent**</span></span>](--namespacedeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="b3e66-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3e66-140">Requirements</span></span>



| <span data-ttu-id="b3e66-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3e66-141">Requirement</span></span> | <span data-ttu-id="b3e66-142">Wert</span><span class="sxs-lookup"><span data-stu-id="b3e66-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b3e66-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3e66-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b3e66-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3e66-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b3e66-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3e66-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b3e66-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3e66-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b3e66-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3e66-147">Namespace</span></span><br/>                | <span data-ttu-id="b3e66-148">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="b3e66-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b3e66-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3e66-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e66-150">**\_\_Ereignis**</span><span class="sxs-lookup"><span data-stu-id="b3e66-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="b3e66-151">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="b3e66-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="b3e66-152">Bestimmen des zu empfangenden Ereignis Typs</span><span class="sxs-lookup"><span data-stu-id="b3e66-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

