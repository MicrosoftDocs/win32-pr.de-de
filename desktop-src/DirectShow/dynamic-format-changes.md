---
description: Dynamische Format Änderungen
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Dynamische Format Änderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339656"
---
# <a name="dynamic-format-changes"></a><span data-ttu-id="4eb6d-103">Dynamische Format Änderungen</span><span class="sxs-lookup"><span data-stu-id="4eb6d-103">Dynamic Format Changes</span></span>

<span data-ttu-id="4eb6d-104">Wenn zwei Filter eine Verbindung herstellen, stimmen Sie einem Medientyp zu, der das Format der Daten beschreibt, die der Upstream-Filter bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4eb6d-104">When two filters connect, they agree on a media type, which describes the format of the data that the upstream filter will deliver.</span></span> <span data-ttu-id="4eb6d-105">In den meisten Fällen ist der Medientyp für die Dauer der Verbindung korrigiert.</span><span class="sxs-lookup"><span data-stu-id="4eb6d-105">In most cases, the media type is fixed for the duration of the connection.</span></span> <span data-ttu-id="4eb6d-106">DirectShow bietet jedoch eingeschränkte Unterstützung für Filter zum Ändern des Medientyps.</span><span class="sxs-lookup"><span data-stu-id="4eb6d-106">However, DirectShow does offer limited support for filters to change the media type.</span></span> <span data-ttu-id="4eb6d-107">Wenn ein Filter die Medientypen wechselt, wird er als *dynamische Formatänderung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4eb6d-107">When a filter switches media types, it is called a *dynamic format change*.</span></span> <span data-ttu-id="4eb6d-108">Wenn Sie einen DirectShow-Filter schreiben, sollten Sie sich mit den Mechanismen für dynamische Formatänderungen vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="4eb6d-108">If you are writing a DirectShow filter, you should be aware of the mechanisms for dynamic format changes.</span></span> <span data-ttu-id="4eb6d-109">Auch wenn der Filter solche Änderungen nicht unterstützt, sollte er ordnungsgemäß reagieren, wenn ein anderer Filter ein neues Format anfordert.</span><span class="sxs-lookup"><span data-stu-id="4eb6d-109">Even if your filter does not support such changes, it should respond correctly if another filter requests a new format.</span></span>

<span data-ttu-id="4eb6d-110">DirectShow definiert mehrere verschiedene Mechanismen für dynamische Formatänderungen, abhängig vom Status des Filter Diagramms und dem erforderlichen Änderungstyp.</span><span class="sxs-lookup"><span data-stu-id="4eb6d-110">DirectShow defines several distinct mechanisms for dynamic format changes, depending on the state of filter graph and the type of change that is required.</span></span>

-   <span data-ttu-id="4eb6d-111">Wenn das Diagramm angehalten wurde, können die Pins erneut eine Verbindung herstellen und den Medientyp erneut aushandeln.</span><span class="sxs-lookup"><span data-stu-id="4eb6d-111">If the graph is stopped, the pins can reconnect and renegotiate the media type.</span></span> <span data-ttu-id="4eb6d-112">Weitere Informationen finden Sie unter Verbinden von [Pins](reconnecting-pins.md).</span><span class="sxs-lookup"><span data-stu-id="4eb6d-112">For more information, see [Reconnecting Pins](reconnecting-pins.md).</span></span>
-   <span data-ttu-id="4eb6d-113">Einige Filter können Pins erneut verbinden, auch wenn das Diagramm aktiv ist (wird ausgeführt oder angehalten).</span><span class="sxs-lookup"><span data-stu-id="4eb6d-113">Some filters can reconnect pins even while the graph is active (running or paused).</span></span> <span data-ttu-id="4eb6d-114">Weitere Informationen zu diesem Mechanismus finden Sie unter [Dynamic Reconnection](dynamic-reconnection.md).</span><span class="sxs-lookup"><span data-stu-id="4eb6d-114">For more information about this mechanism, see [Dynamic Reconnection](dynamic-reconnection.md).</span></span>

<span data-ttu-id="4eb6d-115">Wenn das Diagramm aktiv ist, die fraglichen Filter jedoch keine dynamischen Pin-Neuverbindungen unterstützen, gibt es drei mögliche Mechanismen, um das Format zu ändern:</span><span class="sxs-lookup"><span data-stu-id="4eb6d-115">Otherwise, if the graph is active, but the filters in question do not support dynamic pin reconnections, there are three possible mechanisms for changing the format:</span></span>

-   <span data-ttu-id="4eb6d-116">[Queryaccept (Downstream)](queryaccept--downstream.md) wird verwendet, wenn eine Ausgabepin eine Formatänderung an den downstreampeer vorschlägt, aber nur, wenn das neue Format keinen größeren Puffer erfordert.</span><span class="sxs-lookup"><span data-stu-id="4eb6d-116">[QueryAccept (Downstream)](queryaccept--downstream.md) is used when If an output pin proposes a format change to its downstream peer, but only if the new format does not require a larger buffer.</span></span>
-   <span data-ttu-id="4eb6d-117">[Queryaccept (Upstream)](queryaccept--upstream.md) wird verwendet, wenn eine Eingabe-PIN eine Formatänderung an Ihren upstreampeer vorschlägt.</span><span class="sxs-lookup"><span data-stu-id="4eb6d-117">[QueryAccept (Upstream)](queryaccept--upstream.md) is used when an input pin proposes a format change to its upstream peer.</span></span> <span data-ttu-id="4eb6d-118">Das neue Format kann dieselbe Größe aufweisen oder größer sein.</span><span class="sxs-lookup"><span data-stu-id="4eb6d-118">The new format can be the same size, or it can be larger.</span></span>
-   <span data-ttu-id="4eb6d-119">[Receiveconnection](receiveconnection.md) wird verwendet, wenn eine Ausgabepin eine Formatänderung an den downstreampeer vorschlägt und das neue Format einen größeren Puffer erfordert.</span><span class="sxs-lookup"><span data-stu-id="4eb6d-119">[ReceiveConnection](receiveconnection.md) is used when an output pin proposes a format change to its downstream peer, and the new format requires a larger buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4eb6d-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4eb6d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eb6d-121">Verarbeiten von Format Änderungen vom Videorenderer</span><span class="sxs-lookup"><span data-stu-id="4eb6d-121">Handling Format Changes from the Video Renderer</span></span>](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



