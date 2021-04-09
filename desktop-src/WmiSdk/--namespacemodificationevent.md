---
description: Meldet ein Namespace-Änderungs Ereignis, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das generiert wird, wenn ein Namespace geändert wird.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: __NamespaceModificationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5af5783d3ebfbfb4b7842cb86b1919f8dbed1365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759444"
---
# <a name="__namespacemodificationevent-class"></a><span data-ttu-id="762d5-103">\_\_Namespacemodificationevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="762d5-103">\_\_NamespaceModificationEvent class</span></span>

<span data-ttu-id="762d5-104">Die **\_ \_ namespacemodificationevent** -System Klasse meldet ein Namespace-Änderungs Ereignis, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das generiert wird, wenn ein Namespace geändert wird.</span><span class="sxs-lookup"><span data-stu-id="762d5-104">The **\_\_NamespaceModificationEvent** system class reports a namespace modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a namespace is modified.</span></span>

<span data-ttu-id="762d5-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="762d5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="762d5-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="762d5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="762d5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="762d5-107">Syntax</span></span>

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="762d5-108">Member</span><span class="sxs-lookup"><span data-stu-id="762d5-108">Members</span></span>

<span data-ttu-id="762d5-109">Die **\_ \_ namespacemodificationevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="762d5-109">The **\_\_NamespaceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="762d5-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="762d5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="762d5-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="762d5-111">Properties</span></span>

<span data-ttu-id="762d5-112">Die **\_ \_ namespacemodificationevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="762d5-112">The **\_\_NamespaceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="762d5-113">**Previousnamespace**</span><span class="sxs-lookup"><span data-stu-id="762d5-113">**PreviousNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="762d5-114">Datentyp: **\_ \_ Namespace**</span><span class="sxs-lookup"><span data-stu-id="762d5-114">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="762d5-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="762d5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="762d5-116">Kopie der ursprünglichen Version einer [**\_ \_ Namespace**](--namespace.md) Instanz.</span><span class="sxs-lookup"><span data-stu-id="762d5-116">Copy of the original version of a [**\_\_Namespace**](--namespace.md) instance.</span></span> <span data-ttu-id="762d5-117">Die **Name** -Eigenschaft dieser Instanz identifiziert den Namespace, der geändert wird.</span><span class="sxs-lookup"><span data-stu-id="762d5-117">The **Name** property of this instance identifies the namespace that is modified.</span></span>

</dd> <dt>

