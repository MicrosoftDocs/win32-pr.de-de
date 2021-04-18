---
title: Funktionen (Berührungs Treffer Tests)
description: Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Berührungs Treffer-Testfunktionen.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- Benutzereingriff
- input
- Zeiger
- Toucheingabe
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 03fcb4fb3fbe4f56e288703316f4b6e3ff02bba4
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106365443"
---
# <a name="touch-hit-testing-functions"></a><span data-ttu-id="ec738-107">Funktionen für Berührungs Treffer Tests</span><span class="sxs-lookup"><span data-stu-id="ec738-107">Touch Hit Testing functions</span></span>

<span data-ttu-id="ec738-108">Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für [Berührungs Treffer-Testfunktionen](functions.md).</span><span class="sxs-lookup"><span data-stu-id="ec738-108">The topics in this section provide the reference specifications for [Touch Hit Testing functions](functions.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ec738-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ec738-109">In this section</span></span>

| <span data-ttu-id="ec738-110">Thema</span><span class="sxs-lookup"><span data-stu-id="ec738-110">Topic</span></span> | <span data-ttu-id="ec738-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec738-111">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="ec738-112">**Evaluateproximitytopolygon**</span><span class="sxs-lookup"><span data-stu-id="ec738-112">**EvaluateProximityToPolygon**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | <span data-ttu-id="ec738-113">Gibt das Ergebnis eines Polygone als wahrscheinliches Berührungs Ziel (im Vergleich zu allen anderen Polygonen, die den Berührungs Kontaktbereich überschneiden) und einen angepassten Berührungspunkt innerhalb des Polygone zurück.</span><span class="sxs-lookup"><span data-stu-id="ec738-113">Returns the score of a polygon as the probable touch target (compared to all other polygons that intersect the touch contact area) and an adjusted touch point within the polygon.</span></span> <br/> |
| [<span data-ttu-id="ec738-114">**Evaluateproximitytor**</span><span class="sxs-lookup"><span data-stu-id="ec738-114">**EvaluateProximityToRect**</span></span>](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | <span data-ttu-id="ec738-115">Gibt das Ergebnis eines Rechtecks als wahrscheinliches Berührungs Ziel zurück, verglichen mit allen anderen Rechtecke, die den Berührungs Kontaktbereich überschneiden, und einem angepassten Berührungspunkt innerhalb des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="ec738-115">Returns the score of a rectangle as the probable touch target, compared to all other rectangles that intersect the touch contact area, and an adjusted touch point within the rectangle.</span></span> <br/> |
| [<span data-ttu-id="ec738-116">**Packtouchhittestingproximityevaluation**</span><span class="sxs-lookup"><span data-stu-id="ec738-116">**PackTouchHitTestingProximityEvaluation**</span></span>](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | <span data-ttu-id="ec738-117">Gibt das Näherungs Bewertungsergebnis und die angepassten Berührungspunkt Koordinaten als einen gepackten Wert für den [WM_TOUCHHITTESTING Nachrichten](../inputmsg/wm-touchhittesting.md) Rückruf zurück.</span><span class="sxs-lookup"><span data-stu-id="ec738-117">Returns the proximity evaluation score and the adjusted touch-point coordinates as a packed value for the [WM_TOUCHHITTESTING message](../inputmsg/wm-touchhittesting.md) callback.</span></span> <br/> |
| [<span data-ttu-id="ec738-118">**Registertouchhittestingwindow**</span><span class="sxs-lookup"><span data-stu-id="ec738-118">**RegisterTouchHitTestingWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | <span data-ttu-id="ec738-119">Registriert ein Fenster zur Verarbeitung der [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="ec738-119">Registers a window to process the [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) notification</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="ec738-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec738-120">Related topics</span></span>

[<span data-ttu-id="ec738-121">Referenz zu Berührungs Treffer Tests</span><span class="sxs-lookup"><span data-stu-id="ec738-121">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)
