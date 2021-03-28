---
description: Diese Klasse ist die übergeordnete Klasse für Split IO-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: Splitio-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: f2efc14ce8804852f983ebe9dcb852c8c0669899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978841"
---
# <a name="splitio-class"></a><span data-ttu-id="95b03-104">Splitio-Klasse</span><span class="sxs-lookup"><span data-stu-id="95b03-104">SplitIo class</span></span>

<span data-ttu-id="95b03-105">Diese Klasse ist die übergeordnete Klasse für Split IO-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="95b03-105">This class is the parent class for split IO events.</span></span>

<span data-ttu-id="95b03-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="95b03-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b03-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="95b03-107">Syntax</span></span>

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="95b03-108">Member</span><span class="sxs-lookup"><span data-stu-id="95b03-108">Members</span></span>

<span data-ttu-id="95b03-109">Die **splitio** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="95b03-109">The **SplitIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="95b03-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95b03-110">Remarks</span></span>

<span data-ttu-id="95b03-111">Um geteilte e/a-Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das Flag für die Ablaufverfolgungsflag **\_ \_ \_ Split \_ IO** im **enableflags** -Member einer Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion</span><span class="sxs-lookup"><span data-stu-id="95b03-111">To enable split IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_SPLIT\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="95b03-112">Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für Split IO-Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**splitioguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="95b03-112">Event trace consumers can implement special processing for split IO events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**SplitIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="95b03-113">Verwenden Sie den folgenden Ereignistyp, um das tatsächliche Ereignis beim Verarbeiten von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="95b03-113">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="95b03-114">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="95b03-114">Event type</span></span>           | <span data-ttu-id="95b03-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95b03-115">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95b03-116">Ereignistyp Wert, 32</span><span class="sxs-lookup"><span data-stu-id="95b03-116">Event type value, 32</span></span> | <span data-ttu-id="95b03-117">IO-Ereignis aufteilen.</span><span class="sxs-lookup"><span data-stu-id="95b03-117">Split IO event.</span></span> <span data-ttu-id="95b03-118">Die " [**splitio \_ Info**](splitio-info.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="95b03-118">The [**SplitIo\_Info**](splitio-info.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="95b03-119">Split IO-Ereignisse zeigen an, dass die e/a-Anforderungen aufgrund der zugrunde liegenden Spiegelung der Datenträger Hardware in mehrere e/a-Anforderungen aufgeteilt wurden</span><span class="sxs-lookup"><span data-stu-id="95b03-119">Split IO events indicate that the IO requests have been split into multiple disk IO requests due to the underlying mirroring disk hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="95b03-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="95b03-120">Requirements</span></span>



| <span data-ttu-id="95b03-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95b03-121">Requirement</span></span> | <span data-ttu-id="95b03-122">Wert</span><span class="sxs-lookup"><span data-stu-id="95b03-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="95b03-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95b03-123">Minimum supported client</span></span><br/> | <span data-ttu-id="95b03-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95b03-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="95b03-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95b03-125">Minimum supported server</span></span><br/> | <span data-ttu-id="95b03-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95b03-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
