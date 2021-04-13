---
title: Wmpdvd-Protokoll
description: Wmpdvd-Protokoll
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Windows-Media Player, Protokolle
- Windows Media Player-Objektmodell, Protokolle
- Objektmodell, Protokolle
- Windows Media Player ActiveX-Steuerelement, Protokolle für das Objektmodell
- ActiveX-Steuerelement, Protokolle für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Protokolle für das Objektmodell
- Windows Media Player Mobile, Protokolle für das Objektmodell
- Protokolle, Windows Media Player-Objektmodell
- Protokolle, wmpdvd
- Wmpdvd-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4d3949c18a268ea6a2fffc196081ba466b5758
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309872"
---
# <a name="wmpdvd-protocol"></a><span data-ttu-id="b6a84-113">Wmpdvd-Protokoll</span><span class="sxs-lookup"><span data-stu-id="b6a84-113">WMPDVD Protocol</span></span>

<span data-ttu-id="b6a84-114">Mit dem wmpdvd-Protokoll können Sie mithilfe der URL-Syntax Medien von einer DVD angeben.</span><span class="sxs-lookup"><span data-stu-id="b6a84-114">The WMPDVD protocol enables you to specify media from a DVD using URL syntax.</span></span> <span data-ttu-id="b6a84-115">Dies ist die allgemeine Form des Protokolls:</span><span class="sxs-lookup"><span data-stu-id="b6a84-115">This is the general form of the protocol:</span></span>


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



<span data-ttu-id="b6a84-116">Das *Laufwerk* Segment ist der Buchstabe des DVD-Laufwerks. der Doppelpunkt, der normalerweise mit laufwerkspezifiken verwendet wird, ist nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="b6a84-116">The *drive* segment is the letter of the DVD drive; it does not include the colon typically used with drive specifiers.</span></span> <span data-ttu-id="b6a84-117">Dieses Segment ist immer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b6a84-117">This segment is always required.</span></span>

<span data-ttu-id="b6a84-118">Das *Titel* Segment ist die Nummer des zu Wiedergabe enden Titels.</span><span class="sxs-lookup"><span data-stu-id="b6a84-118">The *title* segment is the number of the title to play.</span></span> <span data-ttu-id="b6a84-119">Es ist nicht erforderlich, es sei denn, Sie möchten die Wiedergabe an einem bestimmten Titel oder in einem bestimmten Kapitel eines bestimmten Titels starten.</span><span class="sxs-lookup"><span data-stu-id="b6a84-119">It is not required unless you want to start playback at a specific title or at a specific chapter of a specific title.</span></span>

<span data-ttu-id="b6a84-120">Das *Kapitel* Segment ist die Nummer des zu Wiedergabe enden Kapitels.</span><span class="sxs-lookup"><span data-stu-id="b6a84-120">The *chapter* segment is the number of the chapter to play.</span></span> <span data-ttu-id="b6a84-121">Es ist nicht erforderlich, es sei denn, Sie möchten die Wiedergabe in einem bestimmten Kapitel eines bestimmten Titels starten.</span><span class="sxs-lookup"><span data-stu-id="b6a84-121">It is not required unless you want to start playback at a specific chapter of a specific title.</span></span>

<span data-ttu-id="b6a84-122">Das contentdir-Argument ist der Pfad zu einem Video \_ TS. Die IFO-Datei, die sich im lokalen Speicher oder auf einer Netzwerkfreigabe befinden kann.</span><span class="sxs-lookup"><span data-stu-id="b6a84-122">The contentdir argument is the path to a VIDEO\_TS.IFO file, which may be in local storage or on a network share.</span></span> <span data-ttu-id="b6a84-123">Wenn Sie dieses Segment einschließen, wird das *Laufwerk* Segment ignoriert, obwohl es noch erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b6a84-123">If you include this segment, then the *drive* segment is ignored although it is still required.</span></span> <span data-ttu-id="b6a84-124">Wenn Sie auch das *Titel* Segment oder die *Titel* -und *Kapitel* Segmente einschließen, sind Sie relativ zum im contentdir-Segment angegebenen DVD-Inhalt, nicht zum *Laufwerks* Segment.</span><span class="sxs-lookup"><span data-stu-id="b6a84-124">If you also include the *title* segment or both the *title* and *chapter* segments then they are relative to the DVD content specified in the contentdir segment, not the *drive* segment.</span></span>

<span data-ttu-id="b6a84-125">Im folgenden Beispiel wird das wmpdvd-Protokoll verwendet, um die DVD von Anfang an wiederzugeben, als ob Sie automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b6a84-125">The following example uses the WMPDVD protocol to play the DVD from the beginning, as if it were starting automatically.</span></span>


```C++
player.url = "wmpdvd://F";
```



<span data-ttu-id="b6a84-126">Im folgenden Beispiel wird das wmpdvd-Protokoll verwendet, um die DVD am Anfang des angegebenen Titels wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="b6a84-126">The following example uses the WMPDVD protocol to play the DVD from the beginning of the specified title.</span></span>


```C++
player.url = "wmpdvd://F/2";
```



<span data-ttu-id="b6a84-127">Im folgenden Beispiel wird das wmpdvd-Protokoll verwendet, um die DVD aus dem angegebenen Kapitel wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="b6a84-127">The following example uses the WMPDVD protocol to play the DVD from the specified chapter.</span></span>


```C++
player.url = "wmpdvd://F/2/4";
```



<span data-ttu-id="b6a84-128">Im folgenden Beispiel wird das wmpdvd-Protokoll verwendet, um DVD-Inhalt aus lokalem Speicher wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="b6a84-128">The following example uses the WMPDVD protocol to play DVD content from local storage.</span></span> <span data-ttu-id="b6a84-129">Die *Pfad* Zeichenfolge endet mit dem Ordner, der die Video- \_ TS enthält. IFO-Datei; der Dateiname ist nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="b6a84-129">The *path* string ends with the folder that contains the VIDEO\_TS.IFO file; it does not include the file name.</span></span> <span data-ttu-id="b6a84-130">In diesem Beispiel hat der Wert des *Laufwerks* Segments keine Auswirkung, obwohl es erforderlich ist, und die Wiedergabe beginnt in Kapitel 4 von Titel 2.</span><span class="sxs-lookup"><span data-stu-id="b6a84-130">In this example, the value of the *drive* segment has no effect although it is required, and playback begins in chapter 4 of title 2.</span></span>


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



<span data-ttu-id="b6a84-131">Das Zuweisen einer wmpdvd-Zeichenfolge zur **URL** -Eigenschaft erfordert Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="b6a84-131">Assigning a WMPDVD string to the **url** property requires Windows Media Player 9 Series or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6a84-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6a84-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6a84-133">**Unterstützte Protokolle und Dateitypen**</span><span class="sxs-lookup"><span data-stu-id="b6a84-133">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




