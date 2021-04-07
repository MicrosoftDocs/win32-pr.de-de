---
title: Verwenden von Markern
description: Verwenden von Markern
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media-Format-SDK, Marker
- Advanced Systems Format (ASF), Marker
- ASF (Advanced Systems Format), Marker
- Advanced Systems Format (ASF), suchen nach Markern
- ASF (Advanced Systems Format), suchen nach Markern
- Marker, Info
- Marker, hinzufügen
- Marker, entfernen
- Marker, Abrufen
- Marker, suchen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724115"
---
# <a name="using-markers"></a>Verwenden von Markern

Ein *Marker* ist ein benannter Punkt innerhalb einer ASF-Datei. Jeder Marker besteht aus einem Namen und einem zugeordneten Zeitpunkt, gemessen als Offset vom Anfang der Datei. Eine Anwendung kann Marker verwenden, um verschiedenen Punkten innerhalb des Inhalts Namen zuzuweisen, diese Namen dem Benutzer anzuzeigen und dann die Markerpositionen zu suchen. Eine Anwendung kann Marker zu einer vorhandenen ASF-Datei hinzufügen oder daraus entfernen.

Die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle enthält Methoden zum Arbeiten mit Markern. Das Metadateneditor Objekt unterstützt das Hinzufügen und Entfernen von Markern Die Writer-und Reader-Objekte können Marker abrufen, aber keine Marker hinzufügen oder entfernen.

## <a name="adding-markers"></a>Marker werden hinzugefügt

Fragen Sie zum Hinzufügen eines Markers den Metadateneditor nach der **iwmheaderinfo** -Schnittstelle ab. Anschließend wird die Methode [**iwmheaderinfo:: AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) aufgerufen, wobei der markerName als breit Zeichen-Zeichenfolge und die Zeit in 100-Nanosecond-Einheiten angegeben werden. Die Zeit darf die Datei Dauer nicht überschreiten. Zwei Marker können gleichzeitig vorhanden sein.

Im folgenden Beispiel werden einer Datei mehrere Marker hinzugefügt:


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a>Entfernen von Markern

Um einen Marker zu entfernen, geben Sie [**iwmheaderinfo:: RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker)an, und geben Sie dabei den Index des zu entfernenden Markers an. Marker werden automatisch in zunehmender Reihenfolge sortiert, sodass Index 0 immer der erste Marker ist. Beachten Sie, dass durch den Aufruf von **RemoveMarker** die Indexnummern aller folgenden Marker geändert werden. Der folgende Code, in dem *pinfo* ein Zeiger auf eine **iwmheaderinfo** -Schnittstelle ist, entfernt alle Marker aus einer Datei:


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a>Abrufen von Markern

Um den Namen und die Uhrzeit eines Markers abzurufen, führen Sie die folgenden Schritte aus:

1.  Aufrufen der [**iwmheaderinfo:: getmarkercount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) -Methode, um zu bestimmen, wie viele Marker die Datei enthält.
2.  Ruft die Größe der Zeichenfolge ab, die der markerName enthalten muss. Aufrufen Sie hierzu die [**iwmheaderinfo:: getmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) -Methode. Geben Sie den Index des abzurufenden Markers und **null** für den Zeichen folgen Puffer an (den *pwszmarkername* -Parameter). Die-Methode gibt die Länge der Zeichenfolge, einschließlich des abschließenden ' \\ 0 '-Zeichens, im *pcchmarkernamelen* -Parameter zurück.
3.  Weisen Sie eine Zeichenfolge mit breit Zeichen zu, um den Namen zu erhalten.
4.  Erneutes Aufrufen von **getmarker** , aber dieses Mal wird die Adresse der Zeichenfolge im *pwszmarkername* -Parameter übergeben. Die-Methode schreibt den Markernamen in die Zeichenfolge und gibt die *Markerzeit im pcnsmarkertime* -Parameter zurück.

Der folgende Code durchläuft alle Markierungen in der richtigen Reihenfolge und ruft den Namen und die Uhrzeit ab:


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a>Suchen nach einem Marker

Um die Wiedergabe von einem markerspeicherort aus zu starten, müssen Sie die [**IWMReaderAdvanced2:: startatmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) -Methode des Reader-Objekts aufzurufen und den Index der Markierung angeben. Die restlichen Parameter sind identisch mit denen für die [**iwmreader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) -Methode. Im folgenden Beispiel wird der Reader nach der [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) -Schnittstelle abgefragt und der erste Marker gesucht.


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmheaderinfo-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMReaderAdvanced2:: startatmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




