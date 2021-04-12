---
description: Arbeiten mit Videos
ms.assetid: ef361c85-8f3b-4719-80f2-853c84ae7277
title: Arbeiten mit Videos (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002b32fab6dafea91fb9c15d59a4ca3cca2f03f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348728"
---
# <a name="working-with-video-microsoft-media-foundation"></a><span data-ttu-id="940de-103">Arbeiten mit Videos (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="940de-103">Working with Video (Microsoft Media Foundation)</span></span>

<span data-ttu-id="940de-104">Obwohl die einzelnen Video Codecs ihre eigenen Besonderheiten aufweisen, verwenden alle die gleichen grundlegenden Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="940de-104">Although the individual video codecs have their own peculiarities, all use the same basic procedures.</span></span> <span data-ttu-id="940de-105">In diesem Abschnitt wird beschrieben, wie Sie Videos mit den Windows Media Video Codecs codieren und decodieren und die jeweiligen Features der jeweiligen Features adressiert werden.</span><span class="sxs-lookup"><span data-stu-id="940de-105">This section describes how to encode and decode video with the Windows Media Video codecs, and addresses the particular features of each.</span></span> <span data-ttu-id="940de-106">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="940de-106">This section contains the following topics.</span></span>



| <span data-ttu-id="940de-107">Thema</span><span class="sxs-lookup"><span data-stu-id="940de-107">Topic</span></span>                                                                                                        | <span data-ttu-id="940de-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="940de-108">Description</span></span>                                                                                             |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="940de-109">Auswählen eines Videocodecs</span><span class="sxs-lookup"><span data-stu-id="940de-109">Choosing a Video Codec</span></span>](choosingavideocodec.md)                                                            | <span data-ttu-id="940de-110">Beschreibt die Inhaltstypen, die sich am besten für die Komprimierung mit den einzelnen Windows Media Video Codecs eignen.</span><span class="sxs-lookup"><span data-stu-id="940de-110">Describes the types of content best suited for compression with each of the Windows Media Video codecs.</span></span> |
| [<span data-ttu-id="940de-111">Konfigurieren der Video Codierung</span><span class="sxs-lookup"><span data-stu-id="940de-111">Configuring Video Encoding</span></span>](configuringvideoencoding.md)                                                   | <span data-ttu-id="940de-112">Beschreibt, wie die Video Encoder-DMOS konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="940de-112">Describes how to configure the video encoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="940de-113">Konfigurieren der Video Decodierung</span><span class="sxs-lookup"><span data-stu-id="940de-113">Configuring Video Decoding</span></span>](configuringvideodecoding.md)                                                   | <span data-ttu-id="940de-114">Hier wird beschrieben, wie der Video Decoder-DMOS konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="940de-114">Describes how to configure the video decoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="940de-115">Erzwungene Keyframe-Einfügung</span><span class="sxs-lookup"><span data-stu-id="940de-115">Forced Key Frame Insertion</span></span>](forcedkeyframeinsertion.md)                                                    | <span data-ttu-id="940de-116">Beschreibt, wie angefordert wird, dass ein Beispiel als Keyframe codiert wird.</span><span class="sxs-lookup"><span data-stu-id="940de-116">Describes how to request that a sample be encoded as a key frame.</span></span>                                       |
| [<span data-ttu-id="940de-117">Video Codierung mit Zeilen Sprung</span><span class="sxs-lookup"><span data-stu-id="940de-117">Interlaced Video Encoding</span></span>](interlacedvideoencoding.md)                                                     | <span data-ttu-id="940de-118">Hier wird beschrieben, wie Sie in Windows Media Video Streams eine Verschachtelung erhalten.</span><span class="sxs-lookup"><span data-stu-id="940de-118">Describes how to maintain interlacing in Windows Media Video streams.</span></span>                                   |
| [<span data-ttu-id="940de-119">Verwenden des Windows Media Video 9 Advanced Profile Codec</span><span class="sxs-lookup"><span data-stu-id="940de-119">Using the Windows Media Video 9 Advanced Profile Codec</span></span>](usingthewindowsmediavideo9advancedprofilecodec.md) | <span data-ttu-id="940de-120">Beschreibt die Verwendung des Advanced Profile Codec für Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="940de-120">Describes how to use the Windows Media Video 9 Advanced Profile codec.</span></span>                                  |
| [<span data-ttu-id="940de-121">Verwenden des Windows Media Video 9-Bildschirm Codecs</span><span class="sxs-lookup"><span data-stu-id="940de-121">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)                    | <span data-ttu-id="940de-122">Beschreibt die Verwendung des Windows Media Video 9-Bildschirm Codecs.</span><span class="sxs-lookup"><span data-stu-id="940de-122">Describes how to use the Windows Media Video 9 Screen codec.</span></span>                                            |
| [<span data-ttu-id="940de-123">Verwenden des Windows Media Video 9,1-Abbild Codecs</span><span class="sxs-lookup"><span data-stu-id="940de-123">Using the Windows Media Video 9.1 Image Codec</span></span>](usingthewindowsmediavideo9imagecodec.md)                    | <span data-ttu-id="940de-124">Beschreibt die Verwendung des Windows Media Video 9,1-Bildcodecs.</span><span class="sxs-lookup"><span data-stu-id="940de-124">Describes how to use the Windows Media Video 9.1 Image codec.</span></span>                                           |



 

## <a name="related-topics"></a><span data-ttu-id="940de-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="940de-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="940de-126">Windows Media-Codecs</span><span class="sxs-lookup"><span data-stu-id="940de-126">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



