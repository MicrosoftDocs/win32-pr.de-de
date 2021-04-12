---
description: Ein Poster-Frame wird gepackt.
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Ein Poster-Frame wird gepackt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf06a10d74bb6c81622ac9bad7a1b770f5dc12
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482694"
---
# <a name="grabbing-a-poster-frame"></a><span data-ttu-id="d3fc2-103">Ein Poster-Frame wird gepackt.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-103">Grabbing a Poster Frame</span></span>

<span data-ttu-id="d3fc2-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="d3fc2-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="d3fc2-105">In diesem Artikel wird beschrieben, wie ein Poster-Frame aus einer digitalen Mediendatei mit dem [Media Detector-Objekt (mediadet)](media-detector--mediadet.md) , das mit [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md)bereitgestellt wird, angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-105">This article describes how to display a poster frame from a digital media file, using the [Media Detector (MediaDet)](media-detector--mediadet.md) object provided with [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="d3fc2-106">Der Medien Detektor ist ein Hilfsobjekt, das Formatinformationen aus einer Medien Quelldatei erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-106">The Media Detector is a helper object that can get format information from a media source file.</span></span> <span data-ttu-id="d3fc2-107">Außerdem kann ein Bitmap-Bild von einem Videostream in der Quelldatei abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-107">It can also grab a bitmap image from a video stream in the source file.</span></span> <span data-ttu-id="d3fc2-108">Wenn Sie davon ausgehen, dass die Datei suchbar ist, können Sie das Bild von einem beliebigen Punkt in der Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-108">Assuming the file is seekable, you can obtain the image from any point in the file.</span></span> <span data-ttu-id="d3fc2-109">Das zurückgegebene Image weist immer das 24-Bit-RGB-Format auf.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-109">The returned image is always in 24-bit RGB format.</span></span>

<span data-ttu-id="d3fc2-110">Der Medien Detektor ist kein Filter, und die Anwendung muss nicht den Filter Graph-Manager verwenden oder ein Filter Diagramm erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-110">The Media Detector is not a filter, and the application does not need to use the Filter Graph Manager or create a filter graph.</span></span> <span data-ttu-id="d3fc2-111">Intern erstellt der Medien Detektor ein Filter Diagramm, das den [**Beispiel-Grabber Filter**](sample-grabber-filter.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-111">Internally, the Media Detector creates a filter graph that contains the [**Sample Grabber Filter**](sample-grabber-filter.md).</span></span> <span data-ttu-id="d3fc2-112">Zum Abrufen einer Bitmap sucht das Medien Erkennungs Tool das Filter Diagramm und hält es an und ruft dann die Bitmap aus dem Sample Grabber-Filter ab.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-112">To get a bitmap, the Media Detector seeks and pauses the filter graph, and then retrieves the bitmap from the Sample Grabber filter.</span></span> <span data-ttu-id="d3fc2-113">Die Anwendung kommuniziert mit dem Medien Erkennungs Modul über die [**imediadet**](imediadet.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-113">The application communicates with the Media Detector through the [**IMediaDet**](imediadet.md) interface.</span></span> <span data-ttu-id="d3fc2-114">Der Medien Detektor ist ein gutes Beispiel für das Kapseln eines Filter Diagramms in ein Hilfsobjekt, um Anwendungen vor Diagramm bezogenen Details zu schützen.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-114">The Media Detector is a good example of encapsulating a filter graph inside a helper object, in order to shield applications from graph-related details.</span></span>

