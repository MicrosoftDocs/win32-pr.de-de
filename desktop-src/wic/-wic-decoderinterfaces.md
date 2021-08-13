---
description: Decoderschnittstellen
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Decoderschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a52a0924f6302e45b10cb32a1d621db04967d33a3251ee39cce359e5030af5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393524"
---
# <a name="decoder-interfaces"></a>Decoderschnittstellen

Die folgenden Tabellen zeigen die Schnittstellen, die von Windows WIC-Decodern (Imaging Component) implementiert werden, und das Klassendiagramm zeigt die Vererbungshierarchie.

Container-Level-Decoderschnittstellen



| Schnittstelle                                                                                       | Aufgaben                             | Implementierung                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [Iwicbitmapdecoder](-wic-imp-iwicbitmapdecoder.md)                                             | Dienste auf Containerebene                     | Erforderlich                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | Unterstützung für Statusbenachrichtigungen & Abbruch | Empfohlen                                                                |
| [Iwicmetadatablockreader](-wic-imp-iwicmetadatablockreader.md)                                 | Metadatenenumeration                         | Optional (nur für Formate erforderlich, die Metadaten auf Containerebene unterstützen) |



 

Frame-Level-Decoderschnittstellen



| Schnittstelle                                                           | Aufgaben          | Implementierung                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [Iwicbitmapframedecode](-wic-imp-iwicbitmapframedecode.md)         | Dienste auf Frameebene      | Erforderlich                      |
| [Iwicmetadatablockreader](-wic-imp-iwicmetadatablockreader.md)     | Metadatenenumeration      | Erforderlich                      |
| [IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md) | Transformationen des nativen Decoders | Empfohlen                   |
| [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)                       | Rohdatenverarbeitungsdienste   | Nur für Raw-Formate erforderlich |



 

![WIC-Schnittstellenvererbungshierarchie](graphics/wicinterfaces.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Implementieren eines WIC-Enabled-Decoders](-wic-implementingwicdecoder.md)
</dt> <dt>

[Implementieren von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



