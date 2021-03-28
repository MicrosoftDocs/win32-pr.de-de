---
description: Diese Ereignistyp Klasse wird verwendet, um anzugeben, dass Ereignisse in einer echt Zeit Sitzung verloren gegangen sind. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: RT_LostEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: b689dd95aa1e078572d33de64f245e4844698d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526384"
---
# <a name="rt_lostevent-class"></a><span data-ttu-id="b29a4-104">RT \_ lostevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="b29a4-104">RT\_LostEvent class</span></span>

<span data-ttu-id="b29a4-105">Diese Ereignistyp Klasse wird verwendet, um anzugeben, dass Ereignisse in einer echt Zeit Sitzung verloren gegangen sind.</span><span class="sxs-lookup"><span data-stu-id="b29a4-105">This event type class is used to indicate that events were lost in a real-time session.</span></span>

<span data-ttu-id="b29a4-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="b29a4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b29a4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b29a4-107">Syntax</span></span>

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a><span data-ttu-id="b29a4-108">Member</span><span class="sxs-lookup"><span data-stu-id="b29a4-108">Members</span></span>

<span data-ttu-id="b29a4-109">Die **RT \_ lostevent** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="b29a4-109">The **RT\_LostEvent** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="b29a4-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b29a4-110">Remarks</span></span>

<span data-ttu-id="b29a4-111">Der rtlostevent-Ereignistyp gibt an, dass mindestens ein Ereignis verloren gegangen ist.</span><span class="sxs-lookup"><span data-stu-id="b29a4-111">The RTLostEvent event type indicates that one or more events were lost.</span></span> <span data-ttu-id="b29a4-112">Der rtlostbuffer-Ereignistyp gibt an, dass mindestens ein Puffer verloren gegangen ist.</span><span class="sxs-lookup"><span data-stu-id="b29a4-112">The RTLostBuffer event type indicates that one or more buffers were lost.</span></span> <span data-ttu-id="b29a4-113">Die Ereignis Typen rtlostevent und rtlostbuffer werden übermittelt, bevor Ereignisse aus dem Puffer verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="b29a4-113">The RTLostEvent and RTLostBuffer event types are delivered before processing events from the buffer.</span></span>

<span data-ttu-id="b29a4-114">Rtlostfile gibt an, dass die Unterstützungs Datei, die vom autologger zum Erfassen von Ereignissen verwendet wurde, verloren gegangen ist.</span><span class="sxs-lookup"><span data-stu-id="b29a4-114">The RTLostFile indicates that the backing file used by the AutoLogger to capture events was lost.</span></span>

<span data-ttu-id="b29a4-115">Das Verlust von Ereignissen hängt von der Häufigkeit ab, mit der die Ereignisse protokolliert werden, und davon, wie lange der Consumer die Verarbeitung der Ereignisse verbringt.</span><span class="sxs-lookup"><span data-stu-id="b29a4-115">Loosing events depends on the frequency with which the events are logged and how much time the consumer spends processing the events.</span></span>

## <a name="requirements"></a><span data-ttu-id="b29a4-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b29a4-116">Requirements</span></span>



| <span data-ttu-id="b29a4-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b29a4-117">Requirement</span></span> | <span data-ttu-id="b29a4-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b29a4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------|
| <span data-ttu-id="b29a4-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b29a4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b29a4-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b29a4-120">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b29a4-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b29a4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b29a4-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b29a4-122">None supported</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="b29a4-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b29a4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b29a4-124">**\_Ereignis Verlust**</span><span class="sxs-lookup"><span data-stu-id="b29a4-124">**Lost\_Event**</span></span>](lost-event.md)
</dt> </dl>

 

 




