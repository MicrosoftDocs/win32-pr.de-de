---
description: Andere Quell Objekte
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Andere Quell Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747049"
---
# <a name="other-source-objects"></a><span data-ttu-id="3c28e-103">Andere Quell Objekte</span><span class="sxs-lookup"><span data-stu-id="3c28e-103">Other Source Objects</span></span>

<span data-ttu-id="3c28e-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="3c28e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3c28e-105">Zusätzlich zu Video-und Audioquellen unterstützt [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) die folgenden Quell Objekte.</span><span class="sxs-lookup"><span data-stu-id="3c28e-105">In addition to video and audio sources, [DirectShow Editing Services](directshow-editing-services.md) (DES) supports the following source objects.</span></span>

<span data-ttu-id="3c28e-106">**Bilder**</span><span class="sxs-lookup"><span data-stu-id="3c28e-106">**Still Images**</span></span>

<span data-ttu-id="3c28e-107">Des unterstützt die folgenden Dateiformate für weiterhin Images:</span><span class="sxs-lookup"><span data-stu-id="3c28e-107">DES supports the following file formats for still images:</span></span>

-   <span data-ttu-id="3c28e-108">Bitmap (.bmp)</span><span class="sxs-lookup"><span data-stu-id="3c28e-108">Bitmap (.bmp)</span></span>
-   <span data-ttu-id="3c28e-109">GIF (Graphics Interchange Format)</span><span class="sxs-lookup"><span data-stu-id="3c28e-109">GIF (Graphics Interchange Format)</span></span>
-   <span data-ttu-id="3c28e-110">JPEG (Joint Photographic Experts Group)</span><span class="sxs-lookup"><span data-stu-id="3c28e-110">JPEG (Joint Photographic Experts Group)</span></span>
-   <span data-ttu-id="3c28e-111">Targa-oder Truevision-Grafik Adapter (. TGA): Modus 2 (unkomprimiertes RGB) im 16-Bit-, 24-Bit-oder 32-Bit-Format.</span><span class="sxs-lookup"><span data-stu-id="3c28e-111">Targa or Truevision Graphics Adapter (.tga): Mode 2 (uncompressed RGB) in 16-bit, 24,-bit, or 32-bit format.</span></span>

<span data-ttu-id="3c28e-112">Diese Dateien können als Bilder oder zum Erstellen von Animationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c28e-112">These files can be used as still images or to create animations.</span></span> <span data-ttu-id="3c28e-113">Wenn Sie die Datei für Bitmap-, JPEG-und Targa-Dateien als Image verwenden, müssen Sie die [**iamtimelinesrc:: setdefaultfps**](iamtimelinesrc-setdefaultfps.md) -Methode aufrufen, um die Framerate auf 0 (null) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3c28e-113">For bitmap, JPEG, and Targa files, if you are using the file as a still image, call the [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) method to set the frame rate to zero.</span></span>

<span data-ttu-id="3c28e-114">**DIB-Sequenzen**</span><span class="sxs-lookup"><span data-stu-id="3c28e-114">**DIB Sequences**</span></span>

