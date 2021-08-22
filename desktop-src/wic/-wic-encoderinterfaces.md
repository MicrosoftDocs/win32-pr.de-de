---
description: Encoderschnittstellen
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Encoderschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6169dcf55ffafe0bf4c006b45c173ecc7486555fb001456112f8f333a8ccf2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965123"
---
# <a name="encoder-interfaces"></a>Encoderschnittstellen


Die folgenden Tabellen zeigen die schnittstellen, die von Windows Imaging Component (WIC)-Encodern implementiert werden, und das Klassendiagramm zeigt die Vererbungshierarchie.

Container-Level Encoderschnittstellen



| Schnittstelle                                                                                       | Aufgaben                             | Implementierung                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)                                             | Dienste auf Containerebene                     | Erforderlich                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | Statusbenachrichtigungen & Abbruchunterstützung | Empfohlen                                                                |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)                                 | Metadatenserialisierungsdienste              | Optional (nur für Formate erforderlich, die Metadaten auf Containerebene unterstützen) |



 

Frame-Level Encoderschnittstellen



| Schnittstelle                                                       | Aufgaben                | Implementierung |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)     | Dienste auf Frameebene            | Erforderlich       |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md) | Metadatenserialisierungsdienste | Erforderlich       |



 

![Vererbungshierarchie der wic-Encoderschnittstelle](graphics/wicencoderinterfaces.png)

Sie werden feststellen, dass die Encoderschnittstellen fast Spiegelbilder der Decoderschnittstellen sind und dass die meisten Methoden auf diesen Schnittstellen Methoden auf den zugehörigen Decoderschnittstellen entsprechen. Da Sie nun mit der Implementierung eines WIC-fähigen Decoders vertraut sind, scheint ihnen die Implementierung eines WIC-fähigen Encoders vertraut zu sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Implementieren eines WIC-Enabled Encoders](-wic-implementingwicencoder.md)
</dt> <dt>

[Implementieren von IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



