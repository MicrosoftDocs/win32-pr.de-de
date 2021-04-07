---
description: Implementieren von IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Implementieren von IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88e2f7dfd073405f9de8c82b2ce6d9592b241a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758299"
---
# <a name="implementing-iwicbitmapsource"></a><span data-ttu-id="254ab-103">Implementieren von IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="254ab-103">Implementing IWICBitmapSource</span></span>

## <a name="iwicbitmapsource"></a><span data-ttu-id="254ab-104">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="254ab-104">IWICBitmapSource</span></span>

<span data-ttu-id="254ab-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) ist wichtig für das Arbeiten mit Bildern aus Anwendungs Sicht.</span><span class="sxs-lookup"><span data-stu-id="254ab-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) is important for working with images from an application perspective.</span></span> <span data-ttu-id="254ab-106">Es stellt die Abstraktion der höchsten Ebene für eine Bildquelle dar. alle Windows Imaging Component-Schnittstellen (WIC), die ein Bild darstellen, einschließlich [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)und alle Transformations Schnittstellen ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)und [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)), werden davon abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="254ab-106">It represents the highest level abstraction for an image source, and all Windows Imaging Component (WIC) interfaces that represent an image, including [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), and all the transform interfaces ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) are derived from it.</span></span> <span data-ttu-id="254ab-107">Ein **IWICBitmapSource** -Objekt kann zu einem bestimmten Zeitpunkt von einer tatsächlichen Bitmap im Arbeitsspeicher unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="254ab-107">At any specific time, an **IWICBitmapSource** object may or may not be backed by an actual bitmap in memory.</span></span> <span data-ttu-id="254ab-108">Dies ermöglicht eine sehr effiziente Verarbeitung durch eine Anwendung, da ein Bild als Abstraktion behandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="254ab-108">This enables very efficient processing by an application, because an image can be dealt with as an abstraction.</span></span> <span data-ttu-id="254ab-109">Transformations Vorgänge können in einer Transformations Pipeline verkettet werden, ohne Arbeitsspeicher Ressourcen zu beanspruchen, bis die Anwendung zum Renderingvorgang oder Drucken des Bilds bereit ist. zu diesem Zeitpunkt wird die [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) -Methode für die endgültige Transformation aufgerufen, um mit den ausgewählten Transformationen eine Bitmap im Speicher des Bilds zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="254ab-109">Transform operations can be chained in a transform pipeline without consuming memory resources until the application is ready to render or print the image, at which time it invokes the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the final transform to get a bitmap in memory of the image with the selected transforms applied.</span></span>

``` syntax
interface IWICBitmapSource : IUnknown
{
   // Required methods
   HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
   HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
   HRESULT GetResolution ( double *pDpiX, double *pDpiY );
   HRESULT CopyPixels ( const WICRect *prc,
      UINT cbStride,
      UINT cbBufferSize, 
      BYTE *pbBuffer );
   // Optional method
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

<span data-ttu-id="254ab-110">Aus Codec-Sicht werden die [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Methoden auf dem Frame-Decoderobjekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="254ab-110">From a codec perspective, the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) methods are implemented on the frame decoder object.</span></span> <span data-ttu-id="254ab-111">Diese Methoden werden unter Implementieren von IWICBitmapSource und den anderen Methoden in [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)beschrieben, die von **IWICBitmapSource** abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="254ab-111">These methods are described in Implementing IWICBitmapSource, along with the other methods on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), which is derived from **IWICBitmapSource**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="254ab-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="254ab-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="254ab-113">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="254ab-113">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="254ab-114">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="254ab-114">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="254ab-115">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="254ab-115">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="254ab-116">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="254ab-116">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="254ab-117">**Licher**</span><span class="sxs-lookup"><span data-stu-id="254ab-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="254ab-118">Implementieren von IWICBitmapCodecProgressNotification (Decoder)</span><span class="sxs-lookup"><span data-stu-id="254ab-118">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="254ab-119">Implementieren von IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="254ab-119">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="254ab-120">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="254ab-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="254ab-121">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="254ab-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



