---
description: In diesem Thema wird beschrieben, wie Sie während der Wiedergabe mit mfplay suchen.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Suchen während der Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353161"
---
# <a name="how-to-seek-during-playback"></a><span data-ttu-id="7b88a-103">Suchen während der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="7b88a-103">How to Seek During Playback</span></span>

<span data-ttu-id="7b88a-104">\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7b88a-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7b88a-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7b88a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7b88a-106">\]</span><span class="sxs-lookup"><span data-stu-id="7b88a-106">\]</span></span>

<span data-ttu-id="7b88a-107">In diesem Thema wird beschrieben, wie Sie während der Wiedergabe mit mfplay suchen.</span><span class="sxs-lookup"><span data-stu-id="7b88a-107">This topic describes how to seek during playback using MFPlay.</span></span>

<span data-ttu-id="7b88a-108">**So suchen Sie während der Wiedergabe**</span><span class="sxs-lookup"><span data-stu-id="7b88a-108">**To Seek During Playback**</span></span>

1.  <span data-ttu-id="7b88a-109">Initialisieren Sie eine **PROPVARIANT** , die die Suchzeit in 100-Nanosecond-Einheiten als **großen \_ ganzzahligen** Typ (**VT \_ I8**) enthält.</span><span class="sxs-lookup"><span data-stu-id="7b88a-109">Initialize a **PROPVARIANT** to hold the seek time in 100-nanosecond units, as a **LARGE\_INTEGER** (**VT\_I8**) type.</span></span>
2.  <span data-ttu-id="7b88a-110">[**Imfpmediaplayer:: SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7b88a-110">Call [**IMFPMediaPlayer::SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition).</span></span> <span data-ttu-id="7b88a-111">Geben Sie für den ersten Parameter **MFP \_ PositionType \_ 100 ns** an, und übergeben Sie das **PROPVARIANT** -Zeichen für den zweiten Parameter.</span><span class="sxs-lookup"><span data-stu-id="7b88a-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter, and pass in the **PROPVARIANT** for the second parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b88a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b88a-112">Requirements</span></span>

<span data-ttu-id="7b88a-113">MF Play erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7b88a-113">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b88a-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b88a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b88a-115">Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="7b88a-115">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



