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
# <a name="adding-metadata-to-the-file-sink"></a><span data-ttu-id="15b4c-104">Hinzufügen von Metadaten zur Datei Senke</span><span class="sxs-lookup"><span data-stu-id="15b4c-104">Adding Metadata to the File Sink</span></span>

<span data-ttu-id="15b4c-105">Die ASF-Datei Senke ist eine Implementierung von [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="15b4c-105">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="15b4c-106">Weitere Informationen zum Objektmodell und zur allgemeinen Verwendung von ASF Medien senken finden Sie unter [ASF-Medien senken](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="15b4c-106">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="15b4c-107">Nach [dem Erstellen der ASF-Datei-Senke](creating-the-asf-file-sink.md)muss Sie mit Informationen zu den Datenströmen und den Codierungsinformationen in der Ausgabedatei konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="15b4c-107">After [Creating the ASF file sink](creating-the-asf-file-sink.md), it must be configured with information about the streams and encoding information in the output file.</span></span> <span data-ttu-id="15b4c-108">Diese Prozeduren werden unter [Hinzufügen von streaminginformationen zur ASF-Datei Senke](adding-stream-information-to-the-asf-file-sink.md) und [Festlegen von Eigenschaften in der Datei Senke](setting-properties-in-the-file-sink.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="15b4c-108">These procedures are described in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md) and [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span> <span data-ttu-id="15b4c-109">Darüber hinaus können Sie auch Metadateninformationen hinzufügen, einschließlich Name-Wert-Paaren wie "Author", Title ".</span><span class="sxs-lookup"><span data-stu-id="15b4c-109">In addition, You can also add metadata information includes name/value pairs such as "Author", Title".</span></span> <span data-ttu-id="15b4c-110">In diesem Thema wird die Vorgehensweise beim Hinzufügen von Metadateninformationen zur Datei Senke beschrieben, sodass Sie im endgültigen [ASF-Header Objekt](asf-file-structure.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="15b4c-110">This topic describes the process of adding metadata information to the file sink so that it appears in the final [ASF Header Object](asf-file-structure.md).</span></span>

<span data-ttu-id="15b4c-111">Vor dem Aufbau der Codierungs Topologie können Sie der ASF-Datei-Senke Metadateninformationen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="15b4c-111">You can add metadata information to the ASF file sink before building the encoding topology.</span></span> <span data-ttu-id="15b4c-112">Das Objekt "ASF ContentInfo" für die dateisenke verfolgt die Metadateneigenschaften und wird über die [**imfmetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) -Schnittstelle für die Anwendung verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="15b4c-112">The ASF ContentInfo object for the file sink keeps track of the metadata properties and are exposed to the application through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span> <span data-ttu-id="15b4c-113">Einige dieser Eigenschaften, z. b. "isvbr", die angeben, ob die Datei Datenströme variabler Bitrate (VBR) enthält, werden automatisch durch die Datei-Senke festgelegt, indem die festgelegten Datenstrom Codierungs Eigenschaften verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="15b4c-113">Some of these properties, such as "IsVBR" that indicates if the file contains variable bit rate (VBR) streams, are set automatically by the file sink by parsing the stream encoding properties that are set.</span></span>

<span data-ttu-id="15b4c-114">Eine umfassende Liste der Eigenschaften finden Sie im Thema "Attribut Liste" in der Format-SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="15b4c-114">For a complete list of properties, see the "Attribute List" topic in the Format SDK documentation.</span></span>

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a><span data-ttu-id="15b4c-115">Verwenden der IMF Metadata-Schnittstelle in der ASF-Datei-Senke</span><span class="sxs-lookup"><span data-stu-id="15b4c-115">Using the IMFMetadata Interface on the ASF File Sink</span></span>

1.  <span data-ttu-id="15b4c-116">Fragen Sie das Objekt der ASF File Sink ab, um einen Zeiger auf seine Implementierung der [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15b4c-116">Query the ASF file sink object to get a pointer to its implementation of the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span>
2.  <span data-ttu-id="15b4c-117">Aufrufen von [**IMFMetadataProvider:: getmfmetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) zum Abrufen eines [**imfmetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) -Zeigers.</span><span class="sxs-lookup"><span data-stu-id="15b4c-117">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) to get an [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) pointer.</span></span>

    <span data-ttu-id="15b4c-118">Der *ppresentationdescriptor* -Parameter wird ignoriert, und die Anwendung kann **null** übergeben.</span><span class="sxs-lookup"><span data-stu-id="15b4c-118">The *pPresentationDescriptor* parameter is ignored and the application can pass **NULL**.</span></span> <span data-ttu-id="15b4c-119">Wenn die Anwendung NULL als Datenstrom Bezeichner im *dwstreamidentifier* -Parameter übergibt, ruft die-Methode Metadaten ab, die für die gesamte ASF-Datei gelten.</span><span class="sxs-lookup"><span data-stu-id="15b4c-119">If the application passes zero as the stream identifier in the *dwStreamIdentifier* parameter, the method retrieves metadata that applies to the entire ASF file.</span></span> <span data-ttu-id="15b4c-120">Andernfalls werden nur die Metadaten für den Stream abgerufen.</span><span class="sxs-lookup"><span data-stu-id="15b4c-120">Otherwise, only the metadata for the stream is retrieved.</span></span>

3.  <span data-ttu-id="15b4c-121">Rufen Sie [**imfmetadata:: getallpropertynames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) auf, um die Liste der Datei Codierungs Eigenschaften abzurufen, die für den Medieninhalt festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="15b4c-121">Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to retrieve the list of file-encoding properties set on the media content.</span></span>
4.  <span data-ttu-id="15b4c-122">Wenn Sie [**imfmetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) aufrufen, um die Eigenschaftswerte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="15b4c-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get the property values.</span></span>

## <a name="example"></a><span data-ttu-id="15b4c-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="15b4c-123">Example</span></span>

<span data-ttu-id="15b4c-124">Der folgende Beispielcode zeigt, wie Sie die Eigenschaftsnamen und-Werte auflisten, die für die ASF-Datei festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="15b4c-124">The following example code shows how to enumerate the property names and values that are set on the ASF file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="15b4c-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15b4c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15b4c-126">ASF-Medien senken</span><span class="sxs-lookup"><span data-stu-id="15b4c-126">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="15b4c-127">Komponenten der Pipeline Schicht-ASF</span><span class="sxs-lookup"><span data-stu-id="15b4c-127">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="15b4c-128">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15b4c-128">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



