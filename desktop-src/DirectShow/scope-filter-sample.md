---
description: Bereich Filter Beispiel
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: Bereich Filter Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74ba823e68da1cd1faadd3e1e3acc4e613e2f42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481518"
---
# <a name="scope-filter-sample"></a><span data-ttu-id="730d4-103">Bereich Filter Beispiel</span><span class="sxs-lookup"><span data-stu-id="730d4-103">Scope Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="730d4-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="730d4-104">Description</span></span>

<span data-ttu-id="730d4-105">Der Bereichs Filter ist ein rendererfilter, der Audiodaten als Wellenformen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="730d4-105">The Scope filter is a renderer filter that displays sound data as wave forms.</span></span>

## <a name="usage"></a><span data-ttu-id="730d4-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="730d4-106">Usage</span></span>

<span data-ttu-id="730d4-107">Um diesen Filter zu verwenden, öffnen Sie GraphEdit und stellen eine Audiodatei (oder eine Videodatei mit einem Audiostream) dar.</span><span class="sxs-lookup"><span data-stu-id="730d4-107">To use this filter, open GraphEdit and render an audio file (or a video file with an audio stream).</span></span> <span data-ttu-id="730d4-108">Trennen Sie den audiorenderer temporär, und fügen Sie den Beispiel Filter Infinite-Pin Tee ([Info Filter Sample](inftee-filter-sample.md)) ein.</span><span class="sxs-lookup"><span data-stu-id="730d4-108">Disconnect the audio renderer temporarily and insert the Infinite-Pin Tee ([InfTee Filter Sample](inftee-filter-sample.md)) sample filter.</span></span> <span data-ttu-id="730d4-109">Stellen Sie erneut eine Verbindung mit dem audiorenderer her.</span><span class="sxs-lookup"><span data-stu-id="730d4-109">Reconnect the audio renderer.</span></span> <span data-ttu-id="730d4-110">Verbinden Sie dann die zweite Ausgabe-PIN des Infinite-Pin Tee-Filters mit dem Bereichs Filter.</span><span class="sxs-lookup"><span data-stu-id="730d4-110">Then connect the Infinite-Pin Tee filter's second output pin to the Scope filter.</span></span> <span data-ttu-id="730d4-111">Führen Sie nun das Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="730d4-111">Now run the graph.</span></span>

<span data-ttu-id="730d4-112">Das Fensterbereich wird als Dialogfeld, nicht als tatsächliches Fenster implementiert.</span><span class="sxs-lookup"><span data-stu-id="730d4-112">The Scope window is implemented as a dialog box, not as an actual window.</span></span> <span data-ttu-id="730d4-113">Entwickler, die Steuerelemente zum Ändern von Filter Parametern in Echtzeit erstellen, möchten möglicherweise eine Technik wie diese anstelle von Eigenschaften Seiten verwenden.</span><span class="sxs-lookup"><span data-stu-id="730d4-113">Developers creating control panels to alter filter parameters in real time might want to use a technique like this rather than property pages.</span></span>

<span data-ttu-id="730d4-114">Der Bereichs Filter veranschaulicht das Einrichten eines separaten Threads zum Verarbeiten von Daten.</span><span class="sxs-lookup"><span data-stu-id="730d4-114">The Scope filter demonstrates setting up a separate thread to process data.</span></span> <span data-ttu-id="730d4-115">In diesem Fall werden die Daten einfach in einen separaten Puffer in der [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode kopiert und anschließend im Fensterbereich im separaten Thread gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="730d4-115">In this case, the data is just copied to a separate buffer on the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, and is then drawn on the Scope window on the separate thread.</span></span>

<span data-ttu-id="730d4-116">Mit dem Bereichs Filter können Sie auch die Audioausgabe überwachen, um zu bestimmen, ob Sie das Clipping durchlaufen, sodass Sie den Gewinn anpassen können.</span><span class="sxs-lookup"><span data-stu-id="730d4-116">The Scope filter also enables you to monitor audio output to determine if you are clipping, so you can adjust the gain.</span></span>

<span data-ttu-id="730d4-117">Dieser Filter wird in GraphEdit als "oszillobereich" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="730d4-117">This filter appears in GraphEdit as "Oscilloscope."</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="730d4-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="730d4-118">Downloading the Sample</span></span>

<span data-ttu-id="730d4-119">Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="730d4-119">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="730d4-120">Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK \]*-Stamm \\ Beispiele \\ \\ multimediaredirectshow- \\ Filter \\ Bereich.</span><span class="sxs-lookup"><span data-stu-id="730d4-120">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="730d4-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="730d4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="730d4-122">DirectShow-Beispiele</span><span class="sxs-lookup"><span data-stu-id="730d4-122">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



