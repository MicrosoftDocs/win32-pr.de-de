---
description: Die "camevent"-Klasse ist ein Wrapper für Ereignisse für manuelles Zurücksetzen und automatisches Zurücksetzen.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Camevent-Klasse (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370027"
---
# <a name="camevent-class"></a><span data-ttu-id="ae347-103">Camevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="ae347-103">CAMEvent class</span></span>

![camevent-Klassenhierarchie](images/util06.png)

<span data-ttu-id="ae347-105">Die " **camevent** "-Klasse ist ein Wrapper für Ereignisse für manuelles Zurücksetzen und automatisches Zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="ae347-105">The **CAMEvent** class is a wrapper for manual-reset and auto-reset events.</span></span>

<span data-ttu-id="ae347-106">Diese Klasse bietet eine bequeme Möglichkeit, Ereignisse zu verwalten, anstatt Funktionen wie [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)und [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent)aufrufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="ae347-106">This class provides a convenient way to manage events, rather than calling functions such as [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), and [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).</span></span>



| <span data-ttu-id="ae347-107">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="ae347-107">Protected Member Variables</span></span>                          | <span data-ttu-id="ae347-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae347-108">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="ae347-109">**m \_ hevent**</span><span class="sxs-lookup"><span data-stu-id="ae347-109">**m\_hEvent**</span></span>](camevent-m-hevent.md)              | <span data-ttu-id="ae347-110">Ereignis handle.</span><span class="sxs-lookup"><span data-stu-id="ae347-110">Event handle.</span></span>                                                   |
| <span data-ttu-id="ae347-111">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="ae347-111">Public Methods</span></span>                                      | <span data-ttu-id="ae347-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae347-112">Description</span></span>                                                     |
| [<span data-ttu-id="ae347-113">**Camevent**</span><span class="sxs-lookup"><span data-stu-id="ae347-113">**CAMEvent**</span></span>](camevent-camevent.md)               | <span data-ttu-id="ae347-114">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ae347-114">Constructor method.</span></span>                                             |
| [<span data-ttu-id="ae347-115">**~ Camevent**</span><span class="sxs-lookup"><span data-stu-id="ae347-115">**~CAMEvent**</span></span>](camevent--camevent.md)             | <span data-ttu-id="ae347-116">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ae347-116">Destructor method.</span></span>                                              |
| [<span data-ttu-id="ae347-117">**Azure Functions**</span><span class="sxs-lookup"><span data-stu-id="ae347-117">**Check**</span></span>](camevent-check.md)                     | <span data-ttu-id="ae347-118">Überprüft, ob das Ereignis festgelegt ist, ohne zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="ae347-118">Checks whether the event is set, without blocking.</span></span>              |
| [<span data-ttu-id="ae347-119">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="ae347-119">**Reset**</span></span>](camevent-reset.md)                     | <span data-ttu-id="ae347-120">Legt den Zustand des Ereignisses auf "nicht signalisiert" fest.</span><span class="sxs-lookup"><span data-stu-id="ae347-120">Sets the state of the event to nonsignaled.</span></span>                     |
| [<span data-ttu-id="ae347-121">**Set**</span><span class="sxs-lookup"><span data-stu-id="ae347-121">**Set**</span></span>](camevent-set.md)                         | <span data-ttu-id="ae347-122">Signalisiert das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="ae347-122">Signals the event.</span></span>                                              |
| [<span data-ttu-id="ae347-123">**Wait**</span><span class="sxs-lookup"><span data-stu-id="ae347-123">**Wait**</span></span>](camevent-wait.md)                       | <span data-ttu-id="ae347-124">Blockiert, bis das-Ereignis signalisiert wird, oder bis ein Timeout auftritt.</span><span class="sxs-lookup"><span data-stu-id="ae347-124">Blocks until the event is signaled, or until a time-out occurs.</span></span> |
| <span data-ttu-id="ae347-125">Operatoren</span><span class="sxs-lookup"><span data-stu-id="ae347-125">Operators</span></span>                                           | <span data-ttu-id="ae347-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae347-126">Description</span></span>                                                     |
| [<span data-ttu-id="ae347-127">**Operator handle**</span><span class="sxs-lookup"><span data-stu-id="ae347-127">**operator HANDLE**</span></span>](camevent-operator-handle.md) | <span data-ttu-id="ae347-128">Ruft das Ereignis Handle ab.</span><span class="sxs-lookup"><span data-stu-id="ae347-128">Retrieves the event handle.</span></span>                                     |



 

## <a name="requirements"></a><span data-ttu-id="ae347-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae347-129">Requirements</span></span>



| <span data-ttu-id="ae347-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae347-130">Requirement</span></span> | <span data-ttu-id="ae347-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ae347-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae347-132">Header</span><span class="sxs-lookup"><span data-stu-id="ae347-132">Header</span></span><br/>  | <dl> <span data-ttu-id="ae347-133"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae347-133"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ae347-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ae347-134">Library</span></span><br/> | <dl> <span data-ttu-id="ae347-135">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ae347-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

