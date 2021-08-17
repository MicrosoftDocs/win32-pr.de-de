---
description: Allgemeine Richtlinien für die Implementierung von RAW-Codecs
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Allgemeine Richtlinien für die Implementierung von RAW-Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5081edfc6f49dc1d145fc3e2ce7e5f993fb2e7e250aeb0f1091579dd3f45461
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204628"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a>Allgemeine Richtlinien für die Implementierung von RAW-Codecs

Im Vergleich zu Nicht-RAW-Bildtypen wie JPEG oder TIFF gibt es zwei wichtige Unterschiede im Verhalten von RAW-Bildformaten in Windows:

-   Die meisten RAW-Bildformate werden als "schreibgeschützt" angenommen und unterstützen wahrscheinlich keine Pixelcodierung im RAW-Format. Da jedoch Windows Imaging Component (WIC) einen Encoder erfordert, um das Zurückschreiben von Metadaten zu unterstützen, sollten RAW-Codecautoren planen, mindestens eine Skeleton Encoder-Klasse zu implementieren.
-   Das Decodieren eines RAW-Bilds in voller Größe kann im Vergleich zu anderen Formaten sehr lange dauern. Aus diesem Grund empfiehlt Microsoft, bestimmte Ansätze zu verwenden, um die Latenz bei der Decodierung zu minimieren und die Unterstützung für Szenarien wie schnelles Rendering von Miniaturansichten und Vorschauen sicherzustellen.

    Beispielsweise müssen alle RAW-Codecautoren die [**IWICBitmapSourceTransform-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) implementieren, die einen Mechanismus zur Benachrichtigung des Decoders vor der Zielbitmapgröße bietet, wodurch eine optimierte Decodierung auf eine kleinere Ausgabebildgröße ermöglicht wird.

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

 

 



