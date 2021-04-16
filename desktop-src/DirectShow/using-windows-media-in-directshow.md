---
description: Verwenden von Windows-Medien in DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Verwenden von Windows-Medien in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104393858"
---
# <a name="using-windows-media-in-directshow"></a><span data-ttu-id="ad8c1-103">Verwenden von Windows-Medien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="ad8c1-103">Using Windows Media in DirectShow</span></span>

<span data-ttu-id="ad8c1-104">In diesem Abschnitt wird beschrieben, wie Sie mit DirectShow-Dateien (Advanced Systems Format) wiedergeben und schreiben.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-104">This section describes how to use DirectShow to play and write Advanced Systems Format (ASF) files.</span></span> <span data-ttu-id="ad8c1-105">ASF-Dateien enthalten häufig Audioinhalte und Videoinhalte, die mit den Windows Media Audio-und Video Codecs codiert sind.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-105">ASF files commonly contain audio and video content encoded using the Windows Media Audio and Video codecs.</span></span> <span data-ttu-id="ad8c1-106">Allerdings kann ASF beliebige Datentypen enthalten.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-106">However, ASF can contain any type of data.</span></span>

<span data-ttu-id="ad8c1-107">Die folgenden DirectShow-Filter unterstützen das Lesen und Schreiben von ASF-Dateien:</span><span class="sxs-lookup"><span data-stu-id="ad8c1-107">The following DirectShow filters support reading and writing ASF files:</span></span>

-   <span data-ttu-id="ad8c1-108">[WM-ASF-Lesefilter](wm-asf-reader-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ad8c1-108">[WM ASF Reader Filter](wm-asf-reader-filter.md).</span></span> <span data-ttu-id="ad8c1-109">Liest ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-109">Reads ASF files.</span></span>
-   <span data-ttu-id="ad8c1-110">[WM-ASF-Writer-Filter](wm-asf-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ad8c1-110">[WM ASF Writer Filter](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="ad8c1-111">Wrties von ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-111">Wrties ASF files.</span></span>
-   <span data-ttu-id="ad8c1-112">[DMO-Wrapper Filter](dmo-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ad8c1-112">[DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="ad8c1-113">Umschließt den Windows Media Encoder und Decoder-DMOS.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-113">Wraps the Windows Media encoder and decoder DMOs.</span></span>

### <a name="versions"></a><span data-ttu-id="ad8c1-114">Versionen</span><span class="sxs-lookup"><span data-stu-id="ad8c1-114">Versions</span></span>

<span data-ttu-id="ad8c1-115">Die Filter "WM ASF Reader" und "WM ASF Writer" sind in der DLL mit dem Namen "qasf.dll" verpackt, und die Filter werden zusammen mit dem Namen "qasf Components</span><span class="sxs-lookup"><span data-stu-id="ad8c1-115">The WM ASF Reader and WM ASF Writer filters are packaged in the DLL named qasf.dll, and the filters are collectively named "QASF components."</span></span> <span data-ttu-id="ad8c1-116">Diese Filter sind Wrapper für das Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-116">These filters are wrappers for the Windows Media Format SDK.</span></span> <span data-ttu-id="ad8c1-117">Die dll (qasf.dll) wurde zuerst im DirectX SDK veröffentlicht, aber später im Windows Media-Format SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-117">The DLL (qasf.dll) was first published in the DirectX SDK but was later updated in the Windows Media Format SDK.</span></span> <span data-ttu-id="ad8c1-118">Im folgenden finden Sie den Versionsverlauf der qasf-Filter:</span><span class="sxs-lookup"><span data-stu-id="ad8c1-118">Here is the version history of the QASF filters:</span></span>

-   <span data-ttu-id="ad8c1-119">DirectShow 8,1 unterstützt das Windows Media-Format SDK Version 7,0.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-119">DirectShow 8.1 supports Windows Media Format SDK version 7.0.</span></span>
-   <span data-ttu-id="ad8c1-120">DirectShow 9,0 unterstützt das Windows Media-Format SDK Version 7,1.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-120">DirectShow 9.0 supports Windows Media Format SDK version 7.1.</span></span>
-   <span data-ttu-id="ad8c1-121">Windows XP Service Pack 2 unterstützt das SDK für Windows Media-Format 9.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-121">Windows XP Service Pack 2 supports Windows Media Format 9 SDK.</span></span>
-   <span data-ttu-id="ad8c1-122">Windows Vista unterstützt das SDK für Windows Media-Format 11.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-122">Windows Vista supports Windows Media Format 11 SDK.</span></span>
-   <span data-ttu-id="ad8c1-123">Das Windows Media-Format 9 SDK und höher enthalten entsprechende Versionen von qasf.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-123">Windows Media Format 9 SDK and later contain corresponding versions of QASF.</span></span>

<span data-ttu-id="ad8c1-124">Um die neueste Version von qasf zu erhalten, laden Sie immer das neueste SDK für den Windows Media-Format herunter.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-124">To get the latest version of QASF, always download the latest Windows Media Format SDK.</span></span>

### <a name="legacy-windows-media-source-filter"></a><span data-ttu-id="ad8c1-125">Windows Media-Quell Filter (Legacy)</span><span class="sxs-lookup"><span data-stu-id="ad8c1-125">Legacy Windows Media Source Filter</span></span>

<span data-ttu-id="ad8c1-126">In Windows XP Service Pack 1 und früher ist der Standard Quell Filter für ASF-Dateien (. ASF-, WMV-und. WMA-Dateierweiterungen) der veraltete [Windows Media-Quell Filter](windows-media-source-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ad8c1-126">In Windows XP Service Pack 1 and earlier, the default source filter for ASF files (.asf, .wmv, and .wma file extensions) is the obsolete [Windows Media Source Filter](windows-media-source-filter.md).</span></span> <span data-ttu-id="ad8c1-127">Dieses Verhalten wurde beibehalten, um die Abwärtskompatibilität mit Anwendungen sicherzustellen, die Windows Media Player 6,4 verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-127">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="ad8c1-128">Neue Anwendungen sollten die neueren Versionen von qasf verwenden, sodass der WM-ASF-Reader den Standardfilter für die Wiedergabe von ASF-Dateien filtert.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-128">New applications should use the newer versions of QASF, which make the WM ASF Reader filter the default filter for playing ASF files.</span></span>

<span data-ttu-id="ad8c1-129">Weitere Informationen zur Windows Media Suite von Software Development Kits finden Sie im Abschnitt " [Audiodateien und Video](../audio-and-video.md) " der MDSN-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="ad8c1-129">For more information on the Windows Media suite of software development kits, see the [Audio and Video](../audio-and-video.md) section of the MDSN Library.</span></span>

<span data-ttu-id="ad8c1-130">Dieser Artikel enthält folgende Themen:</span><span class="sxs-lookup"><span data-stu-id="ad8c1-130">This article contains the following topics:</span></span>

-   [<span data-ttu-id="ad8c1-131">Lesen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="ad8c1-131">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
-   [<span data-ttu-id="ad8c1-132">Erstellen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="ad8c1-132">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="ad8c1-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ad8c1-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad8c1-134">Verwenden von DirectShow</span><span class="sxs-lookup"><span data-stu-id="ad8c1-134">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 
