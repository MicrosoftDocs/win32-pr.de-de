---
description: Weitere Informationen finden Sie unter Implementieren eines WIC-Enabled-Decoders.
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implementieren eines WIC-Enabled Decoders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0aa2211c0b21e8f6fc921986406f7079b13c216f0bd7ada684e7748effb6c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205705"
---
# <a name="implementing-a-wic-enabled-decoder"></a>Implementieren eines WIC-Enabled Decoders


Zum Implementieren eines WIC-Decoders (Windows Imaging Component) müssen zwei Klassen geschrieben werden. Die Schnittstellen für diese Klassen entsprechen direkt den Zuständigkeiten des Decoders, die im Abschnitt [Decoding](-wic-howwicworks.md) von How The Windows Imaging Component Works (Funktionsweise der [Windows Imaging-Komponente)](-wic-howwicworks.md)beschrieben sind.

Eine der -Klassen stellt Dienste auf Containerebene bereit und implementiert die [IWICBitmapDecoder-Schnittstelle.](-wic-imp-iwicbitmapdecoder.md) Wenn Ihr Imageformat Metadaten auf Containerebene unterstützt, müssen Sie auch die [IWICMetadataBlockReader-Schnittstelle](-wic-imp-iwicmetadatablockreader.md) für diese Klasse implementieren. Es wird empfohlen, die [IWICBitmapCodecProgressNotification-Schnittstelle](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) sowohl im Decoder als auch im Encoder zu unterstützen, um eine bessere Benutzererfahrung zu ermöglichen.

Die andere Klasse, die Sie implementieren, stellt Dienste auf Frameebene bereit und führt die eigentliche Decodierung der Imagebits für jeden Frame im Container durch. Diese Klasse implementiert die [IWICBitmapFrameDecode-Schnittstelle](-wic-imp-iwicbitmapframedecode.md) und die [IWICMetadataBlockReader-Schnittstelle.](-wic-imp-iwicmetadatablockreader.md) Wenn Sie einen Decoder für ein Rohformat schreiben, implementieren Sie auch die [IWICDevelopRaw-Schnittstelle](-wic-imp-iwicdevelopraw.md) für diese Klasse. Zusätzlich zu den erforderlichen Schnittstellen wird dringend empfohlen, die [IWICBitmapSourceTransform-Schnittstelle](-wic-imp-iwicmetadatablockreader.md) für diese Klasse zu implementieren, um die bestmögliche Leistung für Ihr Bildformat zu ermöglichen.

Eines der von WIC bereitgestellten Objekte ist [**ImagingFactory.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) Sie verwenden häufig die [**IWICComponentFactory-Schnittstelle**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) für dieses Objekt, um verschiedene Komponenten zu erstellen. Da sie häufig verwendet wird, sollten Sie einen Verweis darauf als Membereigenschaft sowohl für Dencoder- als auch für Encoderklassen beibehalten.


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Funktionsweise der Windows Imaging-Komponente](-wic-howwicworks.md)
</dt> <dt>

[Decoderschnittstellen](-wic-decoderinterfaces.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über die Codierung](-wic-creating-encoder.md)
</dt> </dl>

 

 



