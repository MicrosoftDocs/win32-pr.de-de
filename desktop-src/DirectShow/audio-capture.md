---
description: Audioerfassung
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Audioerfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104342018"
---
# <a name="audio-capture"></a><span data-ttu-id="62da2-103">Audioerfassung</span><span class="sxs-lookup"><span data-stu-id="62da2-103">Audio Capture</span></span>

<span data-ttu-id="62da2-104">Eine Anwendung kann mithilfe von DirectShow Audiodaten von Mikrofonen, Band Playern und anderen Geräten über die Eingaben auf der Soundkarte erfassen.</span><span class="sxs-lookup"><span data-stu-id="62da2-104">An application can use DirectShow to capture audio data from microphones, tape players, and other devices, through the inputs on the sound card.</span></span> <span data-ttu-id="62da2-105">Zu den typischen Szenarien gehören:</span><span class="sxs-lookup"><span data-stu-id="62da2-105">Typical scenarios include:</span></span>

-   <span data-ttu-id="62da2-106">Aufzeichnen von VoiceOver-Erzählungen zum späteren DUBBING über einen Videostream.</span><span class="sxs-lookup"><span data-stu-id="62da2-106">Recording a voiceover narration for later dubbing over a video stream.</span></span>
-   <span data-ttu-id="62da2-107">Die typinstallation von Inhalt von Legacy-Inhalt in das digitale Format.</span><span class="sxs-lookup"><span data-stu-id="62da2-107">Converting legacy analog audio content to digital format.</span></span>
-   <span data-ttu-id="62da2-108">Erfassen von Stimme oder Musik für die Übertragung über ein Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="62da2-108">Capturing voice or music for transmission over a network.</span></span>

<span data-ttu-id="62da2-109">Endbenutzer haben mehrere Optionen zum Erfassen von Audio von der Soundkarte auf der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="62da2-109">End users have several options for capturing audio from the sound card to the hard disk.</span></span> <span data-ttu-id="62da2-110">Bei den meisten Karten werden Anwendungen zum Mischen und Aufzeichnen von Audioeingaben bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="62da2-110">Most cards provide applications for mixing and recording from their audio inputs.</span></span> <span data-ttu-id="62da2-111">Windows bietet Sound Recorder, eine einfache hilfsprogrammanwendung für die Aufzeichnung von einem Mikrofon.</span><span class="sxs-lookup"><span data-stu-id="62da2-111">Windows provides Sound Recorder, a simple utility application for recording from a microphone.</span></span> <span data-ttu-id="62da2-112">Der Windows Media Encoder kann als [DirectX-Medienobjekt](directx-media-objects.md) (DMO) in eine DirectShow-Anwendung integriert werden.</span><span class="sxs-lookup"><span data-stu-id="62da2-112">The Windows Media Encoder can be incorporated into a DirectShow application as a [DirectX Media Object](directx-media-objects.md) (DMO).</span></span> <span data-ttu-id="62da2-113">In diesem Abschnitt wird beschrieben, wie Sie die audioerfassungs Funktionalität in Ihre eigene Anwendung mithilfe von DirectShow integrieren.</span><span class="sxs-lookup"><span data-stu-id="62da2-113">This section describes how to integrate audio capture functionality within your own application using DirectShow.</span></span>

<span data-ttu-id="62da2-114">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="62da2-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="62da2-115">Informationen zum audioerfassungs Filter</span><span class="sxs-lookup"><span data-stu-id="62da2-115">About the Audio Capture Filter</span></span>](about-the-audio-capture-filter.md)
-   [<span data-ttu-id="62da2-116">Auswählen eines Erfassungs Geräts</span><span class="sxs-lookup"><span data-stu-id="62da2-116">Selecting a Capture Device</span></span>](selecting-a-capture-device.md)
-   [<span data-ttu-id="62da2-117">Erstellen eines audioerfassungs Diagramms</span><span class="sxs-lookup"><span data-stu-id="62da2-117">Creating an Audio Capture Graph</span></span>](creating-an-audio-capture-graph.md)
-   [<span data-ttu-id="62da2-118">Erstellen eines audioerfassungs Diagramms mit Vorschau</span><span class="sxs-lookup"><span data-stu-id="62da2-118">Creating an Audio Capture Graph with Preview</span></span>](creating-an-audio-capture-graph-with-preview.md)
-   [<span data-ttu-id="62da2-119">Festlegen von Eigenschaften für die Audioerfassung</span><span class="sxs-lookup"><span data-stu-id="62da2-119">Setting Audio Capture Properties</span></span>](setting-audio-capture-properties.md)

## <a name="related-topics"></a><span data-ttu-id="62da2-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62da2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62da2-121">Verwenden von DirectShow</span><span class="sxs-lookup"><span data-stu-id="62da2-121">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



