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
# <a name="implementing-iwicbitmapcodecprogressnotification-encoder"></a>Implementieren von IWICBitmapCodecProgressNotification (Encoder)

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

Obwohl die [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) -Schnittstelle optional ist, wird empfohlen, dass Sie für die Encoder-Klasse auf Container Ebene implementiert wird. Diese Schnittstelle wird in der Implementierung von [IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)ausführlicher erläutert. Die Implementierung ist für den Decoder und den Encoder identisch.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Implementieren von iwicbitmapcoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Implementieren von iwicbitmapframecocode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Implementieren von IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> </dl>

 

 



