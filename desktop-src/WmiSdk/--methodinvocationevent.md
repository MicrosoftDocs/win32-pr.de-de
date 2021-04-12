---
description: Die \_ \_ methodinvocationevent-System Klasse ist definiert, aber nicht implementiert.
ms.assetid: ea736e44-a6bc-41e5-abc5-9e21a5504f44
ms.tgt_platform: multiple
title: __MethodInvocationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodInvocationEvent
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
ms.openlocfilehash: bc7e8d70d027caf31a90d49abc490c2de2d52fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217136"
---
# <a name="__methodinvocationevent-class"></a><span data-ttu-id="c57b1-103">\_\_Methodinvocationevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="c57b1-103">\_\_MethodInvocationEvent class</span></span>

<span data-ttu-id="c57b1-104">Die **\_ \_ methodinvocationevent** -System Klasse ist definiert, aber nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c57b1-104">The **\_\_MethodInvocationEvent** system class is defined but is not implemented.</span></span>

<span data-ttu-id="c57b1-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c57b1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c57b1-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c57b1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c57b1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c57b1-107">Syntax</span></span>

``` syntax
class __MethodInvocationEvent : __InstanceOperationEvent
{
  string       Method;
  __Parameters Parameters;
  boolean      PreCall;
  uint8        SECURITY_DESCRIPTOR[];
  object       TargetInstance;
  uint64       TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="c57b1-108">Member</span><span class="sxs-lookup"><span data-stu-id="c57b1-108">Members</span></span>

<span data-ttu-id="c57b1-109">Die **\_ \_ methodinvocationevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c57b1-109">The **\_\_MethodInvocationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="c57b1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c57b1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c57b1-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c57b1-111">Properties</span></span>

<span data-ttu-id="c57b1-112">Die **\_ \_ methodinvocationevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c57b1-112">The **\_\_MethodInvocationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c57b1-113">**Methode**</span><span class="sxs-lookup"><span data-stu-id="c57b1-113">**Method**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c57b1-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c57b1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c57b1-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c57b1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c57b1-116">Methode, die aufgerufen wird, um das Ereignis zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="c57b1-116">Method invoked to trigger the event.</span></span>

</dd> <dt>

<span data-ttu-id="c57b1-117">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="c57b1-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c57b1-118">Datentyp: **\_ \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="c57b1-118">Data type: **\_\_Parameters**</span></span>
</dt> <dt>

<span data-ttu-id="c57b1-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c57b1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c57b1-120">Verweis auf eine-Instanz, die die Eingabe-und Ausgabeparameter des Methoden Aufrufes darstellt.</span><span class="sxs-lookup"><span data-stu-id="c57b1-120">Reference to an instance that represents the input and output parameters of the method call.</span></span>

</dd> <dt>

<span data-ttu-id="c57b1-121">**Precallup**</span><span class="sxs-lookup"><span data-stu-id="c57b1-121">**PreCall**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c57b1-122">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c57b1-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c57b1-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c57b1-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c57b1-124">**True** gibt an, dass das-Ereignis ausgelöst wird, bevor die-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c57b1-124">If **TRUE**, the event is raised before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="c57b1-125">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c57b1-125">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c57b1-126">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="c57b1-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c57b1-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c57b1-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c57b1-128">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="c57b1-128">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="c57b1-129">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c57b1-129">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="c57b1-130">Weitere Informationen finden Sie unter [Sicherheits Deskriptoren](/windows/desktop/SecAuthZ/security-descriptors).</span><span class="sxs-lookup"><span data-stu-id="c57b1-130">For more information, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

</dd> <dt>

<span data-ttu-id="c57b1-131">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="c57b1-131">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c57b1-132">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c57b1-132">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c57b1-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c57b1-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c57b1-134">Instanz, für die die Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c57b1-134">Instance the method is invoked on.</span></span> <span data-ttu-id="c57b1-135">Diese Eigenschaft wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c57b1-135">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c57b1-136">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="c57b1-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c57b1-137">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c57b1-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c57b1-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c57b1-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c57b1-139">Eindeutiger Wert, der die Uhrzeit angibt, zu der ein Ereignis generiert wird.</span><span class="sxs-lookup"><span data-stu-id="c57b1-139">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="c57b1-140">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="c57b1-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="c57b1-141">Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor.</span><span class="sxs-lookup"><span data-stu-id="c57b1-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="c57b1-142">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c57b1-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="c57b1-143">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c57b1-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c57b1-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c57b1-144">Remarks</span></span>

<span data-ttu-id="c57b1-145">Die **\_ \_ methodinvocationevent** -Klasse wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c57b1-145">The **\_\_MethodInvocationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c57b1-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c57b1-146">Requirements</span></span>



| <span data-ttu-id="c57b1-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c57b1-147">Requirement</span></span> | <span data-ttu-id="c57b1-148">Wert</span><span class="sxs-lookup"><span data-stu-id="c57b1-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c57b1-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c57b1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c57b1-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c57b1-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c57b1-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c57b1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c57b1-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c57b1-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c57b1-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="c57b1-153">Namespace</span></span><br/>                | <span data-ttu-id="c57b1-154">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="c57b1-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c57b1-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c57b1-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c57b1-156">**\_\_Instanceoperationevent**</span><span class="sxs-lookup"><span data-stu-id="c57b1-156">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="c57b1-157">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="c57b1-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

