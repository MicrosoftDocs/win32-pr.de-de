---
description: Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5acb7249854d9ac89b5601fdf83efa397c11c17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116358"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a><span data-ttu-id="959f0-103">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht</span><span class="sxs-lookup"><span data-stu-id="959f0-103">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>

<span data-ttu-id="959f0-104">In diesem Abschnitt werden die grundlegenden Schritte zur Risikominderung und die Planung der zukünftigen Anwendungskompatibilität beschrieben, während Sie probleme beheben.</span><span class="sxs-lookup"><span data-stu-id="959f0-104">This section describes basic mitigation steps and how to plan for future application compatibility while you are addressing any issues now.</span></span>

<span data-ttu-id="959f0-105">Windows Internet Explorer unterstützt nach Möglichkeit die älteren Internet Explorer-Modelle, sodass sich Standorte, die Sie für sie entwickeln, in neueren Versionen von Internet Explorer weiterhin wie erwartet verhalten.</span><span class="sxs-lookup"><span data-stu-id="959f0-105">Windows Internet Explorer supports the legacy Internet Explorer models whenever feasible so that sites that you develop to them continue to behave as expected in newer versions of Internet Explorer.</span></span> <span data-ttu-id="959f0-106">Ab Windows Internet Explorer 8 können Sie Legacyverhalten unterstützen, indem Sie den Renderingmodus seiteweise auswählen.</span><span class="sxs-lookup"><span data-stu-id="959f0-106">Starting with Windows Internet Explorer 8, you can choose to support legacy behaviors by selecting the rendering mode on a page-by-page basis.</span></span>

<span data-ttu-id="959f0-107">Internet Explorer 8 enthält die folgenden Renderingmodi, die Sie mit dem X-UA-kompatiblen Header festlegen können.</span><span class="sxs-lookup"><span data-stu-id="959f0-107">Internet Explorer 8 includes the following rendering modes that you can set by using the X-UA-Compatible header.</span></span>



| <span data-ttu-id="959f0-108">Wert für „content“</span><span class="sxs-lookup"><span data-stu-id="959f0-108">Content value</span></span> | <span data-ttu-id="959f0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="959f0-109">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="959f0-110">IE=5</span><span class="sxs-lookup"><span data-stu-id="959f0-110">IE=5</span></span>          | <span data-ttu-id="959f0-111">Verwenden Sie den quirks-Modus.</span><span class="sxs-lookup"><span data-stu-id="959f0-111">Use quirks mode.</span></span>                                                                      |
| <span data-ttu-id="959f0-112">IE=7</span><span class="sxs-lookup"><span data-stu-id="959f0-112">IE=7</span></span>          | <span data-ttu-id="959f0-113">Verwenden Sie immer den Windows Internet Explorer 7-Modus.</span><span class="sxs-lookup"><span data-stu-id="959f0-113">Always use Windows Internet Explorer 7 mode.</span></span>                                          |
| <span data-ttu-id="959f0-114">IE=EmulateIE7</span><span class="sxs-lookup"><span data-stu-id="959f0-114">IE=EmulateIE7</span></span> | <span data-ttu-id="959f0-115">Wird im Modus Internet Explorer 7 angezeigt, es sei denn, die Website verfügt über den DOCTYPE-Typ derQuirks.</span><span class="sxs-lookup"><span data-stu-id="959f0-115">Display in Internet Explorer 7 mode unless the site has the quirks DOCTYPE.</span></span>           |
| <span data-ttu-id="959f0-116">IE=8</span><span class="sxs-lookup"><span data-stu-id="959f0-116">IE=8</span></span>          | <span data-ttu-id="959f0-117">Verwenden Sie immer Internet Explorer 8 Modus.</span><span class="sxs-lookup"><span data-stu-id="959f0-117">Always use Internet Explorer 8 mode.</span></span>                                                  |
| <span data-ttu-id="959f0-118">IE=EmulateIE8</span><span class="sxs-lookup"><span data-stu-id="959f0-118">IE=EmulateIE8</span></span> | <span data-ttu-id="959f0-119">Überschreiben Sie Kompatibilitätsansicht auf Clientcomputern, und verwenden Sie Internet Explorer 8-Modus.</span><span class="sxs-lookup"><span data-stu-id="959f0-119">Override Compatibility View on client machines and use Internet Explorer 8 mode.</span></span>      |
| <span data-ttu-id="959f0-120">IE=Edge</span><span class="sxs-lookup"><span data-stu-id="959f0-120">IE=Edge</span></span>       | <span data-ttu-id="959f0-121">Anzeige im aktuellen Modus.</span><span class="sxs-lookup"><span data-stu-id="959f0-121">Display in the latest mode.</span></span> <span data-ttu-id="959f0-122">In Internet Explorer 8 entspricht dieser Wert IE=8.</span><span class="sxs-lookup"><span data-stu-id="959f0-122">In Internet Explorer 8, this value is equivalent to IE=8.</span></span> |



 

<span data-ttu-id="959f0-123">In den folgenden Themen wird beschrieben, wie Webanwendungen mithilfe von Kompatibilitätsansicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="959f0-123">The following topics describe how to update web applications by using Compatibility View.</span></span>



| <span data-ttu-id="959f0-124">Thema</span><span class="sxs-lookup"><span data-stu-id="959f0-124">Topic</span></span>                                                                                                  | <span data-ttu-id="959f0-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="959f0-125">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="959f0-126">Was ist Kompatibilitätsansicht</span><span class="sxs-lookup"><span data-stu-id="959f0-126">What Is Compatibility View</span></span>](what-is-compatibility-view-.md)                                          | <span data-ttu-id="959f0-127">Beschreibt Kompatibilitätsansicht.</span><span class="sxs-lookup"><span data-stu-id="959f0-127">Describes Compatibility View.</span></span>                                                  |
| [<span data-ttu-id="959f0-128">Warum benötigen Sie Kompatibilitätsansicht?</span><span class="sxs-lookup"><span data-stu-id="959f0-128">Why Do You Need Compatibility View?</span></span>](why-do-you-need-compatibility-view-.md)                         | <span data-ttu-id="959f0-129">Beschreibt die Gründe für die Verwendung Kompatibilitätsansicht.</span><span class="sxs-lookup"><span data-stu-id="959f0-129">Describes why you should use Compatibility View.</span></span>                               |
| [<span data-ttu-id="959f0-130">Verwenden des Metatags zum Sicherstellen der zukünftigen Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="959f0-130">Use the Meta Tag to Ensure Future Compatibility</span></span>](use-the-meta-tag-to-ensure-future-compatibility.md) | <span data-ttu-id="959f0-131">Beschreibt, wie Sie das Metaelement **verwenden** können, um zukünftige Kompatibilität sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="959f0-131">Describes how you can use the **meta** element to ensure future compatibility.</span></span> |



 

 

 



