---
title: Informationen zu DirectShow (Windows Media-Format 11 SDK)
description: Informationen zu DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd77507643edb220bc71a029779c88fe56760eae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039989"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="d35b6-107">Informationen zu DirectShow (Windows Media-Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="d35b6-107">About DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="d35b6-108">DirectShow ist eine hochstufige, modulare, erweiterbare datenstreamingarchitektur für die Windows-Plattform.</span><span class="sxs-lookup"><span data-stu-id="d35b6-108">DirectShow is a high-level, modular, extensible, data-streaming architecture for the Windows platform.</span></span> <span data-ttu-id="d35b6-109">Es bietet die zugrunde liegenden Softwarekomponenten und APIs (Application Programming Interfaces) für eine Vielzahl digitaler Audio-und Videoanwendungen auf dem Markt heute.</span><span class="sxs-lookup"><span data-stu-id="d35b6-109">It provides the underlying software components and application programming interfaces (APIs) for a wide variety of digital audio and video applications on the market today.</span></span> <span data-ttu-id="d35b6-110">DirectShow ist als Teil des Microsoft DirectX Software Development Kit verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d35b6-110">DirectShow is available as part of the Microsoft DirectX Software Development Kit.</span></span> <span data-ttu-id="d35b6-111">Weitere Informationen zu DirectShow finden Sie im Microsoft Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="d35b6-111">To learn more about DirectShow, see the Microsoft Platform SDK.</span></span>

<span data-ttu-id="d35b6-112">In DirectShow werden alle datenstreamingkomponenten als *Filter* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d35b6-112">In DirectShow, all data streaming components are called *filters*.</span></span> <span data-ttu-id="d35b6-113">Ein Filter kann ein Hardware Gerät, einen Software Encoder oder-Decoder, einen Audio-oder Videorenderer oder eine beliebige Audiovideo-Verarbeitungs Funktion darstellen.</span><span class="sxs-lookup"><span data-stu-id="d35b6-113">A filter may represent a hardware device, a software encoder or decoder, an audio or video renderer, or any audio-video processing capability.</span></span> <span data-ttu-id="d35b6-114">Zum Aktivieren von DirectShow – basierten Anwendungen zum Lesen und Schreiben von Inhalten im Windows Media-Format, einschließlich von Digital Rights Management (DRM) geschütztes Inhalt, stellt Microsoft zwei Filter bereit, die Teile des SDK des Windows Media-Formats Kapseln.</span><span class="sxs-lookup"><span data-stu-id="d35b6-114">To enable DirectShow–based applications to read and write Windows Media Format content, including content protected by Digital Rights Management (DRM), Microsoft provides two filters that encapsulate portions of the Windows Media Format SDK.</span></span> <span data-ttu-id="d35b6-115">Dies sind der [WM-ASF-Reader](wm-asf-reader-filter.md) und der [WM-ASF-Writer](wm-asf-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="d35b6-115">These are the [WM ASF Reader](wm-asf-reader-filter.md) and the [WM ASF Writer](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="d35b6-116">Diese Filter und die Schnittstellen, die Sie verfügbar machen, werden zusammen mit der dll, in der Sie verpackt sind, als qasf-Komponenten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d35b6-116">These filters and the interfaces they expose are collectively referred to as the QASF components, after the DLL in which they are packaged.</span></span> <span data-ttu-id="d35b6-117">(Q steht für Quartz, einen frühen Codenamen für DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="d35b6-117">(The Q stands for Quartz, an early code name for DirectShow.)</span></span>

> [!Note]  
> <span data-ttu-id="d35b6-118">Die Verwendung der Codecs für die Windows Media Audio-und Video 9-Serie über die DirectShow-qasf-Komponenten erfordert Microsoft Windows Millennium Edition oder höher oder DirectX 8,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d35b6-118">The use of the Windows Media Audio and Video 9 Series codecs through the DirectShow QASF components requires Microsoft Windows Millennium Edition or later, or DirectX 8.0 or later.</span></span>

 

<span data-ttu-id="d35b6-119">Das folgende Diagramm zeigt ein DirectShow-Filter Diagramm für die Wiedergabe Windows Media Video Dateien.</span><span class="sxs-lookup"><span data-stu-id="d35b6-119">The following diagram shows a DirectShow filter graph for playing back Windows Media Video files.</span></span>

![Grafik zur Windows Media-Videowiedergabe](images/wmv-wmasfreader.png)

<span data-ttu-id="d35b6-121">Der [WM-ASF-Reader](wm-asf-reader-filter.md) ist eine qasf-Komponente, bei den Decodern handelt es sich um Windows Media-SDK-Komponenten, die im DMO-Wrapper Filter (einer qasf-Komponente) gehostet werden, und die Renderer sind DirectShow-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="d35b6-121">The [WM ASF Reader](wm-asf-reader-filter.md) is a QASF component, the decoders are Windows Media Format SDK components hosted in the DMO Wrapper filter (a QASF component), and the renderers are DirectShow components.</span></span>

 

 




