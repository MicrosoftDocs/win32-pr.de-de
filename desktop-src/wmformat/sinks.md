---
title: Senken
description: Senken
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows Media-Format-SDK, senken
- Windows Media-Format-SDK, Datei senken
- Advanced Systems Format (ASF), senken
- ASF (Advanced Systems Format), senken
- Advanced Systems Format (ASF), Datei senken
- ASF (Advanced Systems Format), Datei senken
- Windows Media-Format-SDK, netzwerksenken
- Windows Media-Format-SDK, pushsenken
- Advanced Systems Format (ASF), netzwerksenken
- ASF (Advanced Systems Format), Netzwerk senken
- Advanced Systems Format (ASF), pushsenken
- ASF (Advanced Systems Format), pushsenken
- senken, Informationen zu
- Datei senken, Informationen zu
- Netzwerk senken
- pushsenken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038580"
---
# <a name="sinks"></a><span data-ttu-id="68d4a-119">Senken</span><span class="sxs-lookup"><span data-stu-id="68d4a-119">Sinks</span></span>

<span data-ttu-id="68d4a-120">Das Writer-Objekt des Windows Media Format SDK übermittelt verarbeitete Inhalte an senken.</span><span class="sxs-lookup"><span data-stu-id="68d4a-120">The writer object of the Windows Media Format SDK delivers processed content to sinks.</span></span> <span data-ttu-id="68d4a-121">Jede Senke ist ein Objekt, das Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="68d4a-121">Each sink is an object that delivers data.</span></span> <span data-ttu-id="68d4a-122">Der Übermittlungs Punkt hängt vom Typ der Senke ab.</span><span class="sxs-lookup"><span data-stu-id="68d4a-122">The point of delivery depends upon the type of sink.</span></span> <span data-ttu-id="68d4a-123">Es gibt drei Arten von senken: Datei senken, Netzwerk senken und pushsenken.</span><span class="sxs-lookup"><span data-stu-id="68d4a-123">There are three types of sinks: file sinks, network sinks, and push sinks.</span></span>

## <a name="file-sinks"></a><span data-ttu-id="68d4a-124">Datei senken</span><span class="sxs-lookup"><span data-stu-id="68d4a-124">File Sinks</span></span>

<span data-ttu-id="68d4a-125">Datei senken schreiben ASF-Inhalte in eine Datei auf einem lokalen Laufwerk oder auf einem Netzwerklaufwerk.</span><span class="sxs-lookup"><span data-stu-id="68d4a-125">File sinks write ASF content to a file on a local or network drive.</span></span> <span data-ttu-id="68d4a-126">Wenn Sie das Writer-Objekt verwenden, um eine Datei zu schreiben, ohne explizit eine File-Senke hinzuzufügen, erstellt der Writer einen für Sie mit dem Namen, den Sie an [**iwmwriter:: setoutputfilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename)übergeben.</span><span class="sxs-lookup"><span data-stu-id="68d4a-126">When you use the writer object to write a file without explicitly adding a file sink, the writer will create one for you using the name you pass to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).</span></span> <span data-ttu-id="68d4a-127">Sie können einem Writer-Objekt mehrere Datei senken zuweisen, um den Inhalt in mehreren Dateien gleichzeitig zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="68d4a-127">You can assign multiple file sinks to a writer object to write the content in several files at once.</span></span>

<span data-ttu-id="68d4a-128">Mithilfe einer Datei Senke können Sie zahlreiche Aspekte der Datei steuern.</span><span class="sxs-lookup"><span data-stu-id="68d4a-128">By using a file sink, you can control many aspects of the file.</span></span> <span data-ttu-id="68d4a-129">Die folgenden Funktionen sind über eine Datei Senke verfügbar.</span><span class="sxs-lookup"><span data-stu-id="68d4a-129">The following features are available through a file sink.</span></span>

-   <span data-ttu-id="68d4a-130">Überwachung von Datei Statistiken.</span><span class="sxs-lookup"><span data-stu-id="68d4a-130">File statistics monitoring.</span></span> <span data-ttu-id="68d4a-131">Sie können die Dateigröße und-Dauer während der Erstellung überwachen.</span><span class="sxs-lookup"><span data-stu-id="68d4a-131">You can monitor the file size and duration as it is being created.</span></span>
-   <span data-ttu-id="68d4a-132">Erstellung von Teil Inhalts Dateien.</span><span class="sxs-lookup"><span data-stu-id="68d4a-132">Partial content file creation.</span></span> <span data-ttu-id="68d4a-133">Datei senken können so konfiguriert werden, dass mit dem Schreiben von Inhalten zu einem bestimmten Zeitpunkt begonnen und das Schreiben zu einem bestimmten Zeitpunkt beendet wird.</span><span class="sxs-lookup"><span data-stu-id="68d4a-133">File sinks can be configured to begin writing content at a specific time and to end writing at a specific time.</span></span> <span data-ttu-id="68d4a-134">Dies ermöglicht es Ihnen, mehrere Dateien zu erstellen, die verschiedene Abschnitte desselben Inhalts in demselben Schreib Durchlauf enthalten.</span><span class="sxs-lookup"><span data-stu-id="68d4a-134">This enables you to create multiple files containing different sections of the same content in the same writing pass.</span></span>

## <a name="network-sinks"></a><span data-ttu-id="68d4a-135">Netzwerk senken</span><span class="sxs-lookup"><span data-stu-id="68d4a-135">Network Sinks</span></span>

<span data-ttu-id="68d4a-136">Netzwerk senken übertragen Inhalte an eine Netzwerkadresse.</span><span class="sxs-lookup"><span data-stu-id="68d4a-136">Network sinks broadcast content to a network address.</span></span> <span data-ttu-id="68d4a-137">Das Lesen von Clients kann eine Verbindung mit der Adresse herstellen, um die Übertragung zu empfangen</span><span class="sxs-lookup"><span data-stu-id="68d4a-137">Reading clients can connect to the address to receive the broadcast.</span></span>

## <a name="push-sinks"></a><span data-ttu-id="68d4a-138">Pushsenken</span><span class="sxs-lookup"><span data-stu-id="68d4a-138">Push Sinks</span></span>

<span data-ttu-id="68d4a-139">Pushsenken übermitteln Inhalte vom Writer an einen Server, auf dem Windows Media Services ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68d4a-139">Push sinks deliver content from the writer to a server running Windows Media Services.</span></span> <span data-ttu-id="68d4a-140">Pushsenken werden in der Regel in Szenarien verwendet, in denen ein Computer Live Inhalte codiert und an einen oder mehrere Server zur breiten Verteilung übergibt.</span><span class="sxs-lookup"><span data-stu-id="68d4a-140">Push sinks are typically used in scenarios where one computer encodes live content and delivers it to one or more servers for wide distribution.</span></span> <span data-ttu-id="68d4a-141">Durch die Verwendung einer Push-Senke können Sie Computern bestimmte Aufgaben zuordnen, um Bandbreite zu sparen und die Leistung der einzelnen Server zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="68d4a-141">Using a push sink enables you to dedicate computers to specific tasks, saving bandwidth and processing power on each server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68d4a-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="68d4a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68d4a-143">**Funktionen zum Schreiben von Dateien**</span><span class="sxs-lookup"><span data-stu-id="68d4a-143">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="68d4a-144">**Arbeiten mit Writer-senken**</span><span class="sxs-lookup"><span data-stu-id="68d4a-144">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




