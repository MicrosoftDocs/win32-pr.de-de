---
description: Implementieren von IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implementieren von IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865548"
---
# <a name="implementing-iwicmetadatablockreader"></a>Implementieren von IWICMetadataBlockReader

## <a name="iwicmetadatablockreader"></a>IWICMetadataBlockReader

Häufig sind mehrere Metadatenblöcke innerhalb eines Bilds vorhanden, von denen jedes verschiedene Informationstypen in unterschiedlichen Formaten verfügbar macht. Im WIC-Modell (Windows Imaging Component, Windows Imaging Component) handelt es sich bei metadatenhandlern um unterschiedliche Komponenten, die wie Decoders zur Laufzeit erkennbar sind. Jedes Metadatenformat verfügt über einen separaten Handler, und jeder dieser Metadatenhandler kann mit jedem Bildformat verwendet werden, das das von ihm verwendete Metadatenformat unterstützt. Wenn Ihr Bildformat also EXIF, XMP, IPTC oder ein anderes Format unterstützt, können Sie die standardmäßigen Metadatenhandler für diese Formate nutzen, die mit WIC ausgeliefert werden, und Sie müssen keine eigenen schreiben. Wenn Sie ein neues Metadatenformat erstellen, müssen Sie selbstverständlich einen Metadatenhandler dafür schreiben, der zur Laufzeit so erkannt und aufgerufen wird, wie es bei den standardmäßigen der Fall ist.

> [!Note]  
> Wenn Ihr Bildformat auf einem Tagged Image File Format (TIFF) oder JPEG-Container basiert, müssen Sie keine Metadatenhandler schreiben (es sei denn, Sie entwickeln ein neues oder proprietäres Metadatenformat). In TIFF-und JPEG-Containern befinden sich Metadatenblöcke innerhalb von ifds, und jeder Container hat eine andere IFD-Struktur. WIC stellt IFD-Handler für beide Containerformate bereit, die in der IFD-Struktur navigieren und an die standardmetadatenhandler delegiert werden, um auf die darin enthaltenen Metadaten zuzugreifen. Wenn Ihr Bildformat also auf einem dieser Container basiert, können Sie die WIC-IFD-Handler automatisch nutzen. Wenn Sie jedoch über ein proprietäres Containerformat verfügen, das über eine eigene, eindeutige Metadatenstruktur der obersten Ebene verfügt, müssen Sie einen Handler schreiben, der in der Struktur der obersten Ebene navigieren und an die entsprechenden Metadaten-Handler delegieren kann, genau wie bei den IFD-Handlern.)

 

Die gleiche Art und Weise, wie WIC eine Abstraktions Ebene für Anwendungen bereitstellt, die Ihnen das Arbeiten mit allen Bildformaten auf die gleiche Weise durch einen konsistenten Satz von Schnittstellen ermöglicht, stellt WIC eine Abstraktions Ebene für Codec-Autoren in Bezug auf Metadatenformate bereit. Wie bereits erwähnt, müssen Codec-Autoren in der Regel nicht direkt mit den verschiedenen Metadatenformaten arbeiten, die möglicherweise in einem Bild vorhanden sind. Jeder Codec-Autor ist jedoch dafür zuständig, die Metadatenblöcke aufzuzählen, damit ein geeigneter Metadatenhandler für jeden Block ermittelt und instanziiert werden kann.

