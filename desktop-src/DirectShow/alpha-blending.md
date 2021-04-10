---
description: Alpha Blending
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: Alpha Blending (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4293448849926cfc6723495619137262e004636e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125209"
---
# <a name="alpha-blending-directshow"></a><span data-ttu-id="98bc5-103">Alpha Blending (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="98bc5-103">Alpha Blending (DirectShow)</span></span>

<span data-ttu-id="98bc5-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="98bc5-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="98bc5-105">In diesem Artikel wird die Alpha Mischung in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="98bc5-105">This article describes alpha blending in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="98bc5-106">Alpha misst die Transparenz eines Pixels oder Bilds.</span><span class="sxs-lookup"><span data-stu-id="98bc5-106">Alpha measures the transparency of a pixel or image.</span></span> <span data-ttu-id="98bc5-107">Bei einem nicht komprimierten RGB-Video mit 32-Bit definieren vier Komponenten die einzelnen Pixel: einen Alphakanal (A) und drei Farbkomponenten (RGB).</span><span class="sxs-lookup"><span data-stu-id="98bc5-107">In 32-bit uncompressed RGB video, four components define each pixel: an alpha channel (A) and three color components (RGB).</span></span> <span data-ttu-id="98bc5-108">Ein Pixel mit einem Alphawert von 0 (null) ist vollständig transparent.</span><span class="sxs-lookup"><span data-stu-id="98bc5-108">A pixel with an alpha value of zero is completely transparent.</span></span> <span data-ttu-id="98bc5-109">Ein Pixel mit einem Alphawert von 255 ist nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="98bc5-109">A pixel with an alpha value of 255 is opaque.</span></span> <span data-ttu-id="98bc5-110">Zwischen diesen Werten hat das Pixel verschiedene Transparenz Grade.</span><span class="sxs-lookup"><span data-stu-id="98bc5-110">Between these values, the pixel has various degrees of transparency.</span></span>

<span data-ttu-id="98bc5-111">DirectShow definiert zwei Medientypen für 32-Bit-RGB-Video:</span><span class="sxs-lookup"><span data-stu-id="98bc5-111">DirectShow defines two media types for 32-bit RGB video:</span></span>

-   <span data-ttu-id="98bc5-112">**Mediasubtype \_ ARGB32**: das Video ist 32-Bit-RGB mit einem gültigen Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="98bc5-112">**MEDIASUBTYPE\_ARGB32**: The video is 32-bit RGB with a valid alpha channel.</span></span>
-   <span data-ttu-id="98bc5-113">**Mediasubtype \_ RGB32**: Pixel sind 32 Bits, aber der Alphakanal ist nicht unbedingt gültig.</span><span class="sxs-lookup"><span data-stu-id="98bc5-113">**MEDIASUBTYPE\_RGB32**: Pixels are 32 bits, but the alpha channel is not necessarily valid.</span></span>

<span data-ttu-id="98bc5-114">Legen Sie zum Durchführen einer Alpha Mischung in des den unkomprimierten Medientyp der Videogruppe auf mediasubtype \_ ARGB32 fest.</span><span class="sxs-lookup"><span data-stu-id="98bc5-114">To perform alpha blending in DES, set the video group's uncompressed media type to MEDIASUBTYPE\_ARGB32.</span></span> <span data-ttu-id="98bc5-115">Aufrufen Sie in C++ die [**iamtimelinegroup:: setmediatype**](iamtimelinegroup-setmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="98bc5-115">In C++, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span> <span data-ttu-id="98bc5-116">Im XTL-Format wird dies auch durch Festlegen des [**Bittiefen**](bitdepth-attribute.md) Attributs des [**Group**](group-element.md) -Elements auf 32 erreicht.</span><span class="sxs-lookup"><span data-stu-id="98bc5-116">In the XTL format, setting the [**bitdepth**](bitdepth-attribute.md) attribute of the [**group**](group-element.md) element to 32 accomplishes this as well.</span></span>

<span data-ttu-id="98bc5-117">Als nächstes benötigen Sie Videodaten, die einen Alphakanal enthalten.</span><span class="sxs-lookup"><span data-stu-id="98bc5-117">Next, you need video data that contains an alpha channel.</span></span> <span data-ttu-id="98bc5-118">Es gibt mehrere Optionen:</span><span class="sxs-lookup"><span data-stu-id="98bc5-118">There are several options:</span></span>

-   <span data-ttu-id="98bc5-119">Sie können eine AVI-Datei verwenden, die bereits über ein 32-Bit-RGB-Video mit Alpha Daten verfügt.</span><span class="sxs-lookup"><span data-stu-id="98bc5-119">You can use an AVI file that already has 32-bit RGB video with alpha data.</span></span> <span data-ttu-id="98bc5-120">Derzeit wird Alpha nicht für MPEG-oder Microsoft Windows Media Format-Quelldateien (WMF) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98bc5-120">Currently, alpha is not supported for MPEG or Microsoft Windows Media Format (WMF) source files.</span></span>
-   <span data-ttu-id="98bc5-121">DES unterstützt 32-Bit-Bitmap-Dateien (BMP) und Targa-Dateien (. TGA) mit Alpha-Daten.</span><span class="sxs-lookup"><span data-stu-id="98bc5-121">DES supports 32-bit bitmap (.bmp) and Targa (.tga) files with alpha data.</span></span>
-   <span data-ttu-id="98bc5-122">Sie können einen benutzerdefinierten Quell Filter schreiben, mit dem 32-Bit-RGB-Daten mit Alpha erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="98bc5-122">You can write a custom source filter that creates 32-bit RGB data with alpha.</span></span> <span data-ttu-id="98bc5-123">Der Typ des Ausgabe Mediums muss **mediasubtype \_ ARGB32** sein.</span><span class="sxs-lookup"><span data-stu-id="98bc5-123">The output media type must be **MEDIASUBTYPE\_ARGB32**.</span></span> <span data-ttu-id="98bc5-124">Verwenden Sie den Filter als untergeordnetes Objekt in einem Zeitachsen-Quell Objekt.</span><span class="sxs-lookup"><span data-stu-id="98bc5-124">Use the filter as the subobject in a timeline source object.</span></span>

<span data-ttu-id="98bc5-125">Wenn die Videoquelle nicht alpha ist, können Sie einen Effekt verwenden, mit dem Alpha Daten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="98bc5-125">If your video source does not have alpha, you can use an effect that creates alpha data.</span></span> <span data-ttu-id="98bc5-126">Der [Alpha Setter-Effekt](alpha-setter-effect.md) legt den Alphakanal für das gesamte Bild auf einen konstanten Wert fest.</span><span class="sxs-lookup"><span data-stu-id="98bc5-126">The [Alpha Setter Effect](alpha-setter-effect.md) sets the alpha channel for the entire image to a constant value.</span></span> <span data-ttu-id="98bc5-127">Um das Alpha im zeitlichen Verlauf zu verändern, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle mit dem Alpha Setter-Effekt.</span><span class="sxs-lookup"><span data-stu-id="98bc5-127">To vary the alpha over time, use the [**IPropertySetter**](ipropertysetter.md) interface with the Alpha Setter Effect.</span></span> <span data-ttu-id="98bc5-128">Die ursprüngliche Quelle muss nicht 32 Bit betragen, solange der nicht komprimierte Medientyp der Gruppe **mediasubtype \_ ARGB32** ist.</span><span class="sxs-lookup"><span data-stu-id="98bc5-128">The original source does not have to be 32 bits, as long as the group's uncompressed media type is **MEDIASUBTYPE\_ARGB32**.</span></span>

<span data-ttu-id="98bc5-129">Übergeben Sie schließlich das Video an einen Effekt oder Übergang, der Alpha Blending durchführt.</span><span class="sxs-lookup"><span data-stu-id="98bc5-129">Finally, pass the video to an effect or transition that performs alpha blending.</span></span> <span data-ttu-id="98bc5-130">Der [compositorübergang](compositor-transition.md) führt Alpha Blending aus, und der [Schlüssel Übergang](key-transition.md) kann durch einen Alpha-Wert Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="98bc5-130">The [Compositor Transition](compositor-transition.md) performs alpha blending, and the [Key Transition](key-transition.md) can key by alpha value.</span></span>

<span data-ttu-id="98bc5-131">Im folgenden XTL-Beispiel Projekt wird Alpha Blending durchführt:</span><span class="sxs-lookup"><span data-stu-id="98bc5-131">The following sample XTL project performs alpha blending:</span></span>


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a><span data-ttu-id="98bc5-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98bc5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98bc5-133">Verwenden von DirectShow-Bearbeitungs Diensten</span><span class="sxs-lookup"><span data-stu-id="98bc5-133">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



