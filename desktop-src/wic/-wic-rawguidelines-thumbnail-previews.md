---
description: Miniaturansichten und Vorschauen
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Miniaturansichten und Vorschauen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 110b0f4da08eaf2b17582dabec1ff7bd6d4f3ab4389c6bcf7654cdb5ca3198a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086883"
---
# <a name="thumbnails-and-previews"></a>Miniaturansichten und Vorschauen

Windows Vista und die Windows Fotogalerie basieren auf Windows Imaging Component (WIC), um schnelle Miniaturansichten und Vorschauen von Bildern zu rendern. Um schnelles Miniaturansichts- und Vorschaurendering zu unterstützen, müssen RAW-Codecs die WIC-Schnittstellen [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) und [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) implementieren. Um eine reaktionsfähige Benutzererfahrung zu unterstützen, ist es äußerst wünschenswert, dass diese Schnittstellen in 200 Millisekunden oder weniger [**eine IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) an den Aufrufer zurückgeben.

Microsoft empfiehlt dringend, dass Besitzer des RAW-Dateiformats eine vorab geenderte Vorschau generieren und diese in der Bilddatei zwischenspeichern. Bei einem gerätespezifischen Format erfolgt dies in der Regel zum Zeitpunkt der Erfassung. Vorschauversionen können jedoch auch neu generiert und in der Imagedatei gespeichert werden, wenn die Eigenschaften der [**IWICDevelopRaw-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) geändert werden, wenn dafür nicht zu viel Arbeit erforderlich ist.

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

 

 