Sie müssen diese Schnittstelle für die Decodierung der Frame-Ebene implementieren. Sie müssen Sie möglicherweise auch in Ihrer Decoder-Klasse auf Container-Ebene implementieren, wenn Ihr Bildformat globale Metadaten außerhalb einzelner Bild Rahmen verfügbar macht.

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [GetContainerFormat](#getcontainerformat)
-   [GetCount](#getcount)
-   [GetEnumerator](#getenumerator)
-   [GetReaderByIndex](#getreaderbyindex)

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) ist identisch mit der Methode [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) bei der [Implementierung von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getcount"></a>GetCount

" [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) " gibt die Anzahl der Metadatenblöcke auf oberster Ebene zurück, die dem Frame zugeordnet sind.

### <a name="getenumerator"></a>GetEnumerator

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) gibt einen Enumerator zurück, der vom Aufrufer verwendet werden kann, um die Metadatenblöcke im Frame aufzulisten und ihre Metadaten zu lesen. Zum Implementieren dieser Methode müssen Sie einen metadatenreader für jeden Metadatenblock erstellen und ein Enumerationsobjekt implementieren, das die Auflistung der metadatenleser auflistet. Das Enumerationsobjekt muss [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) implementieren, damit Sie es in IEnumUnknown umwandeln können, wenn Sie es im Parameter *ppIEnumMetadata* zurückgeben.

Beim Implementieren des enumerationsobjektobjekts können Sie alle metadatenleser erstellen, wenn Sie das [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) -Objekt erstmalig erstellen, oder wenn Sie das Enumerationsobjekt erstmalig erstellen, oder Sie können es verzögert innerhalb der Implementierung der [IEnumUnknown:: Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) -Methode erstellen. In vielen Fällen ist es effizienter, Sie verzögert zu erstellen, aber im folgenden Beispiel werden alle Block Leser im Konstruktor erstellt, um Speicherplatz zu sparen.


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



Um die metadatenleser zu erstellen, verwenden Sie die [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) -Methode. Wenn Sie diese Methode aufrufen, übergeben Sie die GUID des Container Formats im *guidContainerFormat* -Parameter. Wenn Sie den Anbieter für einen metadatenleser bevorzugen, können Sie die GUID Ihres bevorzugten Anbieters im *pguidVendor* -Parameter übergeben. Wenn Ihr Unternehmen beispielsweise Metadatenhandler schreibt und Sie Ihre eigenen, falls vorhanden, verwenden möchten, können Sie die GUID des Anbieters übergeben. In den meisten Fällen würden Sie einfach **null** übergeben und es dem System ermöglichen, den passenden metadatenreader auszuwählen. Wenn Sie einen bestimmten Anbieter anfordern und der Anbieter einen metadatenleser auf dem Computer installiert hat, gibt WIC den Leser dieses Anbieters zurück. Wenn der angeforderte Anbieter jedoch keinen metadatenleser auf dem Computer installiert hat und ein entsprechender metadatenleser verfügbar ist, wird dieser Reader zurückgegeben, auch wenn er nicht vom bevorzugten Anbieter ist. Wenn auf dem Computer kein metadatenleser für den Typ der Metadaten im-Block vorhanden ist, gibt die komponentenfactory den unbekannten Metadatenhandler zurück, der den Metadatenblock als Binary Large Object (BLOB) behandelt und den Metadatenblock aus der Datei deserialisiert, ohne dass versucht wird, ihn zu versuchen.

Führen Sie für den *dwOptions* -Parameter eine OR-Operation zwischen den entsprechenden [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) -Vorgängen mit der entsprechenden [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)aus. Die **WICPersistOptions** beschreiben, wie Ihr Container angelegt wird. Der Standardwert ist Little--in.

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

[**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) geben Sie an, ob Sie den UnknownMetadataHandler zurückerhalten möchten, wenn auf dem Computer kein metadatenleser gefunden wird, der das Metadatenformat eines bestimmten Blocks lesen kann. **WICMetadataCreationAllowUnknown** ist die Standardeinstellung, und Sie sollten immer die Erstellung des UnknownMetadtataHandler zulassen. Der UnknownMetadataHandler behandelt nicht erkannte Metadaten als BLOB. Sie kann Sie nicht analysieren, sondern schreibt Sie als BLOB in den Stream und speichert sie intakt, wenn Sie während der Codierung in den Stream zurückgeschrieben wird. Dadurch ist es sicher, Metadatenhandler für proprietäre Metadaten oder Metadatenformate zu erstellen, die nicht mit dem System ausgeliefert werden. Da Metadaten intakt bleiben, sind die Metadaten weiterhin vorhanden und können gelesen werden, auch wenn kein Handler auf dem Computer vorhanden ist, der Sie erkennt, wenn ein entsprechender Metadatenhandler später installiert wird. Wenn Sie die Erstellung des UnknownMetadataHandler nicht zulassen, besteht die Alternative darin, nicht erkannte Metadaten zu verwerfen oder zu überschreiben. Dies ist eine Form von Datenverlusten.

> [!Note]  
> Wenn Sie einen eigenen Metadatenhandler für proprietäre Metadaten schreiben, sollten Sie keine Verweise auf etwas außerhalb des Metadatenblocks selbst einschließen. Obwohl UnknownMetadataHandler die Metadaten intakt behält, werden die Metadaten beim Bearbeiten von Dateien verschoben, und alle Verweise auf Elemente außerhalb des eigenen Blocks sind in diesem Fall nicht mehr gültig.

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

Der *pIStream* -Parameter ist der tatsächliche Datenstrom, den Sie decodieren. Bevor Sie den Stream übergeben, sollten Sie am Anfang des Metadatenblocks suchen, für den Sie einen Reader anfordern. Der entsprechende metadatenleser für den Metadatenblock an der aktuellen Position im [IStream](/windows/desktop/api/objidl/nn-objidl-istream) wird im *ppiReader* -Parameter zurückgegeben.

### <a name="getreaderbyindex"></a>GetReaderByIndex

[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) gibt den metadatenreader am angeforderten Index in der Auflistung zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Licher**
</dt> <dt>

[Implementieren von IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Implementieren von IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
