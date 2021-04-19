---
description: DMO-Architektur
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: DMO-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343122"
---
# <a name="dmo-architecture"></a><span data-ttu-id="2d69a-103">DMO-Architektur</span><span class="sxs-lookup"><span data-stu-id="2d69a-103">DMO Architecture</span></span>

<span data-ttu-id="2d69a-104">In diesem Abschnitt wird die allgemeine Architektur eines DMO beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2d69a-104">This section describes the overall architecture of a DMO.</span></span>

<span data-ttu-id="2d69a-105">**Streams**</span><span class="sxs-lookup"><span data-stu-id="2d69a-105">**Streams**</span></span>

<span data-ttu-id="2d69a-106">Ein DMO ist ein Objekt, das *m* Eingaben annimmt und *n* Ausgaben erzeugt.</span><span class="sxs-lookup"><span data-stu-id="2d69a-106">A DMO is an object that takes *m* inputs and produces *n* outputs.</span></span> <span data-ttu-id="2d69a-107">Die Eingaben und Ausgaben werden als *Streams* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2d69a-107">The inputs and outputs are called *streams*.</span></span> <span data-ttu-id="2d69a-108">Jeder DMO verfügt über mindestens einen Stream.</span><span class="sxs-lookup"><span data-stu-id="2d69a-108">Every DMO has at least one stream.</span></span> <span data-ttu-id="2d69a-109">Streams sind keine Objekte. auf Sie wird einfach durch die Indexnummer in der DMO verwiesen.</span><span class="sxs-lookup"><span data-stu-id="2d69a-109">Streams are not objects; they are simply referenced on the DMO by index number.</span></span> <span data-ttu-id="2d69a-110">Die Anzahl der Streams ist zur Entwurfszeit korrigiert.</span><span class="sxs-lookup"><span data-stu-id="2d69a-110">The number of streams is fixed at design time.</span></span>

<span data-ttu-id="2d69a-111">**Medientypen**</span><span class="sxs-lookup"><span data-stu-id="2d69a-111">**Media Types**</span></span>

<span data-ttu-id="2d69a-112">Alle Daten werden mit einem *Medientyp* typisiert, der definiert, wie der Inhalt der Daten interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d69a-112">All data is typed using a *media type*, which defines how to interpret the contents of the data.</span></span> <span data-ttu-id="2d69a-113">Beispielsweise ist 320 x 240 24 Bit RGB Video ein Typ. 44,1-Kilohertz (kHz) 16-Bit-Stereo PCM-Audiodatei ist ein anderer Typ.</span><span class="sxs-lookup"><span data-stu-id="2d69a-113">For example, 320 x 240 24-bit RGB video is one type; 44.1-kilohertz (kHz) 16-bit stereo PCM audio is another type.</span></span> <span data-ttu-id="2d69a-114">Medientypen werden mithilfe der [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2d69a-114">Media types are described using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="2d69a-115">Bevor der Client Daten verarbeiten kann, muss er den Medientyp für jeden Stream in der DMO festlegen.</span><span class="sxs-lookup"><span data-stu-id="2d69a-115">Before the client can process any data, it must set the media type for each stream on the DMO.</span></span>

