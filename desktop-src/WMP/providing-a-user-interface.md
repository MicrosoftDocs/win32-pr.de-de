---
title: Bereitstellen einer Benutzeroberfläche
description: Bereitstellen einer Benutzeroberfläche
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Windows Media Player-Plug-ins, Eigenschaften Seiten
- Plug-ins, Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Eigenschaften Seiten
- DSP-Plug-ins, Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Benutzeroberfläche
- DSP-Plug-ins, Benutzeroberfläche
- Eigenschaftenseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207167"
---
# <a name="providing-a-user-interface"></a><span data-ttu-id="f3efa-110">Bereitstellen einer Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="f3efa-110">Providing a User Interface</span></span>

<span data-ttu-id="f3efa-111">DSP-Plug-Ins können eine Eigenschaften Seite zum Erstellen einer Benutzeroberfläche bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f3efa-111">DSP plug-ins can provide a property page to create a user interface.</span></span> <span data-ttu-id="f3efa-112">Zu diesem Zweck muss das Plug-in ein Eigenschaften Seiten Objekt enthalten, das eine Implementierung einer **IPropertyPage** -Schnittstelle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f3efa-112">To do this, the plug-in must include a property page object that provides an implementation of an **IPropertyPage** interface.</span></span> <span data-ttu-id="f3efa-113">Das DSP-Plug-in-Objekt muss **ISpecifyPropertyPages:: GetPages** implementieren, das es Windows Media Player ermöglicht, die richtige Eigenschaften Seite für das Plug-in zu finden und zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f3efa-113">The DSP plug-in object must implement **ISpecifyPropertyPages::GetPages**, which allows Windows Media Player to locate and identify the correct property page for the plug-in.</span></span>

<span data-ttu-id="f3efa-114">**Anzeigen einer Status Grafik**</span><span class="sxs-lookup"><span data-stu-id="f3efa-114">**Displaying a Status Graphic**</span></span>

<span data-ttu-id="f3efa-115">DSP-Plug-Ins können im Bereich Windows-Media Player Status eine kleine Grafik oder eine Reihe von Grafiken anzeigen, um den Benutzer darüber zu benachrichtigen, dass ein Plug-in aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="f3efa-115">DSP plug-ins can display a small graphic, or series of graphics, in the Windows Media Player status area to notify the user that a plug-in is active.</span></span> <span data-ttu-id="f3efa-116">Um diese Funktion zu unterstützen, muss das Plug-in die **IPropertyBag** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="f3efa-116">To support this feature, the plug-in must implement the **IPropertyBag** interface.</span></span> <span data-ttu-id="f3efa-117">Windows Media Player ruft **IPropertyBag:: Read** auf und stellt einen Zeiger auf den angeforderten Eigenschaftsnamen "IconStreams" bereit, bei dem die Groß-/Kleinschreibung beachtet wird, und ein Zeiger auf eine **Variant** -Struktur, die die Daten für die Grafik empfängt.</span><span class="sxs-lookup"><span data-stu-id="f3efa-117">Windows Media Player calls **IPropertyBag::Read**, providing a pointer to the requested property name "IconStreams", which is case-sensitive, and a pointer to a **VARIANT** structure that receives the data for the graphic.</span></span> <span data-ttu-id="f3efa-118">Das Plug-in erstellt ein **IStream** -Objekt (oder ein SafeArray von **IStream** -Objekten, wenn mehrere Grafiken vorhanden sind), lädt dann die Grafikdaten, einschließlich Header Informationen, in den Stream und gibt einen Zeiger auf das **IStream** -Objekt mit dem **punkVal** -Member der **Variant** -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="f3efa-118">The plug-in creates an **IStream** object (or a SAFEARRAY of **IStream** objects if there are multiple graphics), then loads the graphic data, including header information, into the stream, and then returns a pointer to the **IStream** object using the **punkVal** member of the **VARIANT** structure.</span></span> <span data-ttu-id="f3efa-119">Wenn das Plug-in nur eine Grafik liefert, wird das **VT** -Element der **Variant** -Struktur als VT \_ Unknown angegeben.</span><span class="sxs-lookup"><span data-stu-id="f3efa-119">If the plug-in supplies only one graphic, it specifies the **vt** member of the **VARIANT** structure as VT\_UNKNOWN.</span></span> <span data-ttu-id="f3efa-120">Wenn das Plug-in mehrere Grafik- **IStream** -Objekte mithilfe von SAFEARRAY bereitstellt, gibt es das **VT** -Element der **Variant** -Struktur als VT- \_ Array an.</span><span class="sxs-lookup"><span data-stu-id="f3efa-120">If the plug-in supplies multiple graphic **IStream** objects using a SAFEARRAY, it specifies the **vt** member of the **VARIANT** structure as VT\_ARRAY.</span></span>

<span data-ttu-id="f3efa-121">Grafiken können in einer Vielzahl von Dateiformaten gespeichert werden, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="f3efa-121">Graphics can be stored in a variety of file formats, including:</span></span>

<span data-ttu-id="f3efa-122">**BMP**</span><span class="sxs-lookup"><span data-stu-id="f3efa-122">**BMP**</span></span>

<span data-ttu-id="f3efa-123">Microsoft Windows-Bitmapbilder sind nicht komprimiert.</span><span class="sxs-lookup"><span data-stu-id="f3efa-123">Microsoft Windows Bitmap images are uncompressed.</span></span>

<span data-ttu-id="f3efa-124">**JPEG**</span><span class="sxs-lookup"><span data-stu-id="f3efa-124">**JPEG**</span></span>

<span data-ttu-id="f3efa-125">Komprimiertes Bildformat, das häufig für Webseiten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3efa-125">Compressed image format commonly used for webpages.</span></span> <span data-ttu-id="f3efa-126">JPEG-Format Dateien haben in der Regel JPG-Dateinamen Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="f3efa-126">JPEG format files usually have .jpg file name extensions.</span></span>

<span data-ttu-id="f3efa-127">**GIF**</span><span class="sxs-lookup"><span data-stu-id="f3efa-127">**GIF**</span></span>

<span data-ttu-id="f3efa-128">Komprimiertes Bildformat, das häufig für Webseiten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3efa-128">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="f3efa-129">**PNG**</span><span class="sxs-lookup"><span data-stu-id="f3efa-129">**PNG**</span></span>

<span data-ttu-id="f3efa-130">Komprimiertes Bildformat, das häufig für Webseiten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3efa-130">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="f3efa-131">Die maximalen Dimensionen für die DSP-Plug-in-Grafiken sind 38 Pixel breit und 14 Pixel hoch.</span><span class="sxs-lookup"><span data-stu-id="f3efa-131">The maximum dimensions for DSP plug-in graphics are 38 pixels wide and 14 pixels high.</span></span>

<span data-ttu-id="f3efa-132">Der **IStream** -Bytestream, der die Status Grafik enthält, muss Header Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f3efa-132">The **IStream** byte stream containing the status graphic must include header information.</span></span> <span data-ttu-id="f3efa-133">Ohne Header Informationen kann Windows Media Player den Typ der Grafik nicht ordnungsgemäß identifizieren und das Bild daher nicht laden.</span><span class="sxs-lookup"><span data-stu-id="f3efa-133">Without header information, Windows Media Player cannot properly identify the type of graphic and therefore will not load the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3efa-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3efa-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3efa-135">**Übersicht über den DSP-Plug-in-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="f3efa-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




