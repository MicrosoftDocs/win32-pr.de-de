---
description: Direktes Hosting eines DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Direktes Hosting eines DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747657"
---
# <a name="directly-hosting-a-dmo"></a><span data-ttu-id="bac98-103">Direktes Hosting eines DMO</span><span class="sxs-lookup"><span data-stu-id="bac98-103">Directly Hosting a DMO</span></span>

<span data-ttu-id="bac98-104">In diesem Abschnitt wird beschrieben, wie eine Anwendung als direkter Client eines DMO fungieren kann.</span><span class="sxs-lookup"><span data-stu-id="bac98-104">This section describes how an application can act as the direct client of a DMO.</span></span> <span data-ttu-id="bac98-105">Die Anwendung übermittelt Eingaben an den DMO, der DMO erstellt eine Ausgabe, und die Anwendung verwendet die Ausgabe zum Rendern, zur weiteren Verarbeitung usw.</span><span class="sxs-lookup"><span data-stu-id="bac98-105">The application delivers input to the DMO, the DMO creates output, and the application uses the output for rendering, further processing, or anything else.</span></span> <span data-ttu-id="bac98-106">Die Anwendung ist für Probleme verantwortlich, wie z. b. Speicher Belegung, Zeitplanung und Synchronisierung und Threading.</span><span class="sxs-lookup"><span data-stu-id="bac98-106">The application is responsible for issues such as memory allocation, timing and synchronization, and threading.</span></span> <span data-ttu-id="bac98-107">Diese Anforderungen hängen von der Art der Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="bac98-107">These requirements will depend on the nature of the application.</span></span>

<span data-ttu-id="bac98-108">Die Informationen in diesem Abschnitt gelten auch, wenn Sie eine Komponente schreiben, die als Schicht zwischen einer Anwendung und einem DMO fungiert (z. b. ein ActiveX-Steuerelement, das ein DMO hostet).</span><span class="sxs-lookup"><span data-stu-id="bac98-108">The information in this section also applies if you are writing a component that acts as a layer between an application and a DMO (for example, an ActiveX Control that hosts a DMO).</span></span> <span data-ttu-id="bac98-109">Außerdem sollten Sie diesen Abschnitt lesen, wenn Sie ein DMO schreiben, da darin die Funktionen beschrieben werden, die von Ihrem DMO implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="bac98-109">In addition, you should read this section if you are writing a DMO, because it describes the functionality that your DMO must implement.</span></span>

<span data-ttu-id="bac98-110">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="bac98-110">This section contains the following topics:</span></span>

-   [<span data-ttu-id="bac98-111">Festlegen von Medientypen in einem DMO</span><span class="sxs-lookup"><span data-stu-id="bac98-111">Setting Media Types on a DMO</span></span>](setting-media-types-on-a-dmo.md)
-   [<span data-ttu-id="bac98-112">Verarbeiten von Daten in einem DMO</span><span class="sxs-lookup"><span data-stu-id="bac98-112">Processing Data in a DMO</span></span>](processing-data-in-a-dmo.md)
-   [<span data-ttu-id="bac98-113">Direkte Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="bac98-113">In-Place Processing</span></span>](in-place-processing.md)
-   [<span data-ttu-id="bac98-114">Optionale Streams</span><span class="sxs-lookup"><span data-stu-id="bac98-114">Optional Streams</span></span>](optional-streams.md)
-   [<span data-ttu-id="bac98-115">Implementieren von imediabuffer</span><span class="sxs-lookup"><span data-stu-id="bac98-115">Implementing IMediaBuffer</span></span>](implementing-imediabuffer.md)

## <a name="related-topics"></a><span data-ttu-id="bac98-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bac98-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bac98-117">Verwenden von dmos</span><span class="sxs-lookup"><span data-stu-id="bac98-117">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



