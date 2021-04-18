---
description: Media Foundation Transformationen
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Media Foundation Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0518ced06169f6d998bdad1747878d109e0676
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361126"
---
# <a name="media-foundation-transforms"></a><span data-ttu-id="bb261-103">Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="bb261-103">Media Foundation Transforms</span></span>

<span data-ttu-id="bb261-104">Media Foundation Transformationen (MFTs) stellen ein generisches Modell zum Verarbeiten von Mediendaten bereit.</span><span class="sxs-lookup"><span data-stu-id="bb261-104">Media Foundation transforms (MFTs) provide a generic model for processing media data.</span></span> <span data-ttu-id="bb261-105">MFTs werden für Decoders, Encoder und digitale Signalprozessoren (DSPs) verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb261-105">MFTs are used for decoders, encoders, and digital signal processors (DSPs).</span></span> <span data-ttu-id="bb261-106">Kurz gesagt: alles, was sich in der Medien Pipeline zwischen der Medienquelle und der Medien Senke befindet, ist eine MFT.</span><span class="sxs-lookup"><span data-stu-id="bb261-106">In short, anything that sits in the media pipeline between the media source and the media sink is an MFT.</span></span>

<span data-ttu-id="bb261-107">In diesem Abschnitt werden das MFT-Programmiermodell und die Implementierung von MFT beschrieben, mit Empfehlungen für bestimmte Typen von MFTs, wie z. b. Decoders.</span><span class="sxs-lookup"><span data-stu-id="bb261-107">This section describes the MFT programming model and how to implement an MFT, with recommendations for specific types of MFTs, such as decoders.</span></span>



| <span data-ttu-id="bb261-108">Thema</span><span class="sxs-lookup"><span data-stu-id="bb261-108">Topic</span></span>                                                                    | <span data-ttu-id="bb261-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb261-109">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb261-110">Informationen zu MFTs</span><span class="sxs-lookup"><span data-stu-id="bb261-110">About MFTs</span></span>](about-mfts.md)                                             | <span data-ttu-id="bb261-111">Bietet eine kurze Übersicht über MFTs</span><span class="sxs-lookup"><span data-stu-id="bb261-111">Provides a brief overview of MFTs</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="bb261-112">Einfaches MFT-Verarbeitungsmodell</span><span class="sxs-lookup"><span data-stu-id="bb261-112">Basic MFT Processing Model</span></span>](basic-mft-processing-model.md)             | <span data-ttu-id="bb261-113">Beschreibt das grundlegende Modell für die Verarbeitung von Daten mit einem MFT ausführlicher.</span><span class="sxs-lookup"><span data-stu-id="bb261-113">Describes in more detail the basic model for processing data with an MFT.</span></span>                                                                                                                           |
| [<span data-ttu-id="bb261-114">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="bb261-114">Asynchronous MFTs</span></span>](asynchronous-mfts.md)                               | <span data-ttu-id="bb261-115">Beschreibt ein asynchrones Verarbeitungsmodell, das eine Alternative zum grundlegenden Modell ist.</span><span class="sxs-lookup"><span data-stu-id="bb261-115">Describes an asynchronous processing model that is an alternative to the basic model.</span></span><br/> <span data-ttu-id="bb261-116">Die asynchrone Verarbeitung wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bb261-116">Asynchronous processing was introduced in Windows 7.</span></span> <span data-ttu-id="bb261-117">Nicht jedes MFT unterstützt dieses Modell.</span><span class="sxs-lookup"><span data-stu-id="bb261-117">Not every MFT supports this model.</span></span><br/> |
| [<span data-ttu-id="bb261-118">Registrieren und Auflisten von MFTs</span><span class="sxs-lookup"><span data-stu-id="bb261-118">Registering and Enumerating MFTs</span></span>](registering-and-enumerating-mfts.md) | <span data-ttu-id="bb261-119">Informationen zum Registrieren eines MFT und zum Aufzählen von MFTs in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="bb261-119">How to register an MFT and how to enumerate MFTs in the registry.</span></span>                                                                                                                                   |
| [<span data-ttu-id="bb261-120">Einschränkungen bei der Verwendung des Felds</span><span class="sxs-lookup"><span data-stu-id="bb261-120">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)               | <span data-ttu-id="bb261-121">Beschreibt den Mechanismus zum Entsperren eines MFT mit Einschränkungen für das Feld.</span><span class="sxs-lookup"><span data-stu-id="bb261-121">Describes the mechanism for unlocking an MFT that has field-of-use restrictions.</span></span>                                                                                                                    |
| [<span data-ttu-id="bb261-122">Vergleich von MFTs und DMOs</span><span class="sxs-lookup"><span data-stu-id="bb261-122">Comparison of MFTs and DMOs</span></span>](comparison-of-mfts-and-dmos.md)           | <span data-ttu-id="bb261-123">Fasst die Unterschiede zwischen MFTs und DMOS zusammen.</span><span class="sxs-lookup"><span data-stu-id="bb261-123">Summarizes the differences between MFTs and DMOs.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="bb261-124">Schreiben eines benutzerdefinierten MFT</span><span class="sxs-lookup"><span data-stu-id="bb261-124">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)                         | <span data-ttu-id="bb261-125">Richtlinien zum Schreiben einer benutzerdefinierten MFT.</span><span class="sxs-lookup"><span data-stu-id="bb261-125">Guidelines for writing a custom MFT.</span></span>                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="bb261-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb261-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb261-127">Media Foundation Pipeline</span><span class="sxs-lookup"><span data-stu-id="bb261-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="bb261-128">Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="bb261-128">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="bb261-129">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="bb261-129">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




