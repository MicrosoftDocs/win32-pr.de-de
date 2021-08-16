---
description: High Dynamic Range Pixelformate
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: High Dynamic Range Pixelformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a544d2331cc32943e3bc74400e1751111aac69e0a1448103e7651cb51da9353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086913"
---
# <a name="high-dynamic-range-pixel-formats"></a>High Dynamic Range Pixelformate

Codecs sollten Windows WIC-Pixelformate (Imaging Component) verwenden, die den dynamischen Bereich der zugrunde liegenden Sensordaten beibehalten. GUID \_ WICPixelFormat48bppRGB ist ein typisches 16-Bit-Format mit festem Punkt pro Kanal, das verwendet werden kann. Es können auch andere Formate mit höherer Genauigkeit verwendet werden. Microsoft empfiehlt dringend die Unterstützung eines 32-Bit-Gleitkommapixelformats, um die vollständige Unterstützung für die gpu-beschleunigte Renderingpipeline (Windows Presentation Foundation Graphics Processing Unit) zu aktivieren.

Hohe Farbpixelformate: Mit Windows 7 wurden zwei neue WIC-Pixelformate hinzugefügt, um die neuen Anzeigeformate für hohe Farben zu unterstützen. Dies sind: GUID \_ WICPixelFormat32bppRGBA1010102 und GUID \_ WICPixelFormat32bppRGBA1010102XR.

Das Float High Color-Format mit 16 Bit pro Kanal (bpc) wird vom vorhandenen \_ GUID-Format WICPixelFormat64bppRGBAHalf unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC Guidelines for Camera RAW Image Formats](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



