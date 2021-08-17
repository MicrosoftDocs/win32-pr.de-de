---
description: In diesem Thema werden die Anforderungen zum Erstellen benutzerdefinierter Metadatenhandler für die Windows Imaging Component (WIC) vorgestellt, einschließlich Metadatenleser und Writer.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Übersicht über die Metadatenerweiterbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d38206fb02c47edbe9744deb6ceb0093277d8354f8717aa89c3f1976bdeb51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088172"
---
# <a name="metadata-extensibility-overview"></a>Übersicht über die Metadatenerweiterbarkeit

In diesem Thema werden die Anforderungen zum Erstellen benutzerdefinierter Metadatenhandler für die Windows Imaging Component (WIC) vorgestellt, einschließlich Metadatenleser und Writer. Außerdem werden die Anforderungen für die Erweiterung der WIC-Laufzeitkomponentenermittlung auf Ihre benutzerdefinierten Metadatenhandler erläutert.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Introduction (Einführung)](#introduction)
-   [Erstellen eines Metadatenlesers](#creating-a-metadata-reader)
    -   [IWICMetadataReader-Schnittstelle](#iwicmetadatareader-interface)
    -   [IWICPersistStream-Schnittstelle](#iwicpersiststream-interface)
    -   [IWICStreamProvider-Schnittstelle](#iwicstreamprovider-interface)
-   [Erstellen eines Metadatenwriters](#creating-a-metadata-writer)
    -   [IWICMetadataWriter-Schnittstelle](#iwicmetadatawriter-interface)
    -   [IWICPersistStream-Schnittstelle](#iwicpersiststream-interface)
    -   [IWICStreamProvider-Schnittstelle](#iwicstreamprovider-interface)
-   [Installieren und Registrieren eines Metadatenhandlers](#installing-and-registering-a-metadata-handler)
    -   [Registrierungsschlüssel für Metadatenhandler](#metadata-handler-registry-keys)
    -   [Metadatenleser](#metadata-readers)
    -   [Metadatenautoren](#metadata-writers)
    -   [Signieren eines Metadatenhandlers](#signing-a-metadata-handler)
-   [Besondere Überlegungen](#special-considerations)
    -   [PROPVARIANTS](#propvariants)
    -   [8BIM-Handler](#8bim-handlers)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie über umfassende Kenntnisse der WIC, ihrer Komponenten und Metadaten für Bilder verfügen. Weitere Informationen zu WIC-Metadaten finden Sie in der [Übersicht über WIC-Metadaten.](-wic-about-metadata.md) Weitere Informationen zu WIC-Komponenten finden Sie in der [Übersicht über Windows Imaging Component](-wic-about-windows-imaging-codec.md).

## <a name="introduction"></a>Einführung

Wie in der [Übersicht über WIC-Metadaten](-wic-about-metadata.md)erläutert, gibt es in einem Bild häufig mehrere Metadatenblöcke, die jeweils verschiedene Informationstypen in unterschiedlichen Metadatenformaten verfügbar machen. Um mit einem in einem Bild eingebetteten Metadatenformat zu interagieren, muss eine Anwendung einen entsprechenden Metadatenhandler verwenden. WIC bietet mehrere Metadatenhandler (sowohl Metadatenleser als auch Writer), mit denen Sie bestimmte Metadatentypen wie Exif oder XMP lesen und schreiben können.

Zusätzlich zu den bereitgestellten nativen Handlern stellt WIC APIs bereit, mit denen Sie neue Metadatenhandler erstellen können, die an der Ermittlung von WIC-Laufzeitkomponenten beteiligt sind. Dadurch können Anwendungen, die WIC verwenden, Ihre benutzerdefinierten Metadatenformate lesen und schreiben.

Mit den folgenden Schritten können Ihre Metadatenhandler an der WIC-Laufzeitmetadatenermittlung teilnehmen.

-   Implementieren Sie eine Metadatenlesehandlerklasse ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)), die die erforderlichen WIC-Schnittstellen zum Lesen Ihres benutzerdefinierten Metadatenformats verfügbar macht. Dadurch können WIC-basierte Anwendungen Ihr Metadatenformat auf die gleiche Weise lesen wie native Metadatenformate.
-   Implementieren Sie eine Metadaten-Writer-Handlerklasse ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)), die die erforderlichen WIC-Schnittstellen zum Codieren Ihres benutzerdefinierten Metadatenformats verfügbar macht. Dadurch können WIC-basierte Anwendungen Ihr Metadatenformat in unterstützte Bildformate serialisieren.
-   Digital signieren und registrieren Sie Ihre Metadatenhandler. Dadurch können Ihre Metadatenhandler zur Laufzeit ermittelt werden, indem das identifizierende Muster in der Registrierung mit dem in der Imagedatei eingebetteten Muster übereinstimmt.

## <a name="creating-a-metadata-reader"></a>Erstellen eines Metadatenlesers

Der Hauptzugriff auf Metadatenblöcke innerhalb eines Codecs erfolgt über die [**IWICMetadataBlockReader-Schnittstelle,**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) die jeder WIC-Codec implementiert. Diese Schnittstelle listet jeden in ein Bildformat eingebetteten Metadatenblock auf, sodass der entsprechende Metadatenhandler ermittelt und für jeden Block instanziiert werden kann. Die Metadatenblöcke, die von WIC nicht erkannt werden, gelten als unbekannt und werden als GUID CLSID \_ WICUnknownMetadataReader definiert. Damit Ihr Metadatenformat von WIC erkannt wird, müssen Sie eine Klasse erstellen, die drei Schnittstellen implementiert: [**IWICMetadataReader,**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)und [**IWICStreamProvider.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider)

> [!Note]  
> Wenn Ihr Metadatenformat Einschränkungen aufweise, die einige Methoden der erforderlichen Schnittstellen ungeeignet machen, sollten diese Methoden WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION zurückgeben.

 

### <a name="iwicmetadatareader-interface"></a>IWICMetadataReader-Schnittstelle

Die [**IWICMetadataReader-Schnittstelle**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) muss beim Erstellen eines Metadatenreaders implementiert werden. Diese Schnittstelle bietet Zugriff auf die Unterlaufmetadatenelemente innerhalb des Datenstroms eines Metadatenformats.

Der folgende Code zeigt die Definition der Metadatenleserschnittstelle, wie in der Datei wincodecsdk.idl definiert.

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

Die **GetMetadataFormat-Methode** gibt die GUID Ihres Metadatenformats zurück.

Die **GetMetadataHandlerInfo-Methode** gibt eine [**IWICMetadataHandlerInfo-Schnittstelle**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) zurück, die Informationen zu Ihrem Metadatenhandler bereitstellt. Dies schließt Informationen ein, z. B. welche Bildformate das Metadatenformat unterstützen und ob Ihr Metadatenleser Zugriff auf den vollständigen Metadatenstream benötigt.

Die **GetCount-Methode** gibt die Anzahl der einzelnen Metadatenelemente (einschließlich eingebetteter Metadatenblöcke) im Metadatenstream zurück.

Die **GetValueByIndex-Methode** gibt ein Metadatenelement nach einem Indexwert zurück. Mit dieser Methode können Anwendungen jedes Metadatenelement in einem Metadatenblock durchlaufen. Der folgende Code veranschaulicht, wie eine Anwendung diese Methode verwenden kann, um jedes Metadatenelement in einem Metadatenblock abzurufen.


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



Die **GetValue-Methode** ruft ein bestimmtes Metadatenelement nach Schema und/oder ID ab. Diese Methode ähnelt der **GetValueByIndex-Methode,** mit der Ausnahme, dass sie ein Metadatenelement abruft, das über ein bestimmtes Schema oder eine bestimmte ID verfügt.

Die **GetEnumerator-Methode** gibt einen Enumerator jedes Metadatenelements im Metadatenblock zurück. Dadurch können Anwendungen einen Enumerator verwenden, um in Ihrem Metadatenformat zu navigieren.

Wenn Ihr Metadatenformat keine Schemas für Metadatenelemente enthält, wird getValue... -Methoden sollten diese Eigenschaft ignorieren. Wenn Ihr Format jedoch die Schemabenennung unterstützt, sollten Sie einen **NULL-Wert** erwarten.

Wenn ein Metadatenelement ein eingebetteter Metadatenblock ist, erstellen Sie einen Metadatenhandler aus dem Unterstream des eingebetteten Inhalts und geben den neuen Metadatenhandler zurück. Wenn kein Metadatenleser für den geschachtelten Block verfügbar ist, instanziieren Sie einen unbekannten Metadatenreader, und geben Sie einen reader zurück. Um einen neuen Metadatenleser für den eingebetteten Block zu erstellen, rufen Sie die **CreateMetadataReaderFromContainer-** oder **CreateMetadataReader-Methoden** der Komponentenfactory auf, oder rufen Sie die [**WICMatchMetadataContent-Funktion**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) auf.

Wenn der Metadatenstream Big-Endian-Inhalte enthält, ist der Metadatenleser für den Austausch aller verarbeiteten Datenwerte verantwortlich. Es ist auch dafür verantwortlich, alle geschachtelten Metadatenleser darüber zu informieren, dass sie mit Big-Endian-Datenströmen arbeiten. Allerdings sollten alle Werte im Little-Endian-Format zurückgegeben werden.

Implementieren Sie Unterstützung für die Namespacenavigation, indem Sie Abfragen unterstützen, bei denen die Metadatenelement-ID `VT_CLSID` eine (GUID) ist, die einem Metadatenformat entspricht. Wenn während der Analyse ein geschachtelter Metadatenleser für dieses Format identifiziert wird, muss er zurückgegeben werden. Dadurch können Anwendungen einen Metadatenabfrageleser verwenden, um Ihr Metadatenformat zu durchsuchen.

Wenn Sie ein Metadatenelement nach ID abrufen, sollten Sie die [PropVariantChangeType-Funktion](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) verwenden, um die ID in den erwarteten Typ einzubetten. Beispielsweise erziert der IFD-Reader eine ID, die mit `VT_UI2` dem Datentyp einer IFD-Tag-ID USHORT übereinstimmt. Der Eingabetyp und der erwartete Typ müssen beide [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) sein, um dies zu tun. Dies ist nicht erforderlich, aber diese Koersion vereinfacht Code, der den Reader aufruft, um Metadatenelemente abzufragen.

### <a name="iwicpersiststream-interface"></a>IWICPersistStream-Schnittstelle

Die [**IWICPersistStream-Schnittstelle**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) erbt von **IPersistStream** und stellt zusätzliche Methoden zum Speichern und Laden von Objekten mithilfe der [**WICPersistOptions-Enumeration**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) bereit.

Der folgende Code zeigt die Definition der [**IWICPersistStream-Schnittstelle,**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) wie in der Datei wincodecsdk.idl definiert.

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

Die **LoadEx-Methode** stellt Ihrem Metadatenleser einen Datenstrom bereit, der Ihren Metadatenblock enthält. Der Reader analysiert diesen Stream, um auf die zugrunde liegenden Metadatenelemente zuzugreifen. Der Metadatenreader wird mit einem Unterstream initialisiert, der sich am Anfang des Rohdateninhalts befindet. Wenn ihr Reader den vollständigen Stream nicht benötigt, ist der Unterstream auf den Inhalt des Metadatenblocks beschränkt. Andernfalls wird der vollständige Metadatenstream mit der Position bereitgestellt, die am Anfang des Metadatenblocks festgelegt ist.

Die **SaveEx-Methode** wird von Metadatenautoren verwendet, um Ihren Metadatenblock zu serialisieren. Wenn **SaveEx** in einem Metadatenreader verwendet wird, sollte WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION zurückgegeben werden.

### <a name="iwicstreamprovider-interface"></a>IWICStreamProvider-Schnittstelle

Die [**IWICStreamProvider-Schnittstelle**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) ermöglicht es Ihrem Metadatenleser, Verweise auf seinen Inhaltsstream bereitzustellen, Informationen zum Stream bereitzustellen und zwischengespeicherte Versionen des Streams zu aktualisieren.

Der folgende Code zeigt die Definition der [**IWICStreamProvider-Schnittstelle,**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) wie in der Datei wincodecsdk.idl definiert.

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

Die **GetStream-Methode** ruft einen Verweis auf Ihren Metadatenstream ab. Für den zurückgegebenen Stream sollte der Streamzeiger auf die Startposition zurückgesetzt werden. Wenn Ihr Metadatenformat vollständigen Streamzugriff erfordert, sollte die Startposition der Anfang Ihres Metadatenblocks sein.

Die **GetPersistOptions-Methode** gibt die aktuellen Optionen des Streams aus der [**WICPersistOptions-Enumeration**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) zurück.

Die **GetPreferredVendorGUID-Methode** gibt die GUID des Anbieters des Metadatenlesers zurück.

Die **RefreshStream-Methode** aktualisiert den Metadatenstream. Diese Methode muss **LoadEx** mit einem **NULL-Stream** für alle geschachtelten Metadatenblöcke aufrufen. Dies ist erforderlich, da geschachtelte Metadatenblöcke und deren Elemente aufgrund der bearbeitungsbasierten Bearbeitung möglicherweise nicht mehr vorhanden sind.

## <a name="creating-a-metadata-writer"></a>Erstellen eines Metadatenwriters

Ein Metadatenwriter ist ein Typ von Metadatenhandler, der eine Möglichkeit bietet, einen Metadatenblock in einen Bildrahmen oder außerhalb eines einzelnen Frames zu serialisieren, wenn dies vom Bildformat unterstützt wird. Der Hauptzugriff auf die Metadatenautoren innerhalb eines Codecs besteht über die [**IWICMetadataBlockWriter-Schnittstelle,**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) die von jedem WIC-Encoder implementiert wird. Mit dieser Schnittstelle können Anwendungen jeden in ein Bild eingebetteten Metadatenblock aufzählen, sodass der entsprechende Metadatenwriter für jeden Metadatenblock gefunden und instanziiert werden kann. Metadatenblöcke, die keinen entsprechenden Metadatenwriter haben, werden als unbekannt betrachtet und als GUID-CLSID \_ WICUnknownMetadataReader definiert. Damit WIC-fähige Anwendungen Ihr Metadatenformat serialisieren und schreiben können, müssen Sie eine Klasse erstellen, die die folgenden Schnittstellen implementiert: [**IWICMetadataWriter,**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) [**IWICMetadataReader,**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)und [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Wenn ihr Metadatenformat Einschränkungen auftrat, die einige Methoden der erforderlichen Schnittstellen ungeeignet machen, sollten diese Methoden WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION zurückgeben.

 

### <a name="iwicmetadatawriter-interface"></a>IWICMetadataWriter-Schnittstelle

Die [**IWICMetadataWriter-Schnittstelle**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) muss vom Metadatenwriter implementiert werden. Da **IWICMetadataWriter** von [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)erbt, müssen Sie außerdem alle Methoden von **IWICMetadataReader implementieren.** Da beide Handlertypen dieselbe Schnittstellenvererbung erfordern, sollten Sie eine einzelne Klasse erstellen, die sowohl Lese- als auch Schreibfunktionen bietet.

Der folgende Code zeigt die Definition der Metadatenwriterschnittstelle, wie in der Datei wincodecsdk.idl definiert.

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

Die **SetValue-Methode** schreibt das angegebene Metadatenelement in den Metadatenstream.

Die **SetValueByIndex-Methode** schreibt das angegebene Metadatenelement in den angegebenen Index im Metadatenstream. Der Index bezieht sich nicht auf die ID, sondern auf die Position des Elements innerhalb des Metadatenblocks.

Die **RemoveValue-Methode** entfernt das angegebene Metadatenelement aus dem Metadatenstream.

Die **RemoveValueByIndex-Methode** entfernt das Metadatenelement am angegebenen Index aus dem Metadatenstream. Nach dem Entfernen eines Elements wird erwartet, dass die verbleibenden Metadatenelemente den leeren Index belegen, wenn der Index nicht der letzte Index ist. Es wird auch erwartet, dass sich die Anzahl ändert, nachdem das Element entfernt wurde.

Es liegt in der Verantwortung des Metadatenwriters, die [PROPVARIANT-Elemente](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in die zugrunde liegende Struktur zu konvertieren, die für Ihr Format erforderlich ist. Im Gegensatz zum Metadatenleser sollten VARIANT-Typen jedoch normalerweise nicht in verschiedene Typen umbettet werden, da der Aufrufer speziell angibt, welcher Datentyp verwendet werden soll.

Der Metadatenwriter muss alle Metadatenelemente in den Bildstream übertragen, einschließlich ausgeblendeter oder nicht unbekannter Werte. Dies schließt unbekannte geschachtelte Metadatenblöcke ein. Es liegt jedoch in der Verantwortung des Encoders, alle wichtigen Metadatenelemente vor dem Initiieren des Speichervorganges zu setzen.

Wenn der Metadatenstream Big-Endian-Inhalte enthält, ist der Metadatenwriter für den Austausch der verarbeiteten Datenwerte verantwortlich. Er ist auch dafür verantwortlich, alle geschachtelten Metadatenautoren darüber zu informieren, dass sie beim Speichern mit einem Big-Endian-Datenstrom arbeiten.

Implementieren Sie Unterstützung für das Erstellen und Entfernen von Namespaces, indem Sie Set- und Remove-Vorgänge für Metadatenelemente mit einem Typ von (einer GUID) unterstützen, der `VT_CLSID` einem Metadatenformat entspricht. Der Metadatenwriter ruft die [**WICSerializeMetadataContent-Funktion**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) auf, um den geschachtelten Metadatenwriterinhalt ordnungsgemäß in den übergeordneten Metadatenwriter zu einbetten.

Wenn Ihr Metadatenformat die in-place-Codierung unterstützt, sind Sie für die Verwaltung der erforderlichen Auf padding verantwortlich. Weitere Informationen zur in-place-Codierung finden Sie unter [Übersicht über WIC-Metadaten](-wic-about-metadata.md) und [Übersicht über das Lesen und Schreiben von Bildmetadaten.](-wic-codec-readingwritingmetadata.md)

### <a name="iwicpersiststream-interface"></a>IWICPersistStream-Schnittstelle

Die [**IWICPersistStream-Schnittstelle**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) erbt **von IPersistStream** und stellt zusätzliche Methoden zum Speichern und Laden von Objekten mithilfe der [**WICPersistOptions-Enumeration**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) bereit.

Der folgende Code zeigt die Definition der [**IWICPersistStream-Schnittstelle**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) gemäß der Definition in der Datei wincodecsdk.idl.

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

Die **LoadEx-Methode** stellt ihrem Metadatenhandler einen Datenstrom bereit, der Ihren Metadatenblock enthält.

Die **SaveEx-Methode** serialisiert die Metadaten in einen Stream. Wenn der bereitgestellte Stream mit dem Initialisierungsstream identisch ist, sollten Sie eine in-place-Codierung durchführen. Wenn die in-place-Codierung unterstützt wird, sollte diese Methode WINCODEC \_ ERR TOOMUCHMETADATA zurückgeben, wenn nicht genügend Auf padding zum Ausführen der direkt \_ codierten Daten besteht. Wenn die in-place-Codierung nicht unterstützt wird, sollte diese Methode WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION zurückgeben.

Die **IPersistStream::GetSizeMax-Methode** muss implementiert werden und muss die genaue Größe des Metadateninhalts zurückgeben, der beim nachfolgenden Speichern geschrieben wird.

Die **IPersistStream::IsDirty-Methode** sollte implementiert werden, wenn der Metadatenwriter über einen Stream initialisiert wird, damit ein Bild zuverlässig bestimmen kann, ob sich sein Inhalt geändert hat.

Wenn Ihr Metadatenformat geschachtelte Metadatenblöcke unterstützt, sollte Der Metadatenwriter beim Speichern in einem Stream die Serialisierung des Inhalts an die geschachtelten Metadatenschreiber delegieren.

### <a name="iwicstreamprovider-interface"></a>IWICStreamProvider-Schnittstelle

Die Implementierung der [**IWICStreamProvider-Schnittstelle**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) für einen Metadatenwriter ist mit der eines Metadatenlesers identisch. Weitere Informationen finden Sie im Abschnitt Erstellen eines Metadatenlesers in diesem Dokument.

## <a name="installing-and-registering-a-metadata-handler"></a>Installieren und Registrieren eines Metadatenhandlers

Um einen Metadatenhandler zu installieren, müssen Sie die Handler-Assembly bereitstellen und in der Systemregistrierung registrieren. Sie können entscheiden, wie und wann die Registrierungsschlüssel aufgefüllt werden.

> [!Note]  
> Zur Schreibgeschütztkeit werden die tatsächlichen hexadezimalen GUIDs nicht in den Registrierungsschlüsseln angezeigt, die in den folgenden Abschnitten dieses Dokuments gezeigt werden. Den Hexadezimalwert für einen angegebenen Benutzernamen finden Sie in den Dateien wincodec.idl und wincodecsdk.idl.

 

### <a name="metadata-handler-registry-keys"></a>Registrierungsschlüssel für Metadatenhandler

Jeder Metadatenhandler wird durch eine eindeutige CLSID identifiziert, und jeder Handler muss seine CLSID unter der Kategorie-ID-GUID des Metadatenhandlers registrieren. Die Kategorie-ID jedes Handlertyps wird in wincodec.idl definiert. Der Kategorie-ID-Name für Reader ist CATID WICMetadataReader, und der Kategorie-ID-Name für Writer \_ ist CATID \_ WICMetadataWriter.

Jeder Metadatenhandler wird durch eine eindeutige CLSID identifiziert, und jeder Handler muss seine CLSID unter der Kategorie-ID-GUID des Metadatenhandlers registrieren. Die Kategorie-ID jedes Handlertyps wird in wincodec.idl definiert. Der Kategorie-ID-Name für Reader ist CATID WICMetadataReader, und der Kategorie-ID-Name für Writer \_ ist CATID \_ WICMetadataWriter.

> [!Note]  
> In den folgenden Registrierungsschlüsselauflistungen bezieht sich {Reader CLSID} auf die eindeutige CLSID, die Sie für Ihren Metadatenleser bereitstellen. {Writer CLSID} bezieht sich auf die eindeutige CLSID, die Sie für Ihren Metadatenwriter bereitstellen. {Handler CLSID} bezieht sich auf die CLSID des Readers, die CLSID des Writers oder beides, je nachdem, welche Handler Sie bereitstellen. {Container GUID} bezieht sich auf das Containerobjekt (Bildformat oder Metadatenformat), das den Metadatenblock enthalten kann.

 

Die folgenden Registrierungsschlüssel registrieren Ihren Metadatenhandler bei den anderen verfügbaren Metadatenhandlern:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

Zusätzlich zum Registrieren ihrer Handler in ihren jeweiligen Kategorien müssen Sie auch zusätzliche Schlüssel registrieren, die spezifische Informationen für den Handler bereitstellen. Leser und Writer haben ähnliche Registrierungsschlüsselanforderungen. Die folgende Syntax zeigt, wie ein Handler registriert wird. Sowohl der Readerhandler als auch der Writer-Handler müssen auf diese Weise registriert werden, indem die entsprechenden CLSIDs verwendet werden:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a>Metadatenleser

Die Registrierung des Metadatenlesers enthält auch Schlüssel, die beschreiben, wie der Reader in ein Containerformat eingebettet werden kann. Ein Containerformat kann ein Bildformat wie TIFF oder JPEG sein. es kann auch ein anderes Metadatenformat sein, z. B. ein IFD-Metadatenblock. Nativ unterstützte Imagecontainerformate werden in wincodec.idl aufgeführt. Jedes Imagecontainerformat wird als GUID mit einem Namen definiert, der mit GUID \_ ContainerFormat beginnt. Nativ unterstützte Metadatencontainerformate werden in wincodecsdk.idl aufgeführt. Jedes Metadatencontainerformat wird als GUID mit einem Namen definiert, der mit GUID \_ MetadataFormat beginnt.

Die folgenden Schlüssel registrieren einen Container, den der Metadatenleser unterstützt, und die Daten, die zum Lesen aus diesem Container erforderlich sind. Jeder vom Reader unterstützte Container muss auf diese Weise registriert werden.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

Der Musterschlüssel beschreibt das binäre Muster, das verwendet wird, um den Metadatenblock dem Reader zu entsprechen. Beim Definieren eines Musters für Ihren Metadatenleser sollte es zuverlässig genug sein, dass eine positive Übereinstimmung bedeutet, dass der Metadatenleser die Metadaten im zu verarbeitenden Metadatenblock verstehen kann.

Der DataOffset-Schlüssel beschreibt den festen Offset der Metadaten aus dem Blockheader. Dieser Schlüssel ist optional und bedeutet, dass die tatsächlichen Metadaten nicht mit einem festen Offset vom Blockheader gefunden werden können, wenn sie nicht angegeben werden.

### <a name="metadata-writers"></a>Metadaten-Writer

Die Registrierung des Metadatenwriters enthält auch Schlüssel, die beschreiben, wie der Header vor dem Metadateninhalt geschrieben wird, der in ein Containerformat eingebettet ist. Wie beim Reader kann ein Containerformat ein Bildformat oder ein anderer Metadatenblock sein.

Die folgenden Schlüssel registrieren einen Container, den der Metadatenwriter unterstützt, sowie die Daten, die zum Schreiben des Headers und der Metadaten erforderlich sind. Jeder vom Writer unterstützte Container muss auf diese Weise registriert werden.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

Der WriteHeader-Schlüssel beschreibt das binäre Muster des zu schreibenden Metadatenblockheaders. Dieses binäre Muster stimmt mit dem Readermusterschlüssel des Metadatenformats überein.

Der WriteOffset-Schlüssel beschreibt den festen Offset vom Blockheader, in den die Metadaten geschrieben werden sollen. Dieser Schlüssel ist optional und bedeutet, dass die eigentlichen Metadaten nicht mit dem Header geschrieben werden sollten, wenn er nicht angegeben wird.

### <a name="signing-a-metadata-handler"></a>Signieren eines Metadatenhandlers

Alle Metadatenhandler müssen digital signiert werden, um am WIC-Ermittlungsprozess teilnehmen zu können. WIC wird keinen Handler laden, der nicht von einer vertrauenswürdigen Zertifizierungsstelle signiert wurde. Weitere Informationen zum digitalen Signieren finden Sie unter [Einführung in die Codesignatur.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))

## <a name="special-considerations"></a>Besondere Überlegungen

Die folgenden Abschnitte enthalten zusätzliche Informationen, die Sie beim Erstellen eigener Metadatenhandler berücksichtigen müssen.

### <a name="propvariants"></a>PROPVARIANTS

WIC verwendet [propVARIANT,](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) um ein Metadatenelement sowohl für Lese- als auch für Schreibszwecke zu darstellen. Eine PROPVARIANT stellt einen Datentyp und einen Datenwert für ein Metadatenelement bereit, das in einem Metadatenformat verwendet wird. Als Writer eines Metadatenhandlers haben Sie eine große Flexibilität in der Art und Weise, wie Daten im Metadatenformat gespeichert und wie Daten in einem Metadatenblock dargestellt werden. Die folgende Tabelle enthält Richtlinien, die Ihnen bei der Entscheidung für den geeigneten PROPVARIANT-Typ helfen, der in verschiedenen Situationen verwendet werden soll.



| Der Metadatentyp ist...          | PropVARIANT-Typ verwenden      | PROPVARIANT-Eigenschaft                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Leer oder nicht vorhanden.       | VT \_ EMPTY                 | Nicht zutreffend                                                                                                                                                                                                                                                                |
| Nicht definiert.                   | \_VT-BLOB                  | Verwenden Sie die Blob-Eigenschaft, um die Größe und den Zeiger auf das BLOB-Objekt festzulegen, das mit CoTaskMemAlloc zugeordnet wurde.                                                                                                                                                                           |
| Ein Metadatenblock.            | VT \_ UNKNOWN               | Dieser Typ verwendet die eigenschaft "val".                                                                                                                                                                                                                                           |
| Ein Array von Typen.           | VT \_ VECTOR \| VT \_ {type}  | Verwenden Sie die ca{type}-Eigenschaft, um die Anzahl und den Zeiger auf das Array festzulegen, das mit CoTaskMemAlloc zugeordnet wurde.                                                                                                                                                                            |
| Ein Array von Metadatenblöcken. | VT \_ VECTOR \| VT \_ VARIANT | Verwenden Sie die capropvar-Eigenschaft, um das Array von Varianten festzulegen.                                                                                                                                                                                                                       |
| Ein rationaler Wert mit Vorzeichen.     | VT \_ I8                    | Verwenden Sie die hVal-Eigenschaft, um den Wert festzulegen. Legen Sie das hohe Wort auf den Nenner und das niedrige Wort auf den Zähler fest.                                                                                                                                                                |
| Ein rationaler Wert.            | VT \_ UI8                   | Verwenden Sie die eigenschaft "hmVal", um den Wert festzulegen. Legen Sie HighPart auf den Nenner und LowPart auf den Zähler fest. Beachten Sie, dass LowPart ein unsigned int ist. Der Zähler sollte von einem unsigned int in einen int konvertiert werden, um sicherzustellen, dass das Vorzeichenbit beibehalten wird, falls vorhanden. |



 

Um Redundanz bei der Darstellung von Arrayelementen zu vermeiden, verwenden Sie keine sicheren Arrays. verwenden Sie nur einfache Arrays. Dadurch wird die Arbeit reduziert, die eine Anwendung beim Interpretieren von [PROPVARIANT-Typen](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) ausführen muss.

Vermeiden Sie es, Werte nach Möglichkeit inline zu verwenden `VT_BYREF` und zu speichern. `VT_BYREF` ist für kleine Typen (häufig für Metadatenelemente) ineffizient und stellt keine Größeninformationen bereit.

Rufen Sie vor der Verwendung von [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)immer **PropVariantInit** auf, um den Wert zu initialisieren. Wenn Sie mit propvariant fertig sind, rufen Sie immer **PropVariantClear** auf, um den für die Variable belegten Arbeitsspeicher freizugeben.

### <a name="8bim-handlers"></a>8BIM-Handler

Beim Schreiben eines Metadatenhandlers für einen 8BIM-Metadatenblock müssen Sie eine Signatur verwenden, die sowohl die 8BIM-Signatur als auch die ID kapselt. Beispielsweise stellt der native 8BIMIPTC-Metadatenleser die folgenden Registrierungsinformationen für die Readerermittlung bereit:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

Der 8BIMIPTC-Reader verfügt über ein registriertes Muster aus 0x38, 0x42, 0x49, 0x4D, 0x04 0x04. Die ersten vier Bytes (0x38, 0x42, 0x49, 0x4D) sind die 8BIM-Signatur, und die letzten zwei Bytes (0x04, 0x04) sind die ID für den IPTC-Datensatz.

Um also einen 8BIM-Metadatenleser für Auflösungsinformationen zu schreiben, benötigen Sie ein registriertes Muster aus 0x38, 0x42, 0x49, 0x4D, 0x03 0xED. Auch hier sind die ersten vier Bytes (0x38, 0x42, 0x49, 0x4D) die 8BIM-Signatur. Die letzten beiden Bytes (0x03, 0xED) sind jedoch die Auflösungsinformations-ID, die durch das PSD-Format definiert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über die Metadatenabfragesprache](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Übersicht über das Lesen und Schreiben von Bildmetadaten](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Vorgehensweise: Erneutes Codieren eines JPEG-Bilds mit Metadaten](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
