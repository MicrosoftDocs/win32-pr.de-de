---
description: Sie können audiodiagramme jederzeit ändern, um Stimmen oder gesamte unter Diagramme hinzuzufügen oder zu entfernen.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: "So wird's gemacht: Dynamisches Hinzufügen und Entfernen von Stimmen zu bzw. aus einem Audiodiagramm"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb26150b5614ec53e4cc4de5af74e9a14ee2a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129768"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a><span data-ttu-id="bf1c1-103">So wird's gemacht: Dynamisches Hinzufügen und Entfernen von Stimmen zu bzw. aus einem Audiodiagramm</span><span class="sxs-lookup"><span data-stu-id="bf1c1-103">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>

<span data-ttu-id="bf1c1-104">Sie können audiodiagramme jederzeit ändern, um Stimmen oder gesamte unter Diagramme hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-104">You can change audio graphs at any time to add or remove voices or entire subgraphs.</span></span> <span data-ttu-id="bf1c1-105">In diesem Thema wird gezeigt, wie Sie Teilmengen Stimmen aus einem Diagramm hinzufügen oder entfernen, das nach den Schritten in Gewusst [wie: Erstellen eines einfachen audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-105">This topic shows you how to add or remove submix voices from a graph that has been created following the steps in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="bf1c1-106">Eine einzelne Stimme kann Ihre Ausgabe an mehrere Stimmen oder an eine lange Reihe von Stimmen senden.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-106">A single voice can send its output to several voices or to a long chain of voices.</span></span> <span data-ttu-id="bf1c1-107">Das Entfernen oder Hinzufügen einer einzelnen Stimme kann eine große Auswirkung auf ein audiodiagramm haben.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-107">Removing or adding a single voice can have a large effect on an audio graph.</span></span>

## <a name="to-dynamically-change-an-audio-graph"></a><span data-ttu-id="bf1c1-108">So ändern Sie ein audiodiagramm dynamisch</span><span class="sxs-lookup"><span data-stu-id="bf1c1-108">To dynamically change an audio graph</span></span>

<span data-ttu-id="bf1c1-109">Das Hinzufügen und Entfernen von Stimmen aus einem audiodiagramm ähnelt dem Hinzufügen oder Entfernen von Knoten aus einer einzelnen verknüpften Liste oder einem einzelnen verknüpften Diagramm.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-109">Adding and removing voices from an audio graph is very similar to adding or removing nodes from a single-linked list or graph.</span></span>

-   <span data-ttu-id="bf1c1-110">So fügen Sie einem audiodiagramm eine Stimme oder ein unter Diagramm hinzu</span><span class="sxs-lookup"><span data-stu-id="bf1c1-110">To add a voice or subgraph to an audio graph</span></span>

    <span data-ttu-id="bf1c1-111">Legen Sie die Ausgabe einer Stimme im Diagramm, der übergeordneten Stimme, auf die Stimme fest, die mit der [**setoutputvoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) -Funktion hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-111">Set the output of a voice in the graph, the parent voice, to the voice to be added using the [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) function.</span></span> <span data-ttu-id="bf1c1-112">Legen Sie die Ausgabe der neuen Stimme auf das ursprüngliche untergeordnete Element der übergeordneten Stimme fest.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-112">Set the output of the new voice to the original child of the parent voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   <span data-ttu-id="bf1c1-113">So entfernen Sie eine Stimme oder ein unter Diagramm aus einem audiodiagramm</span><span class="sxs-lookup"><span data-stu-id="bf1c1-113">To remove a voice or subgraph from an audio graph</span></span>

    <span data-ttu-id="bf1c1-114">Legen Sie die Ausgabesprache des übergeordneten Elements der zu entfernenden Stimme auf das untergeordnete Element der zu entfernenden Stimme fest.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-114">Set the output voice of the parent of the voice being removed to the child of the voice being removed.</span></span> <span data-ttu-id="bf1c1-115">Wenn sich die zu entfernende Stimme am Ende des Diagramms befindet, sollte die übergeordnete Stimme so geändert werden, dass Sie auf die Master Stimme verweist.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-115">If the voice being removed is at the end of the graph, the parent voice should be changed to point to the master voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

<span data-ttu-id="bf1c1-116">Beachten Sie, dass für die Übersichtlichkeit jedes übergeordnete Element in diesen Beispielen nur ein untergeordnetes</span><span class="sxs-lookup"><span data-stu-id="bf1c1-116">Note that for clarity each parent only has one child in these examples.</span></span> <span data-ttu-id="bf1c1-117">Wenn ein übergeordneter Knoten über mehrere untergeordnete Knoten verfügt, enthält seine sendlist anstelle eines Zeigers nur eine Stimme ein Array von Stimmen.</span><span class="sxs-lookup"><span data-stu-id="bf1c1-117">If a parent node has multiple children, its sendlist will contain an array of voices instead of a pointer to just one voice.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf1c1-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf1c1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf1c1-119">Audiodiagramme</span><span class="sxs-lookup"><span data-stu-id="bf1c1-119">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="bf1c1-120">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="bf1c1-120">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="bf1c1-121">So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="bf1c1-121">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="bf1c1-122">So wird's gemacht: Verwenden von Submixstimmen</span><span class="sxs-lookup"><span data-stu-id="bf1c1-122">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="bf1c1-123">So wird's gemacht: Erstellen einer Effektkette</span><span class="sxs-lookup"><span data-stu-id="bf1c1-123">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 
