---
description: Implementieren von IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implementieren von IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbb32ca6bf5ce0714c06a6f355c319908c6dd3a61b1ac27f6baf13f6285183ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772260"
---
# <a name="implementing-iwicmetadatablockreader"></a>Implementieren von IWICMetadataBlockReader

## <a name="iwicmetadatablockreader"></a>Iwicmetadatablockreader

In einem Bild sind häufig mehrere Metadatenblöcke vorhanden, die jeweils unterschiedliche Arten von Informationen in unterschiedlichen Formaten verfügbar machen. Im Windows Imaging Component (WIC)-Modell sind Metadatenhandler unterschiedliche Komponenten, die wie Decoder zur Laufzeit erkennbar sind. Jedes Metadatenformat verfügt über einen separaten Handler, und jeder dieser Metadatenhandler kann mit jedem Bildformat verwendet werden, das das verarbeitete Metadatenformat unterstützt. Wenn Ihr Imageformat EXIF, XMP, IPTC oder ein anderes Format unterstützt, können Sie daher die Standardmetadatenhandler für diese Formate nutzen, die in WIC enthalten sind, und Sie müssen keine eigenen schreiben. Wenn Sie ein neues Metadatenformat erstellen, müssen Sie dafür natürlich einen Metadatenhandler schreiben, der zur Laufzeit wie die Standardhandler gefunden und aufgerufen wird.

> [!Note]  
> Wenn Ihr Bildformat auf einem Tagged Image File Format-Container (TIFF) oder JPEG-Container basiert, müssen Sie keine Metadatenhandler schreiben (es sei denn, Sie entwickeln ein neues oder proprietäres Metadatenformat). In TIFF- und JPEG-Containern befinden sich Metadatenblöcke innerhalb von IFDs, und jeder Container hat eine andere IFD-Struktur. WIC stellt IFD-Handler für beide Containerformate bereit, die durch die IFD-Struktur navigieren und an die Standardmetadatenhandler delegieren, um auf die metadaten in ihnen zugreifen zu können. Wenn Ihr Imageformat also auf einem dieser Container basiert, können Sie automatisch die WIC IFD-Handler nutzen. Wenn Sie jedoch über ein proprietäres Containerformat verfügen, das über eine eigene eindeutige Metadatenstruktur auf oberster Ebene verfügt, müssen Sie einen Handler schreiben, der durch diese Struktur der obersten Ebene navigieren und an die entsprechenden Metadatenhandler delegieren kann, genau wie die IFD-Handler.)

 

Genauso wie WIC eine Abstraktionsebene für Anwendungen bietet, die es ihnen ermöglicht, mit allen Bildformaten auf die gleiche Weise über einen konsistenten Satz von Schnittstellen zu arbeiten, bietet WIC eine Abstraktionsebene für Codecautoren in Bezug auf Metadatenformate. Wie bereits erwähnt, müssen Codecautoren in der Regel nicht direkt mit den verschiedenen Metadatenformaten arbeiten, die möglicherweise in einem Bild vorhanden sind. Jeder Codecautor ist jedoch dafür verantwortlich, eine Möglichkeit zum Aufzählen der Metadatenblöcke zu bieten, damit ein geeigneter Metadatenhandler für jeden Block gefunden und instanziiert werden kann.

Sie müssen diese Schnittstelle in Ihrer Decodierungsklasse auf Frameebene implementieren. Möglicherweise müssen Sie sie auch in ihrer Decoderklasse auf Containerebene implementieren, wenn ihr Bildformat globale Metadaten außerhalb einzelner Bildrahmen verfügbar macht.

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
-   [Getenumerator](#getenumerator)
-   [GetReaderByIndex](#getreaderbyindex)

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat entspricht**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) der [GetContainerFormat-Methode](-wic-imp-iwicbitmapdecoder.md) unter [Implementing IWICBitmapDecoder ( Implementieren von IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)).

### <a name="getcount"></a>GetCount

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) gibt die Anzahl der Metadatenblöcke der obersten Ebene zurück, die dem Frame zugeordnet sind.

### <a name="getenumerator"></a>GetEnumerator

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) gibt einen Enumerator zurück, mit dem der Aufrufer die Metadatenblöcke im Frame aufzählen und deren Metadaten lesen kann. Um diese Methode zu implementieren, müssen Sie einen Metadatenreader für jeden Metadatenblock erstellen und ein Enumerationsobjekt implementieren, das die Auflistung von Metadatenlesern aufzählt. Das Enumerationsobjekt muss [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) implementieren, damit Sie es in IEnumUnknown casten können, wenn Sie es im *ppIEnumMetadata-Parameter* zurückgeben.