<span data-ttu-id="762d5-118">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="762d5-118">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="762d5-119">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="762d5-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="762d5-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="762d5-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="762d5-121">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="762d5-121">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="762d5-122">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="762d5-122">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="762d5-123">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="762d5-123">**SECURITY\_DESCRIPTOR**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="762d5-124">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="762d5-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="762d5-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="762d5-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="762d5-126">Deskriptor, den der Ereignis Anbieter verwendet, um die Benutzer zu ermitteln, die ein Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="762d5-126">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="762d5-127">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="762d5-127">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="762d5-128">Eine Zugriffs Steuerungs Liste (Access Control List, ACL) für **null** in der [**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) gewährt allen Benutzern uneingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="762d5-128">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="762d5-129">Weitere Informationen finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="762d5-129">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="762d5-130">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="762d5-130">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="762d5-131">Datentyp: **\_ \_ Namespace**</span><span class="sxs-lookup"><span data-stu-id="762d5-131">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="762d5-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="762d5-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="762d5-133">Kopie der geänderten [**\_ \_ Namespace**](--namespace.md) Instanz.</span><span class="sxs-lookup"><span data-stu-id="762d5-133">Copy of the [**\_\_Namespace**](--namespace.md) instance that is modified.</span></span> <span data-ttu-id="762d5-134">Die **Name** -Eigenschaft der **\_ \_ Namespace** Instanz gibt den Namespace an, der geändert wird.</span><span class="sxs-lookup"><span data-stu-id="762d5-134">The **Name** property of the **\_\_Namespace** instance indicates the namespace that is modified.</span></span> <span data-ttu-id="762d5-135">Diese Eigenschaft wird von der Klasse [**\_ \_ namespaceoperationevent**](--namespaceoperationevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="762d5-135">This property is inherited from class [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="762d5-136">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="762d5-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="762d5-137">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="762d5-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="762d5-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="762d5-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="762d5-139">Eindeutiger Wert, der die Uhrzeit angibt, zu der ein Ereignis generiert wird.</span><span class="sxs-lookup"><span data-stu-id="762d5-139">Unique value that indicates the time that an event is generated.</span></span> <span data-ttu-id="762d5-140">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="762d5-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="762d5-141">Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor.</span><span class="sxs-lookup"><span data-stu-id="762d5-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="762d5-142">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="762d5-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="762d5-143">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="762d5-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="762d5-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="762d5-144">Remarks</span></span>

<span data-ttu-id="762d5-145">Die **\_ \_ namespacemodificationevent** -Klasse wird von [**\_ \_ namespaceoperationevent**](--namespaceoperationevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="762d5-145">The **\_\_NamespaceModificationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

<span data-ttu-id="762d5-146">Die einzigen Unterschiede zwischen dem Ziel Namespace und dem vorherigen Namespace sind die Qualifizierer und Eigenschaften mit Ausnahme von [**Name**](--namespace.md).</span><span class="sxs-lookup"><span data-stu-id="762d5-146">The only differences between the target namespace and the previous namespace is the qualifiers and properties except [**Name**](--namespace.md).</span></span>

<span data-ttu-id="762d5-147">Beachten Sie, dass die [**Name**](--namespace.md) -Eigenschaft einer **\_ \_ Namespace** Instanz nicht geändert werden kann, da Namespaces nicht umbenannt werden können.</span><span class="sxs-lookup"><span data-stu-id="762d5-147">Note that the [**Name**](--namespace.md) property of a **\_\_Namespace** instance cannot change because namespaces cannot be renamed.</span></span> <span data-ttu-id="762d5-148">Um den Namen eines Namespace zu ändern, muss die **\_ \_ Namespace** Instanz gelöscht und mit einem neuen Namen neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="762d5-148">To modify the name of a namespace, the **\_\_Namespace** instance must be deleted and re-created with a new name.</span></span> <span data-ttu-id="762d5-149">Daher werden Namespace Änderungs Ereignisse generiert, wenn eine Änderung an Qualifizierern und anderen Eigenschaften als **Name** auftritt.</span><span class="sxs-lookup"><span data-stu-id="762d5-149">Therefore, namespace modification events are generated when a change occurs to qualifiers and properties other than **Name**.</span></span> <span data-ttu-id="762d5-150">Ein Namespace-Änderungs Ereignis wird nicht generiert, wenn eine Art von Änderung im Namespace auftritt.</span><span class="sxs-lookup"><span data-stu-id="762d5-150">A namespace modification event is not generated when any kind of change occurs within the namespace.</span></span> <span data-ttu-id="762d5-151">Ein Namespace-Änderungs Ereignis wird nur generiert, wenn eine Namespace Instanz geändert wird.</span><span class="sxs-lookup"><span data-stu-id="762d5-151">A namespace modification event is generated only when a namespace instance is modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="762d5-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="762d5-152">Requirements</span></span>



| <span data-ttu-id="762d5-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="762d5-153">Requirement</span></span> | <span data-ttu-id="762d5-154">Wert</span><span class="sxs-lookup"><span data-stu-id="762d5-154">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="762d5-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="762d5-155">Minimum supported client</span></span><br/> | <span data-ttu-id="762d5-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="762d5-156">Windows Vista</span></span><br/>       |
| <span data-ttu-id="762d5-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="762d5-157">Minimum supported server</span></span><br/> | <span data-ttu-id="762d5-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="762d5-158">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="762d5-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="762d5-159">Namespace</span></span><br/>                | <span data-ttu-id="762d5-160">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="762d5-160">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="762d5-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="762d5-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="762d5-162">**\_\_Namespaceoperationevent**</span><span class="sxs-lookup"><span data-stu-id="762d5-162">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="762d5-163">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="762d5-163">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

