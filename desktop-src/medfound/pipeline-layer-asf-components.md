---
description: Im Media Foundations-Pipeline Modell ist eine Medienquelle mit einer Transformation verbunden, die weiter mit einer Medien Senke verbunden ist.
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: Komponenten der Pipeline Schicht-ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372915"
---
# <a name="pipeline-layer-asf-components"></a><span data-ttu-id="70dfa-103">Komponenten der Pipeline Schicht-ASF</span><span class="sxs-lookup"><span data-stu-id="70dfa-103">Pipeline Layer ASF Components</span></span>

<span data-ttu-id="70dfa-104">In Media Foundation Pipeline Modell ist eine Medienquelle mit einer Transformation verbunden, die weiter mit einer Medien Senke verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="70dfa-104">In Media Foundation's pipeline model, a media source is connected to a transform which is further connected to a media sink.</span></span> <span data-ttu-id="70dfa-105">Die in der Quelle enthaltenen Daten fließen durch die Transformation und generieren Ausgabemedien Beispiele in der Senke für die Wiedergabe oder Codierung.</span><span class="sxs-lookup"><span data-stu-id="70dfa-105">The data contained in the source flows through the transform and generates output media samples in the sink for the purpose of playback or encoding.</span></span> <span data-ttu-id="70dfa-106">Abhängig davon, ob die Anwendung ASF-Inhalte wiedergeben oder in eine ASF-Datei codieren möchte, muss die Anwendung die Pipeline anders erstellen.</span><span class="sxs-lookup"><span data-stu-id="70dfa-106">Depending on whether the application wants to playback ASF content or encode to an ASF file, the application must build the pipeline differently.</span></span>

<span data-ttu-id="70dfa-107">Die folgenden Themen enthalten Informationen zu den Komponenten der Pipeline Schicht.</span><span class="sxs-lookup"><span data-stu-id="70dfa-107">The following topics contain information about the pipeline layer components.</span></span>

-   [<span data-ttu-id="70dfa-108">ASF-Medienquelle</span><span class="sxs-lookup"><span data-stu-id="70dfa-108">ASF Media Source</span></span>](asf-media-source.md)
-   [<span data-ttu-id="70dfa-109">Windows Media Encoder</span><span class="sxs-lookup"><span data-stu-id="70dfa-109">Windows Media Encoders</span></span>](windows-media-encoders.md)
-   [<span data-ttu-id="70dfa-110">ASF-Medien senken</span><span class="sxs-lookup"><span data-stu-id="70dfa-110">ASF Media Sinks</span></span>](asf-media-sinks.md)

<span data-ttu-id="70dfa-111">Die drei Hauptkomponenten einer ASF-Pipeline für die Wiedergabe lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="70dfa-111">The three main components of an ASF pipeline for playback are as follows:</span></span>

-   <span data-ttu-id="70dfa-112">Die ASF-Medienquelle wird von Media Foundation bereitgestellt, die eine ASF-Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="70dfa-112">ASF media source is provided by Media Foundation that represents an ASF file.</span></span>
-   <span data-ttu-id="70dfa-113">Audioresamplers, Grafik Bild-Resizers usw., (Transformation)</span><span class="sxs-lookup"><span data-stu-id="70dfa-113">Audio resamplers, video image resizers, etc., (transform)</span></span>
-   <span data-ttu-id="70dfa-114">Audiodatei und Videorenderer (senken)</span><span class="sxs-lookup"><span data-stu-id="70dfa-114">Audio and Video renderer (sinks)</span></span>

