---
description: Microsoft Media Foundation ist die Multimedia-Plattform der nächsten Generation für Windows, mit der Entwickler, Consumer und Inhaltsanbieter die neue Welle von Premium-Inhalten mit verbesserter Stabilität, unvergleichlicher Qualität und nahtloser Interoperabilität nutzen können.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: Info über Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a166482bbb0291f702a0e402441e292109a3e10
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106357145"
---
# <a name="about-media-foundation"></a><span data-ttu-id="c9685-103">Info über Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9685-103">About Media Foundation</span></span>

<span data-ttu-id="c9685-104">Microsoft Media Foundation ist die Multimedia-Plattform der nächsten Generation für Windows, mit der Entwickler, Consumer und Inhaltsanbieter die neue Welle von Premium-Inhalten mit verbesserter Stabilität, unvergleichlicher Qualität und nahtloser Interoperabilität nutzen können.</span><span class="sxs-lookup"><span data-stu-id="c9685-104">Microsoft Media Foundation is the next generation multimedia platform for Windows that enables developers, consumers, and content providers to embrace the new wave of premium content with enhanced robustness, unparalleled quality, and seamless interoperability.</span></span>

<span data-ttu-id="c9685-105">Media Foundation erfordert Windows Vista oder höher.</span><span class="sxs-lookup"><span data-stu-id="c9685-105">Media Foundation requires Windows Vista or later.</span></span> <span data-ttu-id="c9685-106">Dabei wird das Component Object Model (com) verwendet, und es ist C/C++ erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c9685-106">It uses the component object model (COM) and requires C/C++.</span></span> <span data-ttu-id="c9685-107">Microsoft stellt keine verwaltete API für Media Foundation bereit.</span><span class="sxs-lookup"><span data-stu-id="c9685-107">Microsoft does not provide a managed API for Media Foundation.</span></span>

