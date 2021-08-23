---
description: Schnittstellenmethode – Anforderungen
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: Schnittstellenmethode – Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8525f7b04fe82247ecd64a38f5f1acc298be5d3ace56303072268fed6a4a3cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086923"
---
# <a name="interface-method-requirements"></a>Schnittstellenmethode – Anforderungen

Nicht jede Methode auf jeder Schnittstelle muss über eine -Implementierung verfügen. Einige Codecs verfügen beispielsweise über globale Metadaten, Miniaturansichten oder Farbkontexte, während andere Codecs diese nur pro Frame bereitstellen. Wenn Codecautoren diese nur pro Frame bereitstellen, müssen sie nur [**get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) oder ColorContexts implementieren oder die [**GetMetadataQueryReader-**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) oder [**GetMetadataQueryWriter-Methoden**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) für [**DEN IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) und [**DEN IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) anstelle von [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) und [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)implementieren. Ebenso verwenden einige Codecs keine indizierten Formate und sind daher nicht erforderlich, um die [**Methoden CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) und [**SetPalette zu**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) implementieren. Diese Methoden sind daher optional und bleiben dem Ermessen des Codec-Erstellers überlassen. Die meisten anderen Methoden sind erforderlich.

Für Windows 7 [**sind Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) / [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) und [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) erforderlich und müssen entweder für die Klassen auf Enthalten-Ebene oder für die Klassen auf Frameebene implementiert werden. Wenn Ihr Bilddateiformat keine Vorschauen oder Miniaturansichten an einem dieser Speicherorte unterstützt, sollten Sie das Bilddateiformat überarbeiten, um eine solche Unterstützung zu bieten.

Wenn eine Methode nicht implementiert ist, ist es wichtig, einen entsprechenden Fehler zurück zu geben, damit der Aufrufer feststellen kann, dass das angeforderte Feature nicht unterstützt wird. Wenn Codec-Autoren beispielsweise keine Miniaturansichten auf Containerebene unterstützen, sollten sie [WINCODEC \_ ERR \_ CODECNOTHUMBNAIL](-wic-codec-error-codes.md) zurückgeben, wenn eine Anwendung [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md)aufruft, und wenn sie keine Palette haben, sollten sie [WINCODEC \_ ERR \_ PALETTEUNAVAILABLE zurückgeben.](-wic-codec-error-codes.md) Wenn kein geeigneter [WINCODEC \_ ERR-Code](-wic-codec-error-codes.md) vorhanden ist, sollte der Codec E NOTIMPL für \_ nichtimplementierte Methoden zurückgeben.

In den folgenden Tabellen sind die erforderlichen und optionalen Methoden für jede Windows WIC-Schnittstellen (Imaging Component) aufgeführt.

[**Iwicbitmapdecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



Erforderlich

[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[**Initialisieren**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[**Getframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

Optional

[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)2

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

¹Erstützt, wenn Ihr Imagedateiformat Vorschauversionen auf Containerebene unterstützt. Wenn dies nicht der Fall ist, wird dringend empfohlen, das Bilddateiformat zu überarbeiten, um dies zu unterstützen. Wenn hier implementiert, ist eine entsprechende [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) für die Codierungsklasse auf Containerebene erforderlich.

Reliquired entweder hier oder in der Decodierungsklasse auf Frameebene, je nachdem, wo in Ihrem Bilddateiformat Miniaturansichten gespeichert werden. Wenn dies hier implementiert wird, ist eine entsprechende [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) für die Codierungsklasse auf Containerebene erforderlich.

[**Iwicbitmapframedecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



Erforderlich

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[**Copypixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

Optional

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)

[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

Erforderlich, je nachdem, wo im Bilddateiformat Miniaturansichten gespeichert werden, entweder hier oder in der Decodierungsklasse auf Containerebene. Wenn dies hier implementiert wird, ist eine entsprechende [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) für die Encoderklasse auf Frameebene erforderlich.

[**Iwicmetadatablockreader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



Erforderlich

[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[**Getenumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



Erforderlich

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[**Copypixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

Optional

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

Siehe [Unterstützung für IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md)weiter unten in diesem Dokument.

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



Erforderlich

[**Initialisieren**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

Optional

[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)2

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

¹Erstützt, wenn Ihr Bilddateiformat Vorschauversionen auf Frameebene unterstützt.

Je nachdem, wo in Ihrem Bilddateiformat Miniaturansichten gespeichert werden, ist dies entweder hier oder in der Codierungsklasse auf Frameebene erforderlich. Wenn dies hier implementiert wird, ist eine entsprechende [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) für die Decodierungsklasse auf Containerebene erforderlich.

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



Erforderlich

[**Initialisieren**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[**Setsize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[**Writepixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

Optional

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)

[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

Ist entweder hier oder in der Codierungsklasse auf Containerebene erforderlich, je nachdem, wo in Ihrem Bilddateiformat Miniaturansichten gespeichert werden. Wenn dies hier implementiert wird, ist eine entsprechende [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) für die Decodierungsklasse auf Frameebene erforderlich.

[**Iwicmetadatablockreader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



Erforderlich

[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

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

 

 
