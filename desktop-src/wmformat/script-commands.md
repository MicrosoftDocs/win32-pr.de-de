---
title: Skriptbefehle
description: Skriptbefehle
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Windows Media-Format-SDK, Skript Befehle
- Advanced Systems Format (ASF), Skript Befehle
- ASF (Advanced Systems Format), Skript Befehle
- Windows Media-Format-SDK, Skript Datenströme
- Advanced Systems Format (ASF), Skript Datenströme
- ASF (Advanced Systems Format), Skript Datenströme
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- Skripts, Befehle
- Skripts, Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039812"
---
# <a name="script-commands"></a><span data-ttu-id="30412-114">Skriptbefehle</span><span class="sxs-lookup"><span data-stu-id="30412-114">Script Commands</span></span>

<span data-ttu-id="30412-115">Die vom Windows Media SDK unterstützten Skript Befehle sind einfache Zeichen folgen Paare für Name und Wert.</span><span class="sxs-lookup"><span data-stu-id="30412-115">The script commands supported by the Windows Media Format SDK are simple name and value string pairs.</span></span> <span data-ttu-id="30412-116">Ein allgemeiner Skript Befehl ist beispielsweise "URL", der von Windows Media Player und anderen Wiedergabe-Anwendungen zum Öffnen von Webseiten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="30412-116">For example, a common script command is "URL", which is used by Windows Media Player and other playing applications to open Web pages.</span></span> <span data-ttu-id="30412-117">Die andere Hälfte des Skript Paars für den Befehl "URL" enthält eine gültige URL (Uniform Resource Serverlocatorpunkt), z `https://www.adatum.com` . b..</span><span class="sxs-lookup"><span data-stu-id="30412-117">The other half of the script pair for "URL" command contains a valid uniform resource locator (URL), such as `https://www.adatum.com`.</span></span> <span data-ttu-id="30412-118">Von den Objekten dieses SDK werden keine Unterstützung für bestimmte Befehle bereitgestellt. die Anwendung muss Logik enthalten, um beliebige Befehle zu verarbeiten, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="30412-118">No support is provided by the objects of this SDK for any specific commands; your application must include logic to handle whatever commands you use.</span></span> <span data-ttu-id="30412-119">Sie können die von Windows Media Player unterstützten Befehle verwenden, um die Kompatibilität mit den meisten Playern aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="30412-119">You can use the commands supported by Windows Media Player to maintain compatibility with most players.</span></span>

<span data-ttu-id="30412-120">Skript Befehle können auf eine von zwei Arten übermittelt werden: in einem Skript Datenstrom oder im Dateiheader.</span><span class="sxs-lookup"><span data-stu-id="30412-120">Script commands can be delivered in one of two ways: in a script stream or in the file header.</span></span>

## <a name="script-streams"></a><span data-ttu-id="30412-121">Skript Datenströme</span><span class="sxs-lookup"><span data-stu-id="30412-121">Script Streams</span></span>

<span data-ttu-id="30412-122">Sie können Skript Befehle in einem eigenen Stream in einer ASF-Datei bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="30412-122">You can deliver script commands in their own stream in an ASF file.</span></span> <span data-ttu-id="30412-123">Jede Stichprobe in einem Skript Datenstrom enthält die zwei Zeichen Folgen des Name-Wert-Paars.</span><span class="sxs-lookup"><span data-stu-id="30412-123">Each sample in a script stream contains the two strings of the name/value pair.</span></span> <span data-ttu-id="30412-124">Der Vorteil der Verwendung eines Skript Datenstroms besteht darin, dass die Befehle zur richtigen Präsentationszeit zugestellt werden.</span><span class="sxs-lookup"><span data-stu-id="30412-124">The advantage of using a script stream is that the commands will be delivered at the correct presentation time.</span></span>

## <a name="script-commands-in-the-file-header"></a><span data-ttu-id="30412-125">Skript Befehle im Datei Header</span><span class="sxs-lookup"><span data-stu-id="30412-125">Script Commands in the File Header</span></span>

<span data-ttu-id="30412-126">Skript Befehle können zum Abrufen zum Zeitpunkt der Wiedergabe in den Dateiheader eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="30412-126">Script commands can be included in the file header for retrieval at the time of playback.</span></span> <span data-ttu-id="30412-127">Die Spiel Ende Anwendung ist dafür verantwortlich, die Skript Befehle zum richtigen Zeitpunkt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="30412-127">The playing application is responsible for executing the script commands at the proper time.</span></span> <span data-ttu-id="30412-128">Der Vorteil der Verwendung von Skript Befehlen im Dateiheader besteht darin, dass alle Skript Befehle verfügbar sind, bevor Sie mit dem empfangen von Beispielen beginnen.</span><span class="sxs-lookup"><span data-stu-id="30412-128">The advantage of using script commands in the file header is that all of the script commands are available before beginning to receive samples.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30412-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30412-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30412-130">**Funktionen der ASF-Datei**</span><span class="sxs-lookup"><span data-stu-id="30412-130">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="30412-131">**Verwenden von Skript Befehlen**</span><span class="sxs-lookup"><span data-stu-id="30412-131">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




