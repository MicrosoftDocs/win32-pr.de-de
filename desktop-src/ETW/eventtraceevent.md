---
description: Die übergeordnete Klasse für Protokoll Header Ereignisse. Diese Klasse ist immer die erste Ereignis Ablauf Verfolgungs Klasse, die an einen Consumer gesendet wird (dieses Ereignis wird nicht an Echt Zeit Consumer gesendet). Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: fb507d9a-6ed2-4cb1-8cea-85c0a3832e51
title: Eventtraceevent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTraceEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0036ee0a49225568aac066735824fe55ce8f0fa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977672"
---
# <a name="eventtraceevent-class"></a><span data-ttu-id="aad39-105">Eventtraceevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="aad39-105">EventTraceEvent class</span></span>

<span data-ttu-id="aad39-106">Die übergeordnete Klasse für Protokoll Header Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="aad39-106">The parent class for log header events.</span></span> <span data-ttu-id="aad39-107">Diese Klasse ist immer die erste Ereignis Ablauf Verfolgungs Klasse, die an einen Consumer gesendet wird (dieses Ereignis wird nicht an Echt Zeit Consumer gesendet).</span><span class="sxs-lookup"><span data-stu-id="aad39-107">This class is always the first event trace class sent to a consumer (this event is not sent to real-time consumers).</span></span>

<span data-ttu-id="aad39-108">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="aad39-108">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aad39-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="aad39-109">Syntax</span></span>

``` syntax
[Guid("{68fdd900-4a3e-11d1-84f4-0000f80464e3}")]
class EventTraceEvent : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="aad39-110">Member</span><span class="sxs-lookup"><span data-stu-id="aad39-110">Members</span></span>

<span data-ttu-id="aad39-111">Die **eventtraceevent** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="aad39-111">The **EventTraceEvent** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="aad39-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="aad39-112">Requirements</span></span>



| <span data-ttu-id="aad39-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aad39-113">Requirement</span></span> | <span data-ttu-id="aad39-114">Wert</span><span class="sxs-lookup"><span data-stu-id="aad39-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aad39-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aad39-115">Minimum supported client</span></span><br/> | <span data-ttu-id="aad39-116">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aad39-116">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="aad39-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aad39-117">Minimum supported server</span></span><br/> | <span data-ttu-id="aad39-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aad39-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aad39-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aad39-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad39-120">**MSNT \_ systemtrace**</span><span class="sxs-lookup"><span data-stu-id="aad39-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="aad39-121">**EventTrace- \_ Header**</span><span class="sxs-lookup"><span data-stu-id="aad39-121">**EventTrace\_Header**</span></span>](eventtrace-header.md)
</dt> </dl>

 

 




