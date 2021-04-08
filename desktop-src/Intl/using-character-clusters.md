---
description: Zeichen Cluster sind Symbol Sequenzen, die nicht zwischen Zeilen aufgeteilt werden können.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Verwenden von Zeichen Clustern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11357a929cf8fec2a7b0caa2bb6ae1ac403e3b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760488"
---
# <a name="using-character-clusters"></a><span data-ttu-id="86e2a-103">Verwenden von Zeichen Clustern</span><span class="sxs-lookup"><span data-stu-id="86e2a-103">Using Character Clusters</span></span>

<span data-ttu-id="86e2a-104">Zeichen Cluster sind Symbol Sequenzen, die nicht zwischen Zeilen aufgeteilt werden können.</span><span class="sxs-lookup"><span data-stu-id="86e2a-104">Character clusters are glyph sequences that cannot be split between lines.</span></span> <span data-ttu-id="86e2a-105">Einige Sprachen, z. b. Thai und indic, schränken die Platzierung von Caretzeichen auf Punkte zwischen Clustern ein.</span><span class="sxs-lookup"><span data-stu-id="86e2a-105">Some languages, for example Thai and Indic, restrict caret placement to points between clusters.</span></span> <span data-ttu-id="86e2a-106">Diese Einschränkung gilt für Einfügevorgänge, die mit Tastatur-oder Mausaktionen initiiert wurden (Treffer Tests).</span><span class="sxs-lookup"><span data-stu-id="86e2a-106">This restriction applies to caret movement initiated with keyboard or mouse actions (hit testing).</span></span>

<span data-ttu-id="86e2a-107">Unischreiber stellt Cluster Informationen sowohl in den visuellen Attributen in einer [**Skript- \_ visattr**](/windows/win32/api/usp10/ns-usp10-script_visattr) -Struktur als auch in den logischen Attributen bereit, die in einer [**Skript- \_ logattr**](/windows/win32/api/usp10/ns-usp10-script_logattr) -Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="86e2a-107">Uniscribe provides cluster information in both the visual attributes contained in a [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure, and the logical attributes contained in a [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="86e2a-108">Nachdem die Anwendung [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)aufgerufen hat, werden die Cluster Informationen sowohl durch Sequenzen desselben Werts im **\_ logattr-Skript des Skripts** als auch durch den **fclusterstart** -Member im **Skript ' \_ visattr** '-Array dargestellt.</span><span class="sxs-lookup"><span data-stu-id="86e2a-108">After the application calls [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), the cluster information is represented both by sequences of the same value in the **SCRIPT\_LOGATTR** array, and by the **fClusterStart** member in the **SCRIPT\_VISATTR** array.</span></span>

<span data-ttu-id="86e2a-109">[**Scriptbreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) ruft auch das **fcharstopmember** der Skript- [**\_ logattr**](/windows/win32/api/usp10/ns-usp10-script_logattr) -Struktur ab, um die Cluster Positionen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="86e2a-109">[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) also retrieves the **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure to identify cluster positions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86e2a-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="86e2a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86e2a-111">Verwenden von uniscri</span><span class="sxs-lookup"><span data-stu-id="86e2a-111">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



