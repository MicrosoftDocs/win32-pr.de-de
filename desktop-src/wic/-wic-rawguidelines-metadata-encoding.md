---
description: Codierung
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Codierung (Windows Imaging-Komponente)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6d15b983b7455d0fe0c406cbad64dbbb77588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350800"
---
# <a name="encoding-windows-imaging-component"></a>Codierung (Windows Imaging-Komponente)

Der codierautor muss folgende Aktionen ausführen:

-   Implementieren Sie die [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) -Schnittstelle und die [**iwicbitmapframekocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Schnittstelle.
-   Implementieren Sie [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) auf dem Frame Encoder. Wenn der Codec Metadaten auf Container Ebene unterstützt, muss diese Schnittstelle sowohl für den Encoder auf Container Ebene als auch für den Frame Encoder implementiert werden.
-   Wenn das Containerformat implizit irgendwelche obligatorischen Metadatenblöcke enthält, instanziieren Sie einen metadatenwriter für jeden dieser Blöcke. Beispielsweise erfordert das TIFF-Format für jeden Frame ein Schnittstellen Gerät (IFD), sodass der IFD-Writer immer verfügbar gemacht werden muss.
-   Implementieren Sie Unterstützung für die Verwaltung der Auflistung von metadatenwritern. Der blockwriter verwaltet alle Bestell Anforderungen oder Container Beschränkungen für die Arten von metadatenblöcken, die codiert werden können. Der blockwriter muss überprüfen, ob alle neuen metadatenwriter innerhalb des Container Formats eingebettet werden können.
-   Beim Codieren des bildstreams wird [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) aufgerufen, um den Inhalt jedes metadatenwriters in den Stream zu serialisieren. Wenn der Metadatenblock "Critical"-Metadaten enthält, muss der Encoder die kritischen Metadatenelemente festlegen, bevor er den metadatenwriter anfordert, Inhalte zu serialisieren.
-   Suchen Sie nach unbekannten metadatenhandlern, um sicherzustellen, dass redundante Metadatenblöcke nicht vorhanden sind. Dies ist wichtig, da bei der Beibehaltung von Metadaten in einem decodieren oder Codieren von Szenarien unbekannte Blöcke möglicherweise ein Duplikat erforderlicher Metadatenblöcke sind.

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

 

 