<span data-ttu-id="70dfa-115">Weitere Informationen zum Erstellen einer Wiedergabe Pipeline finden Sie unter [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="70dfa-115">For information about building a playback pipeline, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="70dfa-116">Die drei Hauptkomponenten einer ASF-Pipeline für die Codierung lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="70dfa-116">The three main components of an ASF pipeline for encoding are as follows:</span></span>

-   <span data-ttu-id="70dfa-117">Medienquelle, die die Daten in einem Format darstellt, das konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="70dfa-117">Media source representing the data in a format that needs to be converted.</span></span> <span data-ttu-id="70dfa-118">Diese Komponente kann eine der Standard Medienquellen sein, die von Media Foundation bereitgestellt werden, oder eine benutzerdefinierte Quelle, die die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="70dfa-118">This component can be one of the default media sources provided by Media Foundation or a custom source that exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>
-   <span data-ttu-id="70dfa-119">Windows Media Encoder (Transform), die die Formatkonvertierung durchführen.</span><span class="sxs-lookup"><span data-stu-id="70dfa-119">Windows Media encoders (transform) that perform the format conversion.</span></span>
-   <span data-ttu-id="70dfa-120">Von Media Foundation bereitgestellte ASF-Medien senken, die in einer von der Anwendung angegebenen Ausgabedatei ASF-Objekte und Medien Beispiele schreiben.</span><span class="sxs-lookup"><span data-stu-id="70dfa-120">ASF media sinks provided by Media Foundation that write ASF objects and media samples in an output file specified by the application.</span></span>

<span data-ttu-id="70dfa-121">Die Pipeline wird in einer Topologie dargestellt, und jedes Objekt in der Pipeline wird von einem topologieknoten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="70dfa-121">The pipeline is represented in a topology and each object in the pipeline is represented by a topology node.</span></span> <span data-ttu-id="70dfa-122">Sowohl bei der Wiedergabe als auch bei der Codierung werden alle Pipeline Vorgänge von der Medien Sitzung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="70dfa-122">Both for playback and encoding, all of the pipeline operations are handled by the Media Session.</span></span> <span data-ttu-id="70dfa-123">Eine der Zuständigkeiten der Medien Sitzung besteht darin, sicherzustellen, dass die Pipeline über alle Komponenten verfügt, die zum Generieren der Ausgabe erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="70dfa-123">One of responsibilities of the Media Session is to make sure that the pipeline has all the components required to generate output.</span></span> <span data-ttu-id="70dfa-124">Wenn sich z. b. in einer Codierungs Pipeline das Format der Audioquelle von dem Zielformat unterscheidet, fügt die Medien Sitzung zusätzliche Transformations Komponenten wie den Resampler ein, der die entsprechenden Abtastraten Konvertierungen ausführt.</span><span class="sxs-lookup"><span data-stu-id="70dfa-124">For example, in an encoding pipeline, if the audio source format is different than the target format, the Media Session inserts additional transform components such as the resampler that performs appropriate sample rate conversions.</span></span> <span data-ttu-id="70dfa-125">Die Datenflusssteuerung durch die Pipeline wird auch von der Medien Sitzung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="70dfa-125">The data flow control through the pipeline is also managed by the Media Session.</span></span> <span data-ttu-id="70dfa-126">In einem Wiedergabe Szenario, in dem die Medien Sitzung gestartet wird, sendet die Medien Sitzung Beispiele an SAR und EVR, das Sie auf dem Ausgabegerät rendert.</span><span class="sxs-lookup"><span data-stu-id="70dfa-126">In a playback scenario, starting the Media Session the Media Session sends samples to SAR and EVR, which renders them on the output device.</span></span> <span data-ttu-id="70dfa-127">Bei der Codierung beginnt das Starten der Medien Sitzung mit dem Codierungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="70dfa-127">For encoding, starting the Media Session begins the encoding process.</span></span> <span data-ttu-id="70dfa-128">Die Sitzung benachrichtigt die Anwendung asynchron, wenn die Codierung vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="70dfa-128">The session asynchronously notifies the application when the encoding is complete.</span></span>

<span data-ttu-id="70dfa-129">Das folgende Thema enthält Schritt-für-Schritt-Anleitungen zum Verwenden der Pipeline Schicht Komponenten zum Erstellen einer Codierungs Topologie.</span><span class="sxs-lookup"><span data-stu-id="70dfa-129">The following topic contains step-by-step instructions about using the pipeline layer components to build an encoding topology.</span></span> <span data-ttu-id="70dfa-130">Komponenten zum Lesen und Schreiben von ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="70dfa-130">components for reading and writing ASF files.</span></span>

-   [<span data-ttu-id="70dfa-131">Tutorial: 1-Pass-Windows-Medien Codierung</span><span class="sxs-lookup"><span data-stu-id="70dfa-131">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a><span data-ttu-id="70dfa-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="70dfa-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70dfa-133">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="70dfa-133">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



