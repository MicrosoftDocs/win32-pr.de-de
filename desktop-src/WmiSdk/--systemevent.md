---
description: Stellt ein System Ereignis dar.
ms.assetid: 84099483-03e4-4c21-b680-f0975b18c1f6
ms.tgt_platform: multiple
title: __SystemEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7cc443c9e130106c2f5e8a05a1a2983927f1963e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217407"
---
# <a name="__systemevent-class"></a><span data-ttu-id="beb65-103">\_\_Systemevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="beb65-103">\_\_SystemEvent class</span></span>

<span data-ttu-id="beb65-104">Die System Klasse **\_ \_ systemevent** stellt ein System Ereignis dar.</span><span class="sxs-lookup"><span data-stu-id="beb65-104">The **\_\_SystemEvent** system class represents a system event.</span></span>

<span data-ttu-id="beb65-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="beb65-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="beb65-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="beb65-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb65-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="beb65-107">Syntax</span></span>

``` syntax
class __SystemEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="beb65-108">Member</span><span class="sxs-lookup"><span data-stu-id="beb65-108">Members</span></span>

<span data-ttu-id="beb65-109">Die **\_ \_ systemevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="beb65-109">The **\_\_SystemEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="beb65-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="beb65-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="beb65-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="beb65-111">Properties</span></span>

<span data-ttu-id="beb65-112">Die **\_ \_ systemevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="beb65-112">The **\_\_SystemEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="beb65-113">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="beb65-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beb65-114">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="beb65-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="beb65-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="beb65-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="beb65-116">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="beb65-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="beb65-117">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="beb65-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="beb65-118">Eine **null** -Access Control Liste (ACL) in der [**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) gewährt allen Benutzern uneingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="beb65-118">A **NULL** Access Control List (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="beb65-119">Weitere Informationen finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="beb65-119">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="beb65-120">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="beb65-120">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beb65-121">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="beb65-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="beb65-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="beb65-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="beb65-123">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="beb65-123">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="beb65-124">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="beb65-124">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="beb65-125">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="beb65-125">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="beb65-126">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="beb65-126">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="beb65-127">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="beb65-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="beb65-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="beb65-128">Remarks</span></span>

<span data-ttu-id="beb65-129">Die **\_ \_ systemevent** -Klasse wird von der [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) -Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="beb65-129">The **\_\_SystemEvent** class is derived from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="beb65-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="beb65-130">Requirements</span></span>



| <span data-ttu-id="beb65-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="beb65-131">Requirement</span></span> | <span data-ttu-id="beb65-132">Wert</span><span class="sxs-lookup"><span data-stu-id="beb65-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="beb65-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="beb65-133">Minimum supported client</span></span><br/> | <span data-ttu-id="beb65-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="beb65-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="beb65-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="beb65-135">Minimum supported server</span></span><br/> | <span data-ttu-id="beb65-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="beb65-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="beb65-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="beb65-137">Namespace</span></span><br/>                | <span data-ttu-id="beb65-138">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="beb65-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="beb65-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="beb65-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb65-140">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="beb65-140">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

[<span data-ttu-id="beb65-141">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="beb65-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

