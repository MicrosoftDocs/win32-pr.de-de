---
title: Arbeiten mit Writer-senken
description: Arbeiten mit Writer-senken
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- Advanced Systems Format (ASF), Writer-senken
- ASF (Advanced Systems Format), Writer-senken
- Advanced Systems Format (ASF), senken
- ASF (Advanced Systems Format), senken
- senken, Writer-senken
- Writer-senken, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b690d9e1ab25d15f7c1e8612bf20e32f87c81
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723368"
---
# <a name="working-with-writer-sinks"></a><span data-ttu-id="7b2c4-109">Arbeiten mit Writer-senken</span><span class="sxs-lookup"><span data-stu-id="7b2c4-109">Working with Writer Sinks</span></span>

<span data-ttu-id="7b2c4-110">Das Writer-Objekt des SDK für den Windows Media-Format verarbeitet Eingabemedien Daten in einen Bit-Stream.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-110">The writer object of the Windows Media Format SDK processes input media data into a bit stream.</span></span> <span data-ttu-id="7b2c4-111">Allerdings stellt das Writer-Objekt den Bitstream nicht an das endgültige Ziel (entweder an eine Datei oder an einen Netzwerk Speicherort) bereit.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-111">However, the writer object does not deliver the bit stream to its final destination (either to a file or a network location).</span></span> <span data-ttu-id="7b2c4-112">Wenn Sie den ASF-Inhalt in ein verwendbares Format schreiben möchten, müssen Sie Writer-senken verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-112">To write the ASF content to a usable format, you must use writer sinks.</span></span>

<span data-ttu-id="7b2c4-113">Das Writer-Objekt unterstützt drei Arten von senken: Datei senken, Netzwerk senken und pushsenken.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-113">The writer object supports three types of sinks: file sinks, network sinks, and push sinks.</span></span> <span data-ttu-id="7b2c4-114">Eine File-Senke schreibt ASF-Inhalte in eine ASF-Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-114">A file sink writes ASF content to an ASF file on disk.</span></span> <span data-ttu-id="7b2c4-115">Eine Netzwerk Senke überträgt ASF-Inhalte über eine Netzwerkadresse.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-115">A network sink broadcasts ASF content from a network address.</span></span> <span data-ttu-id="7b2c4-116">Eine Push-Senke liefert Daten an einen Server, auf dem Windows Media Services ausgeführt wird, sodass der Server den Inhalt für die gewünschte Zielgruppe verfügbar machen kann.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-116">A push sink delivers data to a server running Windows Media Services so that the server can make the content available to its intended audience.</span></span> <span data-ttu-id="7b2c4-117">Sie können auch eigene senken zur Bereitstellung von ASF-Daten auf die gleiche Weise erstellen, die für Ihre Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-117">You can also create your own sinks to deliver ASF data in whatever way is required by your application.</span></span> <span data-ttu-id="7b2c4-118">Weitere Informationen zu Netzwerk senken und pushsenken finden Sie unter [Senden von ASF-Daten über ein Netzwerk](sending-asf-data-over-a-network.md).</span><span class="sxs-lookup"><span data-stu-id="7b2c4-118">For information about network sinks and push sinks, see [Sending ASF Data Over a Network](sending-asf-data-over-a-network.md).</span></span> <span data-ttu-id="7b2c4-119">Im restlichen Teil dieses Abschnitts werden Writer-senken erläutert.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-119">The remainder of this section discusses writer sinks.</span></span>

<span data-ttu-id="7b2c4-120">Sie können einen oder mehrere senken für jede Instanz des verwendeten Writers konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-120">You can configure one or more sinks for each instance of the writer you use.</span></span> <span data-ttu-id="7b2c4-121">Jede Senke verarbeitet nur ein einzelnes Ziel.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-121">Each sink handles only a single destination.</span></span> <span data-ttu-id="7b2c4-122">Wenn Sie z. b. drei Dateien gleichzeitig schreiben möchten, müssen Sie jeweils eine separate Datei-Senke erstellen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-122">For example, if you want to write three files at once, you must create and configure a separate file sink for each.</span></span>

<span data-ttu-id="7b2c4-123">In den folgenden Abschnitten wird die Verwendung von Writer-senken beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-123">The following sections describe the use of writer sinks.</span></span>



| <span data-ttu-id="7b2c4-124">`Section`</span><span class="sxs-lookup"><span data-stu-id="7b2c4-124">Section</span></span>                                                                      | <span data-ttu-id="7b2c4-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b2c4-125">Description</span></span>                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="7b2c4-126">Hinzufügen von senken zum Writer</span><span class="sxs-lookup"><span data-stu-id="7b2c4-126">Adding Sinks to the Writer</span></span>](adding-sinks-to-the-writer.md)                 | <span data-ttu-id="7b2c4-127">Hier wird beschrieben, wie dem Writer senken hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-127">Describes how to add sinks to the writer.</span></span>                                        |
| [<span data-ttu-id="7b2c4-128">Auflisten von senken</span><span class="sxs-lookup"><span data-stu-id="7b2c4-128">Enumerating Sinks</span></span>](enumerating-sinks.md)                                   | <span data-ttu-id="7b2c4-129">Beschreibt, wie die senken aufgelistet werden, die dem Writer hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-129">Describes how to enumerate the sinks that have been added to the writer.</span></span>         |
| [<span data-ttu-id="7b2c4-130">Erhalten von Fehlermeldungen aus einer Senke</span><span class="sxs-lookup"><span data-stu-id="7b2c4-130">Getting Error Messages from a Sink</span></span>](getting-error-messages-from-a-sink.md) | <span data-ttu-id="7b2c4-131">Beschreibt das Konfigurieren von senken, um Statusmeldungen an Ihre Anwendung zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-131">Describes how to configure sinks to deliver status messages to your application.</span></span> |
| [<span data-ttu-id="7b2c4-132">Verwenden von Dateisenken</span><span class="sxs-lookup"><span data-stu-id="7b2c4-132">Using File Sinks</span></span>](using-file-sinks.md)                                     | <span data-ttu-id="7b2c4-133">Beschreibt, wie eine Writer-Datei-Senke zum Erstellen einer ASF-Datei auf dem Datenträger verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-133">Describes how to use a writer file sink to create an ASF file on disk.</span></span>           |
| [<span data-ttu-id="7b2c4-134">Verwenden von benutzerdefinierten senken</span><span class="sxs-lookup"><span data-stu-id="7b2c4-134">Using Custom Sinks</span></span>](using-custom-sinks.md)                                 | <span data-ttu-id="7b2c4-135">Hier wird beschrieben, wie Sie Ihre eigenen benutzerdefinierten senken zum Übermitteln von ASF-Daten erstellen und verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b2c4-135">Describes how to create and use your own custom sinks to deliver ASF data.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="7b2c4-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b2c4-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b2c4-137">**Iwmschreiteradvanced-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7b2c4-137">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="7b2c4-138">**Iwmschreitersink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7b2c4-138">**IWMWriterSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[<span data-ttu-id="7b2c4-139">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="7b2c4-139">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




