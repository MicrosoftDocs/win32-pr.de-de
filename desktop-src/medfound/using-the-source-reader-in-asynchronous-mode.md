---
description: In diesem Thema wird beschrieben, wie der Quellleser im asynchronen Modus verwendet wird.
ms.assetid: 9D3C2780-D7DB-4151-8474-9A19EC94F6BE
title: Verwenden des Quelllesers im asynchronen Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 514331f9d1635cbe83222ccf413b1dbb5a7d350b4656e23ed27ccede5c0be6f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237505"
---
# <a name="using-the-source-reader-in-asynchronous-mode"></a>Verwenden des Quelllesers im asynchronen Modus

In diesem Thema wird beschrieben, wie der [Quellleser](source-reader.md) im asynchronen Modus verwendet wird. Im asynchronen Modus stellt die Anwendung eine Rückrufschnittstelle bereit, die verwendet wird, um die Anwendung zu benachrichtigen, dass Daten verfügbar sind.

In diesem Thema wird davon ausgegangen, dass Sie das Thema Verwenden des Quelllesers zum Verarbeiten von [Mediendaten bereits gelesen haben.](processing-media-data-with-the-source-reader.md)

## <a name="using-asynchronous-mode"></a>Verwenden des asynchronen Modus

Der Quellleser arbeitet entweder im synchronen modus oder im asynchronen Modus. Im Codebeispiel im vorherigen Abschnitt wird davon ausgegangen, dass der Quellleser den synchronen Modus verwendet, der die Standardeinstellung ist. Im synchronen Modus wird die [**METHODE 10001::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) blockiert, während die Medienquelle das nächste Beispiel erzeugt. Eine Medienquelle ruft in der Regel Daten aus einer externen Quelle ab (z. B. aus einer lokalen Datei oder einer Netzwerkverbindung), sodass die Methode den aufrufenden Thread für einen spürbaren Zeitraum blockieren kann.

Im asynchronen Modus gibt [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) sofort zurück, und die Arbeit wird in einem anderen Thread ausgeführt. Nachdem der Vorgang abgeschlossen ist, ruft der Quellleser die Anwendung über die [**RÜCKRUF-Schnittstelle DESTSourceReaderCallbacks**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) auf. Um den asynchronen Modus verwenden zu können, müssen Sie wie folgt einen Rückrufzeiger bereitstellen, wenn Sie den Quellleser zum ersten Mal erstellen:

1.  Erstellen Sie einen Attributspeicher, indem Sie die [**MFCreateAttributes-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) aufrufen.
2.  Legen Sie das [ \_ \_ \_ ASYNC CALLBACK-Attribut des MF-QUELLLESERS \_ ](mf-source-reader-async-callback.md) für den Attributspeicher fest. Der Attributwert ist ein Zeiger auf Ihr Rückrufobjekt.
3.  Wenn Sie den Quellleser erstellen, übergeben Sie den Attributspeicher an die *Erstellungsfunktion im pAttributes-Parameter.* Alle Funktionen zum Erstellen des Quelllesers verfügen über diesen Parameter.

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



Nachdem Sie den Quellleser erstellt haben, können Sie nicht zwischen synchronen und asynchronen Modi wechseln.

Um Daten im asynchronen Modus zu erhalten, rufen Sie die [**ReadSample-Methode**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) auf, legen aber die letzten vier Parameter auf **NULL** fest, wie im folgenden Beispiel gezeigt.


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



Wenn die [**ReadSample-Methode**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) asynchron abgeschlossen wird, ruft der Quellleser die [**METHODE ZU ERHALTENSourceReaderCallback::OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) auf. Diese Methode verfügt über fünf Parameter:

-   *hrStatus:* Enthält einen **HRESULT-Wert.** Dies ist der gleiche Wert, den [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) im synchronen Modus zurückgeben würde. Wenn *hrStatus* einen Fehlercode enthält, können Sie die verbleibenden Parameter ignorieren.
-   *dwStreamIndex,* *dwStreamFlags,* llTimestamp und *pSample:* Diese drei Parameter entsprechen den letzten drei Parametern in [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample). Sie enthalten die Streamnummer, Statusflags bzw. [**den BZW. den 100000-Zeiger .**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



Darüber hinaus definiert die Rückrufschnittstelle zwei weitere Methoden:

-   [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent). Benachrichtigt die Anwendung, wenn bestimmte Ereignisse in der Medienquelle auftreten, z. B. Pufferungs- oder Netzwerkverbindungsereignisse.
-   [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush). Wird aufgerufen, [**wenn die Flush-Methode**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) abgeschlossen ist.

## <a name="implementing-the-callback-interface"></a>Implementieren der Rückrufschnittstelle

Die Rückrufschnittstelle muss threadsicher sein, da [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) und die anderen Rückrufmethoden von Arbeitsthreads aufgerufen werden.

Es gibt verschiedene Ansätze, die Sie beim Implementieren des Rückrufs verfolgen können. Beispielsweise können Sie die ganze Arbeit innerhalb des Rückrufs oder den Rückruf verwenden, um die Anwendung zu benachrichtigen (z. B. durch Signalisieren eines Ereignishandpunkts) und dann im Anwendungsthread arbeiten.

Die [**OnReadSample-Methode**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) wird einmal für jeden Aufruf aufgerufen, den Sie an die [**METHODE ZUEsourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) stellen. Um das nächste Beispiel zu erhalten, rufen **Sie ReadSample erneut** auf. Wenn ein Fehler auftritt, **wird OnReadSample** mit einem Fehlercode für den *hrStatus-Parameter* aufgerufen.

Das folgende Beispiel zeigt eine minimale Implementierung der Rückrufschnittstelle. Zuerst ist hier die Deklaration einer Klasse, die die -Schnittstelle implementiert.


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



In diesem Beispiel sind die Methoden [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) und [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) nicht von Interesse, daher geben sie einfach **S OK \_ zurück.** Die -Klasse verwendet ein Ereignishand handle, um die Anwendung zu signalisieren. dieses Handle wird über den Konstruktor bereitgestellt.

In diesem minimalen Beispiel gibt die [**OnReadSample-Methode**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) nur den Zeitstempel im Konsolenfenster aus. Anschließend werden der Statuscode und das Flag für das Ende des Streams gespeichert, und das Ereignishand handle wird signalisiert:


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



Der folgende Code zeigt, dass die Anwendung diese Rückrufklasse verwenden würde, um alle Videoframes aus einer Mediendatei zu lesen:


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

[Quellleser](source-reader.md)
</dt> </dl>

 

 



