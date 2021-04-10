---
description: Implementieren von IWICBitmapCodecProgressNotification (Encoder)
ms.assetid: d470ec93-d329-48c0-9556-0c15daece491
title: Implementieren von IWICBitmapCodecProgressNotification (Encoder)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260fac41068de0695813d569881e4a71938eb83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867336"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-encoder"></a><span data-ttu-id="39690-103">Implementieren von IWICBitmapCodecProgressNotification (Encoder)</span><span class="sxs-lookup"><span data-stu-id="39690-103">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="39690-104">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="39690-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="39690-105">Obwohl die [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) -Schnittstelle optional ist, wird empfohlen, dass Sie für die Encoder-Klasse auf Container Ebene implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="39690-105">Although the [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) interface is optional, it is recommended that it be implemented on the container-level encoder class.</span></span> <span data-ttu-id="39690-106">Diese Schnittstelle wird in der Implementierung von [IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)ausführlicher erläutert.</span><span class="sxs-lookup"><span data-stu-id="39690-106">This interface is discussed in more details in [Implementing IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md).</span></span> <span data-ttu-id="39690-107">Die Implementierung ist für den Decoder und den Encoder identisch.</span><span class="sxs-lookup"><span data-stu-id="39690-107">The implementation is the same for either the decoder and the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39690-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39690-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="39690-109">**Licher**</span><span class="sxs-lookup"><span data-stu-id="39690-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="39690-110">Implementieren von iwicbitmapcoder</span><span class="sxs-lookup"><span data-stu-id="39690-110">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="39690-111">Implementieren von iwicbitmapframecocode</span><span class="sxs-lookup"><span data-stu-id="39690-111">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="39690-112">Schreiben eines WIC-Enabled Codecs</span><span class="sxs-lookup"><span data-stu-id="39690-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="39690-113">Übersicht über die Windows Imaging-Komponente</span><span class="sxs-lookup"><span data-stu-id="39690-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="39690-114">Implementieren von IWICBitmapCodecProgressNotification (Decoder)</span><span class="sxs-lookup"><span data-stu-id="39690-114">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> </dl>

 

 



