---
title: Programmier Handbuch zum Windows Media-Format-SDK
description: Programmier Handbuch zum Windows Media-Format-SDK
ms.assetid: 9b382c88-e4a9-4aed-a250-250fabface44
keywords:
- Windows Media-Format-SDK, Programmier Handbuch
- Windows Media-Format-SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), Programmier Handbuch
- ASF (Advanced Systems Format), Programmier Handbuch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4ea4f6819a31693d7c9d149717324ef6dcc65a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341346"
---
# <a name="windows-media-format-sdk-programming-guide"></a><span data-ttu-id="55566-107">Programmier Handbuch zum Windows Media-Format-SDK</span><span class="sxs-lookup"><span data-stu-id="55566-107">Windows Media Format SDK Programming Guide</span></span>

<span data-ttu-id="55566-108">Das Programmier Handbuch soll Sie dabei unterstützen, zu erfahren, wie Sie das Microsoft Windows Media-Format Software Development Kit (SDK) zum Erstellen von Anwendungen verwenden, die mit Dateien im Advanced Systems-Format (ASF) arbeiten.</span><span class="sxs-lookup"><span data-stu-id="55566-108">The Programming Guide is intended to help you learn how to use the Microsoft Windows Media Format Software Development Kit (SDK) to build applications that work with files using the Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="55566-109">Mit dem Windows Media-Format-SDK können Sie Anwendungen erstellen, die digitale Medienströme in schreiben und Datenströme aus den ASF-Dateien lesen.</span><span class="sxs-lookup"><span data-stu-id="55566-109">You can use the Windows Media Format SDK to create applications that write digital media streams to and read streams from ASF files.</span></span> <span data-ttu-id="55566-110">Dieses SDK unterstützt auch die Bearbeitung von Metadaten in ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="55566-110">This SDK also supports the editing of metadata in ASF files.</span></span> <span data-ttu-id="55566-111">Außerdem kann dieses SDK verwendet werden, um Metadaten in MP3-Dateien zu lesen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="55566-111">In addition, this SDK can be used to read and manipulate metadata in MP3 files.</span></span>

<span data-ttu-id="55566-112">In den folgenden Abschnitten werden die erforderlichen Schritte zum Schreiben, lesen und Bearbeiten von ASF-Dateien mit diesem SDK ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="55566-112">The following sections explain in detail the steps required to write, read, and edit ASF files by using this SDK.</span></span>



