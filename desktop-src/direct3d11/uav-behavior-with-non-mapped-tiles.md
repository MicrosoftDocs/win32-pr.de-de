---
title: UAV-verhalten bei nicht zugeordneten Kacheln
description: Das Verhalten von Lese-und Schreibvorgängen für die ungeordnete Zugriffs Ansicht (UAV) hängt von der Hardwareunterstützung ab.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9909f8faecd3345761ae26e60835c77aae9ab3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947469"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a><span data-ttu-id="e9411-103">UAV-verhalten bei nicht zugeordneten Kacheln</span><span class="sxs-lookup"><span data-stu-id="e9411-103">UAV behavior with non-mapped tiles</span></span>

<span data-ttu-id="e9411-104">Das Verhalten von Lese-und Schreibvorgängen für die ungeordnete Zugriffs Ansicht (UAV) hängt von der Hardwareunterstützung ab.</span><span class="sxs-lookup"><span data-stu-id="e9411-104">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="e9411-105">Eine Aufschlüsselung der Anforderungen finden Sie unter Allgemeines Lese-und Schreibverhalten für die [Features der gekachelten Ressourcen](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="e9411-105">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="e9411-106">In diesem Abschnitt wird das ideale Verhalten zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="e9411-106">This section summarizes the ideal behavior.</span></span>

<span data-ttu-id="e9411-107">Shadervorgänge, die von einer nicht zugeordneten Kachel in einer UAV lesen, geben 0 (null) in allen nicht fehlenden Komponenten des Formats und die Standardeinstellung für fehlende Komponenten zurück.</span><span class="sxs-lookup"><span data-stu-id="e9411-107">Shader operations that read from a non-mapped tile in a UAV return 0 in all non-missing components of the format, and the default for missing components.</span></span>

<span data-ttu-id="e9411-108">Shadervorgänge, die versuchen, in eine nicht zugeordnete Kachel zu schreiben, bewirken, dass nichts in den nicht zugeordneten Bereich geschrieben wird (während Schreibvorgänge in einen zugeordneten Bereich fortgesetzt werden).</span><span class="sxs-lookup"><span data-stu-id="e9411-108">Shader operations that attempt to write to a non-mapped tile cause nothing to be written to the non-mapped area (while writes to a mapped area proceed).</span></span> <span data-ttu-id="e9411-109">Diese ideale Definition für die Schreib Behandlung ist für [Ebene 2](tier-2.md)nicht erforderlich. Schreibvorgänge in nicht zugeordnete Kacheln können in einem Cache landen, den nachfolgende Lesevorgänge aufnehmen können.</span><span class="sxs-lookup"><span data-stu-id="e9411-109">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9411-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9411-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9411-111">Pipeline Zugriff auf gekachelte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e9411-111">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




