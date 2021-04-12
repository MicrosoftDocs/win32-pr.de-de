---
description: In diesem Thema werden die Anforderungen für das Erstellen von benutzerdefinierten metadatenhandlern für die Windows Imaging Component (WIC) vorgestellt, einschließlich der Metadaten-Reader und Writer.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Übersicht über die metadatenerweiterbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216819"
---
# <a name="metadata-extensibility-overview"></a>Übersicht über die metadatenerweiterbarkeit

In diesem Thema werden die Anforderungen für das Erstellen von benutzerdefinierten metadatenhandlern für die Windows Imaging Component (WIC) vorgestellt, einschließlich der Metadaten-Reader und Writer. Außerdem werden die Anforderungen für die Erweiterung der WIC-Laufzeitkomponenten Ermittlung erläutert, um Ihre benutzerdefinierten Metadatenhandler einzubeziehen.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Introduction (Einführung)](#introduction)
-   [Erstellen eines metadatenreaders](#creating-a-metadata-reader)
    -   [IWICMetadataReader-Schnittstelle](#iwicmetadatareader-interface)
    -   [IWICPersistStream-Schnittstelle](#iwicpersiststream-interface)
    -   [Iwicstreamprovider-Schnittstelle](#iwicstreamprovider-interface)
-   [Erstellen eines metadatenwriters](#creating-a-metadata-writer)
    -   [IWICMetadataWriter-Schnittstelle](#iwicmetadatawriter-interface)
    -   [IWICPersistStream-Schnittstelle](#iwicpersiststream-interface)
    -   [Iwicstreamprovider-Schnittstelle](#iwicstreamprovider-interface)
-   [Installieren und Registrieren eines metadatenhandlers](#installing-and-registering-a-metadata-handler)
    -   [Metadatenhandler-Registrierungsschlüssel](#metadata-handler-registry-keys)
    -   [Metadatenleser](#metadata-readers)
    -   [Metadatenschreiber](#metadata-writers)
    -   [Signieren eines metadatenhandlers](#signing-a-metadata-handler)
-   [Besondere Überlegungen](#special-considerations)
    -   [Propvarianten](#propvariants)
    -   [8bim-Handler](#8bim-handlers)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie über ein tiefgreifendes Verständnis von WIC, seinen Komponenten und Metadaten für Images verfügen. Weitere Informationen zu WIC-Metadaten finden Sie in der [WIC-Metadatenübersicht](-wic-about-metadata.md). Weitere Informationen zu WIC-Komponenten finden Sie unter [Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md).

## <a name="introduction"></a>Einführung

Wie in der [Übersicht über WIC-Metadaten](-wic-about-metadata.md)erläutert, gibt es häufig mehrere Metadatenblöcke innerhalb eines Bilds, von denen jedes verschiedene Informationstypen in verschiedenen Metadatenformaten verfügbar macht. Um mit einem in einem Bild eingebetteten Metadatenformat zu interagieren, muss eine Anwendung einen geeigneten Metadatenhandler verwenden. WIC stellt mehrere Metadatenhandler (sowohl metadatenreader als auch Writer) bereit, die es Ihnen ermöglichen, bestimmte Metadatentypen wie EXIF oder XMP zu lesen und zu schreiben.

Zusätzlich zu den bereitgestellten systemeigenen Handlern bietet WIC APIs, mit denen Sie neue Metadatenhandler erstellen können, die an der WIC-Laufzeitkomponenten Ermittlung beteiligt sind. Dadurch können Anwendungen, die WIC verwenden, Ihre benutzerdefinierten Metadatenformate lesen und schreiben.

Die folgenden Schritte ermöglichen es ihren metadatenhandlern, an der Ermittlung der Lauf Zeit Metadaten von WIC teilzunehmen.

-   Implementieren Sie eine metadatenleser-Handlerklasse ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)), die die erforderlichen WIC-Schnittstellen zum Lesen des benutzerdefinierten metadatenformats verfügbar macht. Dadurch können WIC-basierte Anwendungen ihr Metadatenformat auf die gleiche Weise wie Native Metadatenformate lesen.
-   Implementieren Sie eine metadatenwriter-Handlerklasse ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)), die die erforderlichen WIC-Schnittstellen für die Codierung Ihres benutzerdefinierten metadatenformats verfügbar macht Dies ermöglicht es WIC-basierten Anwendungen, Ihr Metadatenformat in Unterstützte Bildformate zu serialisieren.
-   Signieren Sie Ihre Metadatenhandler Digital, und registrieren Sie Sie. Dadurch können Ihre Metadatenhandler zur Laufzeit ermittelt werden, indem das identifizierende Muster in der Registrierung mit dem in die Bilddatei eingebetteten Muster übereinstimmt.

## <a name="creating-a-metadata-reader"></a>Erstellen eines metadatenreaders

Der Haupt Zugriff auf Metadatenblöcke innerhalb eines Codecs ist die [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) -Schnittstelle, die von jedem WIC-Codec implementiert wird. Diese Schnittstelle listet jeden der in ein Bildformat eingebetteten Metadatenblöcke auf, sodass der geeignete Metadatenhandler für jeden Block ermittelt und instanziiert werden kann. Die Metadatenblöcke, die nicht von WIC erkannt werden, gelten als unbekannt und sind als GUID CLSID \_ WICUnknownMetadataReader definiert. Damit Ihr Metadatenformat von WIC erkannt wird, müssen Sie eine Klasse erstellen, die drei Schnittstellen implementiert: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)und [**iwicstreamprovider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Wenn Ihr Metadatenformat Einschränkungen aufweist, die einige Methoden der erforderlichen Schnittstellen ungeeignet sind, sollte diese Methode wincodec \_ Err \_ unsupportedoperation zurückgeben.

 

### <a name="iwicmetadatareader-interface"></a>IWICMetadataReader-Schnittstelle

Die [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) -Schnittstelle muss beim Erstellen eines metadatenreaders implementiert werden. Diese Schnittstelle ermöglicht den Zugriff auf die zugrunde liegenden Metadatenelemente innerhalb des Datenstroms eines metadatenformats.

Der folgende Code zeigt die Definition der metadatenleseschnittstelle, wie in der Datei wincodecsdk. idl definiert.

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

Die **GetMetadataFormat** -Methode gibt die GUID Ihres metadatenformats zurück.

Die **GetMetadataHandlerInfo** -Methode gibt eine [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) -Schnittstelle zurück, die Informationen über Ihren Metadatenhandler bereitstellt. Hierzu gehören Informationen wie z. b. Welche Bildformate das Metadatenformat unterstützen und ob Ihr metadatenleser Zugriff auf den vollständigen Metadatenstream benötigt.

Die **GetCount** -Methode gibt die Anzahl einzelner Metadatenelemente (einschließlich eingebetteter Metadatenblöcke) zurück, die im Metadatenstream enthalten sind.

Die **getvaluebyindex** -Methode gibt ein Metadatenelement durch einen Indexwert zurück. Diese Methode ermöglicht es Anwendungen, jedes Metadatenelement in einem Metadatenblock zu durchlaufen. Der folgende Code veranschaulicht, wie eine Anwendung diese Methode verwenden kann, um jedes Metadatenelement in einem Metadatenblock abzurufen.


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



Die **GetValue** -Methode ruft ein bestimmtes Metadatenelement nach Schema und/oder ID ab. Diese Methode ähnelt der **getvaluebyindex** -Methode, mit der Ausnahme, dass Sie ein Metadatenelement mit einem bestimmten Schema oder einer ID abruft.

Die **GetEnumerator** -Methode gibt einen Enumerator für jedes Metadatenelement im Metadatenblock zurück. Dadurch können Anwendungen einen Enumerator für die Navigation in Ihrem Metadatenformat verwenden.

Wenn Ihr Metadatenformat keine Schemas für Metadatenelemente enthält, wird der GetValue... Methoden sollten diese Eigenschaft ignorieren. Wenn Ihr Format jedoch Schema Benennung unterstützt, sollten Sie einen **null** -Wert erwarten.

Wenn ein Metadatenelement ein eingebetteter Metadatenblock ist, erstellen Sie einen Metadatenhandler aus dem unter Datenstrom des eingebetteten Inhalts, und geben Sie den neuen Metadatenhandler zurück. Wenn kein metadatenleser für den gruppierten Block verfügbar ist, instanziieren Sie einen unbekannten metadatenreader, und geben Sie ihn zurück. Um einen neuen metadatenleser für den eingebetteten Block zu erstellen, rufen Sie die **CreateMetadataReaderFromContainer** -oder **CreateMetadataReader** -Methode der komponentenfactory auf, oder rufen Sie die [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) -Funktion auf

Wenn der Metadatenstream Big-Endian-Inhalte enthält, ist der metadatenleser für das Austauschen von Datenwerten zuständig, die er verarbeitet. Es ist auch dafür verantwortlich, dass die Leser von blendbenutzern darüber informiert werden, dass Sie mit Big-Endian-Datenströmen arbeiten. Allerdings sollten alle Werte im Little-Endian-Format zurückgegeben werden.

Implementieren Sie Unterstützung für die Namespace Navigation durch Unterstützung von Abfragen, bei denen die metadatenelementid eine `VT_CLSID` (GUID) ist, die einem Metadatenformat entspricht. Wenn ein geschzigter metadatenleser für dieses Format während der-Verarbeitung identifiziert wird, muss er zurückgegeben werden. Dadurch können Anwendungen einen Metadatenabfrage-Reader verwenden, um Ihr Metadatenformat zu durchsuchen.

Wenn Sie ein Metadatenelement anhand der ID erhalten, sollten Sie die [Funktion "propvariantchangetype](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) " verwenden, um die ID in den erwarteten Typ umzuwandeln. Beispielsweise wandelt der IFD-Reader eine ID in den Typ `VT_UI2` um, damit er mit dem Datentyp einer IFD-tagkennung ushort übereinstimmt. Der Eingabetyp und der erwartete Typ müssen hierfür beide [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) sein. Dies ist nicht erforderlich, aber durch diese Umwandlung wird der Code vereinfacht, der den Reader aufruft, um Metadatenelemente abzufragen.

### <a name="iwicpersiststream-interface"></a>IWICPersistStream-Schnittstelle

Die [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) -Schnittstelle erbt von **IPersistStream** und bietet zusätzliche Methoden zum Speichern und Laden von Objekten mithilfe der [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) -Enumeration.

Der folgende Code zeigt die Definition der [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) -Schnittstelle, wie in der Datei wincodecsdk. idl definiert.

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

Die **Loadex** -Methode stellt ihrem metadatenleser einen Datenstrom mit Ihrem Metadatenblock bereit. Der Reader analysiert diesen Stream für den Zugriff auf die zugrunde liegenden Metadatenelemente. Ihr metadatenleser wird mit einem unter Datenstrom initialisiert, der am Anfang des rohmetadateninhalts positioniert ist. Wenn der Reader den vollständigen Stream nicht benötigt, ist der unter Datenstrom auf den Inhalt des Metadatenblocks beschränkt. Andernfalls wird der vollständige Metadatenstream mit dem Positionswert bereitgestellt, der am Anfang des Metadatenblocks festgelegt ist.

Die **saveex** -Methode wird von metadatenwritern verwendet, um den Metadatenblock zu serialisieren. Wenn **saveex** in einem metadatenreader verwendet wird, sollte wincodec \_ Err \_ unsupportedoperation zurückgegeben werden.

### <a name="iwicstreamprovider-interface"></a>Iwicstreamprovider-Schnittstelle

Die [**iwicstreamprovider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) -Schnittstelle ermöglicht es Ihrem metadatenleser, Verweise auf seinen Inhaltsstream bereitzustellen, Informationen zum Stream bereitzustellen und zwischengespeicherte Versionen des Streams zu aktualisieren.

Der folgende Code zeigt die Definition der [**iwicstreamprovider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) -Schnittstelle, wie in der Datei wincodecsdk. idl definiert.

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

Die **GetStream** -Methode ruft einen Verweis auf den Metadatenstream ab. Der zurückgegebene Stream sollte den Datenstrom Zeiger auf die Startposition zurücksetzen. Wenn Ihr Metadatenformat vollen Datenstrom Zugriff erfordert, sollte die Startposition der Anfang des Metadatenblocks sein.

Die **getpersistoptions** -Methode gibt die aktuellen Optionen des Streams aus der [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) -Enumeration zurück.

Die **getpreferredvendorguid** -Methode gibt die GUID des Anbieters des metadatenreaders zurück.

Die **freshstream** -Methode aktualisiert den Metadatenstream. Diese Methode muss **Loadex** mit einem **null** -Datenstrom für alle gruppierten Metadatenblöcke aufzurufen. Dies ist erforderlich, da geschachtelte Metadata-Blöcke und deren Elemente aufgrund einer direkten Bearbeitung möglicherweise nicht mehr vorhanden sind.

## <a name="creating-a-metadata-writer"></a>Erstellen eines metadatenwriters

Ein metadatenwriter ist ein Typ von Metadatenhandler, der eine Möglichkeit bietet, einen Metadatenblock in einen Bildframe zu serialisieren oder außerhalb eines einzelnen Frames, wenn er vom Bildformat unterstützt wird. Der Haupt Zugriff auf die metadatenwriter innerhalb eines Codecs ist die [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) -Schnittstelle, die jeder WIC-Encoder implementiert. Diese Schnittstelle ermöglicht es Anwendungen, jeden der in ein Bild eingebetteten Metadatenblöcke aufzulisten, damit der entsprechende metadatenwriter für jeden Metadatenblock ermittelt und instanziiert werden kann. Metadatenblöcke, die keinen entsprechenden metadatenwriter aufweisen, werden als unbekannt angesehen und als GUID CLSID \_ WICUnknownMetadataReader definiert. Um für WIC-aktivierte Anwendungen das Serialisieren und Schreiben Ihres metadatenformats zu ermöglichen, müssen Sie eine Klasse erstellen, die die folgenden Schnittstellen implementiert: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)und [**iwicstreamprovider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).

> [!Note]  
> Wenn Ihr Metadatenformat Einschränkungen aufweist, die einige Methoden der erforderlichen Schnittstellen ungeeignet sind, sollte diese Methode wincodec \_ Err \_ unsupportedoperation zurückgeben.

 

### <a name="iwicmetadatawriter-interface"></a>IWICMetadataWriter-Schnittstelle

Die [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) -Schnittstelle muss von Ihrem metadatenwriter implementiert werden. Da **IWICMetadataWriter** außerdem von [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)erbt, müssen Sie auch alle Methoden von **IWICMetadataReader** implementieren. Da beide Handlertypen dieselbe Schnittstellen Vererbung erfordern, können Sie eine einzelne Klasse erstellen, die sowohl Lese-als auch Schreibfunktionen bereitstellt.

Der folgende Code zeigt die Definition der metadatenwriter-Schnittstelle, wie in der Datei wincodecsdk. idl definiert.

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

Die **SetValue** -Methode schreibt das angegebene Metadatenelement in den Metadatenstream.

Die **setvaluebyindex** -Methode schreibt das angegebene Metadatenelement in den angegebenen Index im Metadatenstream. Der Index verweist nicht auf die ID, sondern auf die Position des Elements im Metadatenblock.

Die **removeValue** -Methode entfernt das angegebene Metadatenelement aus dem Metadatenstream.

Die **removevaluebyindex** -Methode entfernt das Metadatenelement am angegebenen Index aus dem Metadatenstream. Nach dem Entfernen eines Elements wird erwartet, dass die verbleibenden Metadatenelemente den frei gewordenen Index belegen, wenn der Index nicht der letzte Index ist. Außerdem wird erwartet, dass sich die Anzahl ändert, nachdem das Element entfernt wurde.

Der metadatenwriter ist dafür verantwortlich, die [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Elemente in die zugrunde liegende Struktur zu konvertieren, die für Ihr Format erforderlich ist. Im Gegensatz zum metadatenreader sollten Variant-Typen jedoch normalerweise nicht in verschiedene Typen umgewandelt werden, da der Aufrufer speziell angibt, welcher Datentyp verwendet werden soll.

Ihr metadatenwriter muss alle Metadatenelemente in den Bildstream einbinden, einschließlich ausgeblendeter oder unbekannter Werte. Dies schließt unbekannte gruppierten Metadatenblöcke ein. Es ist jedoch Aufgabe des Encoders, alle kritischen Metadatenelemente festzulegen, bevor der Speichervorgang initiiert wird.

Wenn der Metadatenstream Big-Endian-Inhalte enthält, ist der metadatenwriter für das Austauschen von Datenwerten zuständig, die er verarbeitet. Es ist auch dafür verantwortlich, dass alle gruppierten metadatenwriter darüber informiert werden, dass Sie mit einem Big-Endian-Datenstream arbeiten, wenn Sie gespeichert werden.

Implementieren Sie Unterstützung für das Erstellen und Entfernen von Namespaces durch Unterstützung von Set-und Remove-Vorgängen für Metadatenelemente mit einem Typ `VT_CLSID` (GUID), der einem Metadatenformat entspricht. Der metadatenwriter Ruft die [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) -Funktion auf, um den Inhalt des eingefügten metadatenwriters ordnungsgemäß in den übergeordneten metadatenwriter

Wenn Ihr Metadatenformat eine direkte Codierung unterstützt, sind Sie für die Verwaltung der erforderlichen Auffüll Vorgänge verantwortlich. Weitere Informationen zur direkten Codierung finden Sie unter Übersicht über [WIC-Metadaten](-wic-about-metadata.md) und [Übersicht über das Lesen und Schreiben von Bild Metadaten](-wic-codec-readingwritingmetadata.md).

### <a name="iwicpersiststream-interface"></a>IWICPersistStream-Schnittstelle

Die [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) -Schnittstelle erbt von **IPersistStream** und bietet zusätzliche Methoden zum Speichern und Laden von Objekten mithilfe der [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) -Enumeration.

Der folgende Code zeigt die Definition der [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) -Schnittstelle, wie in der Datei wincodecsdk. idl definiert.

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

Die **Loadex** -Methode stellt ihrem Metadatenhandler einen Datenstrom mit Ihrem Metadatenblock bereit.

Die **saveex** -Methode serialisiert die Metadaten in einen Stream. Wenn der angegebene Stream mit dem Initialisierungs Datenstrom identisch ist, sollten Sie eine direkte Codierung durchführen. Wenn die direkte Codierung unterstützt wird, sollte diese Methode wincodec \_ Err " \_ deomuchmetadata" zurückgeben, wenn nicht genügend Auffüll Vorgänge vorhanden sind, um eine direkte Codierung auszuführen. Wenn die direkte Codierung nicht unterstützt wird, sollte diese Methode wincodec \_ Err \_ unsupportedoperation zurückgeben.

Die **IPersistStream:: GetSizeMax** -Methode muss implementiert werden und muss die genaue Größe des metadateninhalts zurückgeben, der in der nachfolgenden Speicherung geschrieben würde.

Die **IPersistStream:: IsDirty** -Methode sollte implementiert werden, wenn der metadatenwriter über einen Stream initialisiert wird, damit ein Bild zuverlässig ermitteln kann, ob sich der Inhalt geändert hat.

Wenn Ihr Metadatenformat gruppierten Metadatenblöcke unterstützt, sollte Ihr metadatenwriter an die gruppierten metadatenwriter delegieren, die den Inhalt beim Speichern in einem Stream serialisieren.

### <a name="iwicstreamprovider-interface"></a>Iwicstreamprovider-Schnittstelle

Die Implementierung der [**iwicstreamprovider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) -Schnittstelle für einen metadatenwriter ist mit der Implementierung eines metadatenreaders identisch. Weitere Informationen finden Sie im Abschnitt Erstellen eines metadatenreaders in diesem Dokument.

## <a name="installing-and-registering-a-metadata-handler"></a>Installieren und Registrieren eines metadatenhandlers

Zum Installieren eines metadatenhandlers müssen Sie die Handlerassembly bereitstellen und in der Systemregistrierung registrieren. Sie können entscheiden, wie und wann die Registrierungsschlüssel aufgefüllt werden.

> [!Note]  
> Zur besseren Lesbarkeit werden die tatsächlichen hexadezimalen GUIDs nicht in den Registrierungs Schlüsseln angezeigt, die in den folgenden Abschnitten dieses Dokuments angezeigt werden. Um den hexadezimalen Wert für einen angegebenen anzeigen Amen zu ermitteln, lesen Sie die Dateien wincodec. idl und wincodecsdk. idl.

 

### <a name="metadata-handler-registry-keys"></a>Metadatenhandler-Registrierungsschlüssel

Jeder Metadatenhandler wird durch eine eindeutige CLSID identifiziert, und jeder Handler muss seine CLSID unter der Kategorie-ID-GUID des metadatenhandlers registrieren. Die Kategoriekennung der einzelnen Handlertypen ist in wincodec. idl; definiert. der Name der Kategorie-ID für Reader lautet CATID \_ WICMetadataReader, und der Name der Kategorie-ID für Writer lautet CATID \_ WICMetadataWriter.

Jeder Metadatenhandler wird durch eine eindeutige CLSID identifiziert, und jeder Handler muss seine CLSID unter der Kategorie-ID-GUID des metadatenhandlers registrieren. Die Kategoriekennung der einzelnen Handlertypen ist in wincodec. idl; definiert. der Name der Kategorie-ID für Reader lautet CATID \_ WICMetadataReader, und der Name der Kategorie-ID für Writer lautet CATID \_ WICMetadataWriter.

> [!Note]  
> In den folgenden Registrierungsschlüssel Listen verweist {Reader CLSID} auf die eindeutige CLSID, die Sie für Ihren metadatenreader bereitstellen. {Writer CLSID} verweist auf die eindeutige CLSID, die Sie für Ihren metadatenwriter bereitstellen. {Handler CLSID} bezieht sich auf die CLSID des Readers, die CLSID des Writers oder beides, abhängig von den Handlern, die Sie bereitstellen. {Container GUID} verweist auf das Container Objekt (Bildformat oder Metadatenformat), das den Metadatenblock enthalten kann.

 

Die folgenden Registrierungsschlüssel registrieren Ihren Metadatenhandler mit den anderen verfügbaren metadatenhandlern:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

Zusätzlich zum Registrieren von Handlern in ihren jeweiligen Kategorien müssen Sie auch zusätzliche Schlüssel registrieren, die für den Handler spezifische Informationen bereitstellen. Leser und Writer haben ähnliche Anforderungen an den Registrierungsschlüssel. Die folgende Syntax zeigt, wie ein Handler registriert wird. Sowohl der Reader-als auch der Writer-Handler müssen auf diese Weise registriert werden, wobei die entsprechenden CLSIDs verwendet werden:

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

Die Registrierung des metadatenreaders umfasst auch Schlüssel, die beschreiben, wie der Reader in ein Containerformat eingebettet werden kann. Ein Containerformat kann ein Bildformat (z. b. TIFF oder JPEG) sein. Es kann auch ein anderes Metadatenformat sein, z. b. ein IFD-Metadatenblock. Nativ unterstützte Bild Containerformate sind in wincodec. idl aufgeführt. jedes Bild Containerformat ist als GUID mit einem Namen definiert, der mit dem GUID- \_ Containerformat beginnt. Nativ unterstützte metadatencontainerformate sind in wincodecsdk. idl aufgeführt. jedes metadatencontainerformat ist als GUID mit einem Namen definiert, der mit GUID \_ MetadataFormat beginnt.

Mit den folgenden Schlüsseln wird ein Container registriert, den der metadatenreader unterstützt, sowie die Daten, die zum Lesen aus diesem Container benötigt werden. Jeder Container, der vom Reader unterstützt wird, muss auf diese Weise registriert werden.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

Der Muster Schlüssel beschreibt das binäre Muster, das verwendet wird, um den Metadatenblock mit dem Reader abzugleichen. Wenn Sie ein Muster für den metadatenreader definieren, sollte es zuverlässig genug sein, dass eine positive Übereinstimmung bedeutet, dass der metadatenleser die Metadaten im Metadatenblock, der verarbeitet wird, verstehen kann.

Der DataOffset-Schlüssel beschreibt den fixierten Offset der Metadaten aus dem Block Header. Dieser Schlüssel ist optional. wenn er nicht angegeben ist, bedeutet dies, dass die eigentlichen Metadaten nicht mithilfe eines Fixed-Offsets aus dem Block Header gefunden werden können.

### <a name="metadata-writers"></a>Metadatenschreiber

Die Registrierung des metadatenwriters umfasst auch Schlüssel, die beschreiben, wie der Header vor dem in ein Containerformat eingebetteten metadateninhalt geschrieben werden soll. Ebenso wie der Reader kann ein Containerformat ein Bildformat oder ein anderer Metadatenblock sein.

Mit den folgenden Schlüsseln wird ein Container registriert, den der metadatenwriter unterstützt, sowie die Daten, die zum Schreiben des Headers und der Metadaten benötigt werden. Jeder Container, der vom Writer unterstützt wird, muss auf diese Weise registriert werden.

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

Der Schlüssel schreibheader beschreibt das binäre Muster des Metadatenblock Headers, der geschrieben werden soll. Dieses binäre Muster stimmt mit dem readermusterschlüssel des metadatenformats überein.

Der Schlüssel "Write-Offset" beschreibt den fixierten Offset aus dem Block Header, bei dem die Metadaten geschrieben werden sollen. Dieser Schlüssel ist optional. wenn er nicht angegeben ist, bedeutet dies, dass die eigentlichen Metadaten nicht mit dem-Header geschrieben werden sollten.

### <a name="signing-a-metadata-handler"></a>Signieren eines metadatenhandlers

Alle Metadatenhandler müssen digital signiert werden, damit Sie am WIC-Ermittlungsprozess teilnehmen können. WIC lädt keinen Handler, der nicht von einer vertrauenswürdigen Zertifizierungsstelle signiert ist. Weitere Informationen zum digitalen Signieren finden [Sie unter Einführung in die Code Signatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).

## <a name="special-considerations"></a>Besondere Überlegungen

Die folgenden Abschnitte enthalten zusätzliche Informationen, die Sie berücksichtigen müssen, wenn Sie Ihre eigenen Metadatenhandler erstellen.

### <a name="propvariants"></a>Propvarianten

WIC verwendet eine [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) , um ein Metadatenelement für Lese-und Schreibvorgänge darzustellen. Eine PROPVARIANT bietet einen Datentyp und Datenwert für ein Metadatenelement, das in einem Metadatenformat verwendet wird. Als Writer eines metadatenhandlers haben Sie viel Flexibilität bei der Speicherung von Daten im Metadatenformat und der Darstellung von Daten in einem Metadatenblock. In der folgenden Tabelle finden Sie Richtlinien, die Ihnen bei der Entscheidung helfen, den geeigneten PROPVARIANT-Typ in unterschiedlichen Situationen zu verwenden.



| Metadatentyp ist...          | PROPVARIANT-Typ verwenden      | PROPVARIANT-Eigenschaft                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Leer oder nicht vorhanden.       | VT \_ leer                 | Nicht zutreffend                                                                                                                                                                                                                                                                |
| Nicht definiert.                   | VT- \_ BLOB                  | Verwenden Sie die BLOB-Eigenschaft, um die Größe und den Zeiger auf das BLOB-Objekt festzulegen, das mithilfe von cotaskmemzugewieszugewiesen wurde.                                                                                                                                                                           |
| Ein Metadatenblock.            | VT \_ unbekannt               | Dieser Typ verwendet die punkVal-Eigenschaft.                                                                                                                                                                                                                                           |
| Ein Array von Typen.           | VT \_ Vector \| VT \_ {Type}  | Verwenden Sie die Eigenschaft "ca {Type}", um die Anzahl und den Zeiger auf das mit cotaskmemzuzugeordnete Array festzulegen.                                                                                                                                                                            |
| Ein Array von metadatenblöcken. | VT \_ Vector \| VT \_ Variant | Verwenden Sie die capropvar-Eigenschaft, um das Array von Varianten festzulegen.                                                                                                                                                                                                                       |
| Ein-Wert mit Vorzeichen.     | VT \_ I8                    | Verwenden Sie die Hval-Eigenschaft, um den Wert festzulegen. Legen Sie das hohe Wort auf den Nenner und das niedrige Wort auf den Zähler fest.                                                                                                                                                                |
| Ein rationeller Wert.            | VT \_ UI8                   | Verwenden Sie die uhval-Eigenschaft, um den Wert festzulegen. Legen Sie das highpart-Element auf den Nenner und den LowPart-Wert auf den Zähler fest. Beachten Sie, dass LowPart ein int ohne Vorzeichen ist. Der Zähler muss von einem Ganzzahl ohne Vorzeichen int in einen int-Wert konvertiert werden, um sicherzustellen, dass das Signier Bit beibehalten wird, wenn es vorhanden ist. |



 

Verwenden Sie keine sicheren Arrays, um Redundanz bei der Darstellung von Array Elementen zu vermeiden. Verwenden Sie nur einfache Arrays. Dadurch wird die Arbeit reduziert, die eine Anwendung bei der Interpretation von [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Typen ausführen muss.

Vermeiden Sie die Verwendung `VT_BYREF` und Speicherung von Werten, wenn dies möglich ist. `VT_BYREF` ist bei kleinen Typen (häufig für Metadatenelemente) ineffizient und stellt keine Größen Informationen bereit.

Bevor Sie eine [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)verwenden, wird immer **propvariantinit** aufgerufen, um den Wert zu initialisieren. Wenn Sie mit dem PROPVARIANT-Vorgang fertig sind, müssen Sie immer **propvariantclear** aufzurufen, um den für die Variable zugeordneten Arbeitsspeicher freizugeben.

### <a name="8bim-handlers"></a>8bim-Handler

Beim Schreiben eines metadatenhandlers für einen 8bim-Metadatenblock müssen Sie eine Signatur verwenden, die sowohl die 8bim-Signatur als auch die ID kapselt. Der Native 8bimiptc-metadatenreader stellt z. b. die folgenden Registrierungsinformationen für die Leser Ermittlung bereit:

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

Der 8bimiptc-Reader hat ein registriertes Muster von 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04. Die ersten vier Bytes (0x38, 0x42, 0x49, 0x4D) sind die 8bim-Signatur, und die letzten zwei Bytes (0x04, 0x04) stellen die ID für den IPTC-Datensatz dar.

Wenn Sie also einen 8bim-metadatenleser für Auflösungsinformationen schreiben möchten, benötigen Sie ein registriertes Muster von 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED. Auch hier handelt es sich bei den ersten vier Bytes (0x38, 0x42, 0x49, 0x4D) um die 8bim-Signatur. Die letzten zwei Bytes (0x03, 0xED) sind jedoch die Auflösungs Informations-ID, wie im PSD-Format definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über die Metadaten-Abfragesprache](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Übersicht über das Lesen und Schreiben von Bild Metadaten](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Gewusst wie: Erneutes Codieren eines JPEG-Bilds mit Metadaten](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