<span data-ttu-id="c9685-108">Die Media Foundation-APIs sind Teil des [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c9685-108">The Media Foundation APIs are part of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c9685-109">Installieren Sie die neueste Version des Windows SDK, um eine Media Foundation Anwendung zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="c9685-109">To develop a Media Foundation application, install the latest version of the Windows SDK.</span></span>

## <a name="audio-and-video-quality"></a><span data-ttu-id="c9685-110">Audioqualität und Video Qualität</span><span class="sxs-lookup"><span data-stu-id="c9685-110">Audio and Video Quality</span></span>

<span data-ttu-id="c9685-111">Media Foundation wurde entwickelt, um die Herausforderungen von hoch Definitions Inhalten zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c9685-111">Media Foundation has been designed to meet the challenges posed by high-definition content.</span></span> <span data-ttu-id="c9685-112">Verbesserungen der Audioqualität und Videoqualität, die auf der gesamten Plattform vorgenommen werden, ermöglichen die Bereitstellung einer hervorgehobenen Oberfläche für den Inhalt der nächsten Generation.</span><span class="sxs-lookup"><span data-stu-id="c9685-112">Audio and video quality enhancements made throughout the platform now make it possible to deliver a great experience for next generation high-definition content.</span></span>

-   <span data-ttu-id="c9685-113">Die DirectX-Videobeschleunigung (DXVA) 2,0 bietet im Vergleich mit DXVA 1,0 eine effizientere Videobeschleunigung mit robusterer und optimierter Video Decodierung und erweiterter Verwendung von Hardware bei der Videoverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="c9685-113">DirectX Video Acceleration (DXVA) 2.0 offers more efficient video acceleration, compared with DXVA 1.0, with more robust and streamlined video decoding and extended use of hardware in video processing.</span></span> <span data-ttu-id="c9685-114">Mit DXVA 2,0 kann Windows einige der anspruchsvollsten hoch Definitions Inhalte mit hoher Qualität und verbesserter Ausfallsicherheit verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c9685-114">With DXVA 2.0, Windows can handle some of the most demanding high-definition content with high quality and improved glitch-resilience.</span></span>

-   <span data-ttu-id="c9685-115">Farb Rauminformationen werden in der gesamten Video Pipeline beibehalten.</span><span class="sxs-lookup"><span data-stu-id="c9685-115">Color-space information is preserved throughout the video pipeline.</span></span> <span data-ttu-id="c9685-116">Benutzer können Videoinhalte mit voller Treue nutzen.</span><span class="sxs-lookup"><span data-stu-id="c9685-116">Users can enjoy video content with full fidelity.</span></span> <span data-ttu-id="c9685-117">Farbinformationen und Zeilen Sprung Bilder werden jetzt für Einzelpass-Kompositionen an Hardware übergeben.</span><span class="sxs-lookup"><span data-stu-id="c9685-117">Color information and interlaced images are now passed to hardware for single-pass compositions.</span></span> <span data-ttu-id="c9685-118">Durch die Beibehaltung von Farb Rauminformationen werden auch unnötige Farb Raum Konvertierungen reduziert, wodurch mehr Zyklen zum Verarbeiten anspruchsvoller HD-Inhalte freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c9685-118">Preserving color-space information also reduces unnecessary color space conversions, which frees more cycles to process demanding HD content.</span></span>
-   <span data-ttu-id="c9685-119">Der Enhanced Video Renderer (EVR) bietet eine bessere Zeit Steuerungs Unterstützung, eine verbesserte Videoverarbeitung und eine verbesserte Ausfallsicherheit.</span><span class="sxs-lookup"><span data-stu-id="c9685-119">The enhanced video renderer (EVR) offers better timing support, enhanced video processing, and improved glitch-resilience.</span></span> <span data-ttu-id="c9685-120">Die Vollbildwiedergabe Unterstützung wurde verbessert, und das Abspielen von Videos im Fenstermodus wurde minimiert.</span><span class="sxs-lookup"><span data-stu-id="c9685-120">Full-screen playback support has been enhanced, and video tearing in windowed mode has been minimized.</span></span>
-   <span data-ttu-id="c9685-121">In Media Foundation wird der Multimedia Class Scheduler Service (MMCSS) verwendet, einem neuen Systemdienst in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c9685-121">Media Foundation uses the Multimedia Class Scheduler Service (MMCSS), a new system service in Windows Vista.</span></span> <span data-ttu-id="c9685-122">Mit MMCSS können Multimediaanwendungen sicherstellen, dass Ihre Zeit empfindliche Verarbeitung priorisierten Zugriff auf CPU-Ressourcen erhält.</span><span class="sxs-lookup"><span data-stu-id="c9685-122">MMCSS enables multimedia applications to ensure that their time-sensitive processing receives prioritized access to CPU resources.</span></span>

## <a name="content-access"></a><span data-ttu-id="c9685-123">Inhalts Zugriff</span><span class="sxs-lookup"><span data-stu-id="c9685-123">Content Access</span></span>

<span data-ttu-id="c9685-124">Da digitale Unterhaltung in den High-Definition-Zeitraum übergeht und Inhalte portabler und allgemeinerer werden, wird der Inhalts Schutz zu einem integralen Bestandteil digitaler Medienprodukte.</span><span class="sxs-lookup"><span data-stu-id="c9685-124">As digital entertainment moves into the high-definition era and content becomes more portable and ubiquitous, content protection will become an integral part of digital media products.</span></span> <span data-ttu-id="c9685-125">Durch die Erweiterbarkeit von Media Foundation wird sichergestellt, dass diese Trends unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c9685-125">The extensibility of Media Foundation ensures that it can support these trends.</span></span>

<span data-ttu-id="c9685-126">Außerdem ermöglicht die Media Foundation Erweiterbarkeit, dass verschiedene Inhalts Schutzsysteme zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c9685-126">In addition, Media Foundation extensibility enables different content protection systems to operate together.</span></span>

## <a name="about-media-foundation"></a><span data-ttu-id="c9685-127">Info über Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9685-127">About Media Foundation</span></span>

<span data-ttu-id="c9685-128">Dieser Abschnitt enthält allgemeine Informationen zu den Media Foundation-APIs.</span><span class="sxs-lookup"><span data-stu-id="c9685-128">This section contains general information about the Media Foundation APIs.</span></span> <span data-ttu-id="c9685-129">Ausführliche Informationen zur Programmierung finden Sie im [Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="c9685-129">Detailed programming information can be found in the [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>



| <span data-ttu-id="c9685-130">`Section`</span><span class="sxs-lookup"><span data-stu-id="c9685-130">Section</span></span>                                                                              | <span data-ttu-id="c9685-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9685-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="c9685-132">Neuerungen bei Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9685-132">What's New for Media Foundation</span></span>](whats-new-for-media-foundation.md)                | <span data-ttu-id="c9685-133">Beschreibt die neuen Funktionen in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c9685-133">Describes new features in Media Foundation.</span></span>                               |
| [<span data-ttu-id="c9685-134">Media Foundation-Header und-Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="c9685-134">Media Foundation Headers and Libraries</span></span>](media-foundation-headers-and-libraries.md) | <span data-ttu-id="c9685-135">Listet die Header-und Bibliotheksdateien auf, die die Media Foundation-APIs definieren.</span><span class="sxs-lookup"><span data-stu-id="c9685-135">Lists the header and library files that define the Media Foundation APIs.</span></span> |
| [<span data-ttu-id="c9685-136">Media Foundation Tools</span><span class="sxs-lookup"><span data-stu-id="c9685-136">Media Foundation Tools</span></span>](media-foundation-tools.md)                                 | <span data-ttu-id="c9685-137">Beschreibt die Entwicklungs Tools, die für Media Foundation verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c9685-137">Describes the development tools that are available for Media Foundation.</span></span>  |



 

<span data-ttu-id="c9685-138">Media Foundation ist nicht in den N-und KN-Editionen von Windows 8 enthalten.</span><span class="sxs-lookup"><span data-stu-id="c9685-138">Media Foundation is not included with the N and KN editions of Windows 8.</span></span> <span data-ttu-id="c9685-139">Weitere Informationen finden Sie unter [Microsoft Windows Media Feature Pack für N-und KN-Versionen aller Windows 8-Editionen](https://support.microsoft.com/kb/2703761).</span><span class="sxs-lookup"><span data-stu-id="c9685-139">For more information, see [Microsoft Windows Media Feature Pack for N and KN Versions of all Windows 8 Editions](https://support.microsoft.com/kb/2703761).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9685-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9685-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9685-141">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9685-141">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



