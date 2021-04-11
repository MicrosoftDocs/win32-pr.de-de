---
description: Das DirectShow SDK und das Windows Media-Format-SDK
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: Das DirectShow SDK und das Windows Media-Format-SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f85c5553c9a1cdd3f62380c9fc90d836a47a650
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351659"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a><span data-ttu-id="3c30b-103">Das DirectShow SDK und das Windows Media-Format-SDK</span><span class="sxs-lookup"><span data-stu-id="3c30b-103">The DirectShow SDK and the Windows Media Format SDK</span></span>

<span data-ttu-id="3c30b-104">DirectShow und das Windows Media-Format SDK bieten ergänzende Lösungen zum Schreiben von Anwendungen, mit denen Windows Media-Format Datenströme erstellt und wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3c30b-104">DirectShow and the Windows Media Format SDK offer complementary solutions for writing applications that create and play back Windows Media Format streams.</span></span> <span data-ttu-id="3c30b-105">Weitere Informationen finden Sie im Abschnitt "[Audiodateien und Video](../audio-and-video.md)" der MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="3c30b-105">For more information, see the "[Audio and Video](../audio-and-video.md)" section of the MSDN Library.</span></span>

<span data-ttu-id="3c30b-106">Der ASF Writer-Filter akzeptiert eine beliebige Anzahl von Eingabedaten strömen und erstellt eine ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="3c30b-106">The ASF Writer filter accepts any number of input streams and creates an ASF file.</span></span> <span data-ttu-id="3c30b-107">Der Filter verwendet das SDK für den Windows Media-Format, um unkomprimierte Audiodateien oder Videodateien in Windows Media-basierte Inhalte zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="3c30b-107">The filter uses the Windows Media Format SDK to convert uncompressed audio or video files to Windows Media-based content.</span></span> <span data-ttu-id="3c30b-108">Der komprimierte Inhalt wird dann im ASF-Container-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3c30b-108">The compressed content is then stored in the ASF container format.</span></span> <span data-ttu-id="3c30b-109">Wenn es sich bei dem Inhalt nur um Audiodaten handelt, erhält die Datei die Erweiterung. WMA und wird als Windows Media Audio Datei bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3c30b-109">If the content is audio only, then the file is given a .wma extension and is referred to as a Windows Media Audio file.</span></span> <span data-ttu-id="3c30b-110">Wenn der Inhalt nur Video-oder Video-und Audioinhalte ist, erhält die Datei die Erweiterung. WMV und wird als Windows Media Video Datei bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3c30b-110">If the content is video only or video and audio, then the file is given a .wmv extension and is referred to as a Windows Media Video file.</span></span> <span data-ttu-id="3c30b-111">Jeder Dateityp kann auch Metadaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="3c30b-111">Either type of file may also include metadata.</span></span>

<span data-ttu-id="3c30b-112">Sie können den WM-ASF-Writer in verschiedenen Szenarien verwenden, einschließlich Digital Video (DV) Capture, audiorekomprimierung und Konvertierung von Audio-Video Interleaved (AVI) oder MPEG Multimedia-Dateien für das Netzwerk Streaming.</span><span class="sxs-lookup"><span data-stu-id="3c30b-112">You can use the WM ASF Writer in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG multimedia files for network streaming.</span></span> <span data-ttu-id="3c30b-113">Dieser Filter bietet die einzige Möglichkeit zum Erstellen von Microsoft® Windows Media™-Audiodateien (WMA) und Windows Media Video-Dateien (WMV) in DirectShow-®.</span><span class="sxs-lookup"><span data-stu-id="3c30b-113">This filter provides the only way to create Microsoft® Windows Media™ Audio (WMA) and Windows Media Video (WMV) files in DirectShow®.</span></span> <span data-ttu-id="3c30b-114">Mit dem Filter können auch Dateien erstellt werden, die durch den Digital Rights Management (DRM) gesichert sind. Außerdem können Sie mit dem Microsoft MPEG-4-Encoder MPEG-4-Inhalte erstellen.</span><span class="sxs-lookup"><span data-stu-id="3c30b-114">The filter can also create files that are secured by Digital Rights Management (DRM), and can also create MPEG-4 content using the Microsoft MPEG-4 Encoder.</span></span> <span data-ttu-id="3c30b-115">Dieser Inhalt wird im ASF-Container-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3c30b-115">This content is stored in the ASF container format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c30b-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c30b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c30b-117">Erstellen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="3c30b-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
