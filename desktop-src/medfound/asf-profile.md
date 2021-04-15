---
description: In diesem Thema wird beschrieben, wie Sie in Microsoft Media Foundation mit ASF-Profilen arbeiten.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: ASF-Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524659"
---
# <a name="asf-profile"></a><span data-ttu-id="edbec-103">ASF-Profil</span><span class="sxs-lookup"><span data-stu-id="edbec-103">ASF Profile</span></span>

<span data-ttu-id="edbec-104">In diesem Thema wird beschrieben, wie Sie in Microsoft Media Foundation mit ASF-Profilen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="edbec-104">This topic describes how to work with ASF profiles in Microsoft Media Foundation.</span></span>

<span data-ttu-id="edbec-105">Eine ASF-Datei (Advanced Systems Format) enthält mindestens einen Stream.</span><span class="sxs-lookup"><span data-stu-id="edbec-105">An Advanced Systems Format (ASF) file contains one or more streams.</span></span> <span data-ttu-id="edbec-106">Für jeden Stream enthält der ASF-Header einen Stream Properties-Header, der den Datenstrom beschreibt.</span><span class="sxs-lookup"><span data-stu-id="edbec-106">For each stream, the ASF header contains a Stream Properties Header that describes the stream.</span></span> <span data-ttu-id="edbec-107">Auf der [wmcontainer](wmcontainer-asf-components.md) -Ebene werden die folgenden Objekte verwendet, um die Eigenschaften der ASF-Streams festzulegen oder zu lesen:</span><span class="sxs-lookup"><span data-stu-id="edbec-107">At the [WMContainer](wmcontainer-asf-components.md) layer, the following objects are used to set or read the properties of the ASF streams:</span></span>

