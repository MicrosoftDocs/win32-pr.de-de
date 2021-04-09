---
title: Berührungs Treffer Tests
description: Die Themen in diesem Abschnitt bieten eine Übersicht über die Unterstützung für Berührungs Treffer Tests in Windows 8.
ms.assetid: bdd7630c-b2d8-4080-a149-efec018f697d
keywords:
- Benutzereingriff
- input
- Zeiger
- Toucheingabe
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 8cf6d28badb47a176a6feccf166344003faf1de8
ms.sourcegitcommit: 9e389b8e39616dcef8f7ff4bc53d945179401478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/07/2020
ms.locfileid: "103857968"
---
# <a name="touch-hit-testing"></a><span data-ttu-id="75917-107">Berührungs Treffer Tests</span><span class="sxs-lookup"><span data-stu-id="75917-107">Touch Hit Testing</span></span>

## <a name="purpose"></a><span data-ttu-id="75917-108">Zweck</span><span class="sxs-lookup"><span data-stu-id="75917-108">Purpose</span></span>

<span data-ttu-id="75917-109">Die Themen in diesem Abschnitt bieten eine Übersicht über die Unterstützung für Berührungs Treffer Tests in Windows.</span><span class="sxs-lookup"><span data-stu-id="75917-109">The topics in this section provide an overview of support for Touch Hit Testing in Windows.</span></span> <span data-ttu-id="75917-110">Mit Berührungs Treffer Tests können Sie ein Eingabe Ziel ermitteln, je nachdem, ob der Inhalts Bereich eines UI-Elements in den Kontaktbereich fällt oder den Kontaktpunkt enthält.</span><span class="sxs-lookup"><span data-stu-id="75917-110">Touch Hit Testing lets you identify an input target based on whether the content area of a UI element falls within the contact area or includes the contact point.</span></span>

<span data-ttu-id="75917-111">Beim Berührungs Treffer Test wird anstelle einer einzelnen x-y-Koordinate eine komplexe Kontakt Geometrie für den gesamten berührungsbereich verwendet.</span><span class="sxs-lookup"><span data-stu-id="75917-111">Touch hit testing uses complex contact geometry for the entire touch area rather than a single interpolated x-y coordinate.</span></span> <span data-ttu-id="75917-112">Die Verwendung der gesamten Kontakt Geometrie verbessert die Genauigkeit und Genauigkeit erheblich, wenn Sie das wahrscheinlichste Ziel der Fingereingabe angeben.</span><span class="sxs-lookup"><span data-stu-id="75917-112">Using the entire contact geometry greatly improves precision and accuracy when you're identifying the most likely target of touch input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="75917-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="75917-113">In this section</span></span>

| <span data-ttu-id="75917-114">Thema</span><span class="sxs-lookup"><span data-stu-id="75917-114">Topic</span></span> | <span data-ttu-id="75917-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75917-115">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="75917-116">Referenz zu Berührungs Treffer Tests</span><span class="sxs-lookup"><span data-stu-id="75917-116">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)<br/> | <span data-ttu-id="75917-117">Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für [Berührungs Treffer Tests](touch-hit-testing-portal.md).</span><span class="sxs-lookup"><span data-stu-id="75917-117">The topics in this section provide the reference specifications for [Touch Hit Testing](touch-hit-testing-portal.md).</span></span><br/> |

## <a name="developer-audience"></a><span data-ttu-id="75917-118">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="75917-118">Developer audience</span></span>

<span data-ttu-id="75917-119">Die APIs für die Berührungs Treffer Tests sind für Entwickler konzipiert, die Benutzeroberflächen-Frameworks erstellen, die eine konsistente, Berührungs optimierte Benutzeroberfläche für alle Desktop Anwendungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="75917-119">The Touch Hit Testing APIs are designed for developers who are building UI frameworks that provide a consistent touch-optimized user experience across desktop applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75917-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75917-120">Related topics</span></span>

[<span data-ttu-id="75917-121">Benutzerinteraktion</span><span class="sxs-lookup"><span data-stu-id="75917-121">User Interaction</span></span>](../user-interaction.md)
