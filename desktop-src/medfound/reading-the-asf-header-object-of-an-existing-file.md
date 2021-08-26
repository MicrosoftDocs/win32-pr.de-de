---
description: Lesen des ASF-Headerobjekts einer vorhandenen Datei
ms.assetid: 0e37f0d3-a37b-4f36-a133-7b1922e9944b
title: Lesen des ASF-Headerobjekts einer vorhandenen Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e653154d632786995bdf45dcfa8e67e3cfd55cdf3f90103ce1cf995179e1266b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887340"
---
# <a name="reading-the-asf-header-object-of-an-existing-file"></a>Lesen des ASF-Headerobjekts einer vorhandenen Datei

Das ASF ContentInfo-Objekt speichert Informationen, die die ASF-Headerobjekte einer Mediendatei darstellt. Ein aufgefülltes ContentInfo-Objekt ist erforderlich, um eine vorhandene ASF-Datei zu lesen und zu analysieren.

Nach dem Erstellen des ContentInfo-Objekts durch Aufrufen der [**MFCreateASFContentInfo-Funktion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) muss die Anwendung es mit Headerinformationen aus der zu lesenden ASF-Datei initialisieren. Rufen Sie ZUM Auffüllen des Objekts [**IMFASFContentInfo::P arseHeader auf.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)

**ParseHeader erfordert** einen Medienpuffer, der das Headerobjekt der ASF-Datei enthält. Eine Möglichkeit besteht in der Auffüllung eines Medienpuffers mit dem Headerobjekt, um einen Bytestream für die Datei zu erstellen, und dann die ersten 30 Bytes von Daten aus dem Bytestream in einen Medienpuffer zu lesen. Sie können dann die Größe erhalten, indem Sie die ersten 24 Bytes des Headerobjekts an die [**IMFASFContentInfo::GetHeaderSize-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) übergeben. Nachdem Sie die Größe erhalten haben, können Sie das gesamte Headerobjekt in einem Medienpuffer lesen und an **ParseHeader übergeben.** Die -Methode beginnt mit der Analyse am Offset ab dem Anfang des Medienpuffers, der im *cbOffsetWithinHeader-Parameter angegeben* ist.

Der folgende Beispielcode erstellt und initialisiert ein ContentInfo-Objekt zum Lesen einer vorhandenen ASF-Datei, die in einem Bytestream enthalten ist. Zunächst definieren wir eine Hilfsfunktion, die Daten aus einem Bytestream liest und einen Medienpuffer zum Halten der Daten zuteilen:


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



Im nächsten Beispiel wird das ASF-Headerobjekt aus einem Bytestream gelesen und ein ASF ContentInfo-Objekt aufgefüllt.


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
> In diesen Beispielen wird die [SafeRelease-Funktion](saferelease.md) verwendet, um Schnittstellenzeigende frei zu geben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF ContentInfo-Objekt](asf-contentinfo-object.md)
</dt> <dt>

[ASF-Headerobjekt](asf-file-structure.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Abrufen von Informationen aus ASF-Headerobjekten](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