-   <span data-ttu-id="edbec-108">*ASF-Profil* Objekt: Beschreibt die Streams und ihre Beziehungen untereinander.</span><span class="sxs-lookup"><span data-stu-id="edbec-108">*ASF profile* object: Describes the streams and their relationships with each other.</span></span> <span data-ttu-id="edbec-109">Das ASF-Profil Objekt macht die [**imfasf profile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="edbec-109">The ASF profile object exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span>
-   <span data-ttu-id="edbec-110">*Stream Configuration* Object: Beschreibt einen Stream.</span><span class="sxs-lookup"><span data-stu-id="edbec-110">*Stream configuration* object: Describes one stream.</span></span> <span data-ttu-id="edbec-111">Das Datenstrom-Konfigurationsobjekt enthält einen Medientyp, der das Format des Streams beschreibt.</span><span class="sxs-lookup"><span data-stu-id="edbec-111">The stream configuration object contains a media type that describes the format of the stream.</span></span> <span data-ttu-id="edbec-112">Für Audiodaten und Videostreams beschreibt der Medientyp genau, wie der Stream konfiguriert ist, und wird von Codecs verwendet, die den Datenstrom codieren oder decodieren.</span><span class="sxs-lookup"><span data-stu-id="edbec-112">For audio and video streams, the media type describes exactly how the stream is configured, and is used by codecs that encode or decode the stream.</span></span> <span data-ttu-id="edbec-113">Das Datenstrom-Konfigurationsobjekt macht die [**imfasf streamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="edbec-113">The stream configuration object exposes the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="edbec-114">Ein gültiges ASF-Profil enthält mindestens ein Datenstrom-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="edbec-114">A valid ASF profile contains at least one stream configuration object.</span></span>
-   <span data-ttu-id="edbec-115">*Gegenseitiges Ausschluss* Objekt: Beschreibt mehrere Datenströme, die nicht gleichzeitig gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="edbec-115">*Mutual exclusion* object: Describes multiple streams that are not intended be read concurrently.</span></span> <span data-ttu-id="edbec-116">Ein gegenseitiges Ausschluss Objekt macht die [**imfassmutualexclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="edbec-116">A mutual exclusion object exposes the [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) interface.</span></span> <span data-ttu-id="edbec-117">Ein ASF-Profil enthält keine oder mehrere gegenseitige Ausschluss Objekte.</span><span class="sxs-lookup"><span data-stu-id="edbec-117">An ASF profile contains zero or more mutual exclusion objects.</span></span>

<span data-ttu-id="edbec-118">Das folgende Diagramm zeigt die Beziehung zwischen dem ASF-Profil und den Objekten, die im Profil enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="edbec-118">The following diagram shows the relationship between the ASF profile and the objects that are contained in the profile.</span></span>

![Strukturdiagramm eines Knoten vom Typ "ASF-Profil" mit untergeordneten Datenstrom Konfigurations Knoten; der erste Punkt zeigt den Medientyp, die nächsten zwei für den gegenseitigen Ausschluss.](images/asf-components02.png)

<span data-ttu-id="edbec-120">Zur Wiedergabe wird das ASF-Profil zum Auflisten der Streams und zum Suchen der Streamformate verwendet.</span><span class="sxs-lookup"><span data-stu-id="edbec-120">For playback, the ASF profile is used to enumerate the streams and find the stream formats.</span></span> <span data-ttu-id="edbec-121">Bei der Codierung wird das ASF-Profil zum Konfigurieren der Streams in der Zieldatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="edbec-121">For encoding, the ASF profile is used to configure the streams in the destination file.</span></span>

<span data-ttu-id="edbec-122">Das ASF-Profil wird auch zum Konfigurieren der [ASF-Medien Senke](asf-media-sinks.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="edbec-122">The ASF profile is also used to configure the [ASF Media Sink](asf-media-sinks.md).</span></span> <span data-ttu-id="edbec-123">Für jeden Datenstrom im ASF-Profil erstellt die ASF-Medien Senke eine entsprechende streamsenke.</span><span class="sxs-lookup"><span data-stu-id="edbec-123">For each stream in the ASF profile, the ASF media sink creates a corresponding stream sink.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="edbec-124">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="edbec-124">In this section</span></span>



| <span data-ttu-id="edbec-125">Thema</span><span class="sxs-lookup"><span data-stu-id="edbec-125">Topic</span></span>                                                                                           | <span data-ttu-id="edbec-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edbec-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="edbec-127">Erstellen eines ASF-Profils</span><span class="sxs-lookup"><span data-stu-id="edbec-127">Creating an ASF Profile</span></span>](creating-an-asf-profile.md)<br/>                               | <span data-ttu-id="edbec-128">Beschreibt, wie ein ASF-Profil Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="edbec-128">Describes how to create an ASF profile object.</span></span><br/>          |
| [<span data-ttu-id="edbec-129">Erstellen und Konfigurieren von ASF-Streams</span><span class="sxs-lookup"><span data-stu-id="edbec-129">Creating and Configuring ASF Streams</span></span>](creating-and-configuring-asf-streams.md)<br/>     | <span data-ttu-id="edbec-130">Beschreibt, wie Datenströme einem ASF-Profil hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="edbec-130">Describes how to add streams to an ASF profile.</span></span><br/>         |
| [<span data-ttu-id="edbec-131">Verwenden des gegenseitigen Ausschlusses für ASF-Streams</span><span class="sxs-lookup"><span data-stu-id="edbec-131">Using Mutual Exclusion for ASF Streams</span></span>](using-mutual-exclusion-for-asf-streams.md)<br/> | <span data-ttu-id="edbec-132">Beschreibt das Hinzufügen von gegenseitigen Ausschlüssen zu ASF-Streams.</span><span class="sxs-lookup"><span data-stu-id="edbec-132">Describes how to add mutual exclusions to ASF streams.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="edbec-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="edbec-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edbec-134">Medientypen</span><span class="sxs-lookup"><span data-stu-id="edbec-134">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="edbec-135">Tutorial: 1-Pass-Windows-Medien Codierung</span><span class="sxs-lookup"><span data-stu-id="edbec-135">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="edbec-136">Tutorial: Schreiben einer WMA-Datei mithilfe der CBR-Codierung</span><span class="sxs-lookup"><span data-stu-id="edbec-136">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[<span data-ttu-id="edbec-137">Wmcontainer-ASF-Komponenten</span><span class="sxs-lookup"><span data-stu-id="edbec-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 




