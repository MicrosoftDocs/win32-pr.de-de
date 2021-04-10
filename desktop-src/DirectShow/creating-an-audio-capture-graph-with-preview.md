---
description: Erstellen eines audioerfassungs Diagramms mit Vorschau
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: Erstellen eines audioerfassungs Diagramms mit Vorschau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2962dc0ffa08e19618d81a03515e970dcb439913
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958104"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a><span data-ttu-id="9201e-103">Erstellen eines audioerfassungs Diagramms mit Vorschau</span><span class="sxs-lookup"><span data-stu-id="9201e-103">Creating an Audio Capture Graph with Preview</span></span>

<span data-ttu-id="9201e-104">Das in [Erstellen eines audioerfassungs Diagramms](creating-an-audio-capture-graph.md) beschriebene Filter Diagramm führt nur die Erfassung durch und ohne Vorschau.</span><span class="sxs-lookup"><span data-stu-id="9201e-104">The filter graph described in [Creating an Audio Capture Graph](creating-an-audio-capture-graph.md) performs capture only, with no preview.</span></span> <span data-ttu-id="9201e-105">Um gleichzeitig eine Vorschau und Erfassung durchführen zu können, muss das Filter Diagramm den [unendlichen Pin-Tee-Filter](infinite-pin-tee-filter.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="9201e-105">To preview and capture at the same time, the filter graph needs to use the [Infinite Pin Tee Filter](infinite-pin-tee-filter.md).</span></span> <span data-ttu-id="9201e-106">Dieser Filter verfügt über eine Eingabe-PIN und erstellt bei Bedarf beliebig viele Ausgabe Pins.</span><span class="sxs-lookup"><span data-stu-id="9201e-106">This filter has one input pin and creates as many output pins as needed.</span></span> <span data-ttu-id="9201e-107">(Er beginnt mit einer Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="9201e-107">(It starts with one output pin.</span></span> <span data-ttu-id="9201e-108">Jedes Mal, wenn Sie eine Ausgabe-PIN verbinden, wird eine andere erstellt.) Der Filter für unendliche Pin-Empfänger übermittelt alle empfangenen Stichproben, unverändert, über alle Ausgabe Pins.</span><span class="sxs-lookup"><span data-stu-id="9201e-108">Each time you connect an output pin, it creates another one.) The Infinite Pin Tee filter delivers every sample that it receives, unchanged, through all of its output pins.</span></span>

<span data-ttu-id="9201e-109">Verbinden Sie den audioerfassungs Filter mit dem unendlichen Pin-Tee, und verbinden Sie den unbegrenzten Pin-Empfänger mit dem Multiplexer und dem [DirectSound-rendererfilter](directsound-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="9201e-109">Connect the Audio Capture Filter to the Infinite Pin Tee, and connect the Infinite Pin Tee to the multiplexer and the [DirectSound Renderer Filter](directsound-renderer-filter.md).</span></span> <span data-ttu-id="9201e-110">Verbinden Sie den Multiplexer wie zuvor mit dem dateiwriter.</span><span class="sxs-lookup"><span data-stu-id="9201e-110">Connect the multiplexer to the file writer, as before.</span></span> <span data-ttu-id="9201e-111">Das folgende Diagramm veranschaulicht das resultierende Filter Diagramm für eine AVI-Datei.</span><span class="sxs-lookup"><span data-stu-id="9201e-111">The following diagram illustrates the resulting filter graph for an AVI file.</span></span>

![audioerfassungs Diagramm mit Vorschau](images/audio-capture-graph.png)

<span data-ttu-id="9201e-113">Da der DirectSound-Renderer der Standardaudiorenderer ist, können Sie einfach die [**igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) -Methode für die Ausgabepin des unendlichen Pin-Ausstellers aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9201e-113">Because the DirectSound Renderer is the default audio renderer, you can simply call the [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) method on the Infinite Pin Tee's output pin.</span></span> <span data-ttu-id="9201e-114">Der Filter Graph-Manager verwendet [Intelligent Connect](intelligent-connect.md) , um den Renderer zu erstellen, ihn dem Filter Diagramm hinzuzufügen und die Pins zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="9201e-114">The Filter Graph Manager uses [Intelligent Connect](intelligent-connect.md) to create the renderer, add it to the filter graph, and connect the pins.</span></span>

> [!Note]  
> <span data-ttu-id="9201e-115">Wenn Sie Audiodaten von einem Mikrofon erfassen und eine Vorschau von einem Redner auf demselben Computer anzeigen, können Sie Audiofeedback erstellen.</span><span class="sxs-lookup"><span data-stu-id="9201e-115">If you capture audio from a microphone and preview it from a speaker on the same computer, you might create audio feedback.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9201e-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9201e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9201e-117">Audioerfassung</span><span class="sxs-lookup"><span data-stu-id="9201e-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



