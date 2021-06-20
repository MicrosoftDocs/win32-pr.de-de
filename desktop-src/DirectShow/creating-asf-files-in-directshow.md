---
description: Erfahren Sie mehr über das Erstellen von ASF-Dateien in DirectShow. ASF ist ein Containerformat, das beliebige Datentypen enthalten kann.
ms.assetid: dffda43a-5831-4889-864f-81351b9e2bb3
title: Erstellen von ASF-Dateien in DirectShow (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4614ed813c2e9f51c77cd8773739188aa5d4d07
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403964"
---
# <a name="creating-asf-files-in-directshow-directshow"></a><span data-ttu-id="79bcd-104">Erstellen von ASF-Dateien in DirectShow (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="79bcd-104">Creating ASF Files in DirectShow (DirectShow)</span></span>

<span data-ttu-id="79bcd-105">In diesem Abschnitt wird beschrieben, wie Sie den DirectShow [WM ASF Writer-Filter](wm-asf-writer-filter.md) verwenden, um Dateien im Advanced Systems Format (ASF) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="79bcd-105">This section describes how to use the DirectShow [WM ASF Writer](wm-asf-writer-filter.md) filter to create files in Advanced Systems Format (ASF).</span></span> <span data-ttu-id="79bcd-106">ASF ist ein Containerformat, das jede Art von komprimierten oder unkomprimierten Daten enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="79bcd-106">ASF is a container format that can contain any type of compressed or uncompressed data.</span></span> <span data-ttu-id="79bcd-107">Windows Media Format-Dateien sind ASF-Dateien, die bestimmte Codecs verwenden, wie im Windows Media Format Software Development Kit (SDK) angegeben.</span><span class="sxs-lookup"><span data-stu-id="79bcd-107">Windows Media Format files are ASF files that use certain codecs as specified in the Windows Media Format Software Development Kit (SDK).</span></span> <span data-ttu-id="79bcd-108">Diese Dateien verwenden die Erweiterungen ".wma" Windows Media Audio Dateien und ".wmv" für Windows Media Video Dateien.</span><span class="sxs-lookup"><span data-stu-id="79bcd-108">These files use the extensions ".wma" for Windows Media Audio files and ".wmv" for Windows Media Video files.</span></span>

<span data-ttu-id="79bcd-109">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="79bcd-109">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="79bcd-110">Das DirectShow SDK und das Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="79bcd-110">The DirectShow SDK and the Windows Media Format SDK</span></span>](the-directshow-sdk-and-the-windows-media-format-sdk.md)
-   [<span data-ttu-id="79bcd-111">Konfigurieren des ASF-Writer</span><span class="sxs-lookup"><span data-stu-id="79bcd-111">Configuring the ASF Writer</span></span>](configuring-the-asf-writer.md)
-   [<span data-ttu-id="79bcd-112">Erstellen von Filterdiagrammen zum Schreiben von ASF-Dateien</span><span class="sxs-lookup"><span data-stu-id="79bcd-112">Building Filter Graphs to Write ASF Files</span></span>](building-filter-graphs-to-write-asf-files.md)
-   [<span data-ttu-id="79bcd-113">Konfigurieren von Profilen und anderen ASF-Dateieigenschaften</span><span class="sxs-lookup"><span data-stu-id="79bcd-113">Configuring Profiles and Other ASF File Properties</span></span>](configuring-profiles-and-other-asf-file-properties.md)
-   [<span data-ttu-id="79bcd-114">Entsperren des Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="79bcd-114">Unlocking the Windows Media Format SDK</span></span>](unlocking-the-windows-media-format-sdk.md)

## <a name="related-topics"></a><span data-ttu-id="79bcd-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79bcd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79bcd-116">Verwenden von Windows Media in DirectShow</span><span class="sxs-lookup"><span data-stu-id="79bcd-116">Using Windows Media in DirectShow</span></span>](using-windows-media-in-directshow.md)
</dt> </dl>

 

 