Beim Implementieren des Enumerationsobjekts können Sie alle Metadatenleser erstellen, wenn Sie das [**IWICMetadataBlockReader-Objekt**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) zum ersten Mal erstellen oder wenn Sie das Enumerationsobjekt erstmalig erstellen, oder Sie können sie in der Implementierung der [IEnumUnknown::Next-Methode](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) lazily erstellen. In vielen Fällen ist es effizienter, sie zu erstellen, aber im folgenden Beispiel werden alle Blockleser im Konstruktor erstellt, um Speicherplatz zu sparen.


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



Zum Erstellen der Metadatenleser verwenden Sie die [**CreateMetadataReaderFromContainer-Methode.**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) Wenn Sie diese Methode aufrufen, übergeben Sie die GUID des Containerformats im *GuidContainerFormat-Parameter.* Wenn Sie den Anbieter für einen Metadatenleser bevorzugen, können Sie die GUID Ihres bevorzugten Anbieters im *pGuidVendor-Parameter* übergeben. Wenn Ihr Unternehmen z. B. Metadatenhandler schreibt und Sie, falls vorhanden, Ihre eigenen verwenden möchten, können Sie die GuiD Ihres Herstellers übergeben. In den meisten Fällen würden Sie einfach NULL **übergeben** und das System den entsprechenden Metadatenleser auswählen lassen. Wenn Sie einen bestimmten Anbieter anfordern und auf dem Computer ein Metadatenleser installiert ist, gibt WIC den Reader dieses Anbieters zurück. Wenn der angeforderte Anbieter jedoch keinen Metadatenleser auf dem Computer installiert hat und ein entsprechender Metadatenleser verfügbar ist, wird dieser Reader zurückgegeben, auch wenn er nicht vom bevorzugten Anbieter ist. Wenn auf dem Computer kein Metadatenleser für den Typ der Metadaten im -Block enthalten ist, gibt die Komponenten-Factory den Unknown Metadata Handler zurück, der den Metadatenblock als Blob (Binary Large Object) behandelt und den Metadatenblock aus der Datei deserialisiert, ohne ihn zu analysen.

Führen Sie *für den dwOptions-Parameter* einen OR-Vorgang zwischen den entsprechenden [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) mit dem entsprechenden [**WICMetadataCreationOptions aus.**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) Die **WICPersistOptions beschreiben,** wie Ihr Container angelegt wird. Little-Endian ist die Standardeinstellung.

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

Die [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) geben an, ob Der UnknownMetadataHandler zurückerlangt werden soll, wenn kein Metadatenleser auf dem Computer gefunden wird, der das Metadatenformat eines bestimmten Blocks lesen kann. **WICMetadataCreationAllowUnknown** ist die Standardeinstellung, und Sie sollten immer die Erstellung des UnknownMetadtataHandler zulassen. UnknownMetadataHandler behandelt nicht unbekannte Metadaten als BLOB. Er kann ihn nicht analysieren, schreibt ihn jedoch als BLOB in den Stream und bleibt erhalten, wenn er während der Codierung in den Stream zurückgeschrieben wird. Dies macht es sicher, Metadatenhandler für proprietäre Metadaten oder Metadatenformate zu erstellen, die nicht im System enthalten sind. Da Metadaten intakt beibehalten werden, auch wenn kein Handler auf dem Computer vorhanden ist, der sie erkennt, sind die Metadaten weiterhin vorhanden und können gelesen werden, wenn später ein entsprechender Metadatenhandler installiert wird. Wenn Sie die Erstellung des UnknownMetadataHandler nicht zulassen, ist die Alternative das Verwerfen oder Überschreiben nicht unbekannter Metadaten. Dies ist eine Form des Datenverlusts.

> [!Note]  
> Wenn Sie einen eigenen Metadatenhandler für proprietäre Metadaten schreiben, sollten Sie niemals Verweise auf etwas außerhalb des Metadatenblocks selbst hinzufügen. Obwohl der UnknownMetadataHandler Metadaten intakt beibewahrt, werden Metadaten verschoben, wenn Dateien bearbeitet werden, und alle Verweise auf etwas außerhalb des eigenen Blocks sind in diesem Fall nicht mehr gültig.

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

Der *pIStream-Parameter* ist der tatsächliche Stream, den Sie decodieren. Bevor Sie den Stream übergeben, sollten Sie am Anfang des Metadatenblocks suchen, für den Sie einen Reader anfordern. Der entsprechende Metadatenleser für den Metadatenblock an der aktuellen Position im [IStream](/windows/desktop/api/objidl/nn-objidl-istream) wird im *Parameter reader zurückgegeben.*

### <a name="getreaderbyindex"></a>GetReaderByIndex

[**GetReaderByIndex gibt**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) den Metadatenleser am angeforderten Index in der Auflistung zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Iwicmetadatablockreader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Implementieren von IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Implementieren von IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
