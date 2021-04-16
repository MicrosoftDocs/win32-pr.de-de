---
description: In diesem Thema wird der Unterschied zwischen vollständigen Medientypen und partiellen Medientypen beschrieben.
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: Vollständige und partielle Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac772c09668ee3db96e42d25b3089fa74be104af
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530524"
---
# <a name="complete-and-partial-media-types"></a><span data-ttu-id="b535c-103">Vollständige und partielle Medientypen</span><span class="sxs-lookup"><span data-stu-id="b535c-103">Complete and Partial Media Types</span></span>

<span data-ttu-id="b535c-104">In diesem Thema wird der Unterschied zwischen vollständigen Medientypen und partiellen Medientypen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b535c-104">This topic describes the difference between complete media types and partial media types.</span></span>

## <a name="complete-media-types"></a><span data-ttu-id="b535c-105">Vervollständigen von Medientypen</span><span class="sxs-lookup"><span data-stu-id="b535c-105">Complete Media Types</span></span>

<span data-ttu-id="b535c-106">Ein *Vollständiger* Medientyp ist eine, die das Format des Mediendaten Stroms vollständig definiert.</span><span class="sxs-lookup"><span data-stu-id="b535c-106">A *complete* media type is one that fully defines the format of the media stream.</span></span> <span data-ttu-id="b535c-107">Bei einem kompletten Medientyp kann eine Pipeline Komponente die dem Medientyp zugeordneten Datenstrom Daten ohne Mehrdeutigkeit analysieren.</span><span class="sxs-lookup"><span data-stu-id="b535c-107">Given a complete media type, a pipeline component can parse the stream data associated with the media type, with no ambiguity.</span></span>

<span data-ttu-id="b535c-108">Für nicht komprimierte Formate definieren die folgenden Themen die Attribute, die für einen kompletten Medientyp erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="b535c-108">For uncompressed formats, the following topics define the attributes that are required for a complete media type:</span></span>

-   <span data-ttu-id="b535c-109">Audiodatei: [nicht komprimierte audiomedientypen](uncompressed-audio-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="b535c-109">Audio: [Uncompressed Audio Media Types](uncompressed-audio-media-types.md)</span></span>
-   <span data-ttu-id="b535c-110">Video: [unkomprimierte Video Medientypen](uncompressed-video-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="b535c-110">Video: [Uncompressed Video Media Types](uncompressed-video-media-types.md)</span></span>

<span data-ttu-id="b535c-111">Bei komprimierten (oder *codierten*) Streams wird die Definition eines gesamten Medientyps durch den Codec definiert.</span><span class="sxs-lookup"><span data-stu-id="b535c-111">For compressed (or *encoded*) streams, the definition of a complete media type is defined by the codec.</span></span> <span data-ttu-id="b535c-112">Wenn jedoch unkomprimierte Typattribute für den komprimierten Datenstrom bekannt sind, sollten diese Werte in den Medientyp für den komprimierten Datenstrom eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="b535c-112">However, if any uncompressed type attributes are known for the compressed stream, these values should be included in the media type for the compressed stream.</span></span> <span data-ttu-id="b535c-113">Wenn z. b. die Frame Größe bekannt ist, legen Sie das Attribut " [**MF \_ MT \_ Frame \_ size**](mf-mt-frame-size-attribute.md) " auf den Medientyp fest, obwohl technisch gesehen ein komprimierter Stream nicht über eine Frame Größe verfügt.</span><span class="sxs-lookup"><span data-stu-id="b535c-113">For example, if the frame size is known, set the [**MF\_MT\_FRAME\_SIZE**](mf-mt-frame-size-attribute.md) attribute on the media type, even though technically a compressed stream does not have a frame size.</span></span>

## <a name="partial-media-types"></a><span data-ttu-id="b535c-114">Partielle Medientypen</span><span class="sxs-lookup"><span data-stu-id="b535c-114">Partial Media Types</span></span>

<span data-ttu-id="b535c-115">Bei einem *partiellen* Medientyp fehlt mindestens eines der für einen vollständigen Medientyp erforderlichen Attribute.</span><span class="sxs-lookup"><span data-stu-id="b535c-115">A *partial* media type is lacks one or more of the attributes needed for a complete media type.</span></span> <span data-ttu-id="b535c-116">Beim Auflisten möglicher Medientypen kann eine Microsoft Media Foundation Komponente einen Wert nicht festlegen, um anzugeben, dass jeder beliebige Wert verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b535c-116">When enumerating possible media types, a Microsoft Media Foundation component may leave a value unset, to indicate that it can handle any value.</span></span> <span data-ttu-id="b535c-117">Beispielsweise kann ein Videoprozessor das Attribut " [**MF \_ MT \_ Frame \_ Rate**](mf-mt-frame-rate-attribute.md) " nicht festlegen, um anzugeben, dass es eine beliebige Framerate verarbeiten kann, und führt ggf. eine Frameraten Konvertierung durch.</span><span class="sxs-lookup"><span data-stu-id="b535c-117">For example, a video processor might leave the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute unset, to indicate that it can handle any frame rate, and will perform a frame-rate conversion if necessary.</span></span>

<span data-ttu-id="b535c-118">Wenn Sie einen partiellen Medientyp erstellen, sollten Sie immer noch so viele Informationen wie Sie wissen einschließen.</span><span class="sxs-lookup"><span data-stu-id="b535c-118">If you create a partial media type, you should still include as much information as you know.</span></span> <span data-ttu-id="b535c-119">Ein Medientyp darf jedoch keine unsicheren Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b535c-119">However, a media type must not include information that is uncertain.</span></span> <span data-ttu-id="b535c-120">Es ist besser, Informationen zu fehlen als falsch.</span><span class="sxs-lookup"><span data-stu-id="b535c-120">It is better for information to be missing than wrong.</span></span>

<span data-ttu-id="b535c-121">Ein partieller Medientyp sollte mindestens zwei Attribute enthalten: " [**MF \_ MT \_ Major \_ Type**](mf-mt-major-type-attribute.md) " und " [**MF \_ MT"- \_ Untertyp**](mf-mt-subtype-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="b535c-121">At a minimum, a partial media type should include just two attributes: [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) and [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md).</span></span>

<span data-ttu-id="b535c-122">In manchen Fällen müssen Media Foundation Komponenten umfassende Medientypen bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="b535c-122">Sometimes Media Foundation components must provide complete media types:</span></span>

-   <span data-ttu-id="b535c-123">Medienquellen müssen komplette Ausgabetypen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b535c-123">Media sources must provide complete output types.</span></span>
-   <span data-ttu-id="b535c-124">Decoders müssen komplette Ausgabetypen bereitstellen, nachdem der Eingabetyp festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="b535c-124">Decoders must provide complete output types, after the input type is set.</span></span> <span data-ttu-id="b535c-125">Bevor der Eingabetyp festgelegt wird, kann ein Decoder einen partiellen Ausgabetyp bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b535c-125">Before the input type is set, a decoder might provide a partial output type.</span></span>
-   <span data-ttu-id="b535c-126">Encoder müssen komplette Eingabetypen bereitstellen, nachdem der Ausgabetyp festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="b535c-126">Encoders must provide complete input types, after the output type is set.</span></span> <span data-ttu-id="b535c-127">Bevor der Ausgabetyp festgelegt wird, kann ein Encoder einen partiellen Eingabetyp bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b535c-127">Before the output type is set, an encoder might provide a partial input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b535c-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b535c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b535c-129">Medientypen</span><span class="sxs-lookup"><span data-stu-id="b535c-129">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



