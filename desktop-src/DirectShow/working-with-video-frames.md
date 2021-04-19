---
description: Arbeiten mit Video Frames
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Arbeiten mit Video Frames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead597fac5a28befc9c9868485840d03b46e5185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356215"
---
# <a name="working-with-video-frames"></a><span data-ttu-id="fc8d8-103">Arbeiten mit Video Frames</span><span class="sxs-lookup"><span data-stu-id="fc8d8-103">Working with Video Frames</span></span>

<span data-ttu-id="fc8d8-104">Unkomprimiertes Video ist eine Sequenz von Bitmaps, die in schneller Folge abgespielt werden, in der Regel mit einer Rate von ungefähr 30 Frames pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-104">Uncompressed video is a sequence of bitmaps played in rapid succession, typically at a rate of about 30 frames per second.</span></span> <span data-ttu-id="fc8d8-105">Da in den meisten Videos ein DirectShow-Filter Diagramm in einem komprimierten Format eingegeben wird, durchläuft der Videostream in der Regel einen Decoder zur Dekomprimierung.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-105">Because most video enters a DirectShow filter graph in a compressed format, the video stream generally goes through a decoder for decompression.</span></span> <span data-ttu-id="fc8d8-106">Viele Decoder geben Daten in einem YUV-Format aus und belassen die endgültige Konvertierung für die Video Hardware direkt vor dem Rendering in RGB.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-106">Many decoders output data in a YUV format and leave the final conversion to RGB for the video hardware just prior to rendering.</span></span> <span data-ttu-id="fc8d8-107">Wenn ein Decoder eine DirectX-Videobeschleunigung verwendet, führt die Video Hardware zusätzliche Arbeit aus, um das Bild zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-107">If a decoder uses DirectX Video Acceleration, the video hardware performs additional work to decode the image.</span></span> <span data-ttu-id="fc8d8-108">Folglich wird die endgültige decokomprimierung der Bitmaps möglicherweise erst ausgeführt, wenn die Daten die Video Hardware erreichen.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-108">Thus, final decompression of the bitmaps may not be performed until the data reaches the video hardware.</span></span>

<span data-ttu-id="fc8d8-109">Um jedoch viele Arten der Videoanalyse,-Verarbeitung oder-Bearbeitung auszuführen, ist es oft notwendig, in einem Typ des RGB-oder YUV-Formats an unkomprimierten Bitmaps zu arbeiten, bevor Sie gerendert oder in eine Datei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-109">But to perform many types of video analysis, processing, or editing, it is often necessary to work on uncompressed bitmaps in some type of RGB or YUV format before they are rendered or written to file.</span></span> <span data-ttu-id="fc8d8-110">Diese Arbeit erfolgt in der Regel in einem Transformations Filter, der auf der [**ctransformfilter**](ctransformfilter.md) -Basisklasse basiert, insbesondere in der **Transformations** Methode.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-110">This work is typically done within a transform filter based on the [**CTransformFilter**](ctransformfilter.md) base class, specifically in the **Transform** method.</span></span> <span data-ttu-id="fc8d8-111">Diese Methode empfängt einen Zeiger auf ein [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Objekt, das die Videodaten kapselt.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-111">This method receives a pointer to an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) object that encapsulates the video data.</span></span> <span data-ttu-id="fc8d8-112">Die **imediasample:: getpointer** -Methode gibt einen Zeiger auf das erste Byte der Rohdaten zurück.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-112">The **IMediaSample::GetPointer** method returns a pointer to the first byte of the raw data.</span></span> <span data-ttu-id="fc8d8-113">Bei nicht komprimierten Frames bestehen diese Daten aus Pixeln, die direkt durch den Filter aufgerufen oder geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-113">For uncompressed frames, this data consists of pixels that can be accessed or modified directly by the filter.</span></span> <span data-ttu-id="fc8d8-114">In den folgenden Abschnitten finden Sie Hintergrundinformationen, die Ihnen helfen, auf diese Weise mit DIB-Daten effektiv zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-114">The following sections provide background information that will help you work effectively with DIB data in this manner.</span></span>

> [!Note]  
> <span data-ttu-id="fc8d8-115">Sie können die Bits auch mithilfe von GDI-, GDI+-, DirectDraw-oder Direct3D-Funktionen ändern, aber diese Techniken gehen über den Rahmen dieses Artikels hinaus.</span><span class="sxs-lookup"><span data-stu-id="fc8d8-115">You can also modify the bits by using GDI, GDI+, DirectDraw or Direct3D functions, but these techniques are beyond the scope of this article.</span></span>

 

<span data-ttu-id="fc8d8-116">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="fc8d8-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="fc8d8-117">Top-Down-und Bottom-Up Disb</span><span class="sxs-lookup"><span data-stu-id="fc8d8-117">Top-Down vs. Bottom-Up DIBs</span></span>](top-down-vs--bottom-up-dibs.md)
-   [<span data-ttu-id="fc8d8-118">Arbeiten mit 16-Bit-RGB</span><span class="sxs-lookup"><span data-stu-id="fc8d8-118">Working with 16-bit RGB</span></span>](working-with-16-bit-rgb.md)

 

 



