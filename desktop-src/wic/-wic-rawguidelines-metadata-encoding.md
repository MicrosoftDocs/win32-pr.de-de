---
description: Codierung
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Codierung (Windows Imaging-Komponente)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b3d6eef499379bbdc668e70d5d0ec4326b390372da910934a6e7c7f547d177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964649"
---
# <a name="encoding-windows-imaging-component"></a>Codierung (Windows Imaging-Komponente)

Der Encoderautor muss folgende Schritte unternehmen:

-   Implementieren [**Sie DIE SCHNITTSTELLEN IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) und [**IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
-   Implementieren [**Sie IWICMetadataBlockWriter für**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) den Frameencoder. Wenn der Codec Metadaten auf Containerebene unterstützt, muss diese Schnittstelle sowohl für den Encoder auf Containerebene als auch für den Frameencoder implementiert werden.
-   Wenn das Containerformat implizit erforderliche Metadatenblöcke enthält, instanziieren Sie einen Metadatenwriter für jeden solchen Block. Beispielsweise erfordert das TIFF-Format ein Schnittstellengerät (Interface Device, IFD) für jeden Frame, sodass der IFD-Writer immer verfügbar gemacht werden muss.
-   Implementieren Sie Unterstützung für die Verwaltung der Auflistung von Metadaten-Writern. Der Blockwriter verwaltet alle Bestellanforderungen oder Containereinschränkungen für die Arten von Metadatenblöcken, die codiert werden können. Der Blockwriter muss überprüfen, ob alle neuen Metadatenwriter in das Containerformat eingebettet werden können.
-   Rufen Sie beim Codieren des Bilddatenstroms [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) auf, um den Inhalt jedes Metadatenwriters in den Stream zu serialisieren. Wenn der Metadatenblock "kritische" Metadaten enthält, muss der Encoder die kritischen Metadatenelemente festlegen, bevor der Metadatenwriter aufgefordert wird, Inhalte zu serialisieren.
-   Suchen Sie nach unbekannten Metadatenhandlern, um sicherzustellen, dass keine redundanten Metadatenblöcke vorhanden sind. Dies ist wichtig, da unbekannte Blöcke beim Beibehalten von Metadaten in einem Decodierungs- oder Codierungsszenario ein Duplikat von obligatorischen Metadatenblöcken sein können.

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

 

 



