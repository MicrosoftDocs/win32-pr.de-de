---
title: Writer-Push-Sink-Objekt
description: Writer-Push-Sink-Objekt
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- Windows Media-Format-SDK, Writer-Push-Sink-Objekte
- Advanced Systems Format (ASF), Writer Push Sink-Objekte
- ASF (Advanced Systems Format), Writer-Push-Sink-Objekte
- Objekte, Writer-Push-Sink-Objekte
- Writer-Push-Sink-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19ea9855219dcb4572ef187ad93e03696b88492
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948425"
---
# <a name="writer-push-sink-object"></a><span data-ttu-id="7f03f-108">Writer-Push-Sink-Objekt</span><span class="sxs-lookup"><span data-stu-id="7f03f-108">Writer Push Sink Object</span></span>

<span data-ttu-id="7f03f-109">Das Writer Push Sink-Objekt verteilt digitale Medien an Publishing Points.</span><span class="sxs-lookup"><span data-stu-id="7f03f-109">The writer push sink object distributes digital media to publishing points.</span></span> <span data-ttu-id="7f03f-110">Beispielsweise kann ein Live Konzert von einem einzelnen Server codiert und dann an verschiedene andere Server übermittelt oder per *Pushvorgang* übertragen werden, die den Inhalt tatsächlich an Benutzer streamen.</span><span class="sxs-lookup"><span data-stu-id="7f03f-110">For example, a live concert can be encoded by a single server and then delivered, or *pushed*, to several other servers that will actually stream the content to users.</span></span>

<span data-ttu-id="7f03f-111">Ein Writer-Push-Sink-Objekt wird von der [**wmkreateschreiterpushsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)-Funktion erstellt, mit der ein Zeiger auf eine **iwmschreiterpushsink** -Schnittstelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7f03f-111">A writer push sink object is created by the function [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), which sets a pointer to an **IWMWriterPushSink** interface.</span></span> <span data-ttu-id="7f03f-112">Die anderen vom-Objekt unterstützten Schnittstellen, die in der folgenden Tabelle aufgeführt sind, können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7f03f-112">The other interfaces supported by the object, listed in the following table, can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="7f03f-113">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7f03f-113">Interface</span></span>                                          | <span data-ttu-id="7f03f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f03f-114">Description</span></span>                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f03f-115">**Iwmregistercallback**</span><span class="sxs-lookup"><span data-stu-id="7f03f-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="7f03f-116">Ermöglicht es der Anwendung, Statusmeldungen aus dem-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7f03f-116">Enables the application to get status messages from the object.</span></span>                                                  |
| [<span data-ttu-id="7f03f-117">**Iwmschreibpushsink**</span><span class="sxs-lookup"><span data-stu-id="7f03f-117">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | <span data-ttu-id="7f03f-118">Verwaltet eine pushverteilungssitzung.</span><span class="sxs-lookup"><span data-stu-id="7f03f-118">Manages a push distribution session.</span></span>                                                                             |
| [<span data-ttu-id="7f03f-119">**Iwmschreibsink**</span><span class="sxs-lookup"><span data-stu-id="7f03f-119">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="7f03f-120">Weist Arbeitsspeicher zu, bestimmt, ob die Senke in Echtzeit ausgeführt wird, und macht mehrere Rückruf Funktionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f03f-120">Allocates memory, determines whether the sink is operating in real time, and exposes several callback functions.</span></span> |



 

<span data-ttu-id="7f03f-121">Die folgende Rückruf Schnittstelle kann von der Anwendung implementiert werden, um den Fortschritt eines Writer-senkenerjektobjekts zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="7f03f-121">The following callback interface can be implemented by the application to track the progress of a writer push sink object.</span></span>



| <span data-ttu-id="7f03f-122">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7f03f-122">Interface</span></span>                                      | <span data-ttu-id="7f03f-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f03f-123">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="7f03f-124">**Iwmstatus Callback**</span><span class="sxs-lookup"><span data-stu-id="7f03f-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="7f03f-125">Erforderlich, wenn Statusinformationen an die Host Anwendung übermittelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7f03f-125">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7f03f-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f03f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f03f-127">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="7f03f-127">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="7f03f-128">**Senden von ASF-Daten an einen Publishing Point**</span><span class="sxs-lookup"><span data-stu-id="7f03f-128">**Sending ASF Data to a Publishing Point**</span></span>](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[<span data-ttu-id="7f03f-129">**Arbeiten mit Writer-senken**</span><span class="sxs-lookup"><span data-stu-id="7f03f-129">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




