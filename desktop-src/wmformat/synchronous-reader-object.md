---
title: Synchrones Reader-Objekt
description: Synchrones Reader-Objekt
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows Media-Format-SDK, synchrone Reader-Objekte
- Advanced Systems Format (ASF), synchrone Reader-Objekte
- ASF (Advanced Systems Format), synchrone Reader-Objekte
- Objekte, synchrone Reader-Objekte
- synchrone Reader, Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106337212"
---
# <a name="synchronous-reader-object"></a><span data-ttu-id="29279-108">Synchrones Reader-Objekt</span><span class="sxs-lookup"><span data-stu-id="29279-108">Synchronous Reader Object</span></span>

<span data-ttu-id="29279-109">Das synchrone Reader-Objekt wird zum Lesen digitaler Mediendateien mithilfe von synchronen Aufrufen verwendet.</span><span class="sxs-lookup"><span data-stu-id="29279-109">The synchronous reader object is used to read digital media files by using synchronous calls.</span></span>

<span data-ttu-id="29279-110">Das synchrone Reader-Objekt wird von der [**wmkreatesynkreader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)-Funktion erstellt, die einen Zeiger auf eine **iwmsynkreader** -Schnittstelle festlegt.</span><span class="sxs-lookup"><span data-stu-id="29279-110">The synchronous reader object is created by the function [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), which sets a pointer to an **IWMSyncReader** interface.</span></span> <span data-ttu-id="29279-111">Die anderen von der synchronen Reader-Schnittstelle unterstützten Schnittstellen können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="29279-111">The other interfaces supported by the synchronous reader interface can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="29279-112">Die folgenden Schnittstellen werden vom synchronen Reader-Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29279-112">The following interfaces are supported by the synchronous reader object.</span></span>



| <span data-ttu-id="29279-113">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="29279-113">Interface</span></span>                                | <span data-ttu-id="29279-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29279-114">Description</span></span>                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29279-115">**Iwmheaderinfo**</span><span class="sxs-lookup"><span data-stu-id="29279-115">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | <span data-ttu-id="29279-116">Legt Header Informationen, wie z. b. Metadaten, [*Marker*](wmformat-glossary.md)usw., fest und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="29279-116">Sets and retrieves header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                            |
| [<span data-ttu-id="29279-117">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="29279-117">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | <span data-ttu-id="29279-118">Listet die verfügbaren Codec-Informationen auf.</span><span class="sxs-lookup"><span data-stu-id="29279-118">Enumerates the available codec information.</span></span> <span data-ttu-id="29279-119">Erbt alle Methoden von **iwmheaderinfo**.</span><span class="sxs-lookup"><span data-stu-id="29279-119">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                      |
| [<span data-ttu-id="29279-120">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="29279-120">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | <span data-ttu-id="29279-121">Unterstützt umfangreiche Attribut Größen, doppelte Attributnamen und Unterstützung mehrerer Sprachen.</span><span class="sxs-lookup"><span data-stu-id="29279-121">Supports large attribute sizes, duplicate attribute names, and multiple language support.</span></span> <span data-ttu-id="29279-122">Erbt alle Methoden von **iwmheaderinfo** und **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="29279-122">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span> |
| [<span data-ttu-id="29279-123">**Iwmprofile**</span><span class="sxs-lookup"><span data-stu-id="29279-123">**IWMProfile**</span></span>](iwmprofile.md)         | <span data-ttu-id="29279-124">Ermöglicht den Zugriff auf die Profilinformationen der in den Reader geladenen Windows-Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="29279-124">Provides access to the profile information of the Windows Media file loaded into the reader.</span></span>                                                                       |
| [<span data-ttu-id="29279-125">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="29279-125">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | <span data-ttu-id="29279-126">Ruft die Globally Unique Identifier (GUID) ab, die dem Profil zugeordnet ist, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="29279-126">Retrieves the globally unique identifier (GUID), if any, associated with the profile.</span></span> <span data-ttu-id="29279-127">Erbt alle Methoden von **iwmprofile**.</span><span class="sxs-lookup"><span data-stu-id="29279-127">Inherits all of the methods of **IWMProfile**.</span></span>                               |
| [<span data-ttu-id="29279-128">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="29279-128">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | <span data-ttu-id="29279-129">Unterstützt die Bandbreiten Freigabe und Datenstrom Priorisierungs Informationen im Profil.</span><span class="sxs-lookup"><span data-stu-id="29279-129">Supports bandwidth sharing and stream prioritization information in the profile.</span></span> <span data-ttu-id="29279-130">Erbt alle Methoden von **iwmprofile** und **IWMProfile2**.</span><span class="sxs-lookup"><span data-stu-id="29279-130">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span>                |
| [<span data-ttu-id="29279-131">**Iwmsynkreader**</span><span class="sxs-lookup"><span data-stu-id="29279-131">**IWMSyncReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | <span data-ttu-id="29279-132">Stellt synchrone Lesefunktionen für digitale Mediendateien bereit.</span><span class="sxs-lookup"><span data-stu-id="29279-132">Provides synchronous reading capabilities for digital media files.</span></span>                                                                                                 |
| [<span data-ttu-id="29279-133">**IWMSyncReader2**</span><span class="sxs-lookup"><span data-stu-id="29279-133">**IWMSyncReader2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | <span data-ttu-id="29279-134">Bietet Unterstützung für das Durchsuchen von SMPTE-Zeit Codes und das manuelle Zuordnen von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="29279-134">Provides support for seeking to SMPTE time codes and for allocating samples manually.</span></span> <span data-ttu-id="29279-135">Erbt alle Methoden von **iwmsynkreader**.</span><span class="sxs-lookup"><span data-stu-id="29279-135">Inherits all of the methods of **IWMSyncReader**.</span></span>                            |



 

## <a name="related-topics"></a><span data-ttu-id="29279-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="29279-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29279-137">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="29279-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="29279-138">**Reader-Objekt**</span><span class="sxs-lookup"><span data-stu-id="29279-138">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="29279-139">**Lesen von Dateien mit dem synchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="29279-139">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




