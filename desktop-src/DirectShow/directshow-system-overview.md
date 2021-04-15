---
description: Übersicht über das DirectShow-System
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: Übersicht über das DirectShow-System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833fed4031c95ddb4ecbf91e7bb27c27741acc18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520587"
---
# <a name="directshow-system-overview"></a><span data-ttu-id="8a488-103">Übersicht über das DirectShow-System</span><span class="sxs-lookup"><span data-stu-id="8a488-103">DirectShow System Overview</span></span>

<span data-ttu-id="8a488-104">**Die Herausforderung von Multimedia**</span><span class="sxs-lookup"><span data-stu-id="8a488-104">**The Challenge of Multimedia**</span></span>

<span data-ttu-id="8a488-105">Das Arbeiten mit Multimedia stellt verschiedene Hauptprobleme dar:</span><span class="sxs-lookup"><span data-stu-id="8a488-105">Working with multimedia presents several major challenges:</span></span>

-   <span data-ttu-id="8a488-106">Multimediarestreams enthalten große Datenmengen, die sehr schnell verarbeitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8a488-106">Multimedia streams contain large amounts of data, which must be processed very quickly.</span></span>
-   <span data-ttu-id="8a488-107">Audiodaten und Videos müssen synchronisiert werden, sodass Sie gleichzeitig gestartet und angehalten werden und mit derselben Rate abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="8a488-107">Audio and video must be synchronized so that it starts and stops at the same time, and plays at the same rate.</span></span>
-   <span data-ttu-id="8a488-108">Daten können aus vielen Quellen stammen, einschließlich lokaler Dateien, Computernetzwerken, Fernsehübertragungen und Videokameras.</span><span class="sxs-lookup"><span data-stu-id="8a488-108">Data can come from many sources, including local files, computer networks, television broadcasts, and video cameras.</span></span>
-   <span data-ttu-id="8a488-109">Die Daten sind in einer Vielzahl von Formaten verfügbar, z. b. Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG) und Digital Video (DV).</span><span class="sxs-lookup"><span data-stu-id="8a488-109">Data comes in a variety of formats, such as Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG), and Digital Video (DV).</span></span>
-   <span data-ttu-id="8a488-110">Der Programmierer weiß im Voraus nicht, welche Hardware Geräte auf dem System des Endbenutzers vorhanden sein werden.</span><span class="sxs-lookup"><span data-stu-id="8a488-110">The programmer does not know in advance what hardware devices will be present on the end-user's system.</span></span>

<span data-ttu-id="8a488-111">**Die DirectShow-Lösung**</span><span class="sxs-lookup"><span data-stu-id="8a488-111">**The DirectShow Solution**</span></span>

<span data-ttu-id="8a488-112">DirectShow ist darauf ausgelegt, jede dieser Herausforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="8a488-112">DirectShow is designed to address each of these challenges.</span></span> <span data-ttu-id="8a488-113">Das Hauptziel des Entwurfs Ziels besteht darin, die Aufgabe der Erstellung digitaler Medienanwendungen auf der Windows-Plattform zu vereinfachen, indem Anwendungen von den komplexen Daten Transporten, Hardware unterschieden und der Synchronisierung isoliert werden.</span><span class="sxs-lookup"><span data-stu-id="8a488-113">Its main design goal is to simplify the task of creating digital media applications on the Windows platform, by isolating applications from the complexities of data transports, hardware differences, and synchronization.</span></span>

<span data-ttu-id="8a488-114">Um den Durchsatz zu erzielen, der zum Streamen von Video-und Audiodaten erforderlich ist, verwendet DirectShow nach Möglichkeit Direct3D und DirectSound.</span><span class="sxs-lookup"><span data-stu-id="8a488-114">To achieve the throughput needed to stream video and audio, DirectShow uses Direct3D and DirectSound whenever possible.</span></span> <span data-ttu-id="8a488-115">Diese Technologien Renderingdaten effizient in den Sound-und Grafikkarten des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="8a488-115">These technologies render data efficiently to the user's sound and graphics cards.</span></span> <span data-ttu-id="8a488-116">In DirectShow wird die Wiedergabe synchronisiert, indem Mediendaten in Zeitstempel Beispielen gekapselt werden.</span><span class="sxs-lookup"><span data-stu-id="8a488-116">DirectShow synchronizes playback by encapsulating media data in time-stamped samples.</span></span> <span data-ttu-id="8a488-117">Für die unterschiedlichsten Quellen, Formate und Hardware Geräte, die möglich sind, verwendet DirectShow eine modulare Architektur, in der die Anwendung verschiedene Softwarekomponenten mit dem Namen " *Filter*" kombiniert und mit diesen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8a488-117">To handle the variety of sources, formats, and hardware devices that are possible, DirectShow uses a modular architecture, in which the application mixes and matches different software components called *filters*.</span></span>

<span data-ttu-id="8a488-118">DirectShow stellt Filter bereit, die das erfassen und Optimieren von Geräten basierend auf dem Windows-Treibermodell (WDM) unterstützen, sowie Filter, die ältere Video für Windows (Vfw)-Erfassungs Karten unterstützen, und Codecs, die für die Schnittstellen von Audiokomprimierungs-Manager (ACM) und Video Compression Manager (VCM) geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="8a488-118">DirectShow provides filters that support capture and tuning devices based on the Windows Driver Model (WDM), as well as filters that support older Video for Windows (VfW) capture cards, and codecs written for the Audio Compression Manager (ACM) and Video Compression Manager (VCM) interfaces.</span></span>

<span data-ttu-id="8a488-119">Das folgende Diagramm zeigt die Beziehung zwischen einer Anwendung, den DirectShow-Komponenten und einigen der Hardware-und Softwarekomponenten, die von DirectShow unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8a488-119">The following diagram shows the relationship between an application, the DirectShow components, and some of the hardware and software components that DirectShow supports.</span></span>

![allgemeine Architektur](images/arch-oview2.png)

<span data-ttu-id="8a488-121">Wie hier gezeigt, kommunizieren DirectShow-Filter mit einer großen Bandbreite von Geräten, darunter das lokale Dateisystem, TV-Tuner und Video Erfassungs Karten, VFW-Codecs, die Videoanzeige (über DirectDraw oder GDI) und die Soundkarte (über DirectSound).</span><span class="sxs-lookup"><span data-stu-id="8a488-121">As illustrated here, DirectShow filters communicate with, and control, a wide variety of devices, including the local file system, TV tuner and video capture cards, VfW codecs, the video display (through DirectDraw or GDI), and the sound card (through DirectSound).</span></span> <span data-ttu-id="8a488-122">Daher isoliert DirectShow die Anwendung von vielen Komplexitäten dieser Geräte.</span><span class="sxs-lookup"><span data-stu-id="8a488-122">Thus, DirectShow insulates the application from many of the complexities of these devices.</span></span> <span data-ttu-id="8a488-123">DirectShow bietet auch systemeigene Komprimierungs-und Dekomprimierungs Filter für bestimmte Dateiformate.</span><span class="sxs-lookup"><span data-stu-id="8a488-123">DirectShow also provides native compression and decompression filters for certain file formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a488-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8a488-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a488-125">Informationen zu DirectShow</span><span class="sxs-lookup"><span data-stu-id="8a488-125">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



