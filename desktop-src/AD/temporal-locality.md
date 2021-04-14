---
title: Temporale Lokalität
description: Temporale Lokalität ist eine Vermeidungsstrategie, die das Fenster für Teil Aktualisierungen reduziert.
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470836"
---
# <a name="temporal-locality"></a><span data-ttu-id="ba1c3-103">Temporale Lokalität</span><span class="sxs-lookup"><span data-stu-id="ba1c3-103">Temporal Locality</span></span>

<span data-ttu-id="ba1c3-104">*Temporale Lokalität* ist eine Vermeidungsstrategie, die das Fenster für Teil Aktualisierungen reduziert.</span><span class="sxs-lookup"><span data-stu-id="ba1c3-104">*Temporal locality* is an avoidance strategy that reduces the window for partial updates.</span></span> <span data-ttu-id="ba1c3-105">Die Replikation von Änderungen von einem bestimmten Quell Replikat wird in aufsteigender Reihenfolge der Anwendungen fortgesetzt</span><span class="sxs-lookup"><span data-stu-id="ba1c3-105">Replication of changes from a given source replica proceeds in ascending USN order.</span></span> <span data-ttu-id="ba1c3-106">Schreibvorgänge, die gleichzeitig ausgeführt werden, verfügen über Verwendungen, die einander "nah" sind und in der Zeit nah verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="ba1c3-106">Writes that occur close together in time will have USNs that are "near" each other, and will be propagated close together in time.</span></span> <span data-ttu-id="ba1c3-107">Anwendungen, die mehrere verknüpfte Objekte erstellen oder aktualisieren, sollten die Objekte möglichst nah beieinander schreiben.</span><span class="sxs-lookup"><span data-stu-id="ba1c3-107">Applications that create or update multiple, related objects should write the objects as close together in time as possible.</span></span> <span data-ttu-id="ba1c3-108">Die Anwendung kann z. b. alle notwendigen Eingaben vom Benutzer erfassen und auf das Verzeichnis anwenden, wenn der Benutzer auf die Schaltfläche "anwenden" klickt.</span><span class="sxs-lookup"><span data-stu-id="ba1c3-108">For example, the application could gather all necessary input from the user and apply it to the directory when the user clicks an "Apply" button.</span></span>

<span data-ttu-id="ba1c3-109">Temporale Lokalität verringert außerdem die Wahrscheinlichkeit einer Konfliktlösung, die interne Inkonsistenzen einführt.</span><span class="sxs-lookup"><span data-stu-id="ba1c3-109">Temporal locality also reduces the odds of collision resolution introducing intra-object inconsistencies.</span></span>

 

 




