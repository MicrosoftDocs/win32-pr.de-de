---
description: Implementieren von iwicbitmapframecocode
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: Implementieren von iwicbitmapframecocode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217384"
---
# <a name="implementing-iwicbitmapframeencode"></a>Implementieren von iwicbitmapframecocode

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**Iwicbitmapframecocode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) ist das Gegenstück zur [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Schnittstelle. Sie können diese Schnittstelle in der Codierungs Klasse auf Frame-Ebene implementieren, bei der es sich um die Klasse handelt, die die tatsächliche Codierung der Bildbits für jeden Frame durchführt.


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [Initialisieren](#initialize)
-   [SetSize und SetResolution](#setsize-and-setresolution)
-   [SetPixelFormat](#setpixelformat)
-   [Setcolorkontexte](#setcolorcontexts)
-   [GetMetadataQueryWriter](#getmetadataquerywriter)
-   [Setminiatur](#setthumbnail)
-   ["WritePixels"](#writepixels)
-   [Schreibgeschützte Datenquelle](#writesource)
-   [Commit](#commit)
-   [SetPalette](#setpalette)

### <a name="initialize"></a>Initialisieren

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) ist die erste Methode, die für ein [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) -Objekt aufgerufen wird, nachdem es instanziiert wurde. Diese Methode verfügt über einen Parameter, der möglicherweise auf **null** festgelegt ist. Dieser Parameter stellt die Codierungsoptionen dar und ist dieselbe [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Instanz, die Sie in der Methode " [**kreatenewframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) " für den Decoder auf Container-Ebene erstellt und an den Aufrufer im pIEncoderOptions-Parameter dieser Methode zurückgegeben haben. Zu diesem Zeitpunkt haben Sie die IPropertyBag2-Struktur mit Eigenschaften aufgefüllt, die die Codierungsoptionen darstellen, die von Ihrem Encoder auf Frame-Ebene unterstützt werden. Der Aufrufer hat nun Werte für diese Eigenschaften bereitgestellt, um bestimmte Codierungs Optionsparameter anzugeben, und übergibt das gleiche Objekt an Sie zurück, um das **IWICBitmapFrameEncode** -Objekt zu initialisieren. Beim Codieren der Bildbits sollten Sie die angegebenen Optionen anwenden.

### <a name="setsize-and-setresolution"></a>SetSize und SetResolution

[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) und [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) sind selbsterklärend. Der Aufrufer verwendet diese Methoden, um die Größe und Auflösung für das codierte Bild anzugeben.

### <a name="setpixelformat"></a>SetPixelFormat

[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) wird verwendet, um ein Pixel Format anzufordern, in dem das Bild codiert werden soll. Wenn das angeforderte Pixel Format nicht unterstützt wird, sollten Sie die GUID des nächstgelegenen Pixel Formats zurückgeben, das in *pPixelFormat* unterstützt wird. Hierbei handelt es sich um einen in/out-Parameter.

### <a name="setcolorcontexts"></a>Setcolorkontexte

[**Setcolorkontexte**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) dient zum Angeben eines oder mehrerer gültiger Farb Kontexte (auch als Farbprofile bezeichnet) für dieses Bild. Es ist wichtig, die Farb Kontexte anzugeben, sodass eine Anwendung, die das Image zu einem späteren Zeitpunkt decodiert, vom Quell Farbprofil in das Ziel Profil des Geräts konvertiert werden kann, das zum Anzeigen oder Drucken des Bilds verwendet wird. Ohne ein Farbprofil ist es nicht möglich, konsistente Farben auf verschiedenen Geräten zu erhalten. Dies kann für Endbenutzer frustrierend sein, wenn Ihre Fotos auf verschiedenen Monitoren anders aussehen, und Sie können die Druckvorgänge nicht so erhalten, wie Sie auf dem Bildschirm angezeigt werden.

### <a name="getmetadataquerywriter"></a>GetMetadataQueryWriter

[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) gibt eine [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) zurück, die eine Anwendung verwenden kann, um bestimmte Metadateneigenschaften in einem Metadatenblock im Bild Rahmen einzufügen oder zu bearbeiten.

Sie können eine [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) aus [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) auf verschiedene Weise instanziieren. Sie können Sie entweder von Ihrer [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)aus erstellen, und zwar auf dieselbe Weise wie [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) von einem [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in der [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) -Methode der [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Schnittstelle aus erstellt wurde.


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



Sie können Sie auch aus einem vorhandenen [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)erstellen, z. b. mit dem, der mit der vorherigen Methode abgerufen wurde.


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



Mit dem *pguidVendor* -Parameter können Sie einen bestimmten Anbieter angeben, den der Abfrage Schreiber beim Instanziieren eines metadatenwriters verwenden soll. Wenn Sie z. b. eigene metadatenwriter bereitstellen, möchten Sie möglicherweise Ihre eigene GUID für den Anbieter angeben. Sie können **null** an diesen Parameter übergeben, wenn Sie nicht über eine bevorzugte Einstellung verfügen.

### <a name="setthumbnail"></a>Setminiatur

[**Setminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) wird verwendet, um eine Miniaturansicht bereitzustellen. Alle Bilder sollten eine Miniaturansicht entweder global, in jedem Frame oder beides bereitstellen. Die Methoden **getminiatur** und **setminiatur** sind auf Container Ebene optional, aber wenn ein Codec wincodec \_ Err \_ codecnominiatur aus der [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) -Methode zurückgibt, ruft die Windows Imaging Component (WIC) die [**getminiatur**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) -Methode für Frame 0 auf. Wenn an keinem Ort eine Miniaturansicht gefunden wird, muss WIC das vollständige Image decodieren und es auf die Miniatur Ansichts Größe skalieren, was bei größeren Images zu einer hohen Leistungs Einbuße kommen könnte.

Die Miniaturansicht sollte eine Größe und Auflösung aufweisen, die Sie schnell decodieren und anzeigen kann. Aus diesem Grund sind Miniaturansichten am häufigsten JPEG-Bilder. Beachten Sie Folgendes: Wenn Sie JPEG für Ihre Miniaturansichten verwenden, müssen Sie keinen JPEG-Encoder schreiben, um Sie zu codieren, oder einen JPEG-Decoder zum Decodieren. Sie sollten immer an den JPEG-CODEC delegieren, der in der WIC-Plattform zum Codieren und Decodieren von Miniaturansichten enthalten ist.

### <a name="writepixels"></a>"WritePixels"

" [**Write Pixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) " ist die Methode, mit der Scan Zeilen aus einer Bitmap im Arbeitsspeicher für die Codierung übergeben werden. Die-Methode wird wiederholt aufgerufen, bis alle Überprüfungs Zeilen übermittelt wurden. Der *LineCount* -Parameter gibt an, wie viele Scan Zeilen in diesem-Befehl geschrieben werden sollen. Der *cbStride* -Parameter gibt die Anzahl der Bytes pro Scan Zeile an. *cbBufferSize* gibt die Größe des Puffers an, der im pbPixels-Parameter übergeben wird, der die eigentlichen zu codierenden Bildbits enthält. Wenn die kombinierte Höhe der Scan Zeilen von kumulativen Aufrufen größer als die in der [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) -Methode angegebene Höhe ist, wird wincodec \_ Err \_ toomanyscanlines zurückgegeben.

Wenn [**wicbitmapcodercacheoption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) den Wert **wicbitmapcodercacheinmemory** hat, sollten die Scan Zeilen im Arbeitsspeicher zwischengespeichert werden, bis alle Überprüfungs Zeilen übergeben wurden. Wenn die Encoder-Cache-Option **wicbitmapcodercachetempfile** ist, sollten die Überprüfungs Zeilen in einer temporären Datei zwischengespeichert werden, die beim Initialisieren des Objekts erstellt wird. In jedem dieser Fälle sollte das Bild erst codiert werden, wenn der Aufrufer den [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit)aufruft. Wenn die Cache Option **wicbitmapcodernocache** ist, sollte der Encoder die Überprüfungs Zeilen nach Möglichkeit codieren, sobald Sie empfangen werden. (In manchen Formaten ist dies nicht möglich, und die Scan Zeilen müssen zwischengespeichert werden, bis Commit aufgerufen wird.)

Die meisten Rohdaten CODECs implementieren keine [**Beschreib tepixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), da Sie das Ändern der Bildbits in der Rohdatendatei nicht unterstützen. Unformatierte Codecs sollten jedoch immer noch " **Write Pixels**" implementieren, denn wenn Metadaten hinzugefügt werden, kann die Größe der Datei erhöht werden, sodass die Datei auf dem Datenträger neu geschrieben werden muss. In diesem Fall müssen die vorhandenen Bildbits kopiert werden können. Dies ist die Methode der Methode " **Write** ".

### <a name="writesource"></a>Schreibgeschützte Datenquelle

" [**Write-ource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) " wird verwendet, um ein [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Objekt zu codieren. Der erste Parameter ist ein Zeiger auf ein **IWICBitmapSource** -Objekt. Der zweite Parameter ist ein WICRect, das den zu codierenden Bereich angibt. Diese Methode kann mehrmals nacheinander aufgerufen werden, solange die Breite jedes Rechtecks dieselbe Breite des zu codierenden endgültigen Bilds hat. Wenn die Breite des Rechtecks, das in den PRC-Parameter übergeben wird, von der in der SetSize-Methode angegebenen Breite abweicht, wird wincodec \_ Err \_ sourcerectdoesnotmatchdimensions zurückgegeben. Wenn die kombinierte Höhe der Scan Zeilen von kumulativen Aufrufen größer als die in der SetSize-Methode angegebene Höhe ist, wird wincodec \_ Err \_ toomanyscanlines zurückgegeben.

Die Cache Optionen funktionieren mit dieser Methode genauso wie mit der zuvor beschriebenen Methode " [**Write Pixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) ".

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) ist die Methode, die die codierten Bildbits in den Dateistream serialisiert und alle metadatenwriter für den Frame durchläuft, der Sie anfordert, ihre Metadaten in den Stream zu serialisieren. Wenn die Encoder-Cache-Option "wicbitmapcodercacheinmemory" oder "wicbitmapcodercachetempfile" ist, ist diese Methode auch für das Codieren des Bilds zuständig. wenn die Cache Option "wicbitmapcodercachetempfile" ist, sollte die **Commit** -Methode auch die temporäre Datei löschen, die zum

Diese Methode wird immer aufgerufen, nachdem alle Scan Zeilen oder Rechtecke, die das Bild bilden, mithilfe der [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) -oder der [**Write-ource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) -Methode übergeben wurden. Die Größe des abschließenden Rechtecks, das durch die akkumulierten Aufrufe von "Write-Pixels" oder "Write-ource" besteht, muss dieselbe Größe aufweisen wie in der SetSize-Methode. Wenn die Größe nicht der erwarteten Größe entspricht, sollte diese Methode wincodecerror \_ unexpectedsize zurückgeben.

Um die metadatenwriter zu durchlaufen und jeden metadatenwriter anzuweisen, seine Metadaten zu serialisieren, rufen Sie den Stream auf, rufen Sie GetWriterByIndex auf, um die Writer für jeden Block zu durchlaufen, und rufen Sie IWICPersistStream. Save für jeden metadatenwriter auf.


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a>SetPalette

Nur Codecs mit indizierten Formaten müssen die [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) -Methode implementieren. Wenn ein Bild ein indiziertes Format verwendet, verwenden Sie diese Methode, um die Palette der Farben anzugeben, die im Bild verwendet werden. Wenn Ihr CODEC kein indiziertes Format hat, geben Sie wincodec \_ Err \_ palettenicht aus dieser Methode zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Implementieren von IWICBitmapCodecProgressNotification (Encoder)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Implementieren von IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
