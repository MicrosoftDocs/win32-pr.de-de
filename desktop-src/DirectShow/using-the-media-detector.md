---
description: Verwenden des Medien Detektors
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: Verwenden des Medien Detektors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355708"
---
# <a name="using-the-media-detector"></a><span data-ttu-id="f8fe4-103">Verwenden des Medien Detektors</span><span class="sxs-lookup"><span data-stu-id="f8fe4-103">Using the Media Detector</span></span>

<span data-ttu-id="f8fe4-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="f8fe4-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f8fe4-105">Der Medien Detektor ist ein Hilfsobjekt, das Informationen über eine Datei abrufen kann, z. b. die Anzahl der Streams, ihren Typ und ihre Dauer.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-105">The media detector is a helper object that can retrieve information about a file, such as the number of streams, their type, and their duration.</span></span> <span data-ttu-id="f8fe4-106">Sie enthält auch Methoden zum Abrufen von Poster-Frames aus einem Videostream.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-106">It also contains methods for retrieving poster frames from a video stream.</span></span> <span data-ttu-id="f8fe4-107">Sie macht die [**imediadet**](imediadet.md) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-107">It exposes the [**IMediaDet**](imediadet.md) interface.</span></span>

<span data-ttu-id="f8fe4-108">Der Medien Detektor arbeitet in einem von zwei Modi.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-108">The media detector operates in one of two modes.</span></span> <span data-ttu-id="f8fe4-109">Wenn Sie eine Instanz des Medien Detektors erstellen, wird diese nicht an eine bestimmte Quelldatei angefügt.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-109">When you create an instance of the media detector, it is not attached to a particular source file.</span></span> <span data-ttu-id="f8fe4-110">In diesem Modus können Sie Datenstrom Informationen aus mehreren Quelldateien abrufen.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-110">In this mode, you can retrieve stream information from multiple source files.</span></span> <span data-ttu-id="f8fe4-111">Nachdem Sie jedoch mithilfe des Medien Detektors einen Poster-Frame abgerufen haben, wechselt er in den *Bitmap*-Abruf Modus.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-111">However, once you use the media detector to obtain a poster frame, it switches to *bitmap grab mode*.</span></span> <span data-ttu-id="f8fe4-112">Im bitmapingmodus wird der Medien Detektor an einen bestimmten Videostream angefügt, und die Datenstrom Informationsmethoden funktionieren nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-112">In bitmap grab mode, the media detector is attached to a specific video stream, and the stream information methods no longer work.</span></span> <span data-ttu-id="f8fe4-113">Außerdem gibt es keine Möglichkeit zum Wechsel des Medien Detektors in seinen Start Modus.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-113">Moreover, there is no way to switch the media detector back to its starting mode.</span></span> <span data-ttu-id="f8fe4-114">Rufen Sie daher alle benötigten Datenströme ab, bevor Sie Poster-Frames abrufen, oder erstellen Sie für jeden Stream neue Instanzen des Medien Detektors.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-114">Therefore, obtain any stream information you need before retrieving poster frames, or else create new instances of the media detector for each stream.</span></span>

<span data-ttu-id="f8fe4-115">Gehen Sie folgendermaßen vor, um streaminformationen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="f8fe4-115">To obtain stream information, do the following:</span></span>

1.  <span data-ttu-id="f8fe4-116">Nennen Sie [**imediadet::p UT \_ filename**](imediadet-put-filename.md) mit dem Namen der Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-116">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) with the name of the source file.</span></span>
2.  <span data-ttu-id="f8fe4-117">Rufen Sie [**imediadet:: get \_ outputstreams**](imediadet-get-outputstreams.md) auf, um die Anzahl der Streams in der Quelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-117">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of streams in the source.</span></span>
3.  <span data-ttu-id="f8fe4-118">Geben Sie eine streamnummer mit [**imediadet an::p UT \_ currentstream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="f8fe4-118">Specify a stream number with [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span> <span data-ttu-id="f8fe4-119">Dann wenden Sie eine oder mehrere der folgenden Methoden an:</span><span class="sxs-lookup"><span data-stu-id="f8fe4-119">Then call one or more of the following methods:</span></span>
    -   <span data-ttu-id="f8fe4-120">[**Imediadet:: get \_ Streamtype**](imediadet-get-streamtype.md): Ruft den Medientyp des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-120">[**IMediaDet::get\_StreamType**](imediadet-get-streamtype.md): Retrieves the stream's media type.</span></span>
    -   <span data-ttu-id="f8fe4-121">[**Imediadet:: get \_ Streamlength**](imediadet-get-streamlength.md): Ruft die Dauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-121">[**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md): Retrieves the duration of the stream.</span></span>
    -   <span data-ttu-id="f8fe4-122">[**Imediadet:: get \_ Framerate: Ruft die Framerate**](imediadet-get-framerate.md)eines Videostreams ab.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-122">[**IMediaDet::get\_FrameRate**](imediadet-get-framerate.md): Retrieves a video stream's frame rate.</span></span>

<span data-ttu-id="f8fe4-123">Um einen Poster-Frame zu erhalten, geben Sie die Datenstrom Nummer an, wie im vorherigen Schritt.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-123">To obtain a poster frame, specify the stream number, as in the previous step.</span></span> <span data-ttu-id="f8fe4-124">Anschließend wird entweder [**imediadet:: getbitmapbits**](imediadet-getbitmapbits.md)aufgerufen, mit dem ein Poster-Frame in einen Puffer kopiert wird, oder [**imediadet:: Beschreib tebitmapbits**](imediadet-writebitmapbits.md), der einen Poster-Frame in einer Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="f8fe4-124">Then call either [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md), which copies a poster frame into a buffer, or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md), which saves a poster frame to a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8fe4-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8fe4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8fe4-126">Arbeiten mit Quellen</span><span class="sxs-lookup"><span data-stu-id="f8fe4-126">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