| <span data-ttu-id="55566-113">`Section`</span><span class="sxs-lookup"><span data-stu-id="55566-113">Section</span></span>                                                                            | <span data-ttu-id="55566-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55566-114">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55566-115">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="55566-115">Getting Started</span></span>](getting-started.md)                                             | <span data-ttu-id="55566-116">Bietet allgemeine Informationen zum Vorbereiten der Verwendung dieses SDK.</span><span class="sxs-lookup"><span data-stu-id="55566-116">Provides general information about getting ready to use this SDK.</span></span>                                                 |
| [<span data-ttu-id="55566-117">Verwenden der Rückruf Methoden</span><span class="sxs-lookup"><span data-stu-id="55566-117">Using the Callback Methods</span></span>](using-the-callback-methods.md)                       | <span data-ttu-id="55566-118">Beschreibt die Rückruf Methoden, die in vielen verschiedenen Tasks verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55566-118">Describes the callback methods used in many different tasks.</span></span>                                                      |
| [<span data-ttu-id="55566-119">Arbeiten mit Profilen</span><span class="sxs-lookup"><span data-stu-id="55566-119">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="55566-120">Beschreibt die Verwendung, Bearbeitung und Erstellung von Profilen.</span><span class="sxs-lookup"><span data-stu-id="55566-120">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="55566-121">Schreiben von ASF-Dateien</span><span class="sxs-lookup"><span data-stu-id="55566-121">Writing ASF Files</span></span>](writing-asf-files.md)                                         | <span data-ttu-id="55566-122">Beschreibt, wie das Writer-Objekt zum Erstellen von ASF-Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="55566-122">Describes how to use the writer object to create ASF files.</span></span>                                                       |
| [<span data-ttu-id="55566-123">Lesen von ASF-Dateien</span><span class="sxs-lookup"><span data-stu-id="55566-123">Reading ASF Files</span></span>](reading-asf-files.md)                                         | <span data-ttu-id="55566-124">Hier wird beschrieben, wie Sie Inhalte von ASF-Dateien empfangen.</span><span class="sxs-lookup"><span data-stu-id="55566-124">Describes how to receive content from ASF files.</span></span>                                                                  |
| [<span data-ttu-id="55566-125">Arbeiten mit Metadaten</span><span class="sxs-lookup"><span data-stu-id="55566-125">Working with Metadata</span></span>](working-with-metadata.md)                                 | <span data-ttu-id="55566-126">Beschreibt, wie der Inhalt des Header Abschnitts einer ASF-Datei verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="55566-126">Describes how to manage the contents of the header section of an ASF file.</span></span>                                        |
| [<span data-ttu-id="55566-127">Arbeiten mit Indizes</span><span class="sxs-lookup"><span data-stu-id="55566-127">Working with Indexes</span></span>](working-with-indexes.md)                                   | <span data-ttu-id="55566-128">Beschreibt das Arbeiten mit Indizes.</span><span class="sxs-lookup"><span data-stu-id="55566-128">Describes how to work with indexes.</span></span>                                                                               |
| [<span data-ttu-id="55566-129">Arbeiten mit Profilen</span><span class="sxs-lookup"><span data-stu-id="55566-129">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="55566-130">Beschreibt die Verwendung, Bearbeitung und Erstellung von Profilen.</span><span class="sxs-lookup"><span data-stu-id="55566-130">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="55566-131">Verwenden von Skript Befehlen</span><span class="sxs-lookup"><span data-stu-id="55566-131">Using Script Commands</span></span>](using-script-commands.md)                                 | <span data-ttu-id="55566-132">Beschreibt, wie Skript Befehle in ihren ASF-Dateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55566-132">Describes how to use script commands in your ASF files.</span></span>                                                           |
| [<span data-ttu-id="55566-133">Kopieren von Daten aus einer Datei in eine andere</span><span class="sxs-lookup"><span data-stu-id="55566-133">Copying Data from One File to Another</span></span>](copying-data-from-one-file-to-another.md) | <span data-ttu-id="55566-134">Beschreibt das Kopieren von Daten aus einer ASF-Datei in eine andere, ohne Decodierung und Codierung.</span><span class="sxs-lookup"><span data-stu-id="55566-134">Describes how to copy data from one ASF file to another, with without decoding and encoding.</span></span>                      |
| [<span data-ttu-id="55566-135">Aktivieren DRM-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="55566-135">Enabling DRM Support</span></span>](enabling-drm-support.md)                                   | <span data-ttu-id="55566-136">Beschreibt, wie die Unterstützung für die Wiedergabe von DRM-geschützten ASF-Dateien aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="55566-136">Describes how to enable support for playback of DRM-protected ASF files.</span></span>                                          |
| [<span data-ttu-id="55566-137">Implementieren von Netzwerkfunktionen</span><span class="sxs-lookup"><span data-stu-id="55566-137">Implementing Network Functionality</span></span>](implementing-network-functionality.md)       | <span data-ttu-id="55566-138">Beschreibt die Verwendung dieses SDK zum Ausführen der Netzwerk Vorgänge, die für erfolgreiche Streamingmedien erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="55566-138">Describes the use of this SDK to perform the network operations that are essential to successful streaming media.</span></span> |
| [<span data-ttu-id="55566-139">Erweiterte Themen</span><span class="sxs-lookup"><span data-stu-id="55566-139">Advanced Topics</span></span>](advanced-topics.md)                                             | <span data-ttu-id="55566-140">Beschreibt, wie einige der erweiterten Features dieses SDK in Ihren Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55566-140">Describes how to use some of the advanced features of this SDK in your applications.</span></span>                              |
| [<span data-ttu-id="55566-141">DirectShow-und Windows-Medien</span><span class="sxs-lookup"><span data-stu-id="55566-141">DirectShow and Windows Media</span></span>](directshow-and-windows-media.md)                   | <span data-ttu-id="55566-142">Beschreibt, wie Sie Microsoft DirectShow zum Erstellen und Lesen von ASF-Dateien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="55566-142">Describes how you can use Microsoft DirectShow to create and read ASF files.</span></span>                                      |
| [<span data-ttu-id="55566-143">Überlegungen zu Projekten</span><span class="sxs-lookup"><span data-stu-id="55566-143">Project Considerations</span></span>](project-considerations.md)                               | <span data-ttu-id="55566-144">Bietet ausführliche Informationen zum Abschließen und Verteilen Ihrer Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="55566-144">Provides details about finishing and distributing your applications.</span></span>                                              |



 

## <a name="related-topics"></a><span data-ttu-id="55566-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55566-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55566-146">**Informationen zum Windows Media-Format-SDK**</span><span class="sxs-lookup"><span data-stu-id="55566-146">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="55566-147">**SDK für Windows Media-Format 11**</span><span class="sxs-lookup"><span data-stu-id="55566-147">**Windows Media Format 11 SDK**</span></span>](windows-media-format-11-sdk.md)
</dt> </dl>

 

 




