---
description: Quality-Control Verwaltung
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Quality-Control Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343542"
---
# <a name="quality-control-management"></a><span data-ttu-id="41d26-103">Quality-Control Verwaltung</span><span class="sxs-lookup"><span data-stu-id="41d26-103">Quality-Control Management</span></span>

<span data-ttu-id="41d26-104">Bei der Qualitätskontrolle handelt es sich um einen Mechanismus, mit dem die Geschwindigkeit des Datenflusses über das Filter Diagramm als Reaktion auf die Laufzeitleistung angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="41d26-104">Quality control is a mechanism for adjusting the rate of data flow through the filter graph in response to run-time performance.</span></span> <span data-ttu-id="41d26-105">Wenn ein rendererfilter zu viele oder zu wenige Daten empfängt, kann er eine *Qualitäts Nachricht* senden.</span><span class="sxs-lookup"><span data-stu-id="41d26-105">If a renderer filter is receiving too much data or too little data, it can send a *quality message*.</span></span> <span data-ttu-id="41d26-106">Die Qualitäts Meldung fordert eine Anpassung in der Datenrate an.</span><span class="sxs-lookup"><span data-stu-id="41d26-106">The quality message requests an adjustment in the data rate.</span></span> <span data-ttu-id="41d26-107">Standardmäßig werden qualitativ hochwertige Nachrichten vom Renderer hoch bewegt, bis Sie einen Filter erreichen, der (sofern vorhanden) Antworten kann.</span><span class="sxs-lookup"><span data-stu-id="41d26-107">By default, quality messages travel upstream from the renderer until they reach a filter that can respond (if any).</span></span> <span data-ttu-id="41d26-108">Eine Anwendung kann auch einen benutzerdefinierten Quality Manager implementieren.</span><span class="sxs-lookup"><span data-stu-id="41d26-108">An application can also implement a custom quality manager.</span></span> <span data-ttu-id="41d26-109">In diesem Fall übergibt der Renderer Qualitäts Meldungen direkt an den Quality Manager der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="41d26-109">In that case, the renderer passes quality messages directly to the application's quality manager.</span></span>

<span data-ttu-id="41d26-110">Dieser Artikel enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="41d26-110">This article contains the following topics.</span></span>

-   [<span data-ttu-id="41d26-111">Qualitäts Meldungen</span><span class="sxs-lookup"><span data-stu-id="41d26-111">Quality Messages</span></span>](quality-messages.md)
-   [<span data-ttu-id="41d26-112">Standardmäßige Qualitätskontrolle</span><span class="sxs-lookup"><span data-stu-id="41d26-112">Default Quality Control</span></span>](default-quality-control.md)

## <a name="related-topics"></a><span data-ttu-id="41d26-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41d26-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41d26-114">Datenfluss für Filter Entwickler</span><span class="sxs-lookup"><span data-stu-id="41d26-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="41d26-115">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="41d26-115">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



