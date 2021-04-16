---
description: Ein Versions Vektor verarbeitet bedingte Kommentare in einer HTML-Webseite. Das heißt, dass Versions Vektoren es Ihnen ermöglichen, Markup basierend auf der Browserversion zu erstellen.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Versionsvektoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41fb0b24a205b280be163caeb63287fc5036b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350548"
---
# <a name="version-vectors"></a><span data-ttu-id="f2581-104">Versionsvektoren</span><span class="sxs-lookup"><span data-stu-id="f2581-104">Version Vectors</span></span>

<span data-ttu-id="f2581-105">Ein *Versions Vektor* verarbeitet bedingte Kommentare in einer HTML-Webseite.</span><span class="sxs-lookup"><span data-stu-id="f2581-105">A *version vector* processes conditional comments in an HTML webpage.</span></span> <span data-ttu-id="f2581-106">Das heißt, dass Versions Vektoren es Ihnen ermöglichen, Markup basierend auf der Browserversion zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f2581-106">That is, version vectors enable you to create markup based on the browser version.</span></span>

<span data-ttu-id="f2581-107">Betrachten Sie das folgende Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="f2581-107">Consider the following code example.</span></span>


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



<span data-ttu-id="f2581-108">Wenn in diesem Fall die Windows Internet Explorer-Browserversion mindestens 5,5 ist, wird der entsprechende Absatz auf der Webseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f2581-108">In this case, if the Windows Internet Explorer browser version is at least 5.5, the corresponding paragraph is displayed in the webpage.</span></span> <span data-ttu-id="f2581-109">Obwohl die erste Bedingung in diesem Beispiel die Funktion von bedingten Kommentaren veranschaulicht, werden diese Kommentare in der Regel nicht verwendet, um Markup wie die erste Bedingung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f2581-109">Although the first condition in this example illustrates the function of conditional comments, these comments are not typically used to display markup like the first condition.</span></span> <span data-ttu-id="f2581-110">Stattdessen sind die verbleibenden bedingten Kommentare im vorherigen Beispiel häufiger.</span><span class="sxs-lookup"><span data-stu-id="f2581-110">Instead, the remaining conditional comments in the previous example are more common.</span></span> <span data-ttu-id="f2581-111">In diesen übrigen Kommentaren verwenden die bedingten Kommentare ein anderes Stylesheet für jede andere Version des Browsers.</span><span class="sxs-lookup"><span data-stu-id="f2581-111">In these remaining comments, the conditional comments use a different style sheet for each different version of the browser.</span></span>

<span data-ttu-id="f2581-112">Im vorangehenden Codebeispiel wird außerdem überprüft, ob Microsoft Internet Explorer 6 und Windows Internet Explorer 7 gleich sind.</span><span class="sxs-lookup"><span data-stu-id="f2581-112">The preceding code example also checks for equality for Microsoft Internet Explorer 6 and Windows Internet Explorer 7.</span></span> <span data-ttu-id="f2581-113">Für Windows Internet Explorer 8 verwendet das Beispiel den GTE-Operator (größer als oder gleich).</span><span class="sxs-lookup"><span data-stu-id="f2581-113">But for Windows Internet Explorer 8, the example uses the gte operator (greater than or equal).</span></span> <span data-ttu-id="f2581-114">Dieser Operator unterstützt in Zukunft das Beispiel, sodass die standardkonforme Version des Stylesheets verwendet wird, wenn eine neue Version des Browsers freigegeben wird (anstatt das falsche Stylesheet oder kein Stylesheet zu verwenden).</span><span class="sxs-lookup"><span data-stu-id="f2581-114">This operator helps future-proof the example so that the most standards-compliant version of the style sheet is used when a new version of the browser is released (instead of using the wrong style sheet or no style sheet).</span></span> <span data-ttu-id="f2581-115">Vorhandene Anwendungen sind häufig nicht in der Lage, eine Version von Internet Explorer in der Vergangenheit 7 (oder die neueste Version von Internet Explorer, für die die Website erstellt wurde) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2581-115">Existing applications often do not consider a version of Internet Explorer past 7 (or the newest version of Internet Explorer that the site is built for).</span></span> <span data-ttu-id="f2581-116">Weitere Informationen zu Versions Vektoren finden Sie unter [Versions Vektoren](/previous-versions/cc817577(v=msdn.10)) in der MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="f2581-116">For more information about version vectors, see [Version Vectors](/previous-versions/cc817577(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2581-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2581-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2581-118">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht</span><span class="sxs-lookup"><span data-stu-id="f2581-118">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



