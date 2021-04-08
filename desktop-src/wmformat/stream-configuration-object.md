---
title: Stream-Konfigurationsobjekt
description: Stream-Konfigurationsobjekt
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Windows Media-Format-SDK, Datenstrom-Konfigurationsobjekte
- Advanced Systems Format (ASF), streamkonfigurationsobjekte
- ASF (Advanced Systems Format), Datenstrom-Konfigurationsobjekte
- Objekte, streamkonfigurationsobjekte
- Stream-Konfigurationsobjekte
- Streams, streamkonfigurationsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101347"
---
# <a name="stream-configuration-object"></a><span data-ttu-id="597a7-109">Stream-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="597a7-109">Stream Configuration Object</span></span>

<span data-ttu-id="597a7-110">Ein Datenstrom-Konfigurationsobjekt wird verwendet, um die Eigenschaften eines Mediendaten Stroms in einer ASF-Datei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="597a7-110">A stream configuration object is used to specify the properties of a media stream in an ASF file.</span></span> <span data-ttu-id="597a7-111">Stream-Konfigurationsobjekte können für vorhandene Datenströme in einem Profil erstellt werden, oder Sie können leer erstellt werden, um neue Daten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="597a7-111">Stream configuration objects can be created for existing streams in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="597a7-112">Streamkonfigurationsobjekte können nicht unabhängig von einem Profil Objekt vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="597a7-112">Stream configuration objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="597a7-113">Zum Speichern des Inhalts eines Datenstrom-Konfigurations Objekts müssen Sie entweder [**iwmprofile:: addstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) zum Hinzufügen eines neuen Streams oder [**iwmprofile:: reconfigstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) zum Speichern von Änderungen, die an einem vorhandenen Stream vorgenommen wurden, hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="597a7-113">To save the contents of a stream configuration object, you must call either [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add a new stream or [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to save changes made to an existing stream.</span></span>

<span data-ttu-id="597a7-114">Verwenden Sie zum Erstellen eines Datenstrom-Konfigurations Objekts eine der folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="597a7-114">To create a stream configuration object, use one of the following methods.</span></span>



| <span data-ttu-id="597a7-115">Methode</span><span class="sxs-lookup"><span data-stu-id="597a7-115">Method</span></span>                                                                | <span data-ttu-id="597a7-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="597a7-116">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="597a7-117">**Iwmprofile:: kreatenewstream**</span><span class="sxs-lookup"><span data-stu-id="597a7-117">**IWMProfile::CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | <span data-ttu-id="597a7-118">Erstellt ein Datenstrom-Konfigurationsobjekt ohne Daten.</span><span class="sxs-lookup"><span data-stu-id="597a7-118">Creates a stream configuration object without any data.</span></span>                                                                          |
| [<span data-ttu-id="597a7-119">**Iwmprofile:: GetStream**</span><span class="sxs-lookup"><span data-stu-id="597a7-119">**IWMProfile::GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | <span data-ttu-id="597a7-120">Erstellt ein Datenstrom-Konfigurationsobjekt, das mit Daten aus einem Profil aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="597a7-120">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="597a7-121">Verwendet den streamindex, um den gewünschten Stream zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="597a7-121">Uses the stream index to identify the desired stream.</span></span>  |
| [<span data-ttu-id="597a7-122">**Iwmprofile:: getstreambynumber**</span><span class="sxs-lookup"><span data-stu-id="597a7-122">**IWMProfile::GetStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | <span data-ttu-id="597a7-123">Erstellt ein Datenstrom-Konfigurationsobjekt, das mit Daten aus einem Profil aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="597a7-123">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="597a7-124">Verwendet die Datenstrom Nummer, um den gewünschten Stream zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="597a7-124">Uses the stream number to identify the desired stream.</span></span> |



 

<span data-ttu-id="597a7-125">Alle Methoden in der vorangehenden Tabelle legen einen Zeiger auf eine **iwmstreamconfig** -Schnittstelle fest.</span><span class="sxs-lookup"><span data-stu-id="597a7-125">All of the methods in the preceding table set a pointer to an **IWMStreamConfig** interface.</span></span> <span data-ttu-id="597a7-126">Die anderen Schnittstellen des Datenstrom-Konfigurations Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="597a7-126">The other interfaces of the stream configuration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="597a7-127">Die folgenden Schnittstellen werden vom Datenstrom-Konfigurationsobjekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="597a7-127">The following interfaces are supported by the stream configuration object.</span></span>



| <span data-ttu-id="597a7-128">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="597a7-128">Interface</span></span>                                        | <span data-ttu-id="597a7-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="597a7-129">Description</span></span>                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="597a7-130">**Iwmmedia-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="597a7-130">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="597a7-131">Legt die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur für den Stream fest und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="597a7-131">Sets and retrieves the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream.</span></span>                                    |
| [<span data-ttu-id="597a7-132">**Iwmpropertyvault**</span><span class="sxs-lookup"><span data-stu-id="597a7-132">**IWMPropertyVault**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | <span data-ttu-id="597a7-133">Legt Eigenschaften fest, die nicht für alle Streams erforderlich sind, wie z. b. Einstellungen für Variablen Bitraten (VBR), und ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="597a7-133">Sets and retrieves properties that are not required for all streams, like variable bit rate (VBR) settings.</span></span>                  |
| [<span data-ttu-id="597a7-134">**Iwmstreamconfig**</span><span class="sxs-lookup"><span data-stu-id="597a7-134">**IWMStreamConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | <span data-ttu-id="597a7-135">Legt alle grundlegenden Informationen zu einem Stream fest und ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="597a7-135">Sets and retrieves all of the basic information about a stream.</span></span>                                                              |
| [<span data-ttu-id="597a7-136">**IWMStreamConfig2**</span><span class="sxs-lookup"><span data-stu-id="597a7-136">**IWMStreamConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | <span data-ttu-id="597a7-137">Konfiguriert die Typen von Dateneinheiten Erweiterungen, die dem Stream zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="597a7-137">Configures the types of data unit extensions associated with the stream.</span></span> <span data-ttu-id="597a7-138">Erbt alle Methoden von **iwmstreamconfig**.</span><span class="sxs-lookup"><span data-stu-id="597a7-138">Inherits all of the methods of **IWMStreamConfig**.</span></span> |
| [<span data-ttu-id="597a7-139">**IWMStreamConfig3**</span><span class="sxs-lookup"><span data-stu-id="597a7-139">**IWMStreamConfig3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | <span data-ttu-id="597a7-140">Legt die Sprache für den Stream fest und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="597a7-140">Sets and retrieves the language for the stream.</span></span> <span data-ttu-id="597a7-141">Erbt alle Methoden von **iwmstreamconfig** und **IWMStreamConfig2**.</span><span class="sxs-lookup"><span data-stu-id="597a7-141">Inherits all of the methods of **IWMStreamConfig** and **IWMStreamConfig2**.</span></span> |
| [<span data-ttu-id="597a7-142">**Iwmvideomedia-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="597a7-142">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="597a7-143">Verwaltet die Eigenschaften eines Videostreams.</span><span class="sxs-lookup"><span data-stu-id="597a7-143">Manages the properties of a video stream.</span></span> <span data-ttu-id="597a7-144">Dies ist eine optionale Schnittstelle, die nur für Videostreams verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="597a7-144">This is an optional interface, and is available only for video streams.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="597a7-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="597a7-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="597a7-146">**Konfigurieren von Streams**</span><span class="sxs-lookup"><span data-stu-id="597a7-146">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="597a7-147">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="597a7-147">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="597a7-148">**Profil-Manager-Objekt**</span><span class="sxs-lookup"><span data-stu-id="597a7-148">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 




