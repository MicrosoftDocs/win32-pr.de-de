---
description: Miniaturansichten und Vorschau
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Miniaturansichten und Vorschau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e279da9771a43eb75bb94faff23d2e6aa29c4ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360721"
---
# <a name="thumbnails-and-previews"></a><span data-ttu-id="ce7c5-103">Miniaturansichten und Vorschau</span><span class="sxs-lookup"><span data-stu-id="ce7c5-103">Thumbnails and Previews</span></span>

<span data-ttu-id="ce7c5-104">Windows Vista und die Windows-Fotogalerie basieren auf Windows Imaging Component (WIC), um schnelle Miniaturansichten und Vorschau Versionen von Bildern zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="ce7c5-104">Windows Vista and the Windows Photo Gallery rely on Windows Imaging Component (WIC) to render fast thumbnails and previews of images.</span></span> <span data-ttu-id="ce7c5-105">Um schnelles Miniaturansichten-und Vorschau Rendering zu unterstützen, müssen unformatierte Codecs die WIC-Schnittstellen [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) und [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) implementieren.</span><span class="sxs-lookup"><span data-stu-id="ce7c5-105">To support fast thumbnail and preview rendering, RAW codecs must implement the WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) and [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) interfaces.</span></span> <span data-ttu-id="ce7c5-106">Um eine reaktionsfähige Benutzeroberfläche zu unterstützen, ist es sehr wünschenswert, dass diese Schnittstellen eine [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) in 200 Millisekunden oder weniger an den Aufrufer zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ce7c5-106">To support a responsive user experience, it is highly desirable that these interfaces return an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to the caller in 200 milliseconds or less.</span></span>

<span data-ttu-id="ce7c5-107">Microsoft empfiehlt dringend, dass Besitzer von rohdatendateiformaten eine Vorschauversion generieren und in der Bilddatei Zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="ce7c5-107">Microsoft strongly recommends that RAW file format owners generate a prerendered preview and cache this in the image file.</span></span> <span data-ttu-id="ce7c5-108">Bei einem in-Device-Format erfolgt dies in der Regel zur Erfassungs Zeit.</span><span class="sxs-lookup"><span data-stu-id="ce7c5-108">For an in-device format, this is usually done at capture time.</span></span> <span data-ttu-id="ce7c5-109">Vorschau Versionen können jedoch auch neu generiert und in der Bilddatei gespeichert werden, wenn die Eigenschaften der [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Schnittstelle geändert werden. Dies ist nicht zu viel Arbeit.</span><span class="sxs-lookup"><span data-stu-id="ce7c5-109">However, previews could also be regenerated and stored in the image file whenever [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface properties are changed-if it does not take too much work to do so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce7c5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce7c5-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ce7c5-111">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ce7c5-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ce7c5-112">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="ce7c5-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="ce7c5-113">WIC-Richtlinien für Kamera Rohbild Formate</span><span class="sxs-lookup"><span data-stu-id="ce7c5-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="ce7c5-114">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="ce7c5-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



