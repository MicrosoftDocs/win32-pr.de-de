---
description: Fungiert als übergeordnete Klasse für alle benutzerdefinierten Ereignis Typen, die auch als extrinsische Ereignisse bezeichnet werden.
ms.assetid: 8fddbcd1-7393-4a3b-8a10-a8b620efc19f
ms.tgt_platform: multiple
title: __ExtrinsicEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtrinsicEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 76af7a9f32c24b8d44f81c60b0f2fca693c26f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217976"
---
# <a name="__extrinsicevent-class"></a><span data-ttu-id="da819-103">\_\_ExtrinsicEvent-Klasse</span><span class="sxs-lookup"><span data-stu-id="da819-103">\_\_ExtrinsicEvent class</span></span>

<span data-ttu-id="da819-104">Die System Klasse " **\_ \_ ExtrinsicEvent** " ist eine abstrakte Basisklasse, die als übergeordnete Klasse für alle benutzerdefinierten Ereignis Typen fungiert, die auch als [extrinsische Ereignisse](determining-the-type-of-event-to-receive.md)bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="da819-104">The **\_\_ExtrinsicEvent** system class is an abstract base class that serves as a parent class for all user-defined event types, also known as [extrinsic events](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="da819-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="da819-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="da819-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="da819-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="da819-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="da819-107">Syntax</span></span>

``` syntax
class __ExtrinsicEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="da819-108">Member</span><span class="sxs-lookup"><span data-stu-id="da819-108">Members</span></span>

<span data-ttu-id="da819-109">Die **\_ \_ ExtrinsicEvent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="da819-109">The **\_\_ExtrinsicEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="da819-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da819-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da819-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="da819-111">Properties</span></span>

<span data-ttu-id="da819-112">Die **\_ \_ ExtrinsicEvent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="da819-112">The **\_\_ExtrinsicEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da819-113">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da819-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da819-114">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="da819-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="da819-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da819-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da819-116">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="da819-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="da819-117">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da819-117">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="da819-118">Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="da819-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="da819-119">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="da819-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da819-120">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="da819-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="da819-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="da819-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da819-122">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="da819-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="da819-123">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="da819-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="da819-124">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="da819-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="da819-125">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="da819-125">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="da819-126">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="da819-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da819-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da819-127">Remarks</span></span>

<span data-ttu-id="da819-128">Die **\_ \_ ExtrinsicEvent** -Klasse wird von [**\_ \_ Event**](--event.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="da819-128">The **\_\_ExtrinsicEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da819-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da819-129">Requirements</span></span>



| <span data-ttu-id="da819-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da819-130">Requirement</span></span> | <span data-ttu-id="da819-131">Wert</span><span class="sxs-lookup"><span data-stu-id="da819-131">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="da819-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da819-132">Minimum supported client</span></span><br/> | <span data-ttu-id="da819-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da819-133">Windows Vista</span></span><br/>       |
| <span data-ttu-id="da819-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da819-134">Minimum supported server</span></span><br/> | <span data-ttu-id="da819-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da819-135">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="da819-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="da819-136">Namespace</span></span><br/>                | <span data-ttu-id="da819-137">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="da819-137">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="da819-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da819-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da819-139">**\_\_Ereignis**</span><span class="sxs-lookup"><span data-stu-id="da819-139">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="da819-140">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="da819-140">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