<span data-ttu-id="d3fc2-115">Das Medien Erkennungs Modul funktioniert in zwei Modi.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-115">The Media Detector operates in two modes.</span></span> <span data-ttu-id="d3fc2-116">Wenn Sie es erstmalig erstellen, befindet sich der Medien Detektor im Modus "Informationserfassung".</span><span class="sxs-lookup"><span data-stu-id="d3fc2-116">When you first create it, the Media Detector is in "information gathering" mode.</span></span> <span data-ttu-id="d3fc2-117">Sie können den Namen einer Mediendatei angeben und Informationen zu den einzelnen Streams in der Datei erhalten, z. b. den Formattyp, die Frame Rate oder die Dauer.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-117">You can specify the name of a media file and get information about each of the streams in the file, such as the format type, the frame rate, or the duration.</span></span> <span data-ttu-id="d3fc2-118">Wenn die Datei einen Videostream enthält, können Sie den Medien Detektor in den Modus "Bitmap-Abruf" wechseln und Bitmaps aus der Quelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-118">If the file contains a video stream, you can switch the Media Detector into "bitmap grab" mode and retrieve bitmaps from the source.</span></span> <span data-ttu-id="d3fc2-119">Wenn Sie dies tun, können Sie das Medien Erkennungs Modul jedoch nicht wieder in den ursprünglichen Modus wechseln. Er ist dauerhaft an den Videostream angefügt.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-119">However, once you do so, you cannot switch the Media Detector back to its original mode; it is permanently attached to that video stream.</span></span> <span data-ttu-id="d3fc2-120">Wenn Sie mit einem anderen Stream oder einer anderen Datei arbeiten möchten, müssen Sie eine neue Instanz des Medien Detektors erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-120">To work with another stream or another file, you must create a new instance of the Media Detector.</span></span>

> [!Note]  
> <span data-ttu-id="d3fc2-121">In den Codebeispielen in diesem Tutorial wird die ATL-Klasse **CComPtr** verwendet, die automatisch Verweis Zähler verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-121">The code examples in this tutorial use the ATL **CComPtr** class, which automatically manages reference counts.</span></span> <span data-ttu-id="d3fc2-122">Wenn Sie es vorziehen, unformatierte Schnittstellen Zeiger zu verwenden, denken Sie daran, alle Schnittstellen freizugeben, wenn Sie damit abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-122">If you prefer to use raw interface pointers, remember to release every interface when you are done with it.</span></span> <span data-ttu-id="d3fc2-123">Aus Gründen der Übersichtlichkeit lassen die Codebeispiele einen Großteil der Fehlerüberprüfung aus, die von einer Anwendung durchgeführt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-123">Also, for brevity the code examples omit much of the error checking that an application should perform.</span></span> <span data-ttu-id="d3fc2-124">Überprüfen Sie im Arbeitscode immer **HRESULT** -Werte.</span><span class="sxs-lookup"><span data-stu-id="d3fc2-124">In working code, always check **HRESULT** values.</span></span>

 

<span data-ttu-id="d3fc2-125">Folgende Themen werden in diesem Lernprogramm behandelt:</span><span class="sxs-lookup"><span data-stu-id="d3fc2-125">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="d3fc2-126">Schritt 1: Erstellen des Windows-Frameworks</span><span class="sxs-lookup"><span data-stu-id="d3fc2-126">Step 1: Create the Windows Framework</span></span>](step-1--create-the-windows-framework.md)
-   [<span data-ttu-id="d3fc2-127">Schritt 2: Hinzufügen eines Menübefehls, um einen Poster-Frame zu erfassen</span><span class="sxs-lookup"><span data-stu-id="d3fc2-127">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [<span data-ttu-id="d3fc2-128">Schritt 3: Implementieren der Frame-Grabbing-Funktion</span><span class="sxs-lookup"><span data-stu-id="d3fc2-128">Step 3: Implement the Frame-Grabbing Function</span></span>](step-3--implement-the-frame-grabbing-function.md)
-   [<span data-ttu-id="d3fc2-129">Schritt 4: Zeichnen der Bitmap im Client Bereich</span><span class="sxs-lookup"><span data-stu-id="d3fc2-129">Step 4: Draw the Bitmap on the Client Area</span></span>](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a><span data-ttu-id="d3fc2-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3fc2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3fc2-131">Verwenden von DirectShow-Bearbeitungs Diensten</span><span class="sxs-lookup"><span data-stu-id="d3fc2-131">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



