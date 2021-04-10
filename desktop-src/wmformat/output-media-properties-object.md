---
title: Eigenschaften Objekt für Ausgabemedien
description: Eigenschaften Objekt für Ausgabemedien
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Windows Media-Format-SDK, Objekte für Ausgabemedien Eigenschaften
- Advanced Systems Format (ASF), Ausgabemedien Eigenschaften Objekte
- ASF (Advanced Systems Format), Ausgabemedien Eigenschaften Objekte
- Objekte, Objekte für Ausgabemedien Eigenschaften
- Objekte der Ausgabemedien Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038686"
---
# <a name="output-media-properties-object"></a><span data-ttu-id="b8c19-108">Eigenschaften Objekt für Ausgabemedien</span><span class="sxs-lookup"><span data-stu-id="b8c19-108">Output Media Properties Object</span></span>

<span data-ttu-id="b8c19-109">Ein Ausgabemedien-Eigenschaften Objekt wird verwendet, um eine Ausgabe Eigenschaft abzurufen und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b8c19-109">An output media properties object is used to retrieve and set an output property.</span></span> <span data-ttu-id="b8c19-110">Ausgabemedien Eigenschaften Objekte werden für unterstützte Ausgabeformate von Streams in einer Datei erstellt, die in ein Reader-Objekt geladen wird.</span><span class="sxs-lookup"><span data-stu-id="b8c19-110">Output media properties objects are created for supported output formats of streams in a file that is loaded into a reader object.</span></span> <span data-ttu-id="b8c19-111">Bei komprimierten Datenströmen werden die Ausgabe Eigenschaften durch die möglichen Ausgaben des Dekomprimierungs Codecs bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b8c19-111">For compressed streams, the output properties are determined by the possible outputs of the decompressing codec.</span></span>

<span data-ttu-id="b8c19-112">Ein Ausgabemedien-Eigenschaften Objekt wird von [**iwmreader:: getOutputProperties**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) erstellt. diese Methode erstellt ein Ausgabemedien-Eigenschaften Objekt, das die Eigenschaften des Standardausgabe Formats enthält.</span><span class="sxs-lookup"><span data-stu-id="b8c19-112">An output media properties object is created by [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) This method creates an output media properties object that contains the properties of the default output format.</span></span> <span data-ttu-id="b8c19-113">Andere Formate können für eine Ausgabe unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b8c19-113">Other formats may be supported for an output.</span></span> <span data-ttu-id="b8c19-114">Zum Abrufen zusätzlicher Ausgabeformate können Sie [**iwmreader:: getoutputformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) aufrufen, um die Anzahl der unterstützten Ausgabeformate abzurufen und Sie dann mithilfe von Aufrufen von [**iwmreader:: getoutputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat)durchlaufen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="b8c19-114">To obtain additional output formats, you can call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported output formats and then loop through them using calls to [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat).</span></span> <span data-ttu-id="b8c19-115">**Getoutputformat** erstellt ein Ausgabemedien Eigenschaften-Objekt, das mit den Daten für das ausgewählte Ausgabeformat aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="b8c19-115">**GetOutputFormat** creates an output media properties object populated with the data for the selected output format.</span></span>

<span data-ttu-id="b8c19-116">Objekte der Ausgabemedien Eigenschaften können auch mit dem synchronen Reader erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b8c19-116">Output media properties objects can also be created with the synchronous reader.</span></span> <span data-ttu-id="b8c19-117">Alle Methodennamen sind identisch mit denen im Reader und werden alle von der [**iwmsynkreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) -Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="b8c19-117">All of the method names are identical to those in the reader and they are all exposed by the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

<span data-ttu-id="b8c19-118">" **GetOutput-** Eigenschaften" und " **getoutputformat** " legen einen Zeiger auf eine [**iwmoutputmediarequicschnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) fest.</span><span class="sxs-lookup"><span data-stu-id="b8c19-118">**GetOutputProps** and **GetOutputFormat** both set a pointer to an [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface.</span></span> <span data-ttu-id="b8c19-119">Die anderen Schnittstellen des Eigenschaften Objekts der Ausgabemedien können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b8c19-119">The other interfaces of the output media properties object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="b8c19-120">Die folgenden Schnittstellen werden von allen Ausgabemedien-Eigenschaften Objekten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b8c19-120">The following interfaces are supported by every output media properties object.</span></span>



| <span data-ttu-id="b8c19-121">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b8c19-121">Interface</span></span>                                          | <span data-ttu-id="b8c19-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8c19-122">Description</span></span>                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8c19-123">**Iwmmedia-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="b8c19-123">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | <span data-ttu-id="b8c19-124">Wird als Basisschnittstelle für die anderen Schnittstellen der Medien Eigenschaft verwendet (Eingabe, Ausgabe und Video).</span><span class="sxs-lookup"><span data-stu-id="b8c19-124">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="b8c19-125">**Iwmoutputmedia-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="b8c19-125">**IWMOutputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | <span data-ttu-id="b8c19-126">Ruft die Eigenschaften einer Ausgabe ab.</span><span class="sxs-lookup"><span data-stu-id="b8c19-126">Retrieves the properties of an output.</span></span>                                                                     |
| [<span data-ttu-id="b8c19-127">**Iwmvideomedia-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="b8c19-127">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | <span data-ttu-id="b8c19-128">Verwaltet die Eigenschaften eines Videostreams.</span><span class="sxs-lookup"><span data-stu-id="b8c19-128">Manages the properties of a video stream.</span></span> <span data-ttu-id="b8c19-129">Dies ist eine optionale Schnittstelle, die nur für Videostreams verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b8c19-129">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b8c19-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8c19-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8c19-131">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="b8c19-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="b8c19-132">**Reader-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b8c19-132">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




