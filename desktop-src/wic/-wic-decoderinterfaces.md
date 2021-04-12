---
description: Decoder-Schnittstellen
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Decoder-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218037"
---
# <a name="decoder-interfaces"></a>Decoder-Schnittstellen

In den folgenden Tabellen werden die von Windows Imaging Component (WIC)-Decodern implementierten Schnittstellen angezeigt, und das Klassendiagramm zeigt die Vererbungs Hierarchie.

Container-Level Decoder-Schnittstellen



| Schnittstelle                                                                                       | Aufgaben                             | Implementierung                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)                                             | Dienste auf Container Ebene                     | Erforderlich                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | Unterstützung für die Fortschritts Benachrichtigung & Abbruch | Empfohlen                                                                |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)                                 | Metadatenenumeration                         | Optional (nur für Formate erforderlich, die Metadaten auf Container Ebene unterstützen) |



 

Frame-Level Decoder-Schnittstellen



| Schnittstelle                                                           | Aufgaben          | Implementierung                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)         | Dienste auf Frame-Ebene      | Erforderlich                      |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)     | Metadatenenumeration      | Erforderlich                      |
| [IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md) | Native Decoder-Transformationen | Empfohlen                   |
| [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)                       | Rohverarbeitungs Dienste   | Nur für RAW-Formate erforderlich |



 

![WIC-Schnittstellen Vererbungs Hierarchie](graphics/wicinterfaces.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Implementieren eines WIC-Enabled Decoders](-wic-implementingwicdecoder.md)
</dt> <dt>

[Implementieren von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



