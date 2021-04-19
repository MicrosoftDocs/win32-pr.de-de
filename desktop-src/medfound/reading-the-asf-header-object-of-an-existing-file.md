---
description: Lesen des ASF-Header Objekts einer vorhandenen Datei
ms.assetid: 0e37f0d3-a37b-4f36-a133-7b1922e9944b
title: Lesen des ASF-Header Objekts einer vorhandenen Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b231cb0b9af6b24f84efaa6403a4774e66bbb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348258"
---
# <a name="reading-the-asf-header-object-of-an-existing-file"></a>Lesen des ASF-Header Objekts einer vorhandenen Datei

Das Objekt "ASF ContentInfo" speichert Informationen, die die Objekte des ASF-Headers einer Mediendatei darstellen. Ein aufgefülltes ContentInfo-Objekt ist erforderlich, um eine vorhandene ASF-Datei zu lesen und zu analysieren.

Nachdem Sie das ContentInfo-Objekt durch Aufrufen der [**mfcreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) -Funktion erstellt haben, muss die Anwendung diese mit Header Informationen aus der zu lesenden ASF-Datei initialisieren. Um das-Objekt aufzufüllen, nennen Sie [**imfasfcontentinfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).

" **Parser Header** " erfordert einen Medien Puffer, der das Header Objekt der ASF-Datei enthält. Eine Möglichkeit besteht darin, einen Medien Puffer mit dem Header Objekt zu füllen, um einen Bytestream für die Datei zu erstellen und dann die ersten 30 Bytes der Daten aus dem Bytestream in einen Medien Puffer zu lesen. Sie können dann die Größe erzielen, indem Sie die ersten 24 Bytes des Header Objekts an die [**imfasfcontentinfo:: gethadersize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) -Methode übergeben. Nachdem Sie die Größe erhalten haben, können Sie das gesamte Header Objekt in einem Medien Puffer lesen und an den- **Header** übergeben. Die-Methode beginnt mit der Verarbeitung am Offset vom Anfang des Medien Puffers, der im Parameter *cboffsetwithinheader* angegeben ist.

Im folgenden Beispielcode wird ein ContentInfo-Objekt erstellt und initialisiert, um eine vorhandene, in einem Bytestream enthaltene ASF-Datei zu lesen. Zuerst definieren wir eine Hilfsfunktion, die Daten aus einem Bytestream liest und einen Medien Puffer zum Speichern der Daten zugeordnet:


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



Im nächsten Beispiel wird das ASF-Header Objekt aus einem Bytestream gelesen und ein "ASF ContentInfo"-Objekt aufgefüllt.


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



> [!Note]  
> In diesen Beispielen wird die [saferelease](saferelease.md) -Funktion verwendet, um Schnittstellen Zeiger freizugeben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-ContentInfo-Objekt](asf-contentinfo-object.md)
</dt> <dt>

[ASF-Header Objekt](asf-file-structure.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Informationen aus den ASF-Header Objekten werden erhalten.](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



