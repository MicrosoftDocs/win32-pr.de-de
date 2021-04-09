---
description: Encoder-und decoderentwicklung
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Encoder-und decoderentwicklung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124555"
---
# <a name="encoder-and-decoder-development"></a><span data-ttu-id="5fb12-103">Encoder-und decoderentwicklung</span><span class="sxs-lookup"><span data-stu-id="5fb12-103">Encoder and Decoder Development</span></span>

<span data-ttu-id="5fb12-104">Dieser Abschnitt enthält Artikel zur Entwicklung von Encodern und Decodern für DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5fb12-104">This section contains articles about encoder and decoder development for DirectShow.</span></span> <span data-ttu-id="5fb12-105">Diese Themen sind für Anwendungsentwickler nicht relevant.</span><span class="sxs-lookup"><span data-stu-id="5fb12-105">These topics are not relevant for application developers.</span></span>

<span data-ttu-id="5fb12-106">Ein Software Decoder, der die DirectX-Video Beschleunigung (VA) unterstützt, muss als DirectShow-Kopier Transformations Filter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="5fb12-106">A software decoder that supports DirectX Video Acceleration (VA) must be implemented as a DirectShow copy transform filter.</span></span> <span data-ttu-id="5fb12-107">Wenn der Decoder DirectX VA nicht unterstützt, kann er auch als DirectX-Medienobjekt (DMO) implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="5fb12-107">If the decoder does not support DirectX VA, it can also be implemented as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="5fb12-108">Ein Decoder, der eine Verbindung mit einem Videorenderer herstellt, sollte nicht als ein transdirektionale Filter implementiert werden, da dies zu einer erheblichen Leistungsminderung führt.</span><span class="sxs-lookup"><span data-stu-id="5fb12-108">A decoder that connects to a video renderer should not be implemented as a trans-in-place filter, because this will result in significant performance degradation.</span></span> <span data-ttu-id="5fb12-109">Informationen zum Schreiben eines Filters für die Kopier Transformation finden Sie unter [Schreiben von Transformations Filtern](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5fb12-109">For information on how to write a copy transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="5fb12-110">Software Encoder können entweder als Transformations Filter oder als DMOS implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="5fb12-110">Software encoders can be implemented as either transform filters or DMOs.</span></span> <span data-ttu-id="5fb12-111">Encoder verwenden nicht DirectX VA, da DirectX VA derzeit nur für die Komprimierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5fb12-111">Encoders do not use DirectX VA, since DirectX VA currently is only used for decompression.</span></span> <span data-ttu-id="5fb12-112">Die in diesem Abschnitt beschriebene Encoder-API-Spezifikation ist für Hardware-und Software Encoder relevant.</span><span class="sxs-lookup"><span data-stu-id="5fb12-112">The Encoder API specification described in this section is relevant for both hardware and software encoders.</span></span>

<span data-ttu-id="5fb12-113">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="5fb12-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="5fb12-114">Encoder-API</span><span class="sxs-lookup"><span data-stu-id="5fb12-114">Encoder API</span></span>](encoder-api.md)
-   [<span data-ttu-id="5fb12-115">Decoder-Schnittstellen und Spezifikationen</span><span class="sxs-lookup"><span data-stu-id="5fb12-115">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
-   [<span data-ttu-id="5fb12-116">Decodereinstellungen für Windows Media Center Edition</span><span class="sxs-lookup"><span data-stu-id="5fb12-116">Decoder Settings for Windows Media Center Edition</span></span>](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a><span data-ttu-id="5fb12-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5fb12-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fb12-118">Verwenden von VMR für DirectShow-Filter Entwickler</span><span class="sxs-lookup"><span data-stu-id="5fb12-118">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



