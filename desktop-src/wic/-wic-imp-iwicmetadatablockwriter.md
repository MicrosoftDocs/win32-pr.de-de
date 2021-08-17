---
description: Implementieren von IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implementieren von IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d49912ece0cc1e3c2299ace0a15f112ef7ab65ac03863b855b8a9ee64e62e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964969"
---
# <a name="implementing-iwicmetadatablockwriter"></a>Implementieren von IWICMetadataBlockWriter

## <a name="iwicmetadatablockwriter"></a>IWICMetadataBlockWriter

-   [InitializeFromBlockReader](#initializefromblockreader)
-   [GetWriterByIndex](#getwriterbyindex)
-   [AddWriter](#addwriter)
-   [SetWriterByIndex](#setwriterbyindex)
-   [RemoveWriterByIndex](#removewriterbyindex)

Die Codierungsklasse auf Frameebene implementiert diese Schnittstelle, um alle Metadatenblöcke verfügbar zu machen und den entsprechenden Metadatenwriter für jeden Block an fordern. Wenn Ihr Bildformat globale Metadaten außerhalb eines einzelnen Frames unterstützt, sollten Sie diese Schnittstelle auch für die Encoderklasse auf Containerebene implementieren. Eine ausführlichere Erläuterung von Metadatenhandlern finden Sie im Abschnitt [**zum IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) im Abschnitt Implementieren eines WIC-Enabled Decoders.

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a>InitializeFromBlockReader

[**InitializeFromBlockReader verwendet**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) [**einen IWICMetadataBlockReader,**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) um den Blockwriter zu initialisieren. Sie können den **IWICMetadataBlockReader** aus dem Decoder erhalten, der das Bild decodiert hat.


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



Da die Initialisierung von [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) mit [**einem IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) einen Metadatenwriter für jeden Metadatenleser instanziiert, der vom **IWICMetadataBlockReader-Objekt** verfügbar gemacht wird, muss die Anwendung nicht explizit einen Writer für jeden Metadatenblock anfordern.

### <a name="getwriterbyindex"></a>GetWriterByIndex

[**GetWriterByIndex gibt**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) das [**IWICMetadataWriter-Objekt**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) für den n-th-Metadatenblock zurück, wobei n der wert ist, der im *nIndex-Parameter übergeben* wird. Wenn kein Metadatenwriter registriert ist, der den Typ der Metadaten im n-th-Block verarbeiten kann, gibt die Komponenten factory den Unknown Metadata Handler zurück, der den Metadatenblock als Blob (Binary Large Object) behandelt. Sie wird als Bitstream serialisiert, ohne zu versuchen, sie zu analysieren.

### <a name="addwriter"></a>AddWriter

[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) ermöglicht einem Aufrufer das Hinzufügen eines neuen Metadatenwriters. Dies ist erforderlich, wenn eine Anwendung Metadaten eines anderen Formats als die vorhandenen Metadatenblöcke hinzufügen möchte. Beispielsweise kann eine Anwendung XMP-Metadaten hinzufügen. Wenn kein XMP-Metadatenblock vorhanden ist, muss die Anwendung einen XMP-Metadatenwriter instanziieren und die **AddWriter-Methode** verwenden, um ihn in die Auflistung der Metadatenschreiber einaufnahme.

### <a name="setwriterbyindex"></a>SetWriterByIndex

[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) wird verwendet, um einen Metadatenwriter an einem bestimmten Index in der Auflistung hinzuzufügen. Wenn an diesem Index derzeit ein Metadatenwriter vorhanden ist, sollte er durch den neuen ersetzt werden.

### <a name="removewriterbyindex"></a>RemoveWriterByIndex

[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) wird verwendet, um einen Metadatenwriter aus der Auflistung zu entfernen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Implementieren von IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[CODEC-Installation und -Registrierung](-wic-codecinstallandreg.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



