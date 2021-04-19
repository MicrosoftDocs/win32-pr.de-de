---
description: Meldet ein Namespace Lösch Ereignis, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das generiert wird, wenn ein untergeordneter Namespace aus dem aktuellen Namespace entfernt wird.
ms.assetid: f7160a90-562d-40d9-9189-32aaabcd81d0
ms.tgt_platform: multiple
title: __NamespaceDeletionEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6e23f909718167760c02bbdb38e2a075d04bc516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373297"
---
# <a name="__namespacedeletionevent-class"></a><span data-ttu-id="1977d-103">\_\_Namespacedeletionevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="1977d-103">\_\_NamespaceDeletionEvent class</span></span>

<span data-ttu-id="1977d-104">Die **\_ \_ Namespace** -System Klasse meldet ein Namespace Lösch Ereignis, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das generiert wird, wenn ein untergeordneter Namespace aus dem aktuellen Namespace entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1977d-104">The **\_\_NamespaceDeletionEvent** system class reports a namespace deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a sub-namespace is removed from the current namespace.</span></span>

<span data-ttu-id="1977d-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1977d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1977d-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1977d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1977d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1977d-107">Syntax</span></span>

``` syntax
class __NamespaceDeletionEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="1977d-108">Member</span><span class="sxs-lookup"><span data-stu-id="1977d-108">Members</span></span>

<span data-ttu-id="1977d-109">Die **\_ \_ namespacedeletionevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1977d-109">The **\_\_NamespaceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="1977d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1977d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1977d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1977d-111">Properties</span></span>

<span data-ttu-id="1977d-112">Die **\_ \_ namespacedeletionevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1977d-112">The **\_\_NamespaceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1977d-113">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1977d-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1977d-114">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="1977d-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1977d-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1977d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1977d-116">Deskriptor, den der Ereignis Anbieter verwendet, um die Benutzer zu ermitteln, die ein Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="1977d-116">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="1977d-117">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1977d-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="1977d-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="1977d-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1977d-119">Datentyp: **\_ \_ Namespace**</span><span class="sxs-lookup"><span data-stu-id="1977d-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="1977d-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1977d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1977d-121">Kopie der [**\_ \_ Namespace**](--namespace.md) Instanz, die gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="1977d-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that is deleted.</span></span> <span data-ttu-id="1977d-122">Die **Name** -Eigenschaft der **\_ \_ Namespace** Instanz identifiziert den Namespace, der gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="1977d-122">The **Name** property of the **\_\_Namespace** instance identifies the namespace that is deleted.</span></span> <span data-ttu-id="1977d-123">Diese Eigenschaft wird von [**\_ \_ namespaceoperationevent**](--namespaceoperationevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1977d-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1977d-124">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="1977d-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1977d-125">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1977d-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1977d-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1977d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1977d-127">Eindeutiger Wert, der die Uhrzeit angibt, zu der ein Ereignis generiert wird.</span><span class="sxs-lookup"><span data-stu-id="1977d-127">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="1977d-128">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="1977d-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="1977d-129">Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor.</span><span class="sxs-lookup"><span data-stu-id="1977d-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="1977d-130">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1977d-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="1977d-131">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1977d-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1977d-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1977d-132">Remarks</span></span>

<span data-ttu-id="1977d-133">Die **\_ \_ namespacedeletionevent** -Klasse wird von [**\_ \_ namespaceoperationevent**](--namespaceoperationevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1977d-133">The **\_\_NamespaceDeletionEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1977d-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1977d-134">Requirements</span></span>



| <span data-ttu-id="1977d-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1977d-135">Requirement</span></span> | <span data-ttu-id="1977d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="1977d-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1977d-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1977d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1977d-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1977d-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1977d-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1977d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1977d-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1977d-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1977d-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="1977d-141">Namespace</span></span><br/>                | <span data-ttu-id="1977d-142">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="1977d-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1977d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1977d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1977d-144">**\_\_Namespaceoperationevent**</span><span class="sxs-lookup"><span data-stu-id="1977d-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="1977d-145">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="1977d-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

