---
description: In der folgenden Tabelle wird beschrieben, in welchen Threads die erkenzercontext-Objekt Ereignisse ausgelöst werden können. Eventthreadserkentionauslöst für den Hintergrund Erkennungs Thread oder für den Thread, der die Erkennungsmethode des erkenzercontext-Objekts aufruft. "Erkentionwithalternativen" im Hintergrund Erkennungs Thread.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Erkenzercontext-Objekt Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc520801ae3391288966e6286d24449be4741b87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960284"
---
# <a name="recognizercontext-object-events"></a><span data-ttu-id="901ca-103">Erkenzercontext-Objekt Ereignisse</span><span class="sxs-lookup"><span data-stu-id="901ca-103">RecognizerContext Object Events</span></span>

<span data-ttu-id="901ca-104">In der folgenden Tabelle wird beschrieben, in welchen Threads die [**erkenzercontext**](inkrecognizercontext-class.md) -Objekt Ereignisse ausgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="901ca-104">The following table describes which threads the [**RecognizerContext**](inkrecognizercontext-class.md) object events can fire on.</span></span>



| <span data-ttu-id="901ca-105">Ereignis</span><span class="sxs-lookup"><span data-stu-id="901ca-105">Event</span></span>                                                                               | <span data-ttu-id="901ca-106">Threads</span><span class="sxs-lookup"><span data-stu-id="901ca-106">Threads</span></span>                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="901ca-107">**Erkennung**</span><span class="sxs-lookup"><span data-stu-id="901ca-107">**Recognition**</span></span>](inkrecognizercontext-recognition.md)                             | <span data-ttu-id="901ca-108">Wird im Hintergrund Erkennungs Thread oder im Thread ausgelöst, der die Erkennungs [**Methode des**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts aufruft.</span><span class="sxs-lookup"><span data-stu-id="901ca-108">Fires on the background recognition thread, or on the thread which calls the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method.</span></span><br/> |
| [<span data-ttu-id="901ca-109">**Erkentionwithalternativen**</span><span class="sxs-lookup"><span data-stu-id="901ca-109">**RecognitionWithAlternates**</span></span>](inkrecognizercontext-recognitionwithalternates.md) | <span data-ttu-id="901ca-110">Wird im Hintergrund Erkennungs Thread ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="901ca-110">Fires on the background recognition thread.</span></span><br/>                                                                                                                                                               |



 

 

 




