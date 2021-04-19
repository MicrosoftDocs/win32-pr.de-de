---
description: Erstellen von ASF-Dateien in DirectShow
ms.assetid: dffda43a-5831-4889-864f-81351b9e2bb3
title: Erstellen von ASF-Dateien in DirectShow (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f5c9ebac0b14b736c47599ee25a1c1c28dd8f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346206"
---
# <a name="creating-asf-files-in-directshow-directshow"></a><span data-ttu-id="e4e66-103">Erstellen von ASF-Dateien in DirectShow (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e4e66-103">Creating ASF Files in DirectShow (DirectShow)</span></span>

<span data-ttu-id="e4e66-104">In diesem Abschnitt wird beschrieben, wie Sie den DirectShow- [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter verwenden, um Dateien im Advanced Systems Format (ASF) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4e66-104">This section describes how to use the DirectShow [WM ASF Writer](wm-asf-writer-filter.md) filter to create files in Advanced Systems Format (ASF).</span></span> <span data-ttu-id="e4e66-105">Bei ASF handelt es sich um ein Containerformat, das beliebige komprimierte oder unkomprimierte Daten enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="e4e66-105">ASF is a container format that can contain any type of compressed or uncompressed data.</span></span> <span data-ttu-id="e4e66-106">Windows Media-Format Dateien sind ASF-Dateien, die bestimmte Codecs verwenden, wie im Windows Media-Format Software Development Kit (SDK) angegeben.</span><span class="sxs-lookup"><span data-stu-id="e4e66-106">Windows Media Format files are ASF files that use certain codecs as specified in the Windows Media Format Software Development Kit (SDK).</span></span> <span data-ttu-id="e4e66-107">Diese Dateien verwenden die Erweiterungen ". wma" für Windows Media Audio Dateien und ". wmv" für Windows Media Video Dateien.</span><span class="sxs-lookup"><span data-stu-id="e4e66-107">These files use the extensions ".wma" for Windows Media Audio files and ".wmv" for Windows Media Video files.</span></span>

<span data-ttu-id="e4e66-108">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="e4e66-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="e4e66-109">Das DirectShow SDK und das Windows Media-Format-SDK</span><span class="sxs-lookup"><span data-stu-id="e4e66-109">The DirectShow SDK and the Windows Media Format SDK</span></span>](the-directshow-sdk-and-the-windows-media-format-sdk.md)
-   [<span data-ttu-id="e4e66-110">Konfigurieren des ASF-Writers</span><span class="sxs-lookup"><span data-stu-id="e4e66-110">Configuring the ASF Writer</span></span>](configuring-the-asf-writer.md)
-   [<span data-ttu-id="e4e66-111">Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien</span><span class="sxs-lookup"><span data-stu-id="e4e66-111">Building Filter Graphs to Write ASF Files</span></span>](building-filter-graphs-to-write-asf-files.md)
-   [<span data-ttu-id="e4e66-112">Konfigurieren von Profilen und anderen ASF-Dateieigenschaften</span><span class="sxs-lookup"><span data-stu-id="e4e66-112">Configuring Profiles and Other ASF File Properties</span></span>](configuring-profiles-and-other-asf-file-properties.md)
-   [<span data-ttu-id="e4e66-113">Entsperren des Windows Media-Format-SDKs</span><span class="sxs-lookup"><span data-stu-id="e4e66-113">Unlocking the Windows Media Format SDK</span></span>](unlocking-the-windows-media-format-sdk.md)

## <a name="related-topics"></a><span data-ttu-id="e4e66-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4e66-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4e66-115">Verwenden von Windows-Medien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="e4e66-115">Using Windows Media in DirectShow</span></span>](using-windows-media-in-directshow.md)
</dt> </dl>

 

 



