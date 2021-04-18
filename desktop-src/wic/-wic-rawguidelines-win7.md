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
# <a name="raw-codec-requirements-for-windows-7"></a>Unformatierte Codec-Anforderungen für Windows 7

Die folgenden Codec-Features sind mindestens erforderlich:

Alle Funktionen, die für die Unterstützung der Windows Vista-Shell und der Fotogalerie erforderlich sind: Miniaturansicht, Vorschau und (persistent) Drehung. Die Rohverarbeitung sollte standardmäßig geeignete as-shot-Einstellungen sein.

Die Unterstützung von Kernmetadaten (sowohl Lese-als auch Schreibvorgänge), nicht-EXIF-Metadaten und EXIF-Metadaten sollten in unformatierten Dateiformaten beibehalten werden, ohne dass Sidecar-Dateien verwendet werden.

Unterstützung für die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) -Schnittstelle. Für Windows 7 erfordert Windows Imaging Component (WIC) WIC, dass alle von [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) verfügbar gemachten Parameter Schnittstellen implementiert werden.

Unterstützung für den Orientierungs Status:

-   90-Abbild Drehungen sollten mithilfe der [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**abtrotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) -Methode angewendet werden. Anwendungen und Windows verwenden diese Methode, um die Bilder (und zwischengespeicherte Miniaturansichten und Vorschau Versionen) zu drehen.
-   Die Anwendung der Rotation mithilfe dieser API sollte auch vom Codec persistent gespeichert werden (siehe weiter oben in diesem Dokument).
-   Anwendungen können die rotationsfunktionen der [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) -API verwenden, aber der Codec serialisiert keine Rotations Einstellungen für diese API, sodass mit [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) durchgeführte Drehungen nicht persistent gespeichert werden.

Unterstützung für hoch Geschwindigkeits-und Vorschau Extraktion. Wenn die maximale Pixel Dimensions Vorschau (Breite oder Höhe) kleiner als 1024 Pixel ist, fordert Windows Vista ein Rendering für die Bildschirm Vorschau an:

-   Die [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**strendermode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) -Methode sollte mindestens den [**wicrawrenderqualitydraftmode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) -und den [**wicrawrenderqualitybestquality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) -Modus unterstützen, um ein schnelleres Rendering von Miniaturansichten und Vorschau Versionen zu ermöglichen, als der Modus für hohe Qualität.
-   Windows ruft [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) mit der angeforderten Bildschirm auflösungsgröße auf.
-   Die Größen der Bildschirmauflösung müssen in der obigen API unterstützt werden.
-   Die konsistente Bildverarbeitung von Miniaturansichten, Vorschau-und Vollbild-Bits aus [**copypixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) ist erforderlich.

Pixel Formate mit hohem dynamischen Bereich (HDR).

XML Paper Specification (XPS)-Druck.

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

 

 



