---
description: 'Weitere Informationen finden Sie unter: Implementieren eines WIC-Enabled Decoders'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implementieren eines WIC-Enabled Decoders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866763"
---
# <a name="implementing-a-wic-enabled-decoder"></a>Implementieren eines WIC-Enabled Decoders


Zum Implementieren eines WIC-Decoders (Windows Imaging Component) müssen zwei Klassen geschrieben werden. Die Schnittstellen für diese Klassen entsprechen direkt den Decoder-Zuständigkeiten, die im Abschnitt [decodieren](-wic-howwicworks.md) der [Funktionsweise der Windows-Abbild](-wic-howwicworks.md)Erstellungs Komponente beschrieben werden.

Eine der-Klassen stellt Dienste auf Container Ebene bereit und implementiert die [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) -Schnittstelle. Wenn Ihr Bildformat Metadaten auf Container Ebene unterstützt, müssen Sie auch die [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) -Schnittstelle für diese Klasse implementieren. Es wird empfohlen, dass Sie die [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) -Schnittstelle sowohl für den Decoder als auch für den Encoder unterstützen, um eine bessere Benutzeroberfläche zu unterstützen.

Die andere Klasse, die Sie implementieren, stellt Dienste auf Frame-Ebene bereit und führt die eigentliche Decodierung der Bildbits für jeden Frame im Container aus. Diese Klasse implementiert die [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) -Schnittstelle und die [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) -Schnittstelle. Wenn Sie einen Decoder für ein Rohdaten Format schreiben, implementieren Sie auch die [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) -Schnittstelle für diese Klasse. Zusätzlich zu den erforderlichen Schnittstellen wird dringend empfohlen, dass Sie die [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) -Schnittstelle für diese Klasse implementieren, um die bestmögliche Leistung für Ihr Bildformat zu aktivieren.

Eines der-Objekte, die von WIC bereitgestellt werden, ist die [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory). Häufig verwenden Sie die [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) -Schnittstelle für dieses Objekt, um verschiedene Komponenten zu erstellen. Da Sie häufig verwendet wird, sollten Sie einen Verweis darauf als Element Eigenschaft in den Decoder-und Encoder-Klassen speichern.


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

**Licher**
</dt> <dt>

[Funktionsweise der Windows-Abbild Erstellungs Komponente](-wic-howwicworks.md)
</dt> <dt>

[Decoder-Schnittstellen](-wic-decoderinterfaces.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über die Codierung](-wic-creating-encoder.md)
</dt> </dl>

 

 



