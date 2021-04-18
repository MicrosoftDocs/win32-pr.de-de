---
description: Die Pipeline Schicht in Microsoft Media Foundation ist die Ebene der Architektur, die Mediendaten direkt generiert oder verarbeitet.
ms.assetid: d6396246-ddc4-4e24-9371-35ddbef59b8a
title: Media Foundation Pipeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f307049d7f88ca6b50479bdb261c75ba20f9b41e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106351839"
---
# <a name="media-foundation-pipeline"></a><span data-ttu-id="e1c93-103">Media Foundation Pipeline</span><span class="sxs-lookup"><span data-stu-id="e1c93-103">Media Foundation Pipeline</span></span>

<span data-ttu-id="e1c93-104">Die *Pipeline* Schicht in Microsoft Media Foundation ist die Ebene der Architektur, die Mediendaten direkt generiert oder verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e1c93-104">The *pipeline* layer in Microsoft Media Foundation is the layer of the architecture that directly generates or processes media data.</span></span>

<span data-ttu-id="e1c93-105">Bei den meisten Anwendungen werden Methoden nicht direkt auf den Pipeline Komponenten aufgerufen, obwohl dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="e1c93-105">Most applications do not call methods directly on the pipeline components, although it is possible to do so.</span></span> <span data-ttu-id="e1c93-106">Lesen Sie diese Themen, wenn Sie eine benutzerdefinierte Pipeline Komponente schreiben.</span><span class="sxs-lookup"><span data-stu-id="e1c93-106">Read these topics if you are writing a custom pipeline component.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e1c93-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="e1c93-107">In this section</span></span>



| <span data-ttu-id="e1c93-108">Thema</span><span class="sxs-lookup"><span data-stu-id="e1c93-108">Topic</span></span>                                                                     | <span data-ttu-id="e1c93-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1c93-109">Description</span></span>                                                                                                                           |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1c93-110">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="e1c93-110">Media Sources</span></span>](media-sources.md)<br/>                             | <span data-ttu-id="e1c93-111">Medienquellen generieren Mediendaten, in der Regel über eine Datei, ein Erfassungsgerät oder einen Netzwerkstream.</span><span class="sxs-lookup"><span data-stu-id="e1c93-111">Media sources generate media data, typically from a file, capture device, or network stream.</span></span> <br/>                              |
| [<span data-ttu-id="e1c93-112">Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="e1c93-112">Media Foundation Transforms</span></span>](media-foundation-transforms.md)<br/> | <span data-ttu-id="e1c93-113">Media Foundation Transformationen (MFTs) verarbeiten von Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="e1c93-113">Media Foundation transforms (MFTs) process media data.</span></span> <span data-ttu-id="e1c93-114">Beispielsweise werden Codecs in Media Foundation als MFTs implementiert.</span><span class="sxs-lookup"><span data-stu-id="e1c93-114">For example, codecs in Media Foundation are implemented as MFTs.</span></span> <br/>   |
| [<span data-ttu-id="e1c93-115">Medien senken</span><span class="sxs-lookup"><span data-stu-id="e1c93-115">Media Sinks</span></span>](media-sinks.md)<br/>                                 | <span data-ttu-id="e1c93-116">Medien senken verbrauchen Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="e1c93-116">Media sinks consume media data.</span></span> <span data-ttu-id="e1c93-117">Beispielsweise könnte eine Medien Senke die Daten in eine Datei schreiben oder die Daten über ein Netzwerk senden.</span><span class="sxs-lookup"><span data-stu-id="e1c93-117">For example, a media sink might write the data to a file, or send the data over a network.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e1c93-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1c93-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1c93-119">Media Foundation und com</span><span class="sxs-lookup"><span data-stu-id="e1c93-119">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="e1c93-120">Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="e1c93-120">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




