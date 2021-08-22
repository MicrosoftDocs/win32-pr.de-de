---
description: Implementieren von IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implementieren von IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79caa17fdb874b9cbee73a9a371c4ba454e72c6eb249a6ca7d626fdd9c86aea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711075"
---
# <a name="implementing-iwicbitmapsourcetransform"></a>Implementieren von IWICBitmapSourceTransform

## <a name="iwicbitmapsourcetransform"></a>IWICBitmapSourceTransform

Obwohl optional, wird dringend empfohlen, dass jeder Decoder diese Schnittstelle in Ihrer Decodierungsklasse auf Frameebene implementiert, da sie erhebliche Leistungsvorteile bieten kann. Wenn eine Anwendung einen bestimmten Bereich anfordert, der von Interesse ist, eine bestimmte Größe, Ausrichtung oder ein bestimmtes Pixelformat anfordert, anstatt nur das gesamte Bild mit voller Auflösung zu decodieren und dann die angeforderten Transformationen anzuwenden, ruft Windows Imaging Component (WIC) [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für diese Schnittstelle auf das [**IWICBitmapFrameDecode-Objekt**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) auf. Wenn der Framedecoder dies unterstützt, ruft WIC die entsprechende Methode oder Die entsprechenden Methoden auf, um zu bestimmen, ob der Framedecoder die angeforderte Transformation ausführen oder das nächstgelegene Format oder Pixelformat bestimmen kann, das der Decoder dem angeforderten formatieren kann. Wenn der Decoder die angeforderte Transformation oder Transformation ausführen kann, ruft WIC [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) mit den entsprechenden Parametern auf. Wenn der Decoder einige, aber nicht alle angeforderten Transformationen ausführen kann, fordert WIC den Decoder auf, die gewünschten Transformationen auszuführen, und verwendet die WIC-Transformationsobjekte ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)und [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)), um die verbleibenden Transformationen auszuführen, die vom Framedecoder nicht im Ergebnis des **CopyPixels-Aufrufs** ausgeführt werden konnten. Wenn der Decoder [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)nicht unterstützt, muss WIC die Transformationsobjekte verwenden, um alle Transformationen auszuführen. In der Regel ist es für den Decoder viel effizienter, während des Decodierungsprozesses Transformationen auszuführen, als das gesamte Bild zu decodieren und dann die Transformationen auszuführen. Dies gilt insbesondere für Vorgänge wie die Skalierung auf eine viel kleinere Größe oder Pixelformatkonvertierungen.


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [DoesSupportTransform](#doessupporttransform)
-   [Copypixels](#copypixels)
-   [GetClosestSize](#getclosestsize)
-   [GetClosestPixelFormat](#getclosestpixelformat)

### <a name="doessupporttransform"></a>DoesSupportTransform

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) fragt, ob der Decoder die angeforderte Drehung oder den flipping-Vorgang unterstützt. Die [**möglicherweise angeforderten WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) sind:


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a>Copypixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) führt die eigentliche Decodierung der Imagebits durch, z. B. die [**CopyPixels-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) auf der [**IWICBitmapSource-Schnittstelle,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) aber die [**CopyPixels-Methode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) auf [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) ist viel leistungsstärker und kann die Bildverarbeitungsleistung erheblich verbessern.

Wenn mehrere Transformationsvorgänge angefordert werden, hängt das Ergebnis von der Reihenfolge ab, in der die Vorgänge ausgeführt werden. Um Vorhersagbarkeit und Konsistenz zwischen Codecs sicherzustellen, ist es wichtig, dass alle Codecs diese Vorgänge in der gleichen Reihenfolge ausführen. Dies ist die kanonische Reihenfolge zum Ausführen dieser Vorgänge.

1.  Skalieren
2.  Crop
3.  Rotate

Die Konvertierung des Pixelformats kann jederzeit ausgeführt werden, da sie keine Auswirkungen auf die anderen Transformationen hat.

Der erste Parameter, *prcSrc,* wird verwendet, um den gewünschten Bereich für das Ausschneiden des Bilds anzugeben. Da die Skalierung vor dem Clipping konventionsbedingt durchgeführt wird, sollte der interessante Bereich nach der Skalierung des Images bestimmt werden, wenn das Bild skaliert und abgeschnitten werden soll.

Der zweite und dritte Parameter geben die Größe an, auf die das Bild skaliert werden soll.

Der *Parameter pguidDstFormat* gibt das angeforderte Pixelformat für das decodierte Bild an. Da WIC [**getClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)bereits aufgerufen hat, sollte dies ein Pixelformat sein, das vom Decoder unterstützt wird.

Der *dstTransform-Parameter* gibt den angeforderten Drehwinkel an und gibt an, ob das Bild vertikal, horizontal oder beides gekippt werden soll. Da WIC [**doesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)bereits aufgerufen hat, sollte die angeforderte Transformation eine sein, die vom Decoder bereits unterstützt wird. Denken Sie daran, dass die Drehung immer nach skalierungs- und clipping durchgeführt werden sollte.

### <a name="getclosestsize"></a>GetClosestSize

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) nimmt zwei Ein-/Aus-Parameter an. Der Aufrufer verwendet die Parameter *puiWidth* und *puiHeight,* um die Größe anzugeben, mit der der Aufrufer das Bild decodieren möchte. Ein Decoder kann ein Bild jedoch nur in eine Größe decodieren, die ein Vielfaches seiner DCT-Größe ist, und verschiedene Bildformate können unterschiedliche DCT-Größen aufweisen. Der Decoder sollte basierend auf seiner eigenen DCT-Größe bestimmen, welche der angeforderten Größe am nächsten liegt, und *puiWidth* und *puiHeight* bei der Rückgabe auf diese Dimensionen festlegen. Wenn eine größere Größe angefordert wird, der Codec jedoch keine Upscaling unterstützt, sollte das Original zurückgegeben werden.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) wird verwendet, um das Pixelformat zu bestimmen, das dem angeforderten Pixelformat am nächsten liegt, das der Decoder ohne Datenverlust bereitstellen kann. Es ist immer vorzuziehen, ein größeres Pixelformat als ein schmaleres zu konvertieren, auch wenn dadurch die Größe des Bilds erhöht wird, da es bei Bedarf immer in ein restriktiveres Format zurückgesetzt werden kann. Nachdem die Daten verloren gegangen sind, können sie jedoch nicht wiederhergestellt werden.

## <a name="continued-reading"></a>Fortlaufendes Lesen

Weitere Informationen zum Erstellen eines WIC-fähigen Codecs finden Sie unter [Implementieren von IWICDevelopRaw.](-wic-imp-iwicdevelopraw.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[**Iwicmetadatablockreader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Implementieren von IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Implementieren von IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
