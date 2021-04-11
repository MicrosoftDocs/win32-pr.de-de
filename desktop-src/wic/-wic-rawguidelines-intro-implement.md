---
description: Allgemeine Richtlinien für die Implementierung von rohcodecs
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Allgemeine Richtlinien für die Implementierung von rohcodecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217374"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a>Allgemeine Richtlinien für die Implementierung von rohcodecs

Im Vergleich zu nicht unformatierten Bild Typen wie JPEG oder TIFF gibt es zwei wichtige Unterschiede in Bezug darauf, wie sich Rohbild Formate in Windows Verhalten:

-   Die meisten Rohbild Formate werden als "schreibgeschützt" angesehen und unterstützen die Pixel Codierung wahrscheinlich nicht in RAW-Format. Da Windows Imaging Component (WIC) jedoch erfordert, dass ein Encoder das Zurückschreiben von Metadaten unterstützt, sollten unformatierte Codec-Autoren mindestens eine Skeleton Encoder-Klasse implementieren.
-   Das Decodieren eines rohimages voller Größe kann im Vergleich zu anderen Formaten sehr lange dauern. Aus diesem Grund empfiehlt Microsoft, bestimmte Ansätze zu beachten, um die Decodierungs Latenz zu minimieren und die Unterstützung für Szenarien wie das schnelle Rendering von Miniaturansichten und Vorschau Versionen zu gewährleisten.

    So müssen z. b. alle unformatierten Codec-Autoren die [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) -Schnittstelle implementieren, die einen Mechanismus bereitstellt, mit dem der Decoder vor der zielbitmapgröße benachrichtigt wird, sodass die optimierte Decodierung für eine kleinere Ausgabe Bildgröße aktiviert werden kann.

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

 

 



