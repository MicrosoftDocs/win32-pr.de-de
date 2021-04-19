---
description: Meldet ein Namespace-Erstellungs Ereignis, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das beim Hinzufügen eines neuen Namespace zum aktuellen Namespace generiert wird.
ms.assetid: 50b9860a-d6e8-4dab-a7d0-09da9dd37b6b
ms.tgt_platform: multiple
title: __NamespaceCreationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 8432bcfb2c96c70b91a7f0d187297217082e2d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368842"
---
# <a name="__namespacecreationevent-class"></a><span data-ttu-id="03d88-103">\_\_Namespacecreationevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="03d88-103">\_\_NamespaceCreationEvent class</span></span>

<span data-ttu-id="03d88-104">Die Namespace-System Klasse meldet ein Namespace-Erstellungs Ereignis, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das beim Hinzufügen eines neuen **\_ \_ Namespaces** zum aktuellen Namespace generiert wird.</span><span class="sxs-lookup"><span data-stu-id="03d88-104">The **\_\_NamespaceCreationEvent** system class reports a namespace creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a new namespace is added to the current namespace.</span></span>

<span data-ttu-id="03d88-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="03d88-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="03d88-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="03d88-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d88-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="03d88-107">Syntax</span></span>

``` syntax
class __NamespaceCreationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="03d88-108">Member</span><span class="sxs-lookup"><span data-stu-id="03d88-108">Members</span></span>

<span data-ttu-id="03d88-109">Die **\_ \_ namespacecreationevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="03d88-109">The **\_\_NamespaceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="03d88-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03d88-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03d88-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="03d88-111">Properties</span></span>

<span data-ttu-id="03d88-112">Die **\_ \_ namespacecreationevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="03d88-112">The **\_\_NamespaceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03d88-113">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="03d88-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d88-114">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="03d88-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="03d88-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03d88-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d88-116">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="03d88-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="03d88-117">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="03d88-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d88-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="03d88-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d88-119">Datentyp: **\_ \_ Namespace**</span><span class="sxs-lookup"><span data-stu-id="03d88-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="03d88-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03d88-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d88-121">Kopie der erstellten [**\_ \_ Namespace**](--namespace.md) Instanz.</span><span class="sxs-lookup"><span data-stu-id="03d88-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that was created.</span></span> <span data-ttu-id="03d88-122">Die **Name** -Eigenschaft der **\_ \_ Namespace** Instanz gibt an, welcher Namespace erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="03d88-122">The **Name** property of the **\_\_Namespace** instance indicates which namespace was created.</span></span> <span data-ttu-id="03d88-123">Diese Eigenschaft wird von [**\_ \_ namespaceoperationevent**](--namespaceoperationevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="03d88-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d88-124">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="03d88-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d88-125">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="03d88-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03d88-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="03d88-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d88-127">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="03d88-127">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="03d88-128">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="03d88-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="03d88-129">Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor.</span><span class="sxs-lookup"><span data-stu-id="03d88-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="03d88-130">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="03d88-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="03d88-131">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="03d88-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03d88-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03d88-132">Remarks</span></span>

<span data-ttu-id="03d88-133">Die **\_ \_ namespacecreationevent** -Klasse wird von [**\_ \_ namespaceoperationevent**](--namespaceoperationevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="03d88-133">The **\_\_NamespaceCreationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03d88-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03d88-134">Requirements</span></span>



| <span data-ttu-id="03d88-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03d88-135">Requirement</span></span> | <span data-ttu-id="03d88-136">Wert</span><span class="sxs-lookup"><span data-stu-id="03d88-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="03d88-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03d88-137">Minimum supported client</span></span><br/> | <span data-ttu-id="03d88-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03d88-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="03d88-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03d88-139">Minimum supported server</span></span><br/> | <span data-ttu-id="03d88-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03d88-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="03d88-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="03d88-141">Namespace</span></span><br/>                | <span data-ttu-id="03d88-142">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="03d88-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="03d88-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03d88-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d88-144">**\_\_Namespaceoperationevent**</span><span class="sxs-lookup"><span data-stu-id="03d88-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="03d88-145">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="03d88-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

