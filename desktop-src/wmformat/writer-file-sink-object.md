---
title: Writer-Dateisenke (Objekt)
description: Writer-Dateisenke (Objekt)
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Windows Media-Format-SDK, Writer File Sink Objects
- Advanced Systems Format (ASF), Writer File Sink Objects
- ASF (Advanced Systems Format), Writer File Sink Objects
- Objekte, Senke-Objekte von Writer-Dateien
- Writer-Datei-Sink-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038688"
---
# <a name="writer-file-sink-object"></a><span data-ttu-id="16bc7-108">Writer-Dateisenke (Objekt)</span><span class="sxs-lookup"><span data-stu-id="16bc7-108">Writer File Sink Object</span></span>

<span data-ttu-id="16bc7-109">Das writerdatei-Sink-Objekt wird beim Schreiben der Windows Media-Ausgabe in eine Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="16bc7-109">The writer file sink object is used when writing Windows Media output to a file.</span></span>

<span data-ttu-id="16bc7-110">Das Writer File Sink-Objekt wird von der [**wmkreateschreiterfilesink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)-Funktion erstellt, die einen Zeiger auf eine **iwmschreiterfilesink** -Schnittstelle festlegt.</span><span class="sxs-lookup"><span data-stu-id="16bc7-110">The writer file sink object is created by the function [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), which sets a pointer to an **IWMWriterFileSink** interface.</span></span> <span data-ttu-id="16bc7-111">Die anderen Schnittstellen des Writer-Datei-Senkenobjekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="16bc7-111">The other interfaces of the writer file sink object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="16bc7-112">Die folgenden Schnittstellen werden vom Writer-Datei-senksobjekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="16bc7-112">The following interfaces are supported by the writer file sink object.</span></span>



| <span data-ttu-id="16bc7-113">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="16bc7-113">Interface</span></span>                                          | <span data-ttu-id="16bc7-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16bc7-114">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16bc7-115">**Iwmregistercallback**</span><span class="sxs-lookup"><span data-stu-id="16bc7-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="16bc7-116">Ermöglicht es der Anwendung, Statusmeldungen aus dem-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="16bc7-116">Enables the application to get status messages from the object.</span></span>                                                                 |
| [<span data-ttu-id="16bc7-117">**Iwmschreibfilesink**</span><span class="sxs-lookup"><span data-stu-id="16bc7-117">**IWMWriterFileSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | <span data-ttu-id="16bc7-118">Öffnet eine Datei, in die das Writer-Objektdaten schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="16bc7-118">Opens a file to which the writer object can write data.</span></span>                                                                         |
| [<span data-ttu-id="16bc7-119">**IWMWriterFileSink2**</span><span class="sxs-lookup"><span data-stu-id="16bc7-119">**IWMWriterFileSink2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | <span data-ttu-id="16bc7-120">Ermöglicht die Erweiterte Verwaltung eines dateisink-Objekts.</span><span class="sxs-lookup"><span data-stu-id="16bc7-120">Provides extended management of a file sink object.</span></span> <span data-ttu-id="16bc7-121">Erbt alle Methoden von **iwmschreiterfilesink**.</span><span class="sxs-lookup"><span data-stu-id="16bc7-121">Inherits all of the methods of **IWMWriterFileSink**.</span></span>                       |
| [<span data-ttu-id="16bc7-122">**IWMWriterFileSink3**</span><span class="sxs-lookup"><span data-stu-id="16bc7-122">**IWMWriterFileSink3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | <span data-ttu-id="16bc7-123">Bietet zusätzliche Optionen zum Schreiben von Dateien.</span><span class="sxs-lookup"><span data-stu-id="16bc7-123">Provides additional options for writing files.</span></span> <span data-ttu-id="16bc7-124">Erbt alle Methoden von **iwmschreiterfilesink** und **IWMWriterFileSink2**.</span><span class="sxs-lookup"><span data-stu-id="16bc7-124">Inherits all of the methods of **IWMWriterFileSink** and **IWMWriterFileSink2**.</span></span> |
| [<span data-ttu-id="16bc7-125">**Iwmschreibsink**</span><span class="sxs-lookup"><span data-stu-id="16bc7-125">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="16bc7-126">Weist Arbeitsspeicher zu, bestimmt, ob die Senke in Echtzeit ausgeführt wird, und verarbeitet mehrere Rückruf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="16bc7-126">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                |



 

<span data-ttu-id="16bc7-127">Die folgende Rückruf Schnittstelle sollte von der Anwendung implementiert werden, um den Fortschritt eines Writer-Datei-Sink-Objekts zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="16bc7-127">The following callback interface should be implemented by the application to track the progress of a writer file sink object.</span></span>



| <span data-ttu-id="16bc7-128">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="16bc7-128">Interface</span></span>                                      | <span data-ttu-id="16bc7-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16bc7-129">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="16bc7-130">**Iwmstatus Callback**</span><span class="sxs-lookup"><span data-stu-id="16bc7-130">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="16bc7-131">Erforderlich, wenn Statusinformationen an die Host Anwendung übermittelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="16bc7-131">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="16bc7-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16bc7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16bc7-133">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="16bc7-133">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="16bc7-134">**Arbeiten mit Writer-senken**</span><span class="sxs-lookup"><span data-stu-id="16bc7-134">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




