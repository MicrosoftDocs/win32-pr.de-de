---
title: Arbeiten mit Ausgaben
description: Arbeiten mit Ausgaben
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows Media-Format-SDK, arbeiten mit Ausgaben
- Advanced Systems Format (ASF), arbeiten mit Ausgaben
- ASF (Advanced Systems Format), arbeiten mit Ausgaben
- Advanced Systems Format (ASF), Ausgabe Nummern und Formate
- ASF (Advanced Systems Format), Ausgabe Nummern und Formate
- ausgabezahlen und Formate, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d089a645838a295e07eb740927d75238473cc4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723456"
---
# <a name="working-with-outputs"></a><span data-ttu-id="ae527-109">Arbeiten mit Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae527-109">Working with Outputs</span></span>

<span data-ttu-id="ae527-110">Standardmäßig wird jedes Beispiel, das Sie von einem Leser Objekt erhalten, einer Ausgabe Nummer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ae527-110">As a default, every sample you receive from either reader object is associated with an output number.</span></span> <span data-ttu-id="ae527-111">Jede Ausgabe Nummer entspricht einem Stream in der ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="ae527-111">Each output number corresponds to a stream in the ASF file.</span></span> <span data-ttu-id="ae527-112">Der Reader weist den Streams in der Dateiausgabe Nummern zu, wenn die Datei geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ae527-112">The reader assigns output numbers to the streams in the file when the file is opened.</span></span> <span data-ttu-id="ae527-113">Normalerweise gibt es eine Ausgabe für jeden Stream in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="ae527-113">Normally there is one output for each stream in a file.</span></span> <span data-ttu-id="ae527-114">Wenn die Datei jedoch den gegenseitigen Ausschluss verwendet, wird jeder Gruppe von sich gegenseitig ausschließenden Streams eine einzelne Ausgabe Nummer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ae527-114">If the file uses mutual exclusion, however, each group of mutually exclusive streams is assigned a single output number.</span></span> <span data-ttu-id="ae527-115">Der Stream, der der Ausgabe Nummer der sich gegenseitig exklusiven Datenströme entspricht, wird entweder vom Reader, bei MBR-Dateien (Multiple Bitrate) oder von der Anwendung bestimmt, wenn Sie die manuelle Datenstrom Auswahl verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae527-115">The stream that corresponds to the output number of the mutually exclusive streams is determined either by the reader, in the case of multiple bit rate (MBR) files, or by your application, if you are using manual stream selection.</span></span>

<span data-ttu-id="ae527-116">Da der im Profil festgelegte Verbindungs Name nicht in der Datei persistent gespeichert wird, erstellt der Reader einen Standard Verbindungs Namen für jede Ausgabe, bei der es sich einfach um eine Zeichen folgen Darstellung der Ausgabe Nummer handelt, z. b. "1", "2", "3" usw.</span><span class="sxs-lookup"><span data-stu-id="ae527-116">Because the connection name set in the profile is not persisted in the file, the reader creates a default connection name for each output that is simply a string representation of the output number, for example "1", "2", "3" and so on.</span></span> <span data-ttu-id="ae527-117">Mit den Verbindungs Namen können Anwendungen und der Reader selbst Ausgaben mit Streams korrelieren.</span><span class="sxs-lookup"><span data-stu-id="ae527-117">The connection names enable applications, and the reader itself, to correlate outputs to streams.</span></span> <span data-ttu-id="ae527-118">In einer Datei mit mehreren Bitraten haben mehrere Streams einen Verbindungs Namen gemeinsam.</span><span class="sxs-lookup"><span data-stu-id="ae527-118">In a multiple bit rate file, several streams share a connection name.</span></span> <span data-ttu-id="ae527-119">Dies ist für den Reader nicht von Bedeutung, da die Ausgabe Eigenschaften für jeden MBR-Datenstrom identisch sind.</span><span class="sxs-lookup"><span data-stu-id="ae527-119">This does not matter to the reader, because the output properties for each MBR stream are identical.</span></span>

<span data-ttu-id="ae527-120">Jede Ausgabe verfügt über ein oder mehrere unterstützte Ausgabeformate.</span><span class="sxs-lookup"><span data-stu-id="ae527-120">Each output has one or more supported output formats.</span></span> <span data-ttu-id="ae527-121">Ein Ausgabeformat ist das Format, das von den vom Reader bereitgestellten nicht komprimierten Beispielen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae527-121">An output format is the format that the uncompressed samples delivered by the reader use.</span></span> <span data-ttu-id="ae527-122">Wenn der Reader eine Datei öffnet, wird das Format der einzelnen Ausgaben auf den Standardwert für den Medien Untertyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ae527-122">When the reader opens a file, it sets the format of each output to the default for the media subtype.</span></span> <span data-ttu-id="ae527-123">Die Anzahl und der Typ der unterstützten Ausgabeformate werden vom Codec bestimmt, der die Mediendaten dekomprimiert.</span><span class="sxs-lookup"><span data-stu-id="ae527-123">The number and type of output formats supported is determined by the codec that decompresses the media data.</span></span>

<span data-ttu-id="ae527-124">In den folgenden Themen wird erläutert, wie Sie mit Ausgaben arbeiten:</span><span class="sxs-lookup"><span data-stu-id="ae527-124">The following topics explain how to work with outputs:</span></span>

-   [<span data-ttu-id="ae527-125">So identifizieren Sie Ausgabe Nummern</span><span class="sxs-lookup"><span data-stu-id="ae527-125">To Identify Output Numbers</span></span>](to-identify-output-numbers.md)
-   [<span data-ttu-id="ae527-126">Zuweisen von Ausgabeformaten</span><span class="sxs-lookup"><span data-stu-id="ae527-126">Assigning Output Formats</span></span>](assigning-output-formats.md)

## <a name="related-topics"></a><span data-ttu-id="ae527-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ae527-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae527-128">**Iwmreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ae527-128">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="ae527-129">**Iwmsynkreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ae527-129">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="ae527-130">**Lesen von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="ae527-130">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




