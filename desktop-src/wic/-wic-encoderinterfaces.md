---
description: Encoder-Schnittstellen
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Encoder-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216818"
---
# <a name="encoder-interfaces"></a>Encoder-Schnittstellen


In den folgenden Tabellen sind die von Windows Imaging Component (WIC)-Encodern implementierten Schnittstellen aufgeführt, und das Klassendiagramm zeigt die Vererbungs Hierarchie.

Container-Level Encoder-Schnittstellen



| Schnittstelle                                                                                       | Aufgaben                             | Implementierung                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [Iwicbitmapcoder](-wic-imp-iwicbitmapencoder.md)                                             | Dienste auf Container Ebene                     | Erforderlich                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | Unterstützung für die Fortschritts Benachrichtigung & Abbruch | Empfohlen                                                                |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)                                 | Dienste für die metadatenserialisierung              | Optional (nur für Formate erforderlich, die Metadaten auf Container Ebene unterstützen) |



 

Frame-Level Encoder-Schnittstellen



| Schnittstelle                                                       | Aufgaben                | Implementierung |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)     | Dienste auf Frame-Ebene            | Erforderlich       |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md) | Dienste für die metadatenserialisierung | Erforderlich       |



 

![Vererbungs Hierarchie der WIC-Codierer](graphics/wicencoderinterfaces.png)

Sie werden bemerken, dass es sich bei den Codierungs Schnittstellen fast um Spiegelbilder der Decoder-Schnittstellen handelt und dass die meisten Methoden dieser Schnittstellen Methoden auf den zugehörigen Decoder-Schnittstellen entsprechen. Nachdem Sie nun mit der Implementierung eines WIC-fähigen Decoders vertraut sind, wird die Implementierung eines WIC-fähigen Encoders ebenfalls vertraut sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Implementieren eines WIC-Enabled Encoders](-wic-implementingwicencoder.md)
</dt> <dt>

[Implementieren von iwicbitmapcoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



