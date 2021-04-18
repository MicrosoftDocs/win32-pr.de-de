---
description: Unformatierte Codec-Anforderungen für Windows 7
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Unformatierte Codec-Anforderungen für Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347677"
---
# <a name="raw-codec-requirements-for-windows-7"></a><span data-ttu-id="bd14e-103">Unformatierte Codec-Anforderungen für Windows 7</span><span class="sxs-lookup"><span data-stu-id="bd14e-103">RAW Codec Requirements for Windows 7</span></span>

<span data-ttu-id="bd14e-104">Die folgenden Codec-Features sind mindestens erforderlich:</span><span class="sxs-lookup"><span data-stu-id="bd14e-104">The following codec features are required at a minimum:</span></span>

<span data-ttu-id="bd14e-105">Alle Funktionen, die für die Unterstützung der Windows Vista-Shell und der Fotogalerie erforderlich sind: Miniaturansicht, Vorschau und (persistent) Drehung.</span><span class="sxs-lookup"><span data-stu-id="bd14e-105">All functionality that is required for Windows Vista shell and Photo Gallery support: thumbnail, preview, and (persisted) rotation.</span></span> <span data-ttu-id="bd14e-106">Die Rohverarbeitung sollte standardmäßig geeignete as-shot-Einstellungen sein.</span><span class="sxs-lookup"><span data-stu-id="bd14e-106">RAW processing should default to appropriate as-shot settings.</span></span>

<span data-ttu-id="bd14e-107">Die Unterstützung von Kernmetadaten (sowohl Lese-als auch Schreibvorgänge), nicht-EXIF-Metadaten und EXIF-Metadaten sollten in unformatierten Dateiformaten beibehalten werden, ohne dass Sidecar-Dateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd14e-107">Support for core metadata (both read and write), Non-EXIF metadata, as well as EXIF metadata, should be persisted inside RAW file formats without use of sidecar files.</span></span>

<span data-ttu-id="bd14e-108">Unterstützung für die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bd14e-108">Support for the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="bd14e-109">Für Windows 7 erfordert Windows Imaging Component (WIC) WIC, dass alle von [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) verfügbar gemachten Parameter Schnittstellen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="bd14e-109">For Windows 7, Windows Imaging Component (WIC)WIC requires that all parameter interfaces exposed by [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) be implemented.</span></span>

<span data-ttu-id="bd14e-110">Unterstützung für den Orientierungs Status:</span><span class="sxs-lookup"><span data-stu-id="bd14e-110">Orientation state support:</span></span>

-   <span data-ttu-id="bd14e-111">90-Abbild Drehungen sollten mithilfe der [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**abtrotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) -Methode angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd14e-111">90 degree-step Image rotations should be applied by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) method.</span></span> <span data-ttu-id="bd14e-112">Anwendungen und Windows verwenden diese Methode, um die Bilder (und zwischengespeicherte Miniaturansichten und Vorschau Versionen) zu drehen.</span><span class="sxs-lookup"><span data-stu-id="bd14e-112">Applications and Windows use this method to rotate the images (and cached thumbnails and previews).</span></span>
-   <span data-ttu-id="bd14e-113">Die Anwendung der Rotation mithilfe dieser API sollte auch vom Codec persistent gespeichert werden (siehe weiter oben in diesem Dokument).</span><span class="sxs-lookup"><span data-stu-id="bd14e-113">Application of rotation by using this API should also be persisted by the codec (see earlier in this paper).</span></span>
-   <span data-ttu-id="bd14e-114">Anwendungen können die rotationsfunktionen der [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) -API verwenden, aber der Codec serialisiert keine Rotations Einstellungen für diese API, sodass mit [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) durchgeführte Drehungen nicht persistent gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="bd14e-114">Applications can use the rotation capabilities of the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) API, but the codec will not serialize any rotation settings on this API, so rotations done using [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) will not be persisted.</span></span>

<span data-ttu-id="bd14e-115">Unterstützung für hoch Geschwindigkeits-und Vorschau Extraktion.</span><span class="sxs-lookup"><span data-stu-id="bd14e-115">High-speed thumbnail and preview extraction support.</span></span> <span data-ttu-id="bd14e-116">Wenn die maximale Pixel Dimensions Vorschau (Breite oder Höhe) kleiner als 1024 Pixel ist, fordert Windows Vista ein Rendering für die Bildschirm Vorschau an:</span><span class="sxs-lookup"><span data-stu-id="bd14e-116">If the preview maximum pixel dimension (width or height) is less than 1024 pixels in size, Windows Vista will request a render for screen preview:</span></span>

-   <span data-ttu-id="bd14e-117">Die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**strendermode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) -Methode sollte mindestens den [**wicrawrenderqualitydraftmode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) -und den [**wicrawrenderqualitybestquality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) -Modus unterstützen, um ein schnelleres Rendering von Miniaturansichten und Vorschau Versionen zu ermöglichen, als der Modus für hohe Qualität.</span><span class="sxs-lookup"><span data-stu-id="bd14e-117">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) method should support at least the [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) and [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) modes to allow faster rendering of thumbnails and previews than the full-quality mode.</span></span>
-   <span data-ttu-id="bd14e-118">Windows ruft [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) mit der angeforderten Bildschirm auflösungsgröße auf.</span><span class="sxs-lookup"><span data-stu-id="bd14e-118">Windows will call [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the requested screen resolution size.</span></span>
-   <span data-ttu-id="bd14e-119">Die Größen der Bildschirmauflösung müssen in der obigen API unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="bd14e-119">Screen resolution sizes must be supported in the above API.</span></span>
-   <span data-ttu-id="bd14e-120">Die konsistente Bildverarbeitung von Miniaturansichten, Vorschau-und Vollbild-Bits aus [**copypixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bd14e-120">Consistent image processing of thumbnail, preview, and full-image bits from [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) is required.</span></span>

<span data-ttu-id="bd14e-121">Pixel Formate mit hohem dynamischen Bereich (HDR).</span><span class="sxs-lookup"><span data-stu-id="bd14e-121">High dynamic range (HDR) pixel formats.</span></span>

<span data-ttu-id="bd14e-122">XML Paper Specification (XPS)-Druck.</span><span class="sxs-lookup"><span data-stu-id="bd14e-122">XML Paper Specification (XPS) printing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd14e-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bd14e-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bd14e-124">**Licher**</span><span class="sxs-lookup"><span data-stu-id="bd14e-124">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bd14e-125">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="bd14e-125">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="bd14e-126">WIC-Richtlinien für Kamera Rohbild Formate</span><span class="sxs-lookup"><span data-stu-id="bd14e-126">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="bd14e-127">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="bd14e-127">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



