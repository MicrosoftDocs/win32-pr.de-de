---
description: Gibt an, wie Timer-Ereignisse für Consumer generiert werden sollen.
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: __TimerInstruction-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6bbbf905a141fb7e9e3621c78709fd78999393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350098"
---
# <a name="__timerinstruction-class"></a><span data-ttu-id="b6e23-103">\_\_Timerinstruction-Klasse</span><span class="sxs-lookup"><span data-stu-id="b6e23-103">\_\_TimerInstruction class</span></span>

<span data-ttu-id="b6e23-104">Die abstrakte System Klasse **\_ \_ timerinstruction** gibt Anweisungen dazu an, wie [Timer-Ereignisse](receiving-a-timed-or-repeating-event.md) für Consumer generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b6e23-104">The **\_\_TimerInstruction** abstract system class specifies instructions on how [timer events](receiving-a-timed-or-repeating-event.md) should be generated for consumers.</span></span>

<span data-ttu-id="b6e23-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b6e23-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b6e23-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b6e23-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6e23-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6e23-107">Syntax</span></span>

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="b6e23-108">Member</span><span class="sxs-lookup"><span data-stu-id="b6e23-108">Members</span></span>

<span data-ttu-id="b6e23-109">Die **\_ \_ timerinstruction** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b6e23-109">The **\_\_TimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="b6e23-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6e23-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6e23-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6e23-111">Properties</span></span>

<span data-ttu-id="b6e23-112">Die **\_ \_ timerinstruction** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b6e23-112">The **\_\_TimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6e23-113">**Skipifbestandene**</span><span class="sxs-lookup"><span data-stu-id="b6e23-113">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e23-114">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b6e23-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b6e23-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6e23-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6e23-116">Beschreibt, ob ein Benachrichtigungs Ereignis generiert und empfangen wird, wenn ein Consumer verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="b6e23-116">Describes whether a notification event will be generated and receive when a consumer becomes available.</span></span>

<dt>

<span data-ttu-id="b6e23-117">false</span><span class="sxs-lookup"><span data-stu-id="b6e23-117">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="b6e23-118">Wenn WMI oder der Consumer wieder verfügbar wird, wird ein Benachrichtigungs Ereignis generiert und empfangen.</span><span class="sxs-lookup"><span data-stu-id="b6e23-118">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="b6e23-119">TRUE</span><span class="sxs-lookup"><span data-stu-id="b6e23-119">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="b6e23-120">Das Timer-Ereignis tritt nicht auf, wenn WMI nicht verfügbar ist, um es im entsprechenden Zeitintervall zu generieren, oder wenn der Consumer, der den Empfang des Ereignisses anfordert, nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b6e23-120">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b6e23-121">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="b6e23-121">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e23-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6e23-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6e23-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b6e23-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6e23-124">Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b6e23-124">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b6e23-125">Eindeutige vom Benutzer zugewiesene Zeichenfolge, die dieses bestimmte Timer-Ereignis bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b6e23-125">Unique user-assigned string that identifies this particular timer event.</span></span> <span data-ttu-id="b6e23-126">Um Namenskonflikte mit anderen Zeit Geber Bezeichners zu vermeiden, kann die Zeichen folgen Form einer DCE-GUID (verteilten Computer Environment) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6e23-126">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment (DCE)-style GUID can be used.</span></span> <span data-ttu-id="b6e23-127">Diese Eigenschaft ist Teil der [**\_ \_ TimerEvent**](--timerevent.md) -Instanz, die das Ereignis darstellt.</span><span class="sxs-lookup"><span data-stu-id="b6e23-127">This property is part of the [**\_\_TimerEvent**](--timerevent.md) instance that represents the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6e23-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6e23-128">Remarks</span></span>

<span data-ttu-id="b6e23-129">Die **\_ \_ timerinstruction** -Klasse wird von [**\_ \_ eventgenerator**](--eventgenerator.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b6e23-129">The **\_\_TimerInstruction** class is derived from [**\_\_EventGenerator**](--eventgenerator.md).</span></span>

<span data-ttu-id="b6e23-130">Die **\_ \_ timerinstruction** -Unterklassen sind [**\_ \_ absolutetimerinstruction**](--absolutetimerinstruction.md), die von Consumern verwendet werden, um sich für ein absolutes Zeit Geber Ereignis und [**\_ \_ intervaltimerinstruction**](--intervaltimerinstruction.md)zu registrieren, das für die Registrierung für ein Intervallzeit Geber Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6e23-130">The **\_\_TimerInstruction** subclasses are [**\_\_AbsoluteTimerInstruction**](--absolutetimerinstruction.md), used by consumers to register for an absolute timer event, and [**\_\_IntervalTimerInstruction**](--intervaltimerinstruction.md), used to register for an interval timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6e23-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6e23-131">Requirements</span></span>



| <span data-ttu-id="b6e23-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6e23-132">Requirement</span></span> | <span data-ttu-id="b6e23-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b6e23-133">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b6e23-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6e23-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e23-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6e23-135">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b6e23-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6e23-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e23-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6e23-137">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b6e23-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6e23-138">Namespace</span></span><br/>                | <span data-ttu-id="b6e23-139">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="b6e23-139">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b6e23-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6e23-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e23-141">**\_\_Eventgenerator**</span><span class="sxs-lookup"><span data-stu-id="b6e23-141">**\_\_EventGenerator**</span></span>](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[<span data-ttu-id="b6e23-142">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="b6e23-142">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

