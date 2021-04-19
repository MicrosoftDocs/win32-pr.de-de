---
description: Herstellen der Verbindung von Filtern
ms.assetid: 6a126dd5-00fa-4ea6-b00a-09b7e1246874
title: Herstellen der Verbindung von Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a72b2540133e84e473e3e82896a6427b923319
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345386"
---
# <a name="how-filters-connect"></a><span data-ttu-id="271f8-103">Herstellen der Verbindung von Filtern</span><span class="sxs-lookup"><span data-stu-id="271f8-103">How Filters Connect</span></span>

<span data-ttu-id="271f8-104">In diesem Artikel wird beschrieben, wie Filter in DirectShow eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="271f8-104">This article describes how filters connect in DirectShow.</span></span> <span data-ttu-id="271f8-105">Der Artikel ist für Filter Entwickler gedacht.</span><span class="sxs-lookup"><span data-stu-id="271f8-105">The article is intended for filter developers.</span></span> <span data-ttu-id="271f8-106">Wenn Sie eine DirectShow-Anwendung schreiben, können Sie die hier dargestellten Details wahrscheinlich ignorieren.</span><span class="sxs-lookup"><span data-stu-id="271f8-106">If you are writing a DirectShow application, you can probably ignore the details presented here.</span></span>

<span data-ttu-id="271f8-107">Dieser Artikel enthält folgende Themen:</span><span class="sxs-lookup"><span data-stu-id="271f8-107">This article contains the following topics:</span></span>

-   [<span data-ttu-id="271f8-108">PIN-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="271f8-108">Pin Connections</span></span>](pin-connections.md)
-   [<span data-ttu-id="271f8-109">Aushandeln von Medientypen</span><span class="sxs-lookup"><span data-stu-id="271f8-109">Negotiating Media Types</span></span>](negotiating-media-types.md)
-   [<span data-ttu-id="271f8-110">Aushandeln von Zuweisungen</span><span class="sxs-lookup"><span data-stu-id="271f8-110">Negotiating Allocators</span></span>](negotiating-allocators.md)
-   [<span data-ttu-id="271f8-111">Bereitstellen einer benutzerdefinierten Zuweisung</span><span class="sxs-lookup"><span data-stu-id="271f8-111">Providing a Custom Allocator</span></span>](providing-a-custom-allocator.md)
-   [<span data-ttu-id="271f8-112">PIN wird wieder hergestellt</span><span class="sxs-lookup"><span data-stu-id="271f8-112">Reconnecting Pins</span></span>](reconnecting-pins.md)

## <a name="related-topics"></a><span data-ttu-id="271f8-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="271f8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="271f8-114">Cbasepin-Verbindungsprozess</span><span class="sxs-lookup"><span data-stu-id="271f8-114">CBasePin Connection Process</span></span>](cbasepin-connection-process.md)
</dt> <dt>

[<span data-ttu-id="271f8-115">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="271f8-115">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



