---
description: Diese Klasse ist die übergeordnete Klasse für Stapel Ablauf Verfolgungs Ereignisse.
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: Stackwalk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ad873815cb5cea40c1a9d2f694eca8d0e90d11b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977624"
---
# <a name="stackwalk-class"></a><span data-ttu-id="1a3a1-103">Stackwalk-Klasse</span><span class="sxs-lookup"><span data-stu-id="1a3a1-103">StackWalk class</span></span>

<span data-ttu-id="1a3a1-104">Diese Klasse ist die übergeordnete Klasse für Stapel Ablauf Verfolgungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="1a3a1-104">This class is the parent class for stack tracing events.</span></span>

<span data-ttu-id="1a3a1-105">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="1a3a1-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a3a1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a3a1-106">Syntax</span></span>

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="1a3a1-107">Member</span><span class="sxs-lookup"><span data-stu-id="1a3a1-107">Members</span></span>

<span data-ttu-id="1a3a1-108">Die **Stackwalk** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="1a3a1-108">The **StackWalk** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a3a1-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a3a1-109">Remarks</span></span>

<span data-ttu-id="1a3a1-110">Um die Stapel Überwachung von Kernel Ereignissen zu aktivieren, müssen Sie die [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) -Funktion und die Kernel Ereignisse und-Typen angeben, für die Sie die Stapel Überwachung aufzeichnen möchten.</span><span class="sxs-lookup"><span data-stu-id="1a3a1-110">To enable stack tracing of kernel events, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function and specify the kernel events and types for which you want to capture the stack trace.</span></span> <span data-ttu-id="1a3a1-111">Um die Stapel Überwachung für andere Ereignisse zu aktivieren, legen Sie den **enableproperty** -Member von Ablauf Verfolgungs [**\_ \_ Parametern aktivieren**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) auf **Ereignis \_ Aktivierung \_ Eigenschaften \_ Stapel \_** Überwachung fest.</span><span class="sxs-lookup"><span data-stu-id="1a3a1-111">To enable stack tracing for other events, set the **EnableProperty** member of [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) to **EVENT\_ENABLE\_PROPERTY\_STACK\_TRACE**.</span></span>

<span data-ttu-id="1a3a1-112">Verwenden Sie den folgenden Ereignistyp, um das tatsächliche Ereignis beim Verarbeiten von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1a3a1-112">Use the following event type to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="1a3a1-113">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="1a3a1-113">Event type</span></span>           | <span data-ttu-id="1a3a1-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a3a1-114">Description</span></span>                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a3a1-115">Ereignistyp Wert, 32</span><span class="sxs-lookup"><span data-stu-id="1a3a1-115">Event type value, 32</span></span> | <span data-ttu-id="1a3a1-116">Stapel Ablauf Verfolgungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1a3a1-116">Stack tracing event.</span></span> <span data-ttu-id="1a3a1-117">Die MOF-Klasse des [**Stackwalk- \_ Ereignisses**](stackwalk-event.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1a3a1-117">The [**StackWalk\_Event**](stackwalk-event.md) MOF class defines the event data for this event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1a3a1-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1a3a1-118">Requirements</span></span>



| <span data-ttu-id="1a3a1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a3a1-119">Requirement</span></span> | <span data-ttu-id="1a3a1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1a3a1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1a3a1-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a3a1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1a3a1-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a3a1-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1a3a1-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a3a1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1a3a1-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a3a1-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 
