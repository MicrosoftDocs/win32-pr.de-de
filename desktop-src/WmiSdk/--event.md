---
description: Ist eine abstrakte Basisklasse, die als übergeordnete Klasse für alle systeminternen und extrinsischen Ereignisse fungiert.
ms.assetid: 4d2e4715-041c-49e9-b948-a148dfe85483
ms.tgt_platform: multiple
title: __Event-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Event
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 39a032b3f082ed64ba7999d20366b89e8b3890c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357091"
---
# <a name="__event-class"></a><span data-ttu-id="69e0a-103">\_\_Ereignisklasse</span><span class="sxs-lookup"><span data-stu-id="69e0a-103">\_\_Event class</span></span>

<span data-ttu-id="69e0a-104">**\_ \_ Bei der Ereignis** System Klasse handelt es sich um eine abstrakte Basisklasse, die als übergeordnete Klasse für alle systeminternen und extrinsischen Ereignisse fungiert.</span><span class="sxs-lookup"><span data-stu-id="69e0a-104">The **\_\_Event** system class is an abstract base class that serves as the parent class for all intrinsic and extrinsic events.</span></span> <span data-ttu-id="69e0a-105">Alle neuen Ereignis Typen müssen letztendlich vom **\_ \_ Ereignis** abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="69e0a-105">All new event types must ultimately derive from **\_\_Event**.</span></span> <span data-ttu-id="69e0a-106">Systeminterne Ereignisse werden direkt von dieser Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="69e0a-106">Intrinsic events derive directly from this class.</span></span> <span data-ttu-id="69e0a-107">Benutzerdefinierte System externe-Ereignisse werden von einer Unterklasse dieser Klasse mit dem Namen " [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md)" abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="69e0a-107">User-defined extrinsic events derive from a subclass of this class called [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span>

<span data-ttu-id="69e0a-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="69e0a-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="69e0a-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="69e0a-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="69e0a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="69e0a-110">Syntax</span></span>

``` syntax
[abstract]
class __Event : __IndicationRelated
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="69e0a-111">Member</span><span class="sxs-lookup"><span data-stu-id="69e0a-111">Members</span></span>

<span data-ttu-id="69e0a-112">Die- **\_ \_ Ereignis** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="69e0a-112">The **\_\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="69e0a-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69e0a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69e0a-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69e0a-114">Properties</span></span>

<span data-ttu-id="69e0a-115">Die- **\_ \_ Ereignis** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="69e0a-115">The **\_\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="69e0a-116">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69e0a-116">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e0a-117">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="69e0a-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="69e0a-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69e0a-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69e0a-119">Deskriptor, den der Ereignis Anbieter verwendet, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="69e0a-119">Descriptor that the event provider uses to determine which users can receive the event.</span></span> <span data-ttu-id="69e0a-120">Weitere Informationen finden Sie unter [WMI-Sicherheits Konstanten](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="69e0a-120">For more information, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="69e0a-121">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="69e0a-121">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69e0a-122">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="69e0a-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="69e0a-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69e0a-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69e0a-124">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wird.</span><span class="sxs-lookup"><span data-stu-id="69e0a-124">Unique value that indicates the time the event is generated.</span></span> <span data-ttu-id="69e0a-125">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="69e0a-125">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="69e0a-126">Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor.</span><span class="sxs-lookup"><span data-stu-id="69e0a-126">The information is in the Coordinated Universal Time (UTC) format.</span></span>

<span data-ttu-id="69e0a-127">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="69e0a-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69e0a-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69e0a-128">Remarks</span></span>

<span data-ttu-id="69e0a-129">Die **\_ \_ Ereignis** Klasse wird von " [**\_ \_ indicationrelated**](--indicationrelated.md)" abgeleitet, die keine Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="69e0a-129">The **\_\_Event** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="69e0a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69e0a-130">Requirements</span></span>



| <span data-ttu-id="69e0a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69e0a-131">Requirement</span></span> | <span data-ttu-id="69e0a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="69e0a-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="69e0a-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69e0a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="69e0a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69e0a-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="69e0a-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69e0a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="69e0a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69e0a-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="69e0a-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="69e0a-137">Namespace</span></span><br/>                | <span data-ttu-id="69e0a-138">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="69e0a-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="69e0a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69e0a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e0a-140">**\_\_Indicationrelated**</span><span class="sxs-lookup"><span data-stu-id="69e0a-140">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="69e0a-141">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="69e0a-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="69e0a-142">Bestimmen des zu empfangenden Ereignis Typs</span><span class="sxs-lookup"><span data-stu-id="69e0a-142">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="69e0a-143">**\_\_Classoperationevent**</span><span class="sxs-lookup"><span data-stu-id="69e0a-143">**\_\_ClassOperationEvent**</span></span>](--classoperationevent.md)
</dt> <dt>

[<span data-ttu-id="69e0a-144">**\_\_Instanceoperationevent**</span><span class="sxs-lookup"><span data-stu-id="69e0a-144">**\_\_InstanceOperationEvent**</span></span>](--instanceoperationevent.md)
</dt> <dt>

[<span data-ttu-id="69e0a-145">**\_\_Namespaceoperationevent**</span><span class="sxs-lookup"><span data-stu-id="69e0a-145">**\_\_NamespaceOperationEvent**</span></span>](--namespaceoperationevent.md)
</dt> </dl>

 

