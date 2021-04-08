---
description: Datenfluss im Filter Diagramm
ms.assetid: 3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3
title: Datenfluss im Filter Diagramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38e0e730dd78e3a42a1121e4a63a053e6016402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860500"
---
# <a name="data-flow-in-the-filter-graph"></a><span data-ttu-id="2ab1d-103">Datenfluss im Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="2ab1d-103">Data Flow in the Filter Graph</span></span>

<span data-ttu-id="2ab1d-104">In diesem Abschnitt wird beschrieben, wie Mediendaten durch das Filter Diagramm verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="2ab1d-104">This section describes how media data moves through the filter graph.</span></span> <span data-ttu-id="2ab1d-105">Normalerweise müssen Sie diese Details nicht kennen, um eine DirectShow-Anwendung zu schreiben. in manchen Situationen ist es jedoch möglicherweise hilfreich.</span><span class="sxs-lookup"><span data-stu-id="2ab1d-105">Usually, you do not need to know these details to write a DirectShow application, although in some situations you may find it helpful.</span></span> <span data-ttu-id="2ab1d-106">Wenn Sie einen DirectShow-Filter schreiben, müssen Sie dieses Material verstehen.</span><span class="sxs-lookup"><span data-stu-id="2ab1d-106">If you are writing a DirectShow filter, you will need to understand this material.</span></span>

<span data-ttu-id="2ab1d-107">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="2ab1d-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="2ab1d-108">Übersicht über den Datenfluss in DirectShow</span><span class="sxs-lookup"><span data-stu-id="2ab1d-108">Overview of Data Flow in DirectShow</span></span>](overview-of-data-flow-in-directshow.md)
-   [<span data-ttu-id="2ab1d-109">Transportprotokolle</span><span class="sxs-lookup"><span data-stu-id="2ab1d-109">Transports</span></span>](transports.md)
-   [<span data-ttu-id="2ab1d-110">Beispiele und Zuweisungen</span><span class="sxs-lookup"><span data-stu-id="2ab1d-110">Samples and Allocators</span></span>](samples-and-allocators.md)
-   [<span data-ttu-id="2ab1d-111">Filter Zustände</span><span class="sxs-lookup"><span data-stu-id="2ab1d-111">Filter States</span></span>](filter-states.md)
-   [<span data-ttu-id="2ab1d-112">Pullmodell</span><span class="sxs-lookup"><span data-stu-id="2ab1d-112">Pull Model</span></span>](pull-model.md)

## <a name="related-topics"></a><span data-ttu-id="2ab1d-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ab1d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ab1d-114">Datenfluss für Filter Entwickler</span><span class="sxs-lookup"><span data-stu-id="2ab1d-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> </dl>

 

 



