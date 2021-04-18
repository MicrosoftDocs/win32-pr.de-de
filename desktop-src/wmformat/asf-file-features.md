---
title: Funktionen der ASF-Datei
description: Funktionen der ASF-Datei
ms.assetid: 6e180f27-69ef-4fe0-b06c-b2ead7be8a05
keywords:
- Windows Media-Format-SDK, Features der ASF-Datei
- Windows Media-Format-SDK, Features
- Advanced Systems Format (ASF), Datei Features
- ASF (Advanced Systems Format), Datei Features
- Advanced Systems Format (ASF), Features
- ASF (Advanced Systems Format), Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871d2986ad85716fe198b9a16e1a3772d1cca5f8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106337476"
---
# <a name="asf-file-features"></a><span data-ttu-id="010ad-109">Funktionen der ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="010ad-109">ASF File Features</span></span>

<span data-ttu-id="010ad-110">Der Hauptzweck des SDK für das Windows Media-Format ist die Unterstützung für das Kapseln digitaler Mediendaten in ASF-Dateien (Advanced Systems Format) und das Bereitstellen der Medien an eine Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="010ad-110">The primary purpose of the Windows Media Format SDK is to provide support for encapsulating digital media data in Advanced Systems Format (ASF) files and delivering the media to a client application.</span></span> <span data-ttu-id="010ad-111">Übermittlungs Szenarien können von der Anwendung bis zur Anwendung abweichen, aber alle verwenden die Struktur der ASF-Datei zwischen Erstellung und Übermittlung.</span><span class="sxs-lookup"><span data-stu-id="010ad-111">Delivery scenarios can vary widely from application to application, but all use the ASF file structure between authoring and delivery.</span></span> <span data-ttu-id="010ad-112">ASF-Dateien entsprechen einer klar definierten, aber sehr flexiblen Struktur.</span><span class="sxs-lookup"><span data-stu-id="010ad-112">ASF files conform to a well defined but very flexible structure.</span></span> <span data-ttu-id="010ad-113">Weitere Informationen zur Struktur der ASF-Datei finden Sie unter [Übersicht über das ASF-Format](overview-of-the-asf-format.md).</span><span class="sxs-lookup"><span data-stu-id="010ad-113">For more information about the ASF file structure, see [Overview of the ASF Format](overview-of-the-asf-format.md).</span></span>

<span data-ttu-id="010ad-114">Ausführliche Informationen zu den Daten in einer ASF-Datei werden in der ASF-Spezifikation bereitgestellt, die Sie von der [Microsoft-Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)herunterladen können.</span><span class="sxs-lookup"><span data-stu-id="010ad-114">Detailed information about the data in an ASF file is provided in the ASF specification, which you can download from the [Microsoft Web site](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span></span>

<span data-ttu-id="010ad-115">Das Windows Media-Format SDK bietet Unterstützung für die Features der ASF-Spezifikation größtenteils über das Profil, das zum Erstellen einer Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="010ad-115">The Windows Media Format SDK provides support for the features of the ASF specification mostly through the profile that is used to create a file.</span></span> <span data-ttu-id="010ad-116">Weitere Informationen zu Profilen finden Sie unter [profile](profiles.md).</span><span class="sxs-lookup"><span data-stu-id="010ad-116">For more information about profiles, see [Profiles](profiles.md).</span></span>

<span data-ttu-id="010ad-117">Die folgenden Funktionen werden in diesem Abschnitt erläutert.</span><span class="sxs-lookup"><span data-stu-id="010ad-117">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="010ad-118">Audiodaten und Videostreams</span><span class="sxs-lookup"><span data-stu-id="010ad-118">Audio and Video Streams</span></span>](audio-and-video-streams.md)
-   [<span data-ttu-id="010ad-119">Bildstreams</span><span class="sxs-lookup"><span data-stu-id="010ad-119">Image Streams</span></span>](image-streams.md)
-   [<span data-ttu-id="010ad-120">Beliebige Streams</span><span class="sxs-lookup"><span data-stu-id="010ad-120">Arbitrary Streams</span></span>](arbitrary-streams.md)
-   [<span data-ttu-id="010ad-121">Skriptbefehle</span><span class="sxs-lookup"><span data-stu-id="010ad-121">Script Commands</span></span>](script-commands.md)
-   [<span data-ttu-id="010ad-122">Dateneinheiten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="010ad-122">Data Unit Extensions</span></span>](data-unit-extensions.md)
-   [<span data-ttu-id="010ad-123">SMPTE-Zeit Code Unterstützung</span><span class="sxs-lookup"><span data-stu-id="010ad-123">SMPTE Time Code Support</span></span>](smpte-time-code-support.md)
-   [<span data-ttu-id="010ad-124">Gegenseitiger Ausschluss</span><span class="sxs-lookup"><span data-stu-id="010ad-124">Mutual Exclusion</span></span>](mutual-exclusion.md)
-   [<span data-ttu-id="010ad-125">Streampriorisierung</span><span class="sxs-lookup"><span data-stu-id="010ad-125">Stream Prioritization</span></span>](stream-prioritization.md)
-   [<span data-ttu-id="010ad-126">Bandbreiten Freigabe</span><span class="sxs-lookup"><span data-stu-id="010ad-126">Bandwidth Sharing</span></span>](bandwidth-sharing.md)
-   [<span data-ttu-id="010ad-127">Indizes</span><span class="sxs-lookup"><span data-stu-id="010ad-127">Indexes</span></span>](indexes.md)
-   [<span data-ttu-id="010ad-128">Marker</span><span class="sxs-lookup"><span data-stu-id="010ad-128">Markers</span></span>](markers.md)
-   [<span data-ttu-id="010ad-129">Reader-Antwort auf ASF-Features</span><span class="sxs-lookup"><span data-stu-id="010ad-129">Reader Response to ASF Features</span></span>](reader-response-to-asf-features.md)

## <a name="related-topics"></a><span data-ttu-id="010ad-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="010ad-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="010ad-131">**Features**</span><span class="sxs-lookup"><span data-stu-id="010ad-131">**Features**</span></span>](features.md)
</dt> </dl>

 

 




