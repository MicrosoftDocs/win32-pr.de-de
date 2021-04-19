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
# <a name="thumbnails-and-previews"></a>Miniaturansichten und Vorschau

Windows Vista und die Windows-Fotogalerie basieren auf Windows Imaging Component (WIC), um schnelle Miniaturansichten und Vorschau Versionen von Bildern zu erzeugen. Um schnelles Miniaturansichten-und Vorschau Rendering zu unterstützen, müssen unformatierte Codecs die WIC-Schnittstellen [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) und [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) implementieren. Um eine reaktionsfähige Benutzeroberfläche zu unterstützen, ist es sehr wünschenswert, dass diese Schnittstellen eine [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) in 200 Millisekunden oder weniger an den Aufrufer zurückgeben.

Microsoft empfiehlt dringend, dass Besitzer von rohdatendateiformaten eine Vorschauversion generieren und in der Bilddatei Zwischenspeichern. Bei einem in-Device-Format erfolgt dies in der Regel zur Erfassungs Zeit. Vorschau Versionen können jedoch auch neu generiert und in der Bilddatei gespeichert werden, wenn die Eigenschaften der [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Schnittstelle geändert werden. Dies ist nicht zu viel Arbeit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC-Richtlinien für Kamera Rohbild Formate](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