<span data-ttu-id="3c28e-115">Bei einer Reihe von Bitmap-, JPEG-oder Targa-Dateien kann die Renderingengine eine DIB-Sequenz erstellen.</span><span class="sxs-lookup"><span data-stu-id="3c28e-115">Given a series of bitmap, JPEG, or Targa files, the render engine can construct a DIB sequence.</span></span> <span data-ttu-id="3c28e-116">Zum Erstellen einer DIB-Sequenz müssen Sie den Dateien numerische sequenzielle Namen wie Image001.bmp, Image002.bmp, Image003.bmp usw. zuordnen.</span><span class="sxs-lookup"><span data-stu-id="3c28e-116">To create a DIB sequence, give the files numerically sequential names, such as Image001.bmp, Image002.bmp, Image003.bmp, and so on.</span></span> <span data-ttu-id="3c28e-117">Verwenden Sie die erste Datei in der Sequenz als Quelle.</span><span class="sxs-lookup"><span data-stu-id="3c28e-117">Use the first file in the sequence as the source.</span></span> <span data-ttu-id="3c28e-118">Legen Sie die Framerate für die Sequenz fest, indem Sie [**iamtimelinesrc:: setdefaultfps**](iamtimelinesrc-setdefaultfps.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3c28e-118">Set the frame rate for the sequence by calling [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md).</span></span> <span data-ttu-id="3c28e-119">Die Renderingengine durchläuft die Bilder in der Sequenz mit der angegebenen Framerate.</span><span class="sxs-lookup"><span data-stu-id="3c28e-119">The render engine cycles through the images in the sequence at the specified frame rate.</span></span>

<span data-ttu-id="3c28e-120">Wenn die Sequenz zu kurz ist, um die Dauer bei Angabe der Framerate auszufüllen, ist der Rest der Dauer solide schwarz.</span><span class="sxs-lookup"><span data-stu-id="3c28e-120">If the sequence is too short to fill the duration, given the frame rate, the rest of the duration is solid black.</span></span> <span data-ttu-id="3c28e-121">Während des Renderings tritt kein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="3c28e-121">No error occurs during rendering.</span></span>

<span data-ttu-id="3c28e-122">**GIF-Quellen**</span><span class="sxs-lookup"><span data-stu-id="3c28e-122">**GIF Sources**</span></span>

<span data-ttu-id="3c28e-123">Des unterstützt GIF-Quellen, einschließlich animierter und transparenter GIFs, mithilfe der GIF89a-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="3c28e-123">DES supports GIF sources, including animated and transparent GIFs, using the GIF89a specification.</span></span> <span data-ttu-id="3c28e-124">Bei einem animierten GIF müssen Sie im Gegensatz zu anderen Dateitypen die Framerate nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="3c28e-124">With an animated GIF, unlike the other file types, you do not need to set the frame rate.</span></span> <span data-ttu-id="3c28e-125">Die GIF-Datei gibt die Verzögerung zwischen den einzelnen Bildern in der Animation an.</span><span class="sxs-lookup"><span data-stu-id="3c28e-125">The GIF file specifies the delay between each image in the animation.</span></span>

<span data-ttu-id="3c28e-126">Zur Unterstützung transparenter-GIFs konvertiert des die transparenten Bereiche im Bild in den RGB-triplergb (0,0).</span><span class="sxs-lookup"><span data-stu-id="3c28e-126">To support transparent GIFs, DES converts transparent regions in the image to the RGB triplet RGB(0,0,0).</span></span> <span data-ttu-id="3c28e-127">Anschließend können Sie den [Schlüssel Übergang](key-transition.md) zu Key auf RGB (0,0) verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c28e-127">You can then use the [Key Transition](key-transition.md) to key on RGB(0,0,0).</span></span>

<span data-ttu-id="3c28e-128">Der konvertiert außerdem alle schwarzen Bereiche, die im Bereich RGB (0 – 7, 0 – 7, 0 – 7) liegen, in den Wert RGB (8, 8, 8) – mit Ausnahme des Transparenz Indexes, wenn er in diesen Bereich fällt.</span><span class="sxs-lookup"><span data-stu-id="3c28e-128">DES also converts any black regions that fall within the range RGB(0–7,0–7,0–7) to the value RGB(8,8,8)—except for the transparency index, if it falls in that range.</span></span> <span data-ttu-id="3c28e-129">Diese Konvertierung ist im Augenblick nicht erkennbar.</span><span class="sxs-lookup"><span data-stu-id="3c28e-129">This conversion is not detectable to the eye.</span></span>

<span data-ttu-id="3c28e-130">**Video Farbquelle**</span><span class="sxs-lookup"><span data-stu-id="3c28e-130">**Video Color Source**</span></span>

<span data-ttu-id="3c28e-131">Das [Video Farb Quellen](video-color-source.md) -Objekt erstellt ein kontinuierliches Video Bild einer voll Tonfarbe.</span><span class="sxs-lookup"><span data-stu-id="3c28e-131">The [Video Color Source](video-color-source.md) object creates a continuous video image of a solid color.</span></span> <span data-ttu-id="3c28e-132">Eine Verwendung für dieses Objekt besteht darin, es zu einer Ebene in einem Übergang zu machen.</span><span class="sxs-lookup"><span data-stu-id="3c28e-132">One use for this object is to make it a layer in a transition.</span></span> <span data-ttu-id="3c28e-133">Verwenden Sie diese z. b. in einem Video, das ein-oder ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c28e-133">For example, use it in a video fade-in or fade-out.</span></span>

<span data-ttu-id="3c28e-134">**Benutzerdefinierte Quell Filter**</span><span class="sxs-lookup"><span data-stu-id="3c28e-134">**Custom Source Filters**</span></span>

<span data-ttu-id="3c28e-135">Des kann einen DirectShow-Quell Filter als Zeitachsen Quelle verwenden, wenn der Filter die folgenden Bedingungen erfüllt:</span><span class="sxs-lookup"><span data-stu-id="3c28e-135">DES can use a DirectShow source filter as a timeline source, if the filter meets the following conditions:</span></span>

-   <span data-ttu-id="3c28e-136">Es unterstützt Suchvorgänge</span><span class="sxs-lookup"><span data-stu-id="3c28e-136">It supports seeking</span></span>
-   <span data-ttu-id="3c28e-137">Sie erzeugt ein Format, das von unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3c28e-137">It produces a format that DES supports.</span></span> <span data-ttu-id="3c28e-138">Das Format kann komprimiert werden, solange das System des Benutzers über einen DirectShow-Filter verfügt, der ihn decodieren kann.</span><span class="sxs-lookup"><span data-stu-id="3c28e-138">The format can be compressed as long as the user's system has a DirectShow filter capable of decoding it.</span></span>

<span data-ttu-id="3c28e-139">Wenn Sie eine benutzerdefinierte Quelle verwenden möchten, geben Sie die CLSID des Filters als untergeordnete GUID des Quell Objekts an.</span><span class="sxs-lookup"><span data-stu-id="3c28e-139">To use a custom source, specify the CLSID of the filter as the subobject GUID of the source object.</span></span> <span data-ttu-id="3c28e-140">Weitere Informationen finden Sie unter unter [geordnete Objekte](subobjects.md).</span><span class="sxs-lookup"><span data-stu-id="3c28e-140">For more information, see [Subobjects](subobjects.md).</span></span> <span data-ttu-id="3c28e-141">Um benutzerdefinierte Eigenschaften zu unterstützen, implementieren Sie Sie als **IDispatch** -"Put"-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3c28e-141">To support custom properties, implement them as **IDispatch** "put" properties.</span></span> <span data-ttu-id="3c28e-142">Nur statische Eigenschaften werden für Quell Objekte unterstützt. dynamische Eigenschaften werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c28e-142">Only static properties are supported on source objects; dynamic properties are not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c28e-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c28e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c28e-144">Arbeiten mit Quellen</span><span class="sxs-lookup"><span data-stu-id="3c28e-144">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



