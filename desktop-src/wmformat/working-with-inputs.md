---
title: Arbeiten mit Eingaben
description: Arbeiten mit Eingaben
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- Windows Media-Format-SDK, arbeiten mit Eingaben
- Advanced Systems Format (ASF), arbeiten mit Eingaben
- ASF (Advanced Systems Format), arbeiten mit Eingaben
- Profile, arbeiten mit Eingaben
- Streams, arbeiten mit Eingaben
- Codecs, arbeiten mit Eingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471116"
---
# <a name="working-with-inputs"></a><span data-ttu-id="5255e-109">Arbeiten mit Eingaben</span><span class="sxs-lookup"><span data-stu-id="5255e-109">Working with Inputs</span></span>

<span data-ttu-id="5255e-110">Ebenso wie die richtige Datenstrom Konfiguration im Profil erforderlich ist, um den Codec zum Komprimieren eines Streams zu erhalten, müssen Sie auch sicherstellen, dass der Typ der nicht komprimierten Medien, die Sie an den Writer übergeben, korrekt beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5255e-110">Just as the proper stream configuration in the profile is required to get the codec to compress a stream, you must also ensure that the type of uncompressed media you pass to the writer is accurately described.</span></span> <span data-ttu-id="5255e-111">Jedem Windows Media-Codec ist ein Standard Eingabetyp zugeordnet, es werden jedoch mehrere Eingabetypen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5255e-111">Every Windows Media codec has an associated default input type, but several input types are supported.</span></span> <span data-ttu-id="5255e-112">Sie können die unterstützten Eingaben überprüfen und den Eintrag auswählen, der Ihren Daten entspricht.</span><span class="sxs-lookup"><span data-stu-id="5255e-112">You can examine the supported inputs and select the one that matches your data.</span></span> <span data-ttu-id="5255e-113">Der Prozess der Arbeit mit Eingaben wird in den folgenden Schritten zusammengefasst:</span><span class="sxs-lookup"><span data-stu-id="5255e-113">The process of working with inputs is summarized in the following steps:</span></span>

1.  <span data-ttu-id="5255e-114">Wenn Sie ein Profil für den Writer laden, weist das Writer-Objekt für jede Verbindung im Profil eine Eingabe Nummer zu.</span><span class="sxs-lookup"><span data-stu-id="5255e-114">When you load a profile for the writer to use, the writer object assigns an input number for each connection in the profile.</span></span> <span data-ttu-id="5255e-115">Weitere Informationen zum Laden von Profilen für den Writer finden [Sie unter So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="5255e-115">For more information about loading profiles for the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="5255e-116">Es gibt eine Verbindung für jeden Stream, es sei denn, Sie verwenden den gegenseitigen Ausschluss mit der Bitrate.</span><span class="sxs-lookup"><span data-stu-id="5255e-116">Unless you are using mutual exclusion by bit rate, there is one connection for each stream.</span></span> <span data-ttu-id="5255e-117">Datenströme, die sich durch die Bitrate gegenseitig ausschließen, haben eine einzelne Verbindung gemeinsam.</span><span class="sxs-lookup"><span data-stu-id="5255e-117">Streams that are mutually exclusive by bit rate share a single connection.</span></span>
2.  <span data-ttu-id="5255e-118">Die Anwendung sollte die Eingabe Nummern für die Datei identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5255e-118">Your application should identify the input numbers for the file.</span></span> <span data-ttu-id="5255e-119">Weitere Informationen zum Identifizieren von Eingabe Nummern finden [Sie unter So identifizieren Sie Eingaben nach Nummer](to-identify-inputs-by-number.md).</span><span class="sxs-lookup"><span data-stu-id="5255e-119">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="5255e-120">Für jede Eingabe sollten Sie sicherstellen, dass das Eingabeformat mit Ihren Daten übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5255e-120">For each input, you should ensure that the input format matches your data.</span></span> <span data-ttu-id="5255e-121">Sie können die vom SDK unterstützten Eingabeformate auflisten.</span><span class="sxs-lookup"><span data-stu-id="5255e-121">You can enumerate the input formats supported by the SDK.</span></span> <span data-ttu-id="5255e-122">Weitere Informationen finden [Sie unter so zählen Sie Eingabeformate auf](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="5255e-122">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span> <span data-ttu-id="5255e-123">Sie können die Eingabeformate von beliebigen Streams oder Streams, die bereits komprimiert sind, nicht aufzählen.</span><span class="sxs-lookup"><span data-stu-id="5255e-123">You cannot enumerate the input formats of arbitrary streams or streams that are already compressed.</span></span> <span data-ttu-id="5255e-124">Weitere Informationen zu diesen besonderen Fällen finden Sie unter [beliebige und vorkomprimierte streameingaben](arbitrary-and-precompressed-stream-inputs.md).</span><span class="sxs-lookup"><span data-stu-id="5255e-124">For more information about these special cases, see [Arbitrary and Precompressed Stream Inputs](arbitrary-and-precompressed-stream-inputs.md).</span></span>
4.  <span data-ttu-id="5255e-125">Weisen Sie das richtige Eingabeformat für jede Verbindung zu.</span><span class="sxs-lookup"><span data-stu-id="5255e-125">Assign the correct input format for each connection.</span></span> <span data-ttu-id="5255e-126">Weitere Informationen finden Sie unter [Zuweisen von Eingabe Formaten](assigning-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="5255e-126">For more information, see [Assigning Input Formats](assigning-input-formats.md).</span></span>
5.  <span data-ttu-id="5255e-127">Einige Codec-und Writer-Funktionen werden zur Codierungs Zeit anstelle von im Profil konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5255e-127">Some codec and writer features are configured at encoding time instead of in the profile.</span></span> <span data-ttu-id="5255e-128">Zum Konfigurieren dieser Features müssen Sie die Eingabeeinstellungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5255e-128">To configure these features, you must use input settings.</span></span> <span data-ttu-id="5255e-129">Weitere Informationen finden [Sie unter So legen Sie Eingabeeinstellungen fest](to-set-input-settings.md).</span><span class="sxs-lookup"><span data-stu-id="5255e-129">For more information, see [To Set Input Settings](to-set-input-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5255e-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5255e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5255e-131">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="5255e-131">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




