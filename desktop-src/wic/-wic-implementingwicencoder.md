---
description: Implementieren eines WIC-Enabled Encoders
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implementieren eines WIC-Enabled Encoders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216968"
---
# <a name="implementing-a-wic-enabled-encoder"></a>Implementieren eines WIC-Enabled Encoders

## <a name="introduction"></a>Einführung

Zum Implementieren eines WIC-Encoders (Windows Imaging Component) müssen zwei Klassen geschrieben werden, ebenso wie bei der Implementierung eines WIC-Decoders. Die Schnittstellen dieser Klassen entsprechen direkt den [Codierungs](-wic-howwicworks.md) Aufgaben, die im Abschnitt Codierung der Funktionsweise der Windows-Abbild Erstellungs Komponente beschrieben werden.

Eine der-Klassen stellt Dienste auf Container Ebene bereit und verwaltet die Serialisierung der einzelnen Bildframes innerhalb des Containers. Diese Klasse implementiert die [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) -Schnittstelle. Wenn Ihr Bildformat Metadaten auf Container Ebene unterstützt, müssen Sie auch die [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) -Schnittstelle für diese Klasse implementieren.

Die andere Klasse stellt Dienste auf Frame-Ebene bereit und übernimmt die eigentliche Codierung der Bildbits für jeden Frame im Container. Außerdem durchläuft Sie die Metadatenblöcke für jeden Frame und fordert die entsprechenden metadatenwriter zum Serialisieren der Blöcke an. Diese Klasse implementiert die **iwicbitmapframekocode** -Schnittstelle und die [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) -Schnittstelle. Diese Klasse sollte über einen IStream-Member verfügen, den die Klasse auf Container Ebene bei der Instanziierung initialisiert, in der die **Commit** -Methode die Frame Daten serialisiert.

In einigen Fällen, z. b. in unformatierten Formaten, möchte der Codec-Autor möglicherweise nicht, dass Anwendungen in das RAW-Format codieren oder erneut codieren können, da der Zweck einer Rohdatendatei darin besteht, die Sensordaten genau so wie von der Kamera zu enthalten. In Fällen, in denen der Codec-Autor die Codierung nicht aktivieren möchte, ist es immer noch erforderlich, einen rudimentären Encoder zu implementieren, um das Hinzufügen von Metadaten zu ermöglichen. In diesem Fall muss der Encoder nur die Methoden unterstützen, die für das Schreiben von Metadaten erforderlich sind, und die Bildbits können unverändert vom Decoder kopiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

**Licher**
</dt> <dt>

[Implementieren von IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Encoder-Schnittstellen](-wic-encoderinterfaces.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



