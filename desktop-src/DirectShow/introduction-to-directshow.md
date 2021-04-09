---
description: Einführung in DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Einführung in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01733db5f8168a67871ec1797f79cd10a90c6c22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124352"
---
# <a name="introduction-to-directshow"></a><span data-ttu-id="6369e-103">Einführung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6369e-103">Introduction to DirectShow</span></span>

<span data-ttu-id="6369e-104">Microsoft® DirectShow® ist eine Architektur für das Streaming von Medien auf der Microsoft Windows®-Plattform.</span><span class="sxs-lookup"><span data-stu-id="6369e-104">Microsoft® DirectShow® is an architecture for streaming media on the Microsoft Windows® platform.</span></span> <span data-ttu-id="6369e-105">DirectShow bietet eine qualitativ hochwertige Erfassung und Wiedergabe von Multimedia-Streams.</span><span class="sxs-lookup"><span data-stu-id="6369e-105">DirectShow provides for high-quality capture and playback of multimedia streams.</span></span> <span data-ttu-id="6369e-106">Es unterstützt eine Vielzahl von Formaten, einschließlich Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3) und wav Soundfiles.</span><span class="sxs-lookup"><span data-stu-id="6369e-106">It supports a wide variety of formats, including Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3), and WAV sound files.</span></span> <span data-ttu-id="6369e-107">Sie unterstützt die Erfassung von digitalen und analogen Geräten basierend auf dem Windows-Treibermodell (WDM) oder Video für Windows.</span><span class="sxs-lookup"><span data-stu-id="6369e-107">It supports capture from digital and analog devices based on the Windows Driver Model (WDM) or Video for Windows.</span></span> <span data-ttu-id="6369e-108">Sie erkennt und verwendet automatisch Video-und audioacceleration-Hardware, wenn Sie verfügbar ist, aber auch Systeme ohne Beschleunigung der Hardware unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6369e-108">It automatically detects and uses video and audio acceleration hardware when available, but also supports systems without acceleration hardware.</span></span>

<span data-ttu-id="6369e-109">DirectShow basiert auf dem Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="6369e-109">DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="6369e-110">Um eine DirectShow-Anwendung oder-Komponente zu schreiben, müssen Sie mit der com-Client Programmierung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="6369e-110">To write a DirectShow application or component, you must understand COM client programming.</span></span> <span data-ttu-id="6369e-111">Bei den meisten Anwendungen müssen Sie keine eigenen com-Objekte implementieren.</span><span class="sxs-lookup"><span data-stu-id="6369e-111">For most applications, you do not need to implement your own COM objects.</span></span> <span data-ttu-id="6369e-112">DirectShow stellt die Komponenten bereit, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="6369e-112">DirectShow provides the components you need.</span></span> <span data-ttu-id="6369e-113">Wenn Sie DirectShow durch Schreiben Ihrer eigenen Komponenten erweitern möchten, müssen Sie Sie jedoch als COM-Objekte implementieren.</span><span class="sxs-lookup"><span data-stu-id="6369e-113">If you want to extend DirectShow by writing your own components, however, you must implement them as COM objects.</span></span>

<span data-ttu-id="6369e-114">DirectShow ist für C++ konzipiert.</span><span class="sxs-lookup"><span data-stu-id="6369e-114">DirectShow is designed for C++.</span></span> <span data-ttu-id="6369e-115">Microsoft stellt keine verwaltete API für DirectShow bereit.</span><span class="sxs-lookup"><span data-stu-id="6369e-115">Microsoft does not provide a managed API for DirectShow.</span></span>

<span data-ttu-id="6369e-116">DirectShow vereinfacht die Medienwiedergabe, die Formatkonvertierung und Erfassungs Tasks.</span><span class="sxs-lookup"><span data-stu-id="6369e-116">DirectShow simplifies media playback, format conversion, and capture tasks.</span></span> <span data-ttu-id="6369e-117">Gleichzeitig ermöglicht Sie den Zugriff auf die zugrunde liegende Stream-Steuerungsarchitektur für Anwendungen, die benutzerdefinierte Lösungen erfordern.</span><span class="sxs-lookup"><span data-stu-id="6369e-117">At the same time, it provides access to the underlying stream control architecture for applications that require custom solutions.</span></span> <span data-ttu-id="6369e-118">Sie können auch eigene DirectShow-Komponenten erstellen, um neue Formate oder benutzerdefinierte Effekte zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6369e-118">You can also create your own DirectShow components to support new formats or custom effects.</span></span>

<span data-ttu-id="6369e-119">Beispiele für die Anwendungs Typen, die Sie mit DirectShow schreiben können, sind u. a. Datei Player, TV-und DVD-Player, Videobearbeitungsanwendungen, Dateiformatkonverter, Audiovideo-Erfassungs Anwendungen, Encoder und Decoders, digitale Signalprozessoren und mehr.</span><span class="sxs-lookup"><span data-stu-id="6369e-119">Examples of the types of application you can write with DirectShow include file players, TV and DVD players, video editing applications, file format converters, audio-video capture applications, encoders and decoders, digital signal processors, and more.</span></span>

<span data-ttu-id="6369e-120">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="6369e-120">This section contains the following topics:</span></span>

-   [<span data-ttu-id="6369e-121">Neues in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6369e-121">What's New in DirectShow</span></span>](whats-new-in-directshow.md)
-   [<span data-ttu-id="6369e-122">Unterstützte Formate in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6369e-122">Supported Formats in DirectShow</span></span>](supported-formats-in-directshow.md)
-   [<span data-ttu-id="6369e-123">FAQ zu DirectShow</span><span class="sxs-lookup"><span data-stu-id="6369e-123">DirectShow FAQ</span></span>](directshow-faq.md)

## <a name="related-topics"></a><span data-ttu-id="6369e-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6369e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6369e-125">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="6369e-125">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="6369e-126">Verwenden von DirectShow</span><span class="sxs-lookup"><span data-stu-id="6369e-126">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



