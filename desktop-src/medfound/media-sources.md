---
description: Medienquellen
ms.assetid: 65132e7d-22f6-4209-bc58-f5ea86ebd514
title: Medienquellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd69b63679ba73bc4049f37207b1d07940edada
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104218980"
---
# <a name="media-sources"></a><span data-ttu-id="48a8f-103">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="48a8f-103">Media Sources</span></span>

<span data-ttu-id="48a8f-104">*Medienquellen* sind Objekte, die Mediendaten in der Media Foundation Pipeline generieren.</span><span class="sxs-lookup"><span data-stu-id="48a8f-104">*Media sources* are objects that generate media data in the Media Foundation pipeline.</span></span> <span data-ttu-id="48a8f-105">In diesem Abschnitt werden die Medienquellen-APIs ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="48a8f-105">This section describes the media source APIs in detail.</span></span> <span data-ttu-id="48a8f-106">Lesen Sie diesen Abschnitt, wenn Sie eine benutzerdefinierte Medienquelle implementieren oder eine Medienquelle außerhalb der Media Foundation Pipeline verwenden.</span><span class="sxs-lookup"><span data-stu-id="48a8f-106">Read this section if you are implementing a custom media source, or using a media source outside of the Media Foundation pipeline.</span></span>

<span data-ttu-id="48a8f-107">Wenn Ihre Anwendung die Steuerungsebene verwendet, muss Sie nur eine begrenzte Teilmenge der Medienquellen-APIs verwenden.</span><span class="sxs-lookup"><span data-stu-id="48a8f-107">If your application uses the control layer, it needs to use only a limited subset of the media source APIs.</span></span> <span data-ttu-id="48a8f-108">Weitere Informationen finden Sie im Thema [Verwenden von Medienquellen mit der Medien Sitzung](using-media-sources-with-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="48a8f-108">For information, see the topic [Using Media Sources with the Media Session](using-media-sources-with-the-media-session.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="48a8f-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="48a8f-109">In this section</span></span>



| <span data-ttu-id="48a8f-110">Thema</span><span class="sxs-lookup"><span data-stu-id="48a8f-110">Topic</span></span>                                                                                                 | <span data-ttu-id="48a8f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48a8f-111">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48a8f-112">Medienquellen-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="48a8f-112">Media Source Object Model</span></span>](media-source-object-model.md)<br/>                                 | <span data-ttu-id="48a8f-113">In diesem Thema wird das Objektmodell für Medienquellen in Microsoft Media Foundation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="48a8f-113">This topic describes the object model for media sources in Microsoft Media Foundation</span></span><br/>                     |
| [<span data-ttu-id="48a8f-114">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="48a8f-114">Presentation Descriptors</span></span>](presentation-descriptors.md)<br/>                                   | <span data-ttu-id="48a8f-115">Ein *Präsentations Deskriptor* ist ein Objekt, das die Beschreibung einer bestimmten Präsentation enthält.</span><span class="sxs-lookup"><span data-stu-id="48a8f-115">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span><br/>      |
| [<span data-ttu-id="48a8f-116">Medienquellen Ereignisse</span><span class="sxs-lookup"><span data-stu-id="48a8f-116">Media Source Events</span></span>](media-source-events.md)<br/>                                             | <span data-ttu-id="48a8f-117">In diesem Thema werden die Ereignisse aufgelistet, die von Medienquellen und Mediendaten strömen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="48a8f-117">This topic lists the events that are sent by media sources and media streams.</span></span><br/>                             |
| [<span data-ttu-id="48a8f-118">Schreiben einer benutzerdefinierten Medienquelle</span><span class="sxs-lookup"><span data-stu-id="48a8f-118">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)<br/>                         | <span data-ttu-id="48a8f-119">In diesem Thema wird beschrieben, wie eine benutzerdefinierte Medienquelle in Media Foundation implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="48a8f-119">This topic describes how to implement a custom media source in Media Foundation.</span></span><br/>                          |
| [<span data-ttu-id="48a8f-120">Fallstudie: MPEG-1-Medienquelle</span><span class="sxs-lookup"><span data-stu-id="48a8f-120">Case Study: MPEG-1 Media Source</span></span>](tutorial--writing-a-custom-media-source.md)<br/>             | <span data-ttu-id="48a8f-121">In diesem Thema wird das [MPEG-1 Media Source](mpeg1source-sample.md) SDK-Beispiel ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="48a8f-121">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span><br/>        |
| [<span data-ttu-id="48a8f-122">Benutzerdefinierte Metadatenanbieter für Mediendateien</span><span class="sxs-lookup"><span data-stu-id="48a8f-122">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)<br/> | <span data-ttu-id="48a8f-123">In diesem Thema wird beschrieben, wie ein benutzerdefinierter shelleigenschaftenhandler für eine Media Foundation Medienquelle geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="48a8f-123">This topic describes how to write a custom Shell property handler for a Media Foundation media source.</span></span><br/>    |
| [<span data-ttu-id="48a8f-124">Quellresolver</span><span class="sxs-lookup"><span data-stu-id="48a8f-124">Source Resolver</span></span>](source-resolver.md)<br/>                                                     | <span data-ttu-id="48a8f-125">Der Source Resolver nimmt einen URL oder Bytedatenstrom und erstellt die entsprechende Medienquelle für den Inhalt.</span><span class="sxs-lookup"><span data-stu-id="48a8f-125">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="48a8f-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48a8f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48a8f-127">Media Foundation Pipeline</span><span class="sxs-lookup"><span data-stu-id="48a8f-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="48a8f-128">Benutzerdefinierte Metadatenanbieter für Mediendateien</span><span class="sxs-lookup"><span data-stu-id="48a8f-128">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)
</dt> <dt>

[<span data-ttu-id="48a8f-129">Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="48a8f-129">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




