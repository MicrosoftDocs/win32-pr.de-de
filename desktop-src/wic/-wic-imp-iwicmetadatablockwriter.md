---
description: Implementieren von IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: Implementieren von IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530269"
---
# <a name="implementing-iwicmetadatablockwriter"></a>Implementieren von IWICMetadataBlockWriter

## <a name="iwicmetadatablockwriter"></a>IWICMetadataBlockWriter

-   [InitializeFromBlockReader](#initializefromblockreader)
-   ["Getschreiterbyindex"](#getwriterbyindex)
-   [AddWriter](#addwriter)
-   [Setschreiterbyindex](#setwriterbyindex)
-   [Removeschreiterbyindex](#removewriterbyindex)

Die Codierungs Klasse auf Frame-Ebene implementiert diese Schnittstelle, um alle Metadatenblöcke verfügbar zu machen und den entsprechenden metadatenwriter für jeden Block anzufordern. Wenn Ihr Bildformat globale Metadaten außerhalb eines einzelnen Frames unterstützt, sollten Sie diese Schnittstelle auch in der Encoder-Klasse auf Container-Ebene implementieren. Eine ausführlichere Erläuterung von metadatenhandlern finden Sie im Abschnitt [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) im Abschnitt über die Implementierung eines WIC-Enabled Decoders.

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

[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) verwendet ein [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) , um den blockwriter zu initialisieren. Sie können den **IWICMetadataBlockReader** aus dem Decoder, der das Bild decodiert hat, erhalten.


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



Da die Initialisierung des [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) mit einem [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) einen metadatenwriter für jeden metadatenreader instanziiert, der vom **IWICMetadataBlockReader** -Objekt verfügbar gemacht wird, muss die Anwendung einen Writer nicht explizit für jeden Metadatenblock anfordern.

### <a name="getwriterbyindex"></a>"Getschreiterbyindex"

[**Getschreiterbyindex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) gibt das [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) -Objekt für den ten-Metadatenblock zurück, wobei n der Wert ist, der im *nIndex* -Parameter übergeben wird. Wenn kein metadatenwriter registriert ist, der den Typ der Metadaten im ten-Block verarbeiten kann, gibt die komponentenfactory den unbekannten Metadatenhandler zurück, der den Metadatenblock als Binary Large Object (BLOB) behandelt. Sie wird als Bitstream serialisiert, ohne zu versuchen, Sie zu analysieren.

### <a name="addwriter"></a>AddWriter

[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) ermöglicht einem Aufrufer, einen neuen metadatenwriter hinzuzufügen. Dies ist erforderlich, wenn eine Anwendung Metadaten eines anderen Formats als einen der vorhandenen Metadatenblöcke hinzufügen möchte. Beispielsweise kann eine Anwendung einige XMP-Metadaten hinzufügen. Wenn kein vorhandener XMP-Metadatenblock vorhanden ist, muss die Anwendung einen XMP-metadatenwriter instanziieren und die **AddWriter** -Methode verwenden, um Sie in die Auflistung von metadatenwritern einzubeziehen.

### <a name="setwriterbyindex"></a>Setschreiterbyindex

[**Setschreiterbyindex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) wird verwendet, um einen metadatenwriter an einem bestimmten Index in der Auflistung hinzuzufügen. Wenn ein metadatenwriter derzeit an diesem Index vorhanden ist, sollte der neue einen metadatenwriter ersetzen.

### <a name="removewriterbyindex"></a>Removeschreiterbyindex

[**Removeschreiterbyindex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) wird verwendet, um einen metadatenwriter aus der Auflistung zu entfernen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Implementieren von iwicbitmapframecocode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Codec-Installation und-Registrierung](-wic-codecinstallandreg.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



