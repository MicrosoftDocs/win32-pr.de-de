---
description: Metronome-Filter Beispiel
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Metronome-Filter Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343940"
---
# <a name="metronome-filter-sample"></a><span data-ttu-id="8e21a-103">Metronome-Filter Beispiel</span><span class="sxs-lookup"><span data-stu-id="8e21a-103">Metronome Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="8e21a-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e21a-104">Description</span></span>

<span data-ttu-id="8e21a-105">Dieser Beispiel Filter zeigt, wie eine verweisuhr implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="8e21a-105">This sample filter shows how to implement a reference clock.</span></span> <span data-ttu-id="8e21a-106">Der Filter verwendet die standardmäßige Mikrofon Eingabe, um Audiospitzen (z. b. Klicks, Hand-claps oder coughs) zu lauschen, die zur Bestimmung der Taktfrequenz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e21a-106">The filter uses your default microphone input to listen for audio spikes (such as clicks, hand claps, or coughs), which it uses to determine a clock rate.</span></span>

## <a name="usage"></a><span data-ttu-id="8e21a-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="8e21a-107">Usage</span></span>

<span data-ttu-id="8e21a-108">Erstellen Sie das Beispiel Projekt, und kopieren Sie die Filter-DLL (Metronom.ax) in Ihr Windows-System Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="8e21a-108">Build the sample project and copy the filter DLL (Metronom.ax) to your Windows system directory.</span></span> <span data-ttu-id="8e21a-109">Führen Sie die Datei Metronom. reg aus, um die dll zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="8e21a-109">Run the Metronom.reg file to register the DLL.</span></span>

<span data-ttu-id="8e21a-110">So verwenden Sie den Filter:</span><span class="sxs-lookup"><span data-stu-id="8e21a-110">To use the filter:</span></span>

1.  <span data-ttu-id="8e21a-111">Erstellen eines Filter Diagramms in GraphEdit, das einen Videostream rendert.</span><span class="sxs-lookup"><span data-stu-id="8e21a-111">Build a filter graph in GraphEdit that renders a video stream.</span></span>
2.  <span data-ttu-id="8e21a-112">Löscht alle gerenderten Audiodatenströme.</span><span class="sxs-lookup"><span data-stu-id="8e21a-112">Delete any rendered audio streams.</span></span>
3.  <span data-ttu-id="8e21a-113">Fügen Sie dem Diagramm den Metronome-Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="8e21a-113">Add the Metronome filter to the graph.</span></span> <span data-ttu-id="8e21a-114">Sie wird in der Kategorie DirectShow-Filter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8e21a-114">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="8e21a-115">Führen Sie das Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="8e21a-115">Run the graph.</span></span> <span data-ttu-id="8e21a-116">Das Video beginnt mit normaler Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="8e21a-116">The video will begin playing at normal speed.</span></span>
5.  <span data-ttu-id="8e21a-117">Legen Sie Ihre Hände, oder verwenden Sie ein Metronome, um eine neue Geschwindigkeit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8e21a-117">Clap your hands or use a metronome to set a new speed.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="8e21a-118">Programmier Hinweise</span><span class="sxs-lookup"><span data-stu-id="8e21a-118">Programming Notes</span></span>

<span data-ttu-id="8e21a-119">Dieser Filter funktioniert nur für Videos.</span><span class="sxs-lookup"><span data-stu-id="8e21a-119">This filter works only for video.</span></span> <span data-ttu-id="8e21a-120">Der audiorenderer ist nicht in der Lage, eine Synchronisierung mit einer sehr unterschiedlichen Takt Rate durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="8e21a-120">The audio renderer is not capable of synchronizing to radically different clock rates.</span></span>

<span data-ttu-id="8e21a-121">Wenn Sie 92-mal pro Minute (einmal alle ~ 652 MS) angleichen, wird das Video mit dem normalen Satz abgespielt.</span><span class="sxs-lookup"><span data-stu-id="8e21a-121">If you clap 92 times per minute (once every ~652 ms), the video will play at the normal rate.</span></span> <span data-ttu-id="8e21a-122">Sie können diese Standardeinstellung ändern, indem Sie den Wert der Konstante `BPM` in Metronom. cpp ändern.</span><span class="sxs-lookup"><span data-stu-id="8e21a-122">You can change this default by changing the value of the constant `BPM` in Metronom.cpp.</span></span>

<span data-ttu-id="8e21a-123">Wenn Sie das applaudieren für einen bestimmten Zeitraum abbrechen und dann erneut mit dem applaudieren beginnen, müssen Sie mit ungefähr derselben Geschwindigkeit erneut starten, oder der Filter ignoriert es.</span><span class="sxs-lookup"><span data-stu-id="8e21a-123">If you stop clapping for a period of time and then start clapping again, you must start again at approximately the same speed, or the filter will ignore it.</span></span> <span data-ttu-id="8e21a-124">Außerdem wird die Geschwindigkeit der Videowiedergabe durch die CPU-Geschwindigkeit eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="8e21a-124">Also, the video playback rate is limited by the CPU speed.</span></span> <span data-ttu-id="8e21a-125">Wenn Sie den Grenzwert für eine beliebige Zeitspanne überschreiten, reagiert der Filter nicht mehr auf Raten Änderungen.</span><span class="sxs-lookup"><span data-stu-id="8e21a-125">If you exceed the limit for any length of time, the filter will stop responding to rate changes.</span></span> <span data-ttu-id="8e21a-126">Wenn dies der Fall ist, wird das Diagramm angehalten und neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="8e21a-126">If this happens, stop the graph and restart.</span></span>

<span data-ttu-id="8e21a-127">Wenn Sie Ihre eigene Uhr implementieren, sind die wichtigsten Regeln, dass die Referenzuhren nicht rückwärts gehen dürfen.</span><span class="sxs-lookup"><span data-stu-id="8e21a-127">If you implement your own clock, the most important rules is that reference clocks must not go backward.</span></span> <span data-ttu-id="8e21a-128">Das heißt, Sie müssen niemals einen Zeitwert melden, der kleiner als der vorherige Zeitwert ist.</span><span class="sxs-lookup"><span data-stu-id="8e21a-128">That is, they must never report a time value less than the previous time value.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="8e21a-129">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="8e21a-129">Downloading the Sample</span></span>

<span data-ttu-id="8e21a-130">Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8e21a-130">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="8e21a-131">Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK Root \]* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Metronome.</span><span class="sxs-lookup"><span data-stu-id="8e21a-131">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Metronome.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e21a-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e21a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e21a-133">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8e21a-133">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="8e21a-134">DirectShow-Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e21a-134">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



