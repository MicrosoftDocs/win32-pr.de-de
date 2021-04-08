---
title: ID3-Unterstützung
description: ID3 ist eine Organisation, die einen Satz von Standards zum Einschließen von Metadaten in MP3-Audiodateien (MPEG Layer 3) definiert hat.
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Windows Media-Format-SDK, ID3-Unterstützung
- Advanced Systems Format (ASF), ID3-Unterstützung
- ASF (Advanced Systems Format), ID3-Unterstützung
- Metadaten, id3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f356dae63b1d3672b584bb61956f478b67a697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713368"
---
# <a name="id3-support"></a><span data-ttu-id="0bfd9-108">ID3-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0bfd9-108">ID3 Support</span></span>

<span data-ttu-id="0bfd9-109">ID3 ist eine Organisation, die einen Satz von Standards zum Einschließen von Metadaten in MP3-Audiodateien (MPEG Layer 3) definiert hat.</span><span class="sxs-lookup"><span data-stu-id="0bfd9-109">ID3 is an organization that has defined a set of standards for including metadata in MPEG Layer-3 (MP3) audio files.</span></span> <span data-ttu-id="0bfd9-110">Die Objekte des SDK für den Windows Media-Format bieten Unterstützung für mit ID3 kompatible Attribute.</span><span class="sxs-lookup"><span data-stu-id="0bfd9-110">The objects of the Windows Media Format SDK provide support for ID3 compatible attributes.</span></span> <span data-ttu-id="0bfd9-111">Drei verschiedene ID3-Versionen werden unterstützt: ID3v1. x, id3v 2.2 und id3v 2.3/v2, 4.</span><span class="sxs-lookup"><span data-stu-id="0bfd9-111">Three distinct ID3 versions are supported: ID3v1.x, ID3v2.2, and ID3v2.3/v2,4.</span></span> <span data-ttu-id="0bfd9-112">Eine Liste der Attribute, die auf ID3-Frames entsprechen, finden Sie [unter Unterstützung von Unterstützung von Unterstützung](id3-tag-support.md).</span><span class="sxs-lookup"><span data-stu-id="0bfd9-112">For a list of the attributes that equate to ID3 frames, see [ID3 Tag Support](id3-tag-support.md).</span></span>

<span data-ttu-id="0bfd9-113">Sofern nicht anders angegeben, wird von den Objekten dieses SDK keine Überprüfung von ID3-Frame-Daten durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="0bfd9-113">Unless otherwise noted, no validation of ID3 frame data is performed by the objects of this SDK.</span></span> <span data-ttu-id="0bfd9-114">Das Metadatenattribut [**WM/ \_ liedsynchron**](wm-lyrics-synchronised.md) speichert z. b. die songtexte mit den entsprechenden Zeitstempeln.</span><span class="sxs-lookup"><span data-stu-id="0bfd9-114">For example, the metadata attribute [**WM/Lyrics\_Synchronised**](wm-lyrics-synchronised.md) stores the song lyrics with corresponding time stamps.</span></span> <span data-ttu-id="0bfd9-115">Wenn Sie ein **\_ synchronisiertes WM/Lied-** Attribut schreiben, werden die Objekte dieses SDK nicht überprüft, um sicherzustellen, dass die Zeitstempel in chronologischer Reihenfolge sind oder eine Überprüfung jeglicher Art ausführen.</span><span class="sxs-lookup"><span data-stu-id="0bfd9-115">When writing a **WM/Lyrics\_Synchronised** attribute, the objects of this SDK will not check to ensure that the time stamps are in chronological order or perform validation of any kind.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bfd9-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0bfd9-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bfd9-117">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0bfd9-117">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="0bfd9-118">**Metadatenfeatures**</span><span class="sxs-lookup"><span data-stu-id="0bfd9-118">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="0bfd9-119">**Arbeiten mit Metadaten**</span><span class="sxs-lookup"><span data-stu-id="0bfd9-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




