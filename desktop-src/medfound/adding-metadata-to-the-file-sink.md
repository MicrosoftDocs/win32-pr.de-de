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
# <a name="adding-metadata-to-the-file-sink"></a><span data-ttu-id="297fc-103">Hinzufügen von Metadaten zur Dateisenke</span><span class="sxs-lookup"><span data-stu-id="297fc-103">Adding Metadata to the File Sink</span></span>

<span data-ttu-id="297fc-104">Die ASF-Dateisenke ist eine Implementierung von [**VONMEDIASink,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="297fc-104">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="297fc-105">Informationen zum Objektmodell und zur allgemeinen Verwendung von ASF-Mediensenken finden Sie unter [ASF-Mediensenken.](asf-media-sinks.md)</span><span class="sxs-lookup"><span data-stu-id="297fc-105">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="297fc-106">Nach [dem Erstellen der ASF-Dateisenke](creating-the-asf-file-sink.md)muss sie mit Informationen zu den Datenströmen und Codierungsinformationen in der Ausgabedatei konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="297fc-106">After [Creating the ASF file sink](creating-the-asf-file-sink.md), it must be configured with information about the streams and encoding information in the output file.</span></span> <span data-ttu-id="297fc-107">Diese Verfahren werden unter [Hinzufügen von Streaminformationen zur ASF-Dateisenke](adding-stream-information-to-the-asf-file-sink.md) und [Festlegen von Eigenschaften in der Dateisenke](setting-properties-in-the-file-sink.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="297fc-107">These procedures are described in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md) and [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span> <span data-ttu-id="297fc-108">Darüber hinaus können Sie Metadateninformationen hinzufügen, einschließlich Name-Wert-Paaren wie "Autor", Titel".</span><span class="sxs-lookup"><span data-stu-id="297fc-108">In addition, You can also add metadata information includes name/value pairs such as "Author", Title".</span></span> <span data-ttu-id="297fc-109">In diesem Thema wird beschrieben, wie Metadateninformationen zur Dateisenke hinzugefügt werden, sodass sie im endgültigen [ASF-Headerobjekt](asf-file-structure.md)angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="297fc-109">This topic describes the process of adding metadata information to the file sink so that it appears in the final [ASF Header Object](asf-file-structure.md).</span></span>

<span data-ttu-id="297fc-110">Sie können der ASF-Dateisenke Metadateninformationen hinzufügen, bevor Sie die Codierungstopologie erstellen.</span><span class="sxs-lookup"><span data-stu-id="297fc-110">You can add metadata information to the ASF file sink before building the encoding topology.</span></span> <span data-ttu-id="297fc-111">Das ASF ContentInfo-Objekt für die Dateisenke verfolgt die Metadateneigenschaften nach und wird für die Anwendung über die [**INTERFACESMetadata-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="297fc-111">The ASF ContentInfo object for the file sink keeps track of the metadata properties and are exposed to the application through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span> <span data-ttu-id="297fc-112">Einige dieser Eigenschaften, z. B. "IsVBR", die angeben, ob die Datei VBR-Datenströme (Variable Bit Rate) enthält, werden automatisch von der Dateisenke festgelegt, indem die festgelegten Streamcodierungseigenschaften analysieren werden.</span><span class="sxs-lookup"><span data-stu-id="297fc-112">Some of these properties, such as "IsVBR" that indicates if the file contains variable bit rate (VBR) streams, are set automatically by the file sink by parsing the stream encoding properties that are set.</span></span>

<span data-ttu-id="297fc-113">Eine vollständige Liste der Eigenschaften finden Sie im Thema "Attributliste" in der Format SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="297fc-113">For a complete list of properties, see the "Attribute List" topic in the Format SDK documentation.</span></span>

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a><span data-ttu-id="297fc-114">Verwenden der INTERFACESMetadata-Schnittstelle für die ASF-Dateisenke</span><span class="sxs-lookup"><span data-stu-id="297fc-114">Using the IMFMetadata Interface on the ASF File Sink</span></span>

1.  <span data-ttu-id="297fc-115">Fragen Sie das ASF-Dateisenkenobjekt ab, um einen Zeiger auf seine Implementierung der [**INTERFACESMetadataProvider-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="297fc-115">Query the ASF file sink object to get a pointer to its implementation of the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span>
2.  <span data-ttu-id="297fc-116">Rufen Sie [**DEN CURSORMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) auf, um einen [**POINTERMetadata-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="297fc-116">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) to get an [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) pointer.</span></span>

    <span data-ttu-id="297fc-117">Der *pPresentationDescriptor-Parameter* wird ignoriert, und die Anwendung kann **NULL** übergeben.</span><span class="sxs-lookup"><span data-stu-id="297fc-117">The *pPresentationDescriptor* parameter is ignored and the application can pass **NULL**.</span></span> <span data-ttu-id="297fc-118">Wenn die Anwendung 0 (null) als Streambezeichner im *dwStreamIdentifier-Parameter* übergibt, ruft die Methode Metadaten ab, die für die gesamte ASF-Datei gelten.</span><span class="sxs-lookup"><span data-stu-id="297fc-118">If the application passes zero as the stream identifier in the *dwStreamIdentifier* parameter, the method retrieves metadata that applies to the entire ASF file.</span></span> <span data-ttu-id="297fc-119">Andernfalls werden nur die Metadaten für den Stream abgerufen.</span><span class="sxs-lookup"><span data-stu-id="297fc-119">Otherwise, only the metadata for the stream is retrieved.</span></span>

3.  <span data-ttu-id="297fc-120">Rufen Sie [**DIE DATEIMETADATA::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) auf, um die Liste der Dateicodierungseigenschaften abzurufen, die für den Medieninhalt festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="297fc-120">Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to retrieve the list of file-encoding properties set on the media content.</span></span>
4.  <span data-ttu-id="297fc-121">Rufen Sie [**DIE EIGENSCHAFTSMETADATA::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) auf, um die Eigenschaftswerte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="297fc-121">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get the property values.</span></span>

## <a name="example"></a><span data-ttu-id="297fc-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="297fc-122">Example</span></span>

<span data-ttu-id="297fc-123">Der folgende Beispielcode zeigt, wie die Eigenschaftennamen und -werte aufzählt werden, die für die ASF-Datei festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="297fc-123">The following example code shows how to enumerate the property names and values that are set on the ASF file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="297fc-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="297fc-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="297fc-125">ASF-Mediensenken</span><span class="sxs-lookup"><span data-stu-id="297fc-125">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="297fc-126">ASF-Komponenten auf Pipelineebene</span><span class="sxs-lookup"><span data-stu-id="297fc-126">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="297fc-127">ASF-Unterstützung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="297fc-127">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



