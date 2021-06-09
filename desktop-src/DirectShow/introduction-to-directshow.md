---
description: Einführung in DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Einführung in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5706ff0dec34c5db3762f5782f96804e5c85e889
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827224"
---
# <a name="introduction-to-directshow"></a><span data-ttu-id="cc502-103">Einführung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="cc502-103">Introduction to DirectShow</span></span>

<span data-ttu-id="cc502-104">Microsoft® DirectShow® ist eine Architektur für Streamingmedien auf der Microsoft Windows®Plattform.</span><span class="sxs-lookup"><span data-stu-id="cc502-104">Microsoft® DirectShow® is an architecture for streaming media on the Microsoft Windows® platform.</span></span> <span data-ttu-id="cc502-105">DirectShow bietet eine qualitativ hochwertige Erfassung und Wiedergabe von Multimediastreams.</span><span class="sxs-lookup"><span data-stu-id="cc502-105">DirectShow provides for high-quality capture and playback of multimedia streams.</span></span> <span data-ttu-id="cc502-106">Es unterstützt eine Vielzahl von Formaten, einschließlich Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3) und WAV-Sounddateien.</span><span class="sxs-lookup"><span data-stu-id="cc502-106">It supports a wide variety of formats, including Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3), and WAV sound files.</span></span> <span data-ttu-id="cc502-107">Es unterstützt die Erfassung von digitalen und analogen Geräten basierend auf Windows-Treibermodell (WDM) oder Video für Windows.</span><span class="sxs-lookup"><span data-stu-id="cc502-107">It supports capture from digital and analog devices based on the Windows Driver Model (WDM) or Video for Windows.</span></span> <span data-ttu-id="cc502-108">Er erkennt und verwendet automatisch Hardware für die Video- und Audiobeschleunigung, wenn verfügbar, unterstützt aber auch Systeme ohne Beschleunigungshardware.</span><span class="sxs-lookup"><span data-stu-id="cc502-108">It automatically detects and uses video and audio acceleration hardware when available, but also supports systems without acceleration hardware.</span></span>

<span data-ttu-id="cc502-109">DirectShow basiert auf dem Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="cc502-109">DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="cc502-110">Um eine DirectShow-Anwendung oder -Komponente zu schreiben, müssen Sie die COM-Clientprogrammierung verstehen.</span><span class="sxs-lookup"><span data-stu-id="cc502-110">To write a DirectShow application or component, you must understand COM client programming.</span></span> <span data-ttu-id="cc502-111">Für die meisten Anwendungen müssen Sie keine eigenen COM-Objekte implementieren.</span><span class="sxs-lookup"><span data-stu-id="cc502-111">For most applications, you do not need to implement your own COM objects.</span></span> <span data-ttu-id="cc502-112">DirectShow stellt die benötigten Komponenten zurVerfingung.</span><span class="sxs-lookup"><span data-stu-id="cc502-112">DirectShow provides the components you need.</span></span> <span data-ttu-id="cc502-113">Wenn Sie DirectShow erweitern möchten, indem Sie Ihre eigenen Komponenten schreiben, müssen Sie diese jedoch als COM-Objekte implementieren.</span><span class="sxs-lookup"><span data-stu-id="cc502-113">If you want to extend DirectShow by writing your own components, however, you must implement them as COM objects.</span></span>

<span data-ttu-id="cc502-114">DirectShow ist für C++ konzipiert.</span><span class="sxs-lookup"><span data-stu-id="cc502-114">DirectShow is designed for C++.</span></span> <span data-ttu-id="cc502-115">Microsoft stellt keine verwaltete API für DirectShow bereit.</span><span class="sxs-lookup"><span data-stu-id="cc502-115">Microsoft does not provide a managed API for DirectShow.</span></span>

<span data-ttu-id="cc502-116">DirectShow vereinfacht die Medienwiedergabe, Formatkonvertierung und Erfassungsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="cc502-116">DirectShow simplifies media playback, format conversion, and capture tasks.</span></span> <span data-ttu-id="cc502-117">Gleichzeitig ermöglicht sie den Zugriff auf die zugrunde liegende Streamsteuerungsarchitektur für Anwendungen, die benutzerdefinierte Lösungen erfordern.</span><span class="sxs-lookup"><span data-stu-id="cc502-117">At the same time, it provides access to the underlying stream control architecture for applications that require custom solutions.</span></span> <span data-ttu-id="cc502-118">Sie können auch eigene DirectShow-Komponenten erstellen, um neue Formate oder benutzerdefinierte Effekte zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cc502-118">You can also create your own DirectShow components to support new formats or custom effects.</span></span>

<span data-ttu-id="cc502-119">Beispiele für die Anwendungstypen, die Sie mit DirectShow schreiben können, sind Dateiplayer, TV- und DVD-Player, Videobearbeitungsanwendungen, Dateiformatkonverter, Audiovideoerfassungsanwendungen, Encoder und Decoder, Digitale Signalprozessoren und mehr.</span><span class="sxs-lookup"><span data-stu-id="cc502-119">Examples of the types of application you can write with DirectShow include file players, TV and DVD players, video editing applications, file format converters, audio-video capture applications, encoders and decoders, digital signal processors, and more.</span></span>

<span data-ttu-id="cc502-120">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="cc502-120">This section contains the following topics:</span></span>

-   [<span data-ttu-id="cc502-121">Neues in DirectShow</span><span class="sxs-lookup"><span data-stu-id="cc502-121">What's New in DirectShow</span></span>](whats-new-in-directshow.md)
-   [<span data-ttu-id="cc502-122">Unterstützte Formate in DirectShow</span><span class="sxs-lookup"><span data-stu-id="cc502-122">Supported Formats in DirectShow</span></span>](supported-formats-in-directshow.md)
-   [<span data-ttu-id="cc502-123">DirectShow – Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="cc502-123">DirectShow FAQ</span></span>](directshow-faq.yml)

## <a name="related-topics"></a><span data-ttu-id="cc502-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc502-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc502-125">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="cc502-125">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="cc502-126">Verwenden von DirectShow</span><span class="sxs-lookup"><span data-stu-id="cc502-126">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



