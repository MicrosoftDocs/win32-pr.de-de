---
description: Allgemeine Richtlinien für die Implementierung von rohcodecs
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Allgemeine Richtlinien für die Implementierung von rohcodecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217374"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a><span data-ttu-id="7f04e-103">Allgemeine Richtlinien für die Implementierung von rohcodecs</span><span class="sxs-lookup"><span data-stu-id="7f04e-103">General Guidelines for Implementing RAW Codecs</span></span>

<span data-ttu-id="7f04e-104">Im Vergleich zu nicht unformatierten Bild Typen wie JPEG oder TIFF gibt es zwei wichtige Unterschiede in Bezug darauf, wie sich Rohbild Formate in Windows Verhalten:</span><span class="sxs-lookup"><span data-stu-id="7f04e-104">Compared to non-RAW image types such as JPEG or TIFF, there are two notable differences in how RAW image formats are expected to behave in Windows:</span></span>

-   <span data-ttu-id="7f04e-105">Die meisten Rohbild Formate werden als "schreibgeschützt" angesehen und unterstützen die Pixel Codierung wahrscheinlich nicht in RAW-Format.</span><span class="sxs-lookup"><span data-stu-id="7f04e-105">Most RAW image formats are presumed to be "read only" and probably will not support pixel encoding to RAW format.</span></span> <span data-ttu-id="7f04e-106">Da Windows Imaging Component (WIC) jedoch erfordert, dass ein Encoder das Zurückschreiben von Metadaten unterstützt, sollten unformatierte Codec-Autoren mindestens eine Skeleton Encoder-Klasse implementieren.</span><span class="sxs-lookup"><span data-stu-id="7f04e-106">However, because Windows Imaging Component (WIC) requires an encoder to support metadata write-back, RAW codec authors should plan to implement at least a skeleton encoder class.</span></span>
-   <span data-ttu-id="7f04e-107">Das Decodieren eines rohimages voller Größe kann im Vergleich zu anderen Formaten sehr lange dauern.</span><span class="sxs-lookup"><span data-stu-id="7f04e-107">Decoding a full-size RAW image can take a long time compared to other formats.</span></span> <span data-ttu-id="7f04e-108">Aus diesem Grund empfiehlt Microsoft, bestimmte Ansätze zu beachten, um die Decodierungs Latenz zu minimieren und die Unterstützung für Szenarien wie das schnelle Rendering von Miniaturansichten und Vorschau Versionen zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="7f04e-108">For this reason, Microsoft recommends that certain approaches be taken to minimize decoding latency and to ensure support for scenarios such as rapid rendering of thumbnails and previews.</span></span>

    <span data-ttu-id="7f04e-109">So müssen z. b. alle unformatierten Codec-Autoren die [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) -Schnittstelle implementieren, die einen Mechanismus bereitstellt, mit dem der Decoder vor der zielbitmapgröße benachrichtigt wird, sodass die optimierte Decodierung für eine kleinere Ausgabe Bildgröße aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f04e-109">For example, all RAW codec authors must implement the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface, which provides a mechanism to notify the decoder in advance of the target bitmap size, thus enabling optimized decoding to a smaller output image size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f04e-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f04e-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7f04e-111">**Licher**</span><span class="sxs-lookup"><span data-stu-id="7f04e-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7f04e-112">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="7f04e-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="7f04e-113">WIC-Richtlinien für Kamera Rohbild Formate</span><span class="sxs-lookup"><span data-stu-id="7f04e-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="7f04e-114">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="7f04e-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



