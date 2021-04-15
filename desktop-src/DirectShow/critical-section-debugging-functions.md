---
description: Kritische Abschnitts Debuggingfunktionen
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Kritische Abschnitts Debuggingfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520992"
---
# <a name="critical-section-debugging-functions"></a><span data-ttu-id="a93d2-103">Kritische Abschnitts Debuggingfunktionen</span><span class="sxs-lookup"><span data-stu-id="a93d2-103">Critical Section Debugging Functions</span></span>

<span data-ttu-id="a93d2-104">Diese Funktionen helfen Ihnen, kritische Abschnitte in Ihrem Code zu debuggen, was die Auffinden der Ursache eines Deadlocks vereinfachen kann.</span><span class="sxs-lookup"><span data-stu-id="a93d2-104">These functions help to debug critical sections in your code, which can make it easier to find the cause of a deadlock.</span></span> <span data-ttu-id="a93d2-105">Diese Funktionen verwenden die [**ccritsec**](ccritsec.md) -Hilfsklasse.</span><span class="sxs-lookup"><span data-stu-id="a93d2-105">These functions use the [**CCritSec**](ccritsec.md) helper class.</span></span>



| <span data-ttu-id="a93d2-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="a93d2-106">Function</span></span>                             | <span data-ttu-id="a93d2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a93d2-107">Description</span></span>                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="a93d2-108">**Critcheckin**</span><span class="sxs-lookup"><span data-stu-id="a93d2-108">**CritCheckIn**</span></span>](critcheckin.md)   | <span data-ttu-id="a93d2-109">Gibt " **true** " zurück, wenn der aktuelle Thread den angegebenen kritischen Abschnitt besitzt.</span><span class="sxs-lookup"><span data-stu-id="a93d2-109">Returns **TRUE** if the current thread owns the specified critical section.</span></span>  |
| [<span data-ttu-id="a93d2-110">**Critcheckout**</span><span class="sxs-lookup"><span data-stu-id="a93d2-110">**CritCheckOut**</span></span>](critcheckout.md) | <span data-ttu-id="a93d2-111">Gibt **false** zurück, wenn der aktuelle Thread den angegebenen kritischen Abschnitt besitzt.</span><span class="sxs-lookup"><span data-stu-id="a93d2-111">Returns **FALSE** if the current thread owns the specified critical section.</span></span> |
| [<span data-ttu-id="a93d2-112">**Dbglocktrace**</span><span class="sxs-lookup"><span data-stu-id="a93d2-112">**DbgLockTrace**</span></span>](dbglocktrace.md) | <span data-ttu-id="a93d2-113">Aktiviert oder deaktiviert die Debugprotokollierung für einen bestimmten kritischen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="a93d2-113">Enables or disables debug logging for a given critical section.</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="a93d2-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a93d2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a93d2-115">Debugging-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="a93d2-115">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



