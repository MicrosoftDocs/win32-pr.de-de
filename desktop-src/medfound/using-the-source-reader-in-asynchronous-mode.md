---
description: In diesem Thema wird beschrieben, wie der Quell Leser im asynchronen Modus verwendet wird.
ms.assetid: 9D3C2780-D7DB-4151-8474-9A19EC94F6BE
title: Verwenden des Quell Readers im asynchronen Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357d0405cb3e594d059b7c93e793250e0be88562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041899"
---
# <a name="using-the-source-reader-in-asynchronous-mode"></a>Verwenden des Quell Readers im asynchronen Modus

In diesem Thema wird beschrieben, wie der [Quell Leser](source-reader.md) im asynchronen Modus verwendet wird. Im asynchronen Modus stellt die Anwendung eine Rückruf Schnittstelle bereit, die verwendet wird, um die Anwendung darüber zu benachrichtigen, dass Daten verfügbar sind.

In diesem Thema wird davon ausgegangen, dass Sie das Thema [zum Verarbeiten von Mediendaten mithilfe des Quell Lesers](processing-media-data-with-the-source-reader.md)bereits gelesen haben.

## <a name="using-asynchronous-mode"></a>Verwenden des asynchronen Modus

Der Quell Reader funktioniert entweder im synchronen oder asynchronen Modus. Im Codebeispiel im vorherigen Abschnitt wird davon ausgegangen, dass der Quell Leser den synchronen Modus verwendet. Dies ist die Standardeinstellung. Im synchronen Modus wird die [**IMF sourcereader:: lesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) -Methode blockiert, während die Medienquelle das nächste Beispiel erzeugt. Eine Medienquelle ruft in der Regel Daten aus einer externen Quelle (z. b. einer lokalen Datei oder einer Netzwerkverbindung) ab, sodass die Methode den aufrufenden Thread für eine merkliche Zeit blockieren kann.

Im asynchronen Modus gibt das "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " sofort zurück, und die Arbeit wird in einem anderen Thread ausgeführt. Nachdem der Vorgang beendet wurde, ruft der Quell Leser die Anwendung über die [**IMF sourcereadercallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) -Rückruf Schnittstelle auf. Um den asynchronen Modus zu verwenden, müssen Sie beim ersten Erstellen des Quell Readers wie folgt einen Rückruf Zeiger bereitstellen:

1.  Erstellen Sie einen Attribut Speicher, indem Sie die [**mfcreateattribute**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) -Funktion aufrufen.
2.  Legen Sie [das \_ \_ \_ Async- \_ Rückruf Attribut des MF-Quell Readers](mf-source-reader-async-callback.md) für den Attribut Speicher fest. Der Attribut Wert ist ein Zeiger auf das Rückruf Objekt.
3.  Wenn Sie den Quell Reader erstellen, übergeben Sie den Attribut Speicher an die Erstellungs Funktion im *pattributes* -Parameter. Alle Funktionen zum Erstellen des Quell Readers verfügen über diesen Parameter.

Das folgende Beispiel zeigt die erforderlichen Schritte:


```C++
HRESULT CreateSourceReaderAsync(
    PCWSTR pszURL, 
    IMFSourceReaderCallback *pCallback, 
    IMFSourceReader **ppReader)
{
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAttributes->SetUnknown(MF_SOURCE_READER_ASYNC_CALLBACK, pCallback);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateSourceReaderFromURL(pszURL, pAttributes, ppReader);

done:
    SafeRelease(&pAttributes);
    return hr;
}
```



Nachdem Sie den Quell Leser erstellt haben, können Sie nicht zwischen synchronen und asynchronen Modi wechseln.

Zum Abrufen von Daten im asynchronen Modus wird die Methode "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " aufgerufen, aber die letzten vier Parameter werden auf **null** festgelegt, wie im folgenden Beispiel gezeigt.


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



Wenn die "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) "-Methode asynchron abgeschlossen wird, ruft der Quell Leser die [**IMF sourcereadercallback:: onlesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) -Methode auf. Diese Methode hat fünf Parameter:

