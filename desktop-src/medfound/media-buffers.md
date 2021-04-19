---
description: Medien Puffer
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Medien Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87316ea64e24173dfa73f2cc2ff280a1281d50f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361769"
---
# <a name="media-buffers"></a><span data-ttu-id="11823-103">Medien Puffer</span><span class="sxs-lookup"><span data-stu-id="11823-103">Media Buffers</span></span>

<span data-ttu-id="11823-104">Ein Medien Puffer ist ein COM-Objekt, das einen Speicherblock verwaltet, der normalerweise Mediendaten enthält.</span><span class="sxs-lookup"><span data-stu-id="11823-104">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="11823-105">Medien Puffer werden verwendet, um Daten von einer Pipeline Komponente in die nächste zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="11823-105">Media buffers are used to move data from one pipeline component to the next.</span></span> <span data-ttu-id="11823-106">Die meisten Anwendungen verwenden keine Medien Puffer direkt, da die Medien Sitzung den gesamten Datenfluss zwischen Pipeline Objekten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="11823-106">Most applications do not use media buffers directly, because the Media Session handles all of the data flow between pipeline objects.</span></span> <span data-ttu-id="11823-107">Sie müssen Medien Puffer verwenden, wenn Sie eine eigene Pipeline Komponente schreiben, oder wenn Sie eine Pipeline Komponente direkt ohne die Medien Sitzung verwenden.</span><span class="sxs-lookup"><span data-stu-id="11823-107">You must use media buffers if you are writing your own pipeline component, or if you are using a pipeline component directly without the Media Session.</span></span>

<span data-ttu-id="11823-108">Medien Puffer machen die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="11823-108">Media buffers exposes the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="11823-109">Diese Schnittstelle ist für das Lesen oder schreiben beliebiger Datentypen konzipiert.</span><span class="sxs-lookup"><span data-stu-id="11823-109">This interface is designed for reading or writing any type of data.</span></span> <span data-ttu-id="11823-110">Nicht komprimierte Videorahmen erfordern eine besondere Behandlung, da Sie möglicherweise in Direct3D-Oberflächen gespeichert werden, die sich im Videospeicher befinden.</span><span class="sxs-lookup"><span data-stu-id="11823-110">Uncompressed video frames require special handling, because they might be stored in Direct3D surfaces located in video memory.</span></span>

<span data-ttu-id="11823-111">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="11823-111">This section contains the following topics.</span></span>



| <span data-ttu-id="11823-112">Thema</span><span class="sxs-lookup"><span data-stu-id="11823-112">Topic</span></span>                                                        | <span data-ttu-id="11823-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11823-113">Description</span></span>                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="11823-114">Arbeiten mit Medien Puffern</span><span class="sxs-lookup"><span data-stu-id="11823-114">Working with Media Buffers</span></span>](working-with-media-buffers.md) | <span data-ttu-id="11823-115">Beschreibt das allgemeine Verhalten von Medien Puffern für alle Medientypen.</span><span class="sxs-lookup"><span data-stu-id="11823-115">Describes the general behavior of media buffers for all media types.</span></span> |
| [<span data-ttu-id="11823-116">Nicht komprimierte Video Puffer</span><span class="sxs-lookup"><span data-stu-id="11823-116">Uncompressed Video Buffers</span></span>](uncompressed-video-buffers.md) | <span data-ttu-id="11823-117">Arbeiten mit Medien Puffern, die nicht komprimierte Video Frames enthalten.</span><span class="sxs-lookup"><span data-stu-id="11823-117">How work with media buffers that contain uncompressed video frames.</span></span>  |
| [<span data-ttu-id="11823-118">DirectX-Oberflächen Puffer</span><span class="sxs-lookup"><span data-stu-id="11823-118">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)         | <span data-ttu-id="11823-119">Beschreibt, wie eine Direct3D-Oberfläche in einem Medien Puffer gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="11823-119">Describes how to store a Direct3D surface in a media buffer.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="11823-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11823-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11823-121">Media Foundation primitiver</span><span class="sxs-lookup"><span data-stu-id="11823-121">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



