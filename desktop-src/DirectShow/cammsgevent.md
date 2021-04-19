---
description: Die "cammsgevent"-Klasse ist ein Wrapper für Ereignis Objekte, die die Nachrichtenverarbeitung durchführen.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: Cammsgevent-Klasse (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367084"
---
# <a name="cammsgevent-class"></a><span data-ttu-id="b9c4e-103">Cammsgevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="b9c4e-103">CAMMsgEvent class</span></span>

![cammsgevent-Klassenhierarchie](images/util06.png)

<span data-ttu-id="b9c4e-105">Die- `CAMMsgEvent` Klasse ist ein Wrapper für Ereignis Objekte, die die Nachrichtenverarbeitung durchführen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-105">The `CAMMsgEvent` class is a wrapper for event objects that perform message processing.</span></span>

<span data-ttu-id="b9c4e-106">Diese Klasse wird vom [**camevent**](camevent.md) -Objekt abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-106">This class derives from the [**CAMEvent**](camevent.md) object.</span></span> <span data-ttu-id="b9c4e-107">Es wird eine Methode hinzugefügt, " [**cammsgevent:: waitmsg**](cammsgevent-waitmsg.md)", die eingehende Nachrichten während des Wartens sendet.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-107">It adds one method, [**CAMMsgEvent::WaitMsg**](cammsgevent-waitmsg.md), which dispatches incoming messages while waiting.</span></span>



| <span data-ttu-id="b9c4e-108">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="b9c4e-108">Public Methods</span></span>                                 | <span data-ttu-id="b9c4e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9c4e-109">Description</span></span>                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="b9c4e-110">**Cammsgevent**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-110">**CAMMsgEvent**</span></span>](cammsgevent-cammsgevent.md) | <span data-ttu-id="b9c4e-111">Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-111">Constructor.</span></span>                                                         |
| [<span data-ttu-id="b9c4e-112">**Waitmsg**</span><span class="sxs-lookup"><span data-stu-id="b9c4e-112">**WaitMsg**</span></span>](cammsgevent-waitmsg.md)         | <span data-ttu-id="b9c4e-113">Wartet, bis das-Ereignis signalisiert wird, während gesendete Nachrichten versendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-113">Waits for the event to be signaled, while dispatching sent messages.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b9c4e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9c4e-114">Requirements</span></span>



| <span data-ttu-id="b9c4e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9c4e-115">Requirement</span></span> | <span data-ttu-id="b9c4e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b9c4e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c4e-117">Header</span><span class="sxs-lookup"><span data-stu-id="b9c4e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b9c4e-118"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9c4e-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b9c4e-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b9c4e-119">Library</span></span><br/> | <dl> <span data-ttu-id="b9c4e-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b9c4e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




