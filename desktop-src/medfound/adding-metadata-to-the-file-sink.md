---
description: Die ASF-Datei Senke ist eine Implementierung von imfmediasink, die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann. Weitere Informationen zum Objektmodell der ASF-Medien senken und zur allgemeinen Verwendung finden Sie unter ASF-Medien senken.
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: Hinzufügen von Metadaten zur Datei Senke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71bb63a10d935b52e6d048dbc5dcd07370dd2ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041777"
---
# <a name="adding-metadata-to-the-file-sink"></a>Hinzufügen von Metadaten zur Datei Senke

Die ASF-Datei Senke ist eine Implementierung von [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann. Weitere Informationen zum Objektmodell und zur allgemeinen Verwendung von ASF Medien senken finden Sie unter [ASF-Medien senken](asf-media-sinks.md).

Nach [dem Erstellen der ASF-Datei-Senke](creating-the-asf-file-sink.md)muss Sie mit Informationen zu den Datenströmen und den Codierungsinformationen in der Ausgabedatei konfiguriert werden. Diese Prozeduren werden unter [Hinzufügen von streaminginformationen zur ASF-Datei Senke](adding-stream-information-to-the-asf-file-sink.md) und [Festlegen von Eigenschaften in der Datei Senke](setting-properties-in-the-file-sink.md)beschrieben. Darüber hinaus können Sie auch Metadateninformationen hinzufügen, einschließlich Name-Wert-Paaren wie "Author", Title ". In diesem Thema wird die Vorgehensweise beim Hinzufügen von Metadateninformationen zur Datei Senke beschrieben, sodass Sie im endgültigen [ASF-Header Objekt](asf-file-structure.md)angezeigt wird.

Vor dem Aufbau der Codierungs Topologie können Sie der ASF-Datei-Senke Metadateninformationen hinzufügen. Das Objekt "ASF ContentInfo" für die dateisenke verfolgt die Metadateneigenschaften und wird über die [**imfmetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) -Schnittstelle für die Anwendung verfügbar gemacht. Einige dieser Eigenschaften, z. b. "isvbr", die angeben, ob die Datei Datenströme variabler Bitrate (VBR) enthält, werden automatisch durch die Datei-Senke festgelegt, indem die festgelegten Datenstrom Codierungs Eigenschaften verarbeitet werden.

Eine umfassende Liste der Eigenschaften finden Sie im Thema "Attribut Liste" in der Format-SDK-Dokumentation.

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a>Verwenden der IMF Metadata-Schnittstelle in der ASF-Datei-Senke

1.  Fragen Sie das Objekt der ASF File Sink ab, um einen Zeiger auf seine Implementierung der [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) -Schnittstelle zu erhalten.
2.  Aufrufen von [**IMFMetadataProvider:: getmfmetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) zum Abrufen eines [**imfmetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) -Zeigers.

    Der *ppresentationdescriptor* -Parameter wird ignoriert, und die Anwendung kann **null** übergeben. Wenn die Anwendung NULL als Datenstrom Bezeichner im *dwstreamidentifier* -Parameter übergibt, ruft die-Methode Metadaten ab, die für die gesamte ASF-Datei gelten. Andernfalls werden nur die Metadaten für den Stream abgerufen.

3.  Rufen Sie [**imfmetadata:: getallpropertynames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) auf, um die Liste der Datei Codierungs Eigenschaften abzurufen, die für den Medieninhalt festgelegt sind.
4.  Wenn Sie [**imfmetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) aufrufen, um die Eigenschaftswerte abzurufen.

## <a name="example"></a>Beispiel

Der folgende Beispielcode zeigt, wie Sie die Eigenschaftsnamen und-Werte auflisten, die für die ASF-Datei festgelegt sind.


```C++
/////////////////////////////////////////////////////////////////////
// Name: ListASFProperties
//
// Enumerates the metadata properties of the ASF file. 
//
// pContentInfo: Pointer to the ASF ContentInfo object.
/////////////////////////////////////////////////////////////////////

HRESULT ListASFProperties(IMFASFContentInfo *pContentInfo)
{
    HRESULT hr = S_OK;
    
    PROPVARIANT varNames;
    PropVariantInit(&varNames);

    PROPVARIANT varValue;
    PropVariantInit(&varValue);

    IMFMetadataProvider* pProvider = NULL;
    IMFMetadata* pMetadata = NULL;

    // Query the ContentInfo object for IMFMetadataProvider.
    CHECK_HR(hr = pContentInfo->QueryInterface(IID_IMFMetadataProvider,
        (void**)&pProvider));

    // Get a pointer to IMFMetadata for file-wide metadata.
    CHECK_HR(hr = pProvider->GetMFMetadata(NULL, 0, 0, &pMetadata));

    // Get the property names that are stored in the metadata object.
    CHECK_HR(hr = pMetadata->GetAllPropertyNames(&varNames));

    // Loop through the properties and get their values.
    if (varNames.vt == (VT_VECTOR | VT_LPWSTR))
    {
        ULONG cElements = varNames.calpwstr.cElems;
        for (ULONG i = 0; i < cElements; i++)
        {
            const WCHAR* sName = varNames.calpwstr.pElems[i];
            CHECK_HR(hr = pMetadata->GetProperty(sName, &varValue));
            //Use the property values. Not shown.
            PropVariantClear(&varValue);
        }
    }
done:
    PropVariantClear(&varNames);
    PropVariantClear(&varValue);
    SAFE_RELEASE (pMetaData);
    SAFE_RELEASE (pProvider);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Medien senken](asf-media-sinks.md)
</dt> <dt>

[Komponenten der Pipeline Schicht-ASF](pipeline-layer-asf-components.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



