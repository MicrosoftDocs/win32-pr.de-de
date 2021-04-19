---
description: Stellt ein Klassen Lösch Ereignis dar, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das beim Entfernen einer Klasse aus dem Namespace generiert wird.
ms.assetid: dd44c03e-4d0d-4750-942d-495893d21650
ms.tgt_platform: multiple
title: __ClassDeletionEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29242335edeffbdc44deebb3acacd5631fcc7b68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349274"
---
# <a name="__classdeletionevent-class"></a><span data-ttu-id="c2007-103">\_\_Classdeletionevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="c2007-103">\_\_ClassDeletionEvent class</span></span>

<span data-ttu-id="c2007-104">Die **\_ \_ classdeletionevent** -System Klasse stellt ein Klassen Lösch Ereignis dar, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das beim Entfernen einer Klasse aus dem Namespace generiert wird.</span><span class="sxs-lookup"><span data-stu-id="c2007-104">The **\_\_ClassDeletionEvent** system class represents a class deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a class is removed from the namespace.</span></span>

<span data-ttu-id="c2007-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c2007-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c2007-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c2007-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2007-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2007-107">Syntax</span></span>

``` syntax
class __ClassDeletionEvent : __ClassOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="c2007-108">Member</span><span class="sxs-lookup"><span data-stu-id="c2007-108">Members</span></span>

<span data-ttu-id="c2007-109">Die **\_ \_ classdeletionevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c2007-109">The **\_\_ClassDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="c2007-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2007-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2007-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2007-111">Properties</span></span>

<span data-ttu-id="c2007-112">Die **\_ \_ classdeletionevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2007-112">The **\_\_ClassDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2007-113">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c2007-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2007-114">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="c2007-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c2007-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2007-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2007-116">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="c2007-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="c2007-117">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2007-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2007-118">**Targetclass**</span><span class="sxs-lookup"><span data-stu-id="c2007-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2007-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="c2007-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c2007-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2007-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2007-121">Kopie der neu gelöschten Klasse, die vom Klassen Lösch Ereignis gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="c2007-121">Copy of the newly deleted class reported by the class deletion event.</span></span> <span data-ttu-id="c2007-122">Diese Eigenschaft wird von [**\_ \_ classoperationevent**](--classoperationevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2007-122">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2007-123">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="c2007-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2007-124">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c2007-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c2007-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2007-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2007-126">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c2007-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="c2007-127">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="c2007-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="c2007-128">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="c2007-128">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="c2007-129">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2007-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="c2007-130">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c2007-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2007-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2007-131">Remarks</span></span>

<span data-ttu-id="c2007-132">Die **\_ \_ classdeletionevent** -Klasse wird von [**\_ \_ classoperationevent**](--classoperationevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c2007-132">The **\_\_ClassDeletionEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2007-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2007-133">Requirements</span></span>



| <span data-ttu-id="c2007-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2007-134">Requirement</span></span> | <span data-ttu-id="c2007-135">Wert</span><span class="sxs-lookup"><span data-stu-id="c2007-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c2007-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2007-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c2007-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2007-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c2007-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2007-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c2007-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2007-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c2007-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2007-140">Namespace</span></span><br/>                | <span data-ttu-id="c2007-141">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="c2007-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c2007-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2007-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2007-143">**\_\_Classoperationevent**</span><span class="sxs-lookup"><span data-stu-id="c2007-143">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="c2007-144">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="c2007-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

