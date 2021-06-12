---
title: Erfahren Sie mehr über DirectShow im Windows Media Format 11 SDK, einer modularen, erweiterbaren Datenstreamingarchitektur auf hoher Ebene für die Windows-Plattform.
description: Informationen zu DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a76d7c8971c452f01176be7472e313181eb2831
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011293"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="92e96-107">Informationen zu DirectShow (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="92e96-107">About DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="92e96-108">DirectShow ist eine umfassende, modulare, erweiterbare Datenstreamingarchitektur für die Windows-Plattform.</span><span class="sxs-lookup"><span data-stu-id="92e96-108">DirectShow is a high-level, modular, extensible, data-streaming architecture for the Windows platform.</span></span> <span data-ttu-id="92e96-109">Es stellt die zugrunde liegenden Softwarekomponenten und Anwendungsprogrammierschnittstellen (APPLICATION Programming Interfaces, APIs) für eine Vielzahl von digitalen Audio- und Videoanwendungen bereit, die heute auf dem Markt verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="92e96-109">It provides the underlying software components and application programming interfaces (APIs) for a wide variety of digital audio and video applications on the market today.</span></span> <span data-ttu-id="92e96-110">DirectShow ist als Teil des Microsoft DirectX Software Development Kit verfügbar.</span><span class="sxs-lookup"><span data-stu-id="92e96-110">DirectShow is available as part of the Microsoft DirectX Software Development Kit.</span></span> <span data-ttu-id="92e96-111">Weitere Informationen zu DirectShow finden Sie im Microsoft Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="92e96-111">To learn more about DirectShow, see the Microsoft Platform SDK.</span></span>

<span data-ttu-id="92e96-112">In DirectShow werden alle Datenstreamingkomponenten als Filter *bezeichnet.*</span><span class="sxs-lookup"><span data-stu-id="92e96-112">In DirectShow, all data streaming components are called *filters*.</span></span> <span data-ttu-id="92e96-113">Ein Filter kann ein Hardwaregerät, einen Softwareencoder oder -decoder, einen Audio- oder Videorenderer oder eine beliebige Audiovideoverarbeitungsfunktion darstellen.</span><span class="sxs-lookup"><span data-stu-id="92e96-113">A filter may represent a hardware device, a software encoder or decoder, an audio or video renderer, or any audio-video processing capability.</span></span> <span data-ttu-id="92e96-114">Damit DirectShow-basierte Anwendungen Inhalte im Windows Media Format lesen und schreiben können, einschließlich von Digital Rights Management (DRM) geschützter Inhalte, stellt Microsoft zwei Filter bereit, die Teile des Windows Media Format SDK kapseln.</span><span class="sxs-lookup"><span data-stu-id="92e96-114">To enable DirectShow–based applications to read and write Windows Media Format content, including content protected by Digital Rights Management (DRM), Microsoft provides two filters that encapsulate portions of the Windows Media Format SDK.</span></span> <span data-ttu-id="92e96-115">Dies sind [der WM ASF-Reader](wm-asf-reader-filter.md) und der [WM ASF Writer.](wm-asf-writer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="92e96-115">These are the [WM ASF Reader](wm-asf-reader-filter.md) and the [WM ASF Writer](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="92e96-116">Diese Filter und die schnittstellen, die sie verfügbar machen, werden zusammen als QASF-Komponenten nach der DLL bezeichnet, in der sie gepackt sind.</span><span class="sxs-lookup"><span data-stu-id="92e96-116">These filters and the interfaces they expose are collectively referred to as the QASF components, after the DLL in which they are packaged.</span></span> <span data-ttu-id="92e96-117">(Das Q steht für "Party", ein früher Codename für DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="92e96-117">(The Q stands for Quartz, an early code name for DirectShow.)</span></span>

> [!Note]  
> <span data-ttu-id="92e96-118">Die Verwendung der Codecs der Windows Media Audio- und Video 9-Serie über die DirectShow QASF-Komponenten erfordert Microsoft Windows Edition Edition oder höher oder DirectX 8.0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="92e96-118">The use of the Windows Media Audio and Video 9 Series codecs through the DirectShow QASF components requires Microsoft Windows Millennium Edition or later, or DirectX 8.0 or later.</span></span>

 

<span data-ttu-id="92e96-119">Das folgende Diagramm zeigt ein DirectShow-Filterdiagramm für die Wiedergabe Windows Media Video Dateien.</span><span class="sxs-lookup"><span data-stu-id="92e96-119">The following diagram shows a DirectShow filter graph for playing back Windows Media Video files.</span></span>

![Wiedergabediagramm für Windows-Medienvideos](images/wmv-wmasfreader.png)

<span data-ttu-id="92e96-121">Der [WM ASF-Reader](wm-asf-reader-filter.md) ist eine QASF-Komponente, die Decoder sind Windows Media Format SDK-Komponenten, die im DMO-Wrapperfilter (eine QASF-Komponente) gehostet werden, und die Renderer sind DirectShow-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="92e96-121">The [WM ASF Reader](wm-asf-reader-filter.md) is a QASF component, the decoders are Windows Media Format SDK components hosted in the DMO Wrapper filter (a QASF component), and the renderers are DirectShow components.</span></span>

 

 




