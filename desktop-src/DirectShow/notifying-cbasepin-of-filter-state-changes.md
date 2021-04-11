---
description: Benachrichtigen von cbasepin mit Filter Zustandsänderungen
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Benachrichtigen von cbasepin mit Filter Zustandsänderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dad6fabc162eb2384283ce2fc8914f76707036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341749"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a><span data-ttu-id="0432c-103">Benachrichtigen von cbasepin mit Filter Zustandsänderungen</span><span class="sxs-lookup"><span data-stu-id="0432c-103">Notifying CBasePin of Filter State Changes</span></span>

<span data-ttu-id="0432c-104">Die **cbasepin** -Klasse wird immer dann benachrichtigt, wenn sich der Status des besitzenden Filters ändert.</span><span class="sxs-lookup"><span data-stu-id="0432c-104">The **CBasePin** class is notified whenever the state of the owning filter changes.</span></span> <span data-ttu-id="0432c-105">Für jeden Zustandsübergang ruft der Filter eine entsprechende Methode für die PIN auf, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0432c-105">For each state transition, the filter calls a corresponding method on the pin, as shown in the following table.</span></span>



| <span data-ttu-id="0432c-106">Neuer Filter Status</span><span class="sxs-lookup"><span data-stu-id="0432c-106">New Filter State</span></span> | <span data-ttu-id="0432c-107">Cbasepin-Methode</span><span class="sxs-lookup"><span data-stu-id="0432c-107">CBasePin Method</span></span>                                 |
|------------------|-------------------------------------------------|
| <span data-ttu-id="0432c-108">Beendet</span><span class="sxs-lookup"><span data-stu-id="0432c-108">Stopped</span></span>          | [<span data-ttu-id="0432c-109">**Cbasepin:: inaktiv**</span><span class="sxs-lookup"><span data-stu-id="0432c-109">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md) |
| <span data-ttu-id="0432c-110">Angehalten</span><span class="sxs-lookup"><span data-stu-id="0432c-110">Paused</span></span>           | [<span data-ttu-id="0432c-111">**Cbasepin:: Active**</span><span class="sxs-lookup"><span data-stu-id="0432c-111">**CBasePin::Active**</span></span>](cbasepin-active.md)     |
| <span data-ttu-id="0432c-112">Wird ausgeführt</span><span class="sxs-lookup"><span data-stu-id="0432c-112">Running</span></span>          | [<span data-ttu-id="0432c-113">**Cbasepin:: Run**</span><span class="sxs-lookup"><span data-stu-id="0432c-113">**CBasePin::Run**</span></span>](cbasepin-run.md)           |



 

<span data-ttu-id="0432c-114">Die abgeleitete Klasse sollte diese Methoden überschreiben, um auf die Zustandsänderung zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="0432c-114">The derived class should override these methods to respond to the state change.</span></span> <span data-ttu-id="0432c-115">Abhängig vom Filter startet die PIN möglicherweise einen Arbeits Thread, der Beispiele bereitstellt, einen Commit oder Decommit für die Arbeitsspeicher Zuweisung durch hat und so weiter.</span><span class="sxs-lookup"><span data-stu-id="0432c-115">Depending on the filter, the pin might start a worker thread that delivers samples, commit or decommit its memory allocator, and so forth.</span></span>

 

 