<span data-ttu-id="2d69a-116">In der Regel kann ein Stream einen Bereich von Medientypen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="2d69a-116">Typically, a stream can accept a range of media types.</span></span> <span data-ttu-id="2d69a-117">Einige DMOS unterstützen eine größere Anzahl von Typen als andere.</span><span class="sxs-lookup"><span data-stu-id="2d69a-117">Some DMOs support a wider range of types than others.</span></span> <span data-ttu-id="2d69a-118">Die DMO-Schnittstellen definieren Methoden für den Client, um die unterstützten Typen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2d69a-118">The DMO interfaces define methods for the client to discover the supported types.</span></span> <span data-ttu-id="2d69a-119">Beispielsweise kann ein DMO RGB-Video in beliebiger bidirektiontiefe unterstützen, während ein anderes nur 24-Bit-RGB unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2d69a-119">For example, one DMO might support RGB video at any bit depth, while another might support only 24-bit RGB.</span></span> <span data-ttu-id="2d69a-120">Außerdem kann ein DMO auf bestimmte Kombinationen von Eingaben und Ausgaben beschränkt sein.</span><span class="sxs-lookup"><span data-stu-id="2d69a-120">Also, a DMO might be limited to certain combinations of inputs and outputs.</span></span> <span data-ttu-id="2d69a-121">Wenn der Eingabetyp beispielsweise ein 16-Bit-Video ist, kann der Ausgabestream die gleiche Bittiefe erfordern.</span><span class="sxs-lookup"><span data-stu-id="2d69a-121">For example, if the input type is 16-bit video, the output stream might require the same bit depth.</span></span> <span data-ttu-id="2d69a-122">Der Client kann die bevorzugten Typen jedes Streams auflisten und dann bestimmte Kombinationen testen.</span><span class="sxs-lookup"><span data-stu-id="2d69a-122">The client can enumerate each stream's preferred types and then test specific combinations.</span></span>

<span data-ttu-id="2d69a-123">**Puffer**</span><span class="sxs-lookup"><span data-stu-id="2d69a-123">**Buffers**</span></span>

<span data-ttu-id="2d69a-124">Im DMO-Standardmodell ordnet der Client separate Eingabepuffer und Ausgabepuffer zu.</span><span class="sxs-lookup"><span data-stu-id="2d69a-124">In the default DMO model, the client allocates separate input buffers and output buffers.</span></span> <span data-ttu-id="2d69a-125">Sie füllt die Eingabepuffer mit Daten und übergibt sie an den DMO, und der DMO schreibt neue Daten in die Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="2d69a-125">It fills the input buffers with data and delivers them to the DMO, and the DMO writes new data into the output buffers.</span></span>

<span data-ttu-id="2d69a-126">Optional kann ein DMO die direkte Verarbeitung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2d69a-126">Optionally, a DMO can support "in-place" processing.</span></span> <span data-ttu-id="2d69a-127">Bei der direkten Verarbeitung schreibt der DMO die Ausgabe direkt in den Eingabepuffer, und zwar über die ursprünglichen Daten.</span><span class="sxs-lookup"><span data-stu-id="2d69a-127">With in-place processing, the DMO writes the output directly into the input buffer, over the original data.</span></span> <span data-ttu-id="2d69a-128">Durch die direkte Verarbeitung entfällt die Notwendigkeit separater Puffer.</span><span class="sxs-lookup"><span data-stu-id="2d69a-128">In-place processing eliminates the need for separate buffers.</span></span> <span data-ttu-id="2d69a-129">Auf der anderen Seite ändert Sie die ursprünglichen Daten, die für einige Anwendungen möglicherweise nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="2d69a-129">On the other hand, it alters the original data, which may not be acceptable for some applications.</span></span>

<span data-ttu-id="2d69a-130">Das standardmäßige (nicht direkte) Puffer Modell wird durch die [**imediaobject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2d69a-130">The default (non-in-place) buffering model is supported through the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="2d69a-131">Alle DMOS müssen diese Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="2d69a-131">All DMOs must implement this interface.</span></span> <span data-ttu-id="2d69a-132">Wenn ein DMO die direkte Verarbeitung unterstützt, wird auch die [**imediaobjectinplace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) -Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="2d69a-132">If a DMO supports in-place processing, it also exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="2d69a-133">Der Client ist für die Zuordnung aller Puffer (Eingabe und Ausgabe) verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="2d69a-133">The client is responsible for allocating all buffers, both input and output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d69a-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d69a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d69a-135">Informationen zu DMOS</span><span class="sxs-lookup"><span data-stu-id="2d69a-135">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



