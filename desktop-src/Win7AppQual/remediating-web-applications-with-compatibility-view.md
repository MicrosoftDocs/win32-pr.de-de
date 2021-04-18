---
description: .
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43f4ff54a919058127a5f72ba60f3683c6583e1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106371828"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a><span data-ttu-id="b291d-103">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht</span><span class="sxs-lookup"><span data-stu-id="b291d-103">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>

<span data-ttu-id="b291d-104">In diesem Abschnitt werden die grundlegenden Schritte zur Entschärfung beschrieben und erläutert, wie Sie zukünftige Anwendungs Kompatibilität planen, während Sie Probleme beheben.</span><span class="sxs-lookup"><span data-stu-id="b291d-104">This section describes basic mitigation steps and how to plan for future application compatibility while you are addressing any issues now.</span></span>

<span data-ttu-id="b291d-105">Windows Internet Explorer unterstützt die älteren Internet Explorer-Modelle, wenn dies möglich ist, sodass Websites, die Sie für diese entwickeln, sich in neueren Versionen von Internet Explorer weiterhin erwartungsgemäß verhalten.</span><span class="sxs-lookup"><span data-stu-id="b291d-105">Windows Internet Explorer supports the legacy Internet Explorer models whenever feasible so that sites that you develop to them continue to behave as expected in newer versions of Internet Explorer.</span></span> <span data-ttu-id="b291d-106">Ab Windows Internet Explorer 8 können Sie das Legacy Verhalten unterstützen, indem Sie den Renderingmodus Seite für Seite auswählen.</span><span class="sxs-lookup"><span data-stu-id="b291d-106">Starting with Windows Internet Explorer 8, you can choose to support legacy behaviors by selecting the rendering mode on a page-by-page basis.</span></span>

<span data-ttu-id="b291d-107">Internet Explorer 8 umfasst die folgenden Renderingmodi, die Sie mit dem X-UA-kompatiblen Header festlegen können.</span><span class="sxs-lookup"><span data-stu-id="b291d-107">Internet Explorer 8 includes the following rendering modes that you can set by using the X-UA-Compatible header.</span></span>



| <span data-ttu-id="b291d-108">Wert für „content“</span><span class="sxs-lookup"><span data-stu-id="b291d-108">Content value</span></span> | <span data-ttu-id="b291d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b291d-109">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b291d-110">IE=5</span><span class="sxs-lookup"><span data-stu-id="b291d-110">IE=5</span></span>          | <span data-ttu-id="b291d-111">Verwenden Sie den quirsmodus.</span><span class="sxs-lookup"><span data-stu-id="b291d-111">Use quirks mode.</span></span>                                                                      |
| <span data-ttu-id="b291d-112">IE = 7</span><span class="sxs-lookup"><span data-stu-id="b291d-112">IE=7</span></span>          | <span data-ttu-id="b291d-113">Verwenden Sie immer den Windows Internet Explorer 7-Modus.</span><span class="sxs-lookup"><span data-stu-id="b291d-113">Always use Windows Internet Explorer 7 mode.</span></span>                                          |
| <span data-ttu-id="b291d-114">IE=EmulateIE7</span><span class="sxs-lookup"><span data-stu-id="b291d-114">IE=EmulateIE7</span></span> | <span data-ttu-id="b291d-115">Anzeige im Internet Explorer 7-Modus, es sei denn, die Website verfügt über den quiringdoctype.</span><span class="sxs-lookup"><span data-stu-id="b291d-115">Display in Internet Explorer 7 mode unless the site has the quirks DOCTYPE.</span></span>           |
| <span data-ttu-id="b291d-116">IE = 8</span><span class="sxs-lookup"><span data-stu-id="b291d-116">IE=8</span></span>          | <span data-ttu-id="b291d-117">Verwenden Sie immer den Internet Explorer 8-Modus.</span><span class="sxs-lookup"><span data-stu-id="b291d-117">Always use Internet Explorer 8 mode.</span></span>                                                  |
| <span data-ttu-id="b291d-118">IE=EmulateIE8</span><span class="sxs-lookup"><span data-stu-id="b291d-118">IE=EmulateIE8</span></span> | <span data-ttu-id="b291d-119">Überschreiben Sie die Kompatibilitäts Ansicht auf Client Computern und den Internet Explorer 8-Modus.</span><span class="sxs-lookup"><span data-stu-id="b291d-119">Override Compatibility View on client machines and use Internet Explorer 8 mode.</span></span>      |
| <span data-ttu-id="b291d-120">IE=Edge</span><span class="sxs-lookup"><span data-stu-id="b291d-120">IE=Edge</span></span>       | <span data-ttu-id="b291d-121">Wird im aktuellen Modus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b291d-121">Display in the latest mode.</span></span> <span data-ttu-id="b291d-122">In Internet Explorer 8 entspricht dieser Wert IE = 8.</span><span class="sxs-lookup"><span data-stu-id="b291d-122">In Internet Explorer 8, this value is equivalent to IE=8.</span></span> |



 

<span data-ttu-id="b291d-123">In den folgenden Themen wird beschrieben, wie Webanwendungen mithilfe der Kompatibilitäts Ansicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b291d-123">The following topics describe how to update web applications by using Compatibility View.</span></span>



| <span data-ttu-id="b291d-124">Thema</span><span class="sxs-lookup"><span data-stu-id="b291d-124">Topic</span></span>                                                                                                  | <span data-ttu-id="b291d-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b291d-125">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="b291d-126">Was ist die Kompatibilitäts Ansicht?</span><span class="sxs-lookup"><span data-stu-id="b291d-126">What Is Compatibility View</span></span>](what-is-compatibility-view-.md)                                          | <span data-ttu-id="b291d-127">Beschreibt die Kompatibilitäts Ansicht.</span><span class="sxs-lookup"><span data-stu-id="b291d-127">Describes Compatibility View.</span></span>                                                  |
| [<span data-ttu-id="b291d-128">Warum benötigen Sie eine Kompatibilitäts Ansicht?</span><span class="sxs-lookup"><span data-stu-id="b291d-128">Why Do You Need Compatibility View?</span></span>](why-do-you-need-compatibility-view-.md)                         | <span data-ttu-id="b291d-129">Beschreibt, warum Sie die Kompatibilitäts Ansicht verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="b291d-129">Describes why you should use Compatibility View.</span></span>                               |
| [<span data-ttu-id="b291d-130">Verwenden des Meta-Tags zum Sicherstellen der zukünftigen Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="b291d-130">Use the Meta Tag to Ensure Future Compatibility</span></span>](use-the-meta-tag-to-ensure-future-compatibility.md) | <span data-ttu-id="b291d-131">Beschreibt, wie Sie mit dem **Meta** -Element zukünftige Kompatibilität gewährleisten können.</span><span class="sxs-lookup"><span data-stu-id="b291d-131">Describes how you can use the **meta** element to ensure future compatibility.</span></span> |



 

 

 