-   *hrStatus*: enthält einen **HRESULT** -Wert. Dies ist derselbe Wert, den "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) " im synchronen Modus zurückgeben würde. Wenn *hrStatus* einen Fehlercode enthält, können Sie die restlichen Parameter ignorieren.
-   *dwstreamindex*, *dwstreamflags*, lltimestamp und *psample*: Diese drei Parameter entsprechen den letzten drei Parametern in "read [**Sample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)". Sie enthalten die Datenstrom Nummer, Statusflags und den [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Zeiger.


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



Außerdem werden von der Rückruf Schnittstelle zwei weitere Methoden definiert:

-   [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent). Benachrichtigt die Anwendung, wenn bestimmte Ereignisse in der Medienquelle auftreten, z. b. Pufferung oder Netzwerk Verbindungs Ereignisse.
-   [**Onflush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush). Wird aufgerufen, wenn die [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) -Methode abgeschlossen wird.

## <a name="implementing-the-callback-interface"></a>Implementieren der Rückruf Schnittstelle

Die Rückruf Schnittstelle muss Thread sicher sein, da [**onlesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) und die anderen Rückruf Methoden von Arbeitsthreads aufgerufen werden.

Es gibt verschiedene Ansätze, die Sie bei der Implementierung des Rückrufs durchführen können. Beispielsweise können Sie die gesamte Arbeit innerhalb des Rückrufs ausführen, oder Sie können den Rückruf verwenden, um die Anwendung zu benachrichtigen (z. b. durch Signalisieren eines Ereignis Handles) und dann die Arbeit aus dem Anwendungs Thread ausführen.

Die [**onlesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) -Methode wird einmal für jeden Aufruf aufgerufen, den Sie an der [**imfsourcereader:: lesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) -Methode vornehmen. Um das nächste Beispiel abzurufen, nennen Sie "read **Sample** " erneut. Wenn ein Fehler auftritt, wird " **onlesesample** " mit einem Fehlercode für den Parameter " *hrStatus* " aufgerufen.

Das folgende Beispiel zeigt eine minimale Implementierung der Rückruf Schnittstelle. Hier ist die Deklaration einer Klasse, die die-Schnittstelle implementiert.


```C++
#include <shlwapi.h>

class SourceReaderCB : public IMFSourceReaderCallback
{
public:
    SourceReaderCB(HANDLE hEvent) : 
      m_nRefCount(1), m_hEvent(hEvent), m_bEOS(FALSE), m_hrStatus(S_OK)
    {
        InitializeCriticalSection(&m_critsec);
    }

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(SourceReaderCB, IMFSourceReaderCallback),
            { 0 },
        };
        return QISearch(this, qit, iid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }
    STDMETHODIMP_(ULONG) Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // IMFSourceReaderCallback methods
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);

    STDMETHODIMP OnEvent(DWORD, IMFMediaEvent *)
    {
        return S_OK;
    }

    STDMETHODIMP OnFlush(DWORD)
    {
        return S_OK;
    }

public:
    HRESULT Wait(DWORD dwMilliseconds, BOOL *pbEOS)
    {
        *pbEOS = FALSE;

        DWORD dwResult = WaitForSingleObject(m_hEvent, dwMilliseconds);
        if (dwResult == WAIT_TIMEOUT)
        {
            return E_PENDING;
        }
        else if (dwResult != WAIT_OBJECT_0)
        {
            return HRESULT_FROM_WIN32(GetLastError());
        }

        *pbEOS = m_bEOS;
        return m_hrStatus;
    }
    
private:
    
    // Destructor is private. Caller should call Release.
    virtual ~SourceReaderCB() 
    {
    }

    void NotifyError(HRESULT hr)
    {
        wprintf(L"Source Reader error: 0x%X\n", hr);
    }

private:
    long                m_nRefCount;        // Reference count.
    CRITICAL_SECTION    m_critsec;
    HANDLE              m_hEvent;
    BOOL                m_bEOS;
    HRESULT             m_hrStatus;

};
```



In diesem Beispiel sind die [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) -Methode und die [**onflush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) -Methode nicht interessiert, sodass Sie einfach **S \_ OK** zurückgeben. Die-Klasse verwendet ein Ereignis handle, um die Anwendung zu signalisieren. Dieses Handle wird durch den-Konstruktor bereitgestellt.

In diesem minimalen Beispiel druckt die [**onlesesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) -Methode nur den Zeitstempel im Konsolenfenster. Anschließend werden der Statuscode und das Flag für das Ende des Streams gespeichert und dem Ereignis Handle signalisiert:


```C++
HRESULT SourceReaderCB::OnReadSample(
    HRESULT hrStatus,
    DWORD /* dwStreamIndex */,
    DWORD dwStreamFlags,
    LONGLONG llTimestamp,
    IMFSample *pSample      // Can be NULL
    )
{
    EnterCriticalSection(&m_critsec);

    if (SUCCEEDED(hrStatus))
    {
        if (pSample)
        {
            // Do something with the sample.
            wprintf(L"Frame @ %I64d\n", llTimestamp);
        }
    }
    else
    {
        // Streaming error.
        NotifyError(hrStatus);
    }

    if (MF_SOURCE_READERF_ENDOFSTREAM & dwStreamFlags)
    {
        // Reached the end of the stream.
        m_bEOS = TRUE;
    }
    m_hrStatus = hrStatus;

    LeaveCriticalSection(&m_critsec);
    SetEvent(m_hEvent);
    return S_OK;
}
```



Der folgende Code zeigt, wie die Anwendung diese Rückruf Klasse verwendet, um alle Video Frames aus einer Mediendatei zu lesen:


```C++
HRESULT ReadMediaFile(PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    SourceReaderCB *pCallback = NULL;

    HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto done;
    }

    // Create an instance of the callback object.
    pCallback = new (std::nothrow) SourceReaderCB(hEvent);
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Create the Source Reader.
    hr = CreateSourceReaderAsync(pszURL, pCallback, &pReader);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConfigureDecoder(pReader, MF_SOURCE_READER_FIRST_VIDEO_STREAM);
    if (FAILED(hr))
    {
        goto done;
    }

    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    while (SUCCEEDED(hr))
    {
        BOOL bEOS;
        hr = pCallback->Wait(INFINITE, &bEOS);
        if (FAILED(hr) || bEOS)
        {
            break;
        }
        hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM,
            0, NULL, NULL, NULL, NULL);
    }

done:
    SafeRelease(&pReader);
    SafeRelease(&pCallback);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quell Leser](source-reader.md)
</dt> </dl>

 

 



