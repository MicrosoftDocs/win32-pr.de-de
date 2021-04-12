---
description: Implementieren von IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implementieren von IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347188"
---
# <a name="implementing-iwicbitmapsourcetransform"></a>Implementieren von IWICBitmapSourceTransform

## <a name="iwicbitmapsourcetransform"></a>IWICBitmapSourceTransform

Obwohl es optional ist, wird dringend empfohlen, dass jeder Decoder diese Schnittstelle in der Decodierung der Frame-Ebene implementiert, da er wichtige Leistungsvorteile bieten kann. Wenn eine Anwendung einen bestimmten Bereich von Interesse, Größe, Ausrichtung oder Pixel Format anfordert, anstatt nur das gesamte Bild bei vollständiger Auflösung zu decodieren und dann die angeforderten Transformationen anzuwenden, ruft Windows Imaging Component (WIC) [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für diese Schnittstelle für das [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Objekt auf. Wenn der Frame-Decoder dies unterstützt, ruft WIC die entsprechenden Methoden oder Methoden auf, um zu bestimmen, ob der Frame-Decoder die angeforderte Transformation durchführen kann, oder um die nächstgelegene Größe oder das Pixel Format festzulegen, die der Decoder für die angeforderte Wenn der Decoder die angeforderte Transformation oder Transformationen ausführen kann, ruft WIC [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) mit den entsprechenden Parametern auf. Wenn der Decoder einige, jedoch nicht alle angeforderten Transformationen ausführen kann, WIC fordert den Decoder dazu auf, diese auszuführen, und verwendet die WIC Transform-Objekte ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)und [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)), um die verbleibenden Transformationen auszuführen, die vom Frame Decoder beim Ergebnis des **copypixel** -Aufrufes nicht ausgeführt werden konnten. Wenn der Decoder [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)nicht unterstützt, muss WIC die Transform-Objekte verwenden, um alle Transformationen auszuführen. Es ist in der Regel viel effizienter, wenn der Decoder während des Decodierungs Prozesses Transformationen ausführt, als das gesamte Bild zu decodieren und dann die Transformationen auszuführen. Dies gilt insbesondere für Vorgänge wie die Skalierung auf eine wesentlich geringere Größe oder Pixel Formatkonvertierungen.


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
-   [CopyPixels](#copypixels)
-   [GetClosestSize](#getclosestsize)
-   [GetClosestPixelFormat](#getclosestpixelformat)

### <a name="doessupporttransform"></a>DoesSupportTransform

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) fragt, ob der Decoder den angeforderten Rotations-oder flippingvorgang unterstützt. Die folgenden [**WICBitmapTransformOptions-Optionen**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) sind möglich:


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



### <a name="copypixels"></a>CopyPixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) führt die eigentliche Dekodierung der Bildbits aus, z. b. die [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) -Methode in der [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Schnittstelle, aber die [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) -Methode für [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) ist viel leistungsfähiger und kann die Bildverarbeitungsleistung erheblich verbessern.

Wenn mehrere Transformations Vorgänge angefordert werden, hängt das Ergebnis von der Reihenfolge ab, in der die Vorgänge ausgeführt werden. Um die Vorhersagbarkeit und Konsistenz zwischen Codecs sicherzustellen, ist es wichtig, dass alle Codecs diese Vorgänge in derselben Reihenfolge ausführen. Dies ist die kanonische Reihenfolge zum Durchführen dieser Vorgänge.

1.  Skalieren
2.  Crop
3.  Rotate

Die Konvertierung von Pixel Formaten kann jederzeit ausgeführt werden, da Sie keine Auswirkungen auf die anderen Transformationen hat.

Der erste Parameter, *prcSrc*, wird verwendet, um den Bereich anzugeben, der für das Abschneiden des Bilds von Interesse ist. Da die Skalierung durchgeführt wird, bevor das Abbild nach der Konvention abgeschnitten wird, muss der relevante Bereich nach dem Skalieren des Bilds festgelegt werden, wenn das Bild skaliert und abgeschnitten werden soll.

Der zweite und dritte Parameter geben die Größe an, in der das Bild skaliert werden soll.

Der *pguidDstFormat* -Parameter gibt das angeforderte Pixel Format für das decodierte Bild an. Da WIC bereits [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)aufgerufen hat, sollte dies ein Pixel Format sein, das der Decoder angibt, dass es unterstützt.

Der *dsttransform* -Parameter gibt den angeforderten Drehwinkel an und gibt an, ob das Bild vertikal, horizontal oder beides gekippt werden soll. Da WIC bereits " [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)" aufgerufen hat, sollte die angeforderte Transformation eine solche Transformation sein, die der Decoder bereits angibt, dass Sie unterstützt. Beachten Sie, dass die Rotation immer nach dem Skalieren und Abschneiden erfolgen sollte.

### <a name="getclosestsize"></a>GetClosestSize

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) übernimmt zwei in/out-Parameter. Der Aufrufer verwendet die Parameter " *puiWidth* " und " *puiHeight* ", um die Größe anzugeben, mit der der Aufrufer das Bild als decodiert eingibt. Ein Decoder kann jedoch ein Bild nur in eine Größe decodieren, die ein Vielfaches seiner DCT-Größe ist, und unterschiedliche Bildformate können unterschiedliche DCT-Größen aufweisen. Der Decoder sollte auf der Grundlage seiner eigenen DCT-Größe ermitteln, dem am nächsten liegenden Wert der angeforderten Größe und dem Wert für " *puiWidth* " und " *puiHeight* " bei der Rückgabe. Wenn eine größere Größe angefordert wird, der Codec jedoch keine upskalierung unterstützt, sollte das Original zurückgegeben werden.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) wird verwendet, um das nächste Pixel Format für das angeforderte Pixel Format festzulegen, das der Decoder ohne Datenverlust bereitstellen kann. Es ist immer empfehlenswert, in ein breiteres Pixel Format zu konvertieren, als es sich um einen engeren handelt, auch wenn die Größe des Bilds vergrößert wird, da es bei Bedarf immer wieder in ein restriktiveres Format konvertiert werden kann. Nachdem die Daten verloren gegangen sind, können Sie jedoch nicht wieder hergestellt werden.

## <a name="continued-reading"></a>Fortgesetztes lesen

Weitere Informationen zum Erstellen eines WIC-fähigen Codecs finden Sie unter Implementieren von [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Licher**
</dt> <dt>

[Implementieren von IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Implementieren von IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
