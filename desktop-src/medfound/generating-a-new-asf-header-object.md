---
description: Erstellen eines neuen ASF-Header Objekts
ms.assetid: cf73306d-156a-45c0-a3d6-ae48734f5709
title: Erstellen eines neuen ASF-Header Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f303be4eb3353a0e7ddf1dad0eff9956f68d7db5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524512"
---
# <a name="generating-a-new-asf-header-object"></a>Erstellen eines neuen ASF-Header Objekts

Um die im ContentInfo-Objekt enthaltenen Informationen in ein binäres Objekt Format des ASF-Headers zu konvertieren, muss die Anwendung [**imfasfcontentinfo:: generateheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)aufrufen. Dieser Rückruf muss erfolgen, nachdem die Datenpakete generiert wurden und das ContentInfo-Objekt aktualisierte Informationen enthält. **Generateheader** gibt einen Zeiger auf einen Medien Puffer zurück, der die Header Informationen im gültigen Format enthält. Die Anwendung kann dann die Daten, auf die vom Medien Puffer verwiesen wird, am Anfang einer neuen ASF-Datei schreiben.

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a>So schreiben Sie ein neues Header Objekt mit dem ContentInfo-Objekt

1.  Rufen Sie [**mfkreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) auf, um ein leeres ContentInfo-Objekt zu erstellen.
2.  Aufrufen von [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) , um das Profil Objekt für das ContentInfo-Objekt bereitzustellen. Weitere Informationen zum Erstellen von Profilen finden Sie unter [Erstellen eines ASF-Profils](creating-an-asf-profile.md).
3.  Aufrufen von [**imfasfcontentinfo:: generateheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) und übergeben von **null** im *piheader* -Parameter und empfangen der Größe des aufgefüllten ContentInfo-Objekts im *pcbheader* -Parameter. Die Anwendung kann diesen Wert verwenden, um Arbeitsspeicher oder den Medien Puffer zuzuweisen, der das Header Objekt enthalten soll.

    Die empfangene Header Größe schließt die Auffüll Größe ein, die abhängig von der tatsächlichen Größe der Header Objekte angepasst wird. Die maximale Größe der Header Objekte beträgt 10 MB. Wenn die Größe diesen Wert überschreitet, schlägt **generateheader** mit dem \_ Fehler "MF E \_ ASF \_ InvalidData" fehl.

4.  Rufen Sie [**mfkreatememorybuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) auf, um in Schritt 3 einen Medien Puffer mit der empfangenen Größe zu erstellen.
5.  Rufen Sie **generateheader** erneut auf, um das neue ASF-Header Objekt aus dem ContentInfo-Objekt im Medien Puffer zu generieren, den Sie in Schritt 4 erstellt haben.

    Die Länge der Daten im Medien Puffer wird aktualisiert, und die neue Größe wird im *pcbheader* -Parameter zurückgegeben.

6.  Schreiben Sie den Inhalt des Medien Puffers am Anfang der Datei. Die Anwendung kann den Bytestream verwenden, um den Schreibvorgang auszuführen. Beispielcode finden Sie unter [**IMF Bytestream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

### <a name="example"></a>Beispiel

Der folgende Beispielcode zeigt, wie ein ContentInfo-Objekt erstellt und ein Medien Puffer generiert wird, um das neue Header Objekt zu speichern. Ein umfassendes Beispiel, in dem dieser Code verwendet wird, finden [Sie unter Tutorial: Kopieren von ASF-Streams aus einer Datei in eine andere](tutorial--copying-asf-streams-from-one-file-to-another.md).


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines ASF-Header Objekts für eine neue Datei](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



