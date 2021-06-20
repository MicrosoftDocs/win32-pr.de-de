---
description: Erfahren Sie mehr über das Hinzufügen von Metadaten zur ASF-Dateisenke, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann.
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: Hinzufügen von Metadaten zur Dateisenke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ea86a09ff9e3d2a25bbf8d00d46691fd803365
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409963"
---
# <a name="adding-metadata-to-the-file-sink"></a>Hinzufügen von Metadaten zur Dateisenke

Die ASF-Dateisenke ist eine Implementierung von [**VONMEDIASink,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann. Informationen zum Objektmodell und zur allgemeinen Verwendung von ASF-Mediensenken finden Sie unter [ASF-Mediensenken.](asf-media-sinks.md)

Nach [dem Erstellen der ASF-Dateisenke](creating-the-asf-file-sink.md)muss sie mit Informationen zu den Datenströmen und Codierungsinformationen in der Ausgabedatei konfiguriert werden. Diese Verfahren werden unter [Hinzufügen von Streaminformationen zur ASF-Dateisenke](adding-stream-information-to-the-asf-file-sink.md) und [Festlegen von Eigenschaften in der Dateisenke](setting-properties-in-the-file-sink.md)beschrieben. Darüber hinaus können Sie Metadateninformationen hinzufügen, einschließlich Name-Wert-Paaren wie "Autor", Titel". In diesem Thema wird beschrieben, wie Metadateninformationen zur Dateisenke hinzugefügt werden, sodass sie im endgültigen [ASF-Headerobjekt](asf-file-structure.md)angezeigt werden.

Sie können der ASF-Dateisenke Metadateninformationen hinzufügen, bevor Sie die Codierungstopologie erstellen. Das ASF ContentInfo-Objekt für die Dateisenke verfolgt die Metadateneigenschaften nach und wird für die Anwendung über die [**INTERFACESMetadata-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) verfügbar gemacht. Einige dieser Eigenschaften, z. B. "IsVBR", die angeben, ob die Datei VBR-Datenströme (Variable Bit Rate) enthält, werden automatisch von der Dateisenke festgelegt, indem die festgelegten Streamcodierungseigenschaften analysieren werden.

Eine vollständige Liste der Eigenschaften finden Sie im Thema "Attributliste" in der Format SDK-Dokumentation.

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a>Verwenden der INTERFACESMetadata-Schnittstelle für die ASF-Dateisenke

1.  Fragen Sie das ASF-Dateisenkenobjekt ab, um einen Zeiger auf seine Implementierung der [**INTERFACESMetadataProvider-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) abzurufen.
2.  Rufen Sie [**DEN CURSORMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) auf, um einen [**POINTERMetadata-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) abzurufen.

    Der *pPresentationDescriptor-Parameter* wird ignoriert, und die Anwendung kann **NULL** übergeben. Wenn die Anwendung 0 (null) als Streambezeichner im *dwStreamIdentifier-Parameter* übergibt, ruft die Methode Metadaten ab, die für die gesamte ASF-Datei gelten. Andernfalls werden nur die Metadaten für den Stream abgerufen.

3.  Rufen Sie [**DIE DATEIMETADATA::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) auf, um die Liste der Dateicodierungseigenschaften abzurufen, die für den Medieninhalt festgelegt sind.
4.  Rufen Sie [**DIE EIGENSCHAFTSMETADATA::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) auf, um die Eigenschaftswerte abzurufen.

## <a name="example"></a>Beispiel

Der folgende Beispielcode zeigt, wie die Eigenschaftennamen und -werte aufzählt werden, die für die ASF-Datei festgelegt sind.


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

[ASF-Mediensenken](asf-media-sinks.md)
</dt> <dt>

[ASF-Komponenten auf Pipelineebene](pipeline-layer-asf-components.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



