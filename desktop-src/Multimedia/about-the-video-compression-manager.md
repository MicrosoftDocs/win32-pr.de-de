---
title: Informationen zum Video Komprimierungs-Manager
description: Informationen zum Video Komprimierungs-Manager
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Windows-Multimedia, Video Komprimierungs-Manager (VCM)
- Multimedia, Video Komprimierungs-Manager (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472948"
---
# <a name="about-the-video-compression-manager"></a><span data-ttu-id="a9a1c-105">Informationen zum Video Komprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="a9a1c-105">About the Video Compression Manager</span></span>

<span data-ttu-id="a9a1c-106">Normalerweise arbeiten installierbare Kompressoren mit Video Bilddaten, die in überlappenden Audiodateien (AVI) gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="a9a1c-106">Typically, installable compressors operate with video-image data stored in audio-video interleaved (AVI) files.</span></span> <span data-ttu-id="a9a1c-107">In dieser Übersicht werden die Programmiertechniken erläutert, die für den Zugriff auf installierbare Kompressoren über VCM verwendet werden, und die folgenden Themen behandelt</span><span class="sxs-lookup"><span data-stu-id="a9a1c-107">This overview explains the programming techniques used to access installable compressors through VCM and covers the following topics:</span></span>

-   <span data-ttu-id="a9a1c-108">VCM und das Video für die Windows-Architektur</span><span class="sxs-lookup"><span data-stu-id="a9a1c-108">VCM and the Video for Windows architecture</span></span>
-   <span data-ttu-id="a9a1c-109">Komprimieren und abkomprimieren von Bilddaten aus Ihrer Anwendung</span><span class="sxs-lookup"><span data-stu-id="a9a1c-109">Compressing and decompressing image data from your application</span></span>
-   <span data-ttu-id="a9a1c-110">Verwenden von VCM-renderatoren zum Zeichnen von Daten aus Ihrer Anwendung</span><span class="sxs-lookup"><span data-stu-id="a9a1c-110">Using VCM renderers to draw data from your application</span></span>
-   <span data-ttu-id="a9a1c-111">VCM-Funktionen und-Strukturen</span><span class="sxs-lookup"><span data-stu-id="a9a1c-111">VCM functions and structures</span></span>

<span data-ttu-id="a9a1c-112">Bevor Sie diese Übersicht lesen, sollten Sie mit den Microsoft Win32-Grafik Diensten vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="a9a1c-112">Before you read this overview, you should be familiar with the Microsoft Win32 graphic services.</span></span> <span data-ttu-id="a9a1c-113">Insbesondere Bitmaps-und [**bitmapbezogene**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) Strukturen, wie z. b. BitmapInfo und [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), werden ausgiebig von VCM verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9a1c-113">In particular, bitmaps and bitmap-related structures, such as [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) and [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), are used extensively by VCM.</span></span> <span data-ttu-id="a9a1c-114">Weitere Informationen zu den **BitmapInfo** -und **BITMAPINFOHEADER** -Strukturen finden Sie unter [Bitmaps](/previous-versions//ms532349(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9a1c-114">For additional information about the **BITMAPINFO** and **BITMAPINFOHEADER** structures, see [Bitmaps](/previous-versions//ms532349(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="a9a1c-115">Der Audiokomprimierungs-Manager (ACM) bietet Unterstützung für Audiokomprimierungs-und dekomprimierungstreiber auf Systemebene.</span><span class="sxs-lookup"><span data-stu-id="a9a1c-115">The audio compression manager (ACM) provides system-level support for audio compression and decompression drivers.</span></span> <span data-ttu-id="a9a1c-116">Eine Beschreibung der Audiokomprimierungs Dienste finden Sie unter [Audiokomprimierungs-Manager](audio-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="a9a1c-116">For a description of the audio compression services, see [Audio Compression Manager](audio-compression-manager.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a9a1c-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9a1c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9a1c-118">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="a9a1c-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 