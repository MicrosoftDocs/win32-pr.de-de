---
description: Implementieren eines WIC-Enabled Encoders
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implementieren eines WIC-Enabled Encoders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7f0bf3c073b3658c6c6edda6cf0761e3d594965b83b1b54206a48b62c96727
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710929"
---
# <a name="implementing-a-wic-enabled-encoder"></a>Implementieren eines WIC-Enabled Encoders

## <a name="introduction"></a>Einführung

Zum Implementieren Windows WIC-Encoders (Imaging Component) müssen zwei Klassen geschrieben werden. Dies gilt auch für die Implementierung eines WIC-Decoders. Die Schnittstellen in diesen Klassen entsprechen direkt den [](-wic-howwicworks.md) Encoderaufgaben, die im Abschnitt Codierung von How The Windows Imaging Component (Funktionsweise der Bildverarbeitungskomponente) beschrieben werden.

Eine der -Klassen stellt Dienste auf Containerebene zur Verfügung und verwaltet die Serialisierung der einzelnen Imageframes innerhalb des Containers. Diese Klasse implementiert die [**IWICBitmapEncoder-Schnittstelle.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) Wenn Ihr Imageformat Metadaten auf Containerebene unterstützt, müssen Sie auch die [**IWICMetadataBlockWriter-Schnittstelle**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) für diese Klasse implementieren.

Die andere Klasse stellt Dienste auf Frameebene zur Verfügung und übernimmt die eigentliche Codierung der Bildbits für jeden Frame im Container. Außerdem werden die Metadatenblöcke für jeden Frame durch iteriert, und die entsprechenden Metadatenautoren werden zum Serialisieren der Blöcke fordert. Diese Klasse implementiert die **IWICBitmapFrameEncode-Schnittstelle** und [**die IWICMetadataBlockWriter-Schnittstelle.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) Diese Klasse sollte über einen IStream-Member verfügen, den die Klasse auf Containerebene bei der Instanziierung initialisiert, in die die **Commit-Methode** die Framedaten serialisiert.

In einigen Fällen, z. B. unformatierten Formaten, möchte der Codec-Autor möglicherweise nicht, dass Anwendungen das Rohformat codieren oder erneut codieren können, da der Zweck einer Rohdatei ist, die Sensordaten genau so zu enthalten, wie sie von der Kamera stammten. In Fällen, in denen der Codecautor die Codierung nicht aktivieren möchte, ist es dennoch erforderlich, einen rohenen Encoder zu implementieren, nur um das Hinzufügen von Metadaten zu ermöglichen. In diesem Fall muss der Encoder nur die Methoden unterstützen, die zum Schreiben von Metadaten erforderlich sind, und kann die Bildbits ohne Änderungen aus dem Decoder kopieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Implementieren von IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Encoderschnittstellen](-wic-encoderinterfaces.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



