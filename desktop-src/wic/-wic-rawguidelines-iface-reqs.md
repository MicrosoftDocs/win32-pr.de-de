---
description: Schnittstellen Methoden Anforderungen
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: Schnittstellen Methoden Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9cabe02900fa789773f4104cf282ab326bd4930
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362851"
---
# <a name="interface-method-requirements"></a>Schnittstellen Methoden Anforderungen

Nicht jede Methode für jede Schnittstelle muss über eine Implementierung verfügen. Einige Codecs verfügen z. b. über globale Metadaten, Miniaturansichten oder Farb Kontexte, während andere Codecs diese nur pro Frame bereitstellen. Wenn Codec-Autoren diese nur pro Frame bereitstellen, müssen Sie nur die [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) -oder ColorContext-Methode implementieren oder die [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) -Methode oder die [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) -Methode für [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) und [**iwicbitmapframecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) anstelle von [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) und [**iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)implementieren. Ebenso verwenden einige Codecs keine indizierten Formate und sind daher nicht zum Implementieren der [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) -und [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) -Methoden erforderlich. Diese Methoden sind daher optional und bleiben dem Ermessen des Codec-Erstellers überlassen. Die meisten anderen Methoden sind erforderlich.

Für Windows 7 sind [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) / [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) und [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) erforderlich. Sie müssen entweder auf den Klassen auf Klassenebene oder auf Frame-Ebene implementiert werden. Wenn Ihr Bild Dateiformat keine Vorschau oder Miniaturansichten an einem dieser Orte unterstützt, sollten Sie das Bild Dateiformat überarbeiten, um eine solche Unterstützung bereitzustellen.

Wenn eine Methode nicht implementiert wird, ist es wichtig, einen entsprechenden Fehler zurückzugeben, damit der Aufrufer feststellen kann, dass die angeforderte Funktion nicht unterstützt wird. Wenn z. b. Codec-Autoren keine Miniaturansichten auf Container Ebene unterstützen, sollten Sie [wincodec \_ Err \_ codecnothumbnail](-wic-codec-error-codes.md) zurückgeben, wenn eine Anwendung [**getminiatur**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md)aufruft. Wenn Sie über keine Palette verfügen, sollten Sie [wincodec \_ Err \_ palettenicht verfügbar](-wic-codec-error-codes.md)zurückgeben. Wenn kein geeigneter [wincodec- \_ Err](-wic-codec-error-codes.md) -Code vorhanden ist, sollte der Codec E \_ notimpl für nicht implementierte Methoden zurückgeben.

In den folgenden Tabellen sind die erforderlichen und optionalen Methoden für jede WIC-Schnittstelle (Windows Imaging Component) aufgelistet.

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



Erforderlich

[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[**Initialisieren**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

Optional

[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²

[**Getcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

¹ erforderlich, wenn das Image Dateiformat Vorschauen auf Container Ebene unterstützt. Wenn dies nicht der Fall ist, wird dringend empfohlen, das Bild Dateiformat zu überarbeiten, um dies zu unterstützen. Wenn Sie hier implementiert sind, ist für die Codieren-Klasse auf Container Ebene eine entsprechende [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) erforderlich.

² ist entweder hier oder auf der decodierklasse auf Frame-Ebene erforderlich, abhängig davon, wo das Bild Dateiformat Miniaturansichten speichert. Wenn Sie hier implementiert sind, ist für die codierklasse auf Container Ebene eine entsprechende [**setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) -Klasse erforderlich.

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



Erforderlich

[**Getcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

Optional

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹

[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

¹ erforderlich entweder hier oder in der Decodierungs Klasse auf Container Ebene, je nachdem, wo Sie das Bild Dateiformat für Miniaturansichten speichert. Wenn Sie hier implementiert sind, ist für die Encoder-Klasse auf Frame-Ebene eine entsprechende [**setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) -Klasse erforderlich.

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



Erforderlich

[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



Erforderlich

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

Optional

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

Weitere Informationen finden Sie [unter Unterstützung für IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md)weiter unten in diesem Dokument.

[**Iwicbitmapcoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



Erforderlich

[**Initialisieren**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[**"Kreatenewframe"**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[**Einzusetzen**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

Optional

[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²

[**Setcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

¹ erforderlich, wenn das Bild Dateiformat Vorschauen auf Frame-Ebene unterstützt.

² ist entweder hier oder auf der codieren-Klasse auf Frame-Ebene erforderlich, abhängig davon, wo Ihr Bild Dateiformat Miniaturansichten speichert. Wenn Sie hier implementiert sind, ist für die decodierklasse auf Container Ebene eine entsprechende [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) -Datei erforderlich.

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



Erforderlich

[**Initialisieren**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[**Setcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[**Setcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[**Projekt Mappe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[**"WritePixels"**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[**Schreibgeschützte Datenquelle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[**Einzusetzen**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

Optional

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹

[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

¹ erforderlich entweder hier oder auf der Codierungs Klasse auf Container Ebene, abhängig davon, wo das Bild Dateiformat Miniaturansichten speichert. Wenn Sie hier implementiert sind, ist für die decodierklasse auf Frame-Ebene eine zugehörige [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) -Datei erforderlich.

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



Erforderlich

[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[**"Getschreiterbyindex"**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[**Setschreiterbyindex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[**Removeschreiterbyindex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

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

 

 
