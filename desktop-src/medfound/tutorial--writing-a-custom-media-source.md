---
description: In diesem Thema wird das MPEG-1 Media Source SDK-Beispiel ausführlich erläutert.
ms.assetid: d392f30c-c963-4eb3-add2-1bb986919c0b
title: 'Fallstudie: MPEG-1-Medienquelle'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e1f72cc6ae6df119439bdae1942732bf8d2fa2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104050678"
---
# <a name="case-study-mpeg-1-media-source"></a>Fallstudie: MPEG-1-Medienquelle

In Microsoft Media Foundation wird das Objekt, das Mediendaten in die Daten Pipeline einführt, als *Medienquelle* bezeichnet. In diesem Thema wird das [MPEG-1 Media Source](mpeg1source-sample.md) SDK-Beispiel ausführlich erläutert.

-   [Voraussetzungen](#prerequisites)
-   [C++-Klassen, die in der MPEG-1-Quelle verwendet werden](#c-classes-used-in-the-mpeg-1-source)
-   [Byte Datenstrom-Handler](#byte-stream-handler)
-   [Präsentations Deskriptor](#presentation-descriptor)
-   [Streamingzustände](#streaming-states)
    -   [Starten](#start)
    -   [Anhalten](#pause)
    -   [Beenden](#stop)
-   [Beispiel Anforderungen](#sample-requests)
-   [Ende des Streams](#end-of-stream)
-   [Asynchrone Vorgänge](#asynchronous-operations)
    -   [Vorgangs Warteschlange](#operation-queue)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie dieses Thema lesen, sollten Sie sich mit den folgenden Media Foundation Konzepten vertraut machen:

-   [Medienquellen-Objektmodell](media-source-object-model.md)
-   [Asynchrone Rückruf Methoden](asynchronous-callback-methods.md).
-   [Arbeits Warteschlangen](work-queues.md)
-   [Medienereignis Generatoren](media-event-generators.md)
-   [Medien Puffer](media-buffers.md)
-   [Medien Beispiele](media-samples.md)
-   [Medientypen](media-types.md)

Außerdem sollten Sie ein grundlegendes Verständnis der Media Foundation Architektur haben, insbesondere der Rolle von Medienquellen in der Pipeline. (Weitere Informationen finden Sie unter [Medienquellen](media-sources.md).)

Außerdem sollten Sie das Thema [Schreiben einer benutzerdefinierten Medienquelle](writing-a-custom-media-source.md)lesen, die eine allgemeinere Übersicht über die hier beschriebenen Schritte bietet.

In diesem Thema wird nicht der gesamte Code aus dem SDK-Beispiel reproduziert, da das Beispiel ziemlich groß ist.

## <a name="c-classes-used-in-the-mpeg-1-source"></a>C++-Klassen, die in der MPEG-1-Quelle verwendet werden

Die Beispiel-MPEG-1-Quelle wird mit den folgenden C++-Klassen implementiert:

-   `MPEG1ByteStreamHandler`. Implementiert den bytestreamhandler für die Medienquelle. Bei einem Bytestream erstellt der bytestreamhandler eine Instanz der Quelle.
-   `MPEG1Source`. Implementiert die Medienquelle.
-   `MPEG1Stream`. Implementiert die Medienstrom Objekte. Die Medienquelle erstellt ein `MPEG1Stream` -Objekt für jeden Audiostream oder Videostream im MPEG-1-Bitstream.
-   `Parser`. Analysiert den MPEG-1-Bitstream. In den meisten Fällen sind die Details dieser Klasse für die Media Foundation-APIs nicht relevant.
-   SourceOP, opqueue: diese beiden Klassen verwalten asynchrone Vorgänge in der Medienquelle. (Siehe [asynchrone Vorgänge](#asynchronous-operations)).

Weitere verschiedene Hilfsklassen werden weiter unten in diesem Thema beschrieben.

## <a name="byte-stream-handler"></a>Byte-Stream Handler

Der *Byte Datenstrom* Handler ist das Objekt, das die Medienquelle erstellt. Der Byte Datenstrom Handler wird vom quellresolver erstellt. Anwendungen interagieren nicht direkt mit dem Byte Datenstrom-Handler. Der quellresolver ermittelt den bytestreamhandler, indem er sich in der Registrierung ansieht. Der Handler wird durch die Dateinamenerweiterung oder den MIME-Typ registriert. Bei der MPEG-1-Quelle wird der Byte Datenstrom Handler für die Dateinamenerweiterung ". mpg" registriert.

> [!Note]  
> Wenn Sie benutzerdefinierte URL-Schemas unterstützen möchten, können Sie auch einen *Schema Handler* schreiben. Die MPEG-1-Quelle ist für lokale Dateien konzipiert, und Media Foundation stellt bereits einen Schema Handler für "file://"-URLs bereit.

 

Der Byte Datenstrom Handler implementiert die [**IMF bytestreamhandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) -Schnittstelle. Diese Schnittstelle verfügt über zwei wichtige Methoden, die implementiert werden müssen:

-   [**Beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). Startet einen asynchronen Vorgang, um die Medienquelle zu erstellen.
-   [**Endkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject). Schließt den asynchronen-Aufrufvorgang ab.

Zwei andere Methoden sind optional und werden im SDK-Beispiel nicht implementiert:

-   [**Cancelobjectcreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation). Bricht die [**beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) -Methode ab. Diese Methode ist nützlich für eine Netzwerkquelle, bei der beim Start eine hohe Latenz auftreten kann.
-   [**Getmaxnummeriofbytesrequirements dforresolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution). Ruft die maximale Anzahl von Bytes ab, die der Handler aus dem Quelldaten Strom liest. Implementieren Sie diese Methode, wenn Sie wissen, wie viel Daten der Byte Strom Handler vor der Erstellung der Medienquelle haben kann. Andernfalls geben Sie einfach **E \_ notimpl** zurück.

Hier ist die Implementierung der [**beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) -Methode:


```C++
HRESULT MPEG1ByteStreamHandler::BeginCreateObject(
        /* [in] */ IMFByteStream *pByteStream,
        /* [in] */ LPCWSTR pwszURL,
        /* [in] */ DWORD dwFlags,
        /* [in] */ IPropertyStore *pProps,
        /* [out] */ IUnknown **ppIUnknownCancelCookie,  // Can be NULL
        /* [in] */ IMFAsyncCallback *pCallback,
        /* [in] */ IUnknown *punkState                  // Can be NULL
        )
{
    if (pByteStream == NULL)
    {
        return E_POINTER;
    }

    if (pCallback == NULL)
    {
        return E_POINTER;
    }

    if ((dwFlags & MF_RESOLUTION_MEDIASOURCE) == 0)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFAsyncResult *pResult = NULL;
    MPEG1Source    *pSource = NULL;

    // Create an instance of the media source.
    hr = MPEG1Source::CreateInstance(&pSource);

    // Create a result object for the caller's async callback.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);
    }

    // Start opening the source. This is an async operation.
    // When it completes, the source will invoke our callback
    // and then we will invoke the caller's callback.
    if (SUCCEEDED(hr))
    {
        hr = pSource->BeginOpen(pByteStream, this, NULL);
    }

    if (SUCCEEDED(hr))
    {
        if (ppIUnknownCancelCookie)
        {
            *ppIUnknownCancelCookie = NULL;
        }

        m_pSource = pSource;
        m_pSource->AddRef();

        m_pResult = pResult;
        m_pResult->AddRef();
    }

// cleanup
    SafeRelease(&pSource);
    SafeRelease(&pResult);
    return hr;
}
```



Die-Methode führt die folgenden Schritte aus:

1.  Erstellt eine neue Instanz eines `MPEG1Source`-Objekts.
2.  Erstellen Sie ein asynchrones Ergebnis Objekt. Dieses Objekt wird später verwendet, um die Rückruf Methode des Quell Resolvers aufzurufen.
3.  Ruft `MPEG1Source::BeginOpen` auf, eine asynchrone Methode, die in der-Klasse definiert ist `MPEG1Source` .
4.  Legt *ppiunknowncancelcookie* auf **null** fest, um den Aufrufer darüber zu informieren, dass [**cancelobjectcreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) nicht unterstützt wird.

`MPEG1Source::BeginOpen`Mit der-Methode wird der Bytestream gelesen und das-Objekt initialisiert `MPEG1Source` . Diese Methode ist nicht Teil der öffentlichen API. Sie können beliebige Mechanismen zwischen dem Handler und der Medienquelle definieren, die Ihren Anforderungen entspricht. Wenn Sie den größten Teil der Logik in die Medienquelle einfügen, bleibt der Byte Strom Handler relativ einfach.

`BeginOpen`Führt die folgenden Schritte aus:

1.  Ruft [**imfbytestream:: getFeatures**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) auf, um zu überprüfen, ob der quellbytestream sowohl lesbar als auch suchbar ist.
2.  Ruft [**imfbytestream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) auf, um eine asynchrone e/a-Anforderung zu starten.

Der Rest der Initialisierung erfolgt asynchron. Die Medienquelle liest genügend Daten aus dem Stream, um die MPEG-1-Sequenz Header zu analysieren. Anschließend wird ein *Präsentations Deskriptor* erstellt, bei dem es sich um das Objekt handelt, das zum Beschreiben der Audiodaten und Videostreams in der Datei verwendet wird. (Weitere Informationen finden Sie unter [Präsentations Deskriptor](#presentation-descriptor).) Wenn der `BeginOpen` Vorgang abgeschlossen ist, ruft der Byte Datenstrom Handler die Rückruf Methode des Quell Resolvers auf. An diesem Punkt ruft der Quell Konflikt Löser [**IMF bytestreamhandler:: endkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject)auf. Die **endkreateobject** -Methode gibt den Status des Vorgangs zurück.


```C++
HRESULT MPEG1ByteStreamHandler::EndCreateObject(
        /* [in] */ IMFAsyncResult *pResult,
        /* [out] */ MF_OBJECT_TYPE *pObjectType,
        /* [out] */ IUnknown **ppObject)
{
    if (pResult == NULL || pObjectType == NULL || ppObject == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    *pObjectType = MF_OBJECT_INVALID;
    *ppObject = NULL;

    hr = pResult->GetStatus();

    if (SUCCEEDED(hr))
    {
        *pObjectType = MF_OBJECT_MEDIASOURCE;

        assert(m_pSource != NULL);

        hr = m_pSource->QueryInterface(IID_PPV_ARGS(ppObject));
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pResult);
    return hr;
}
```



Wenn während dieses Vorgangs ein Fehler auftritt, wird der Rückruf mit einem Fehlerstatus Code aufgerufen.

## <a name="presentation-descriptor"></a>Präsentations Deskriptor

Der Präsentations Deskriptor beschreibt den Inhalt der MPEG-1-Datei, einschließlich der folgenden Informationen:

-   Die Anzahl der Streams.
-   Das Format der einzelnen Datenströme.
-   Datenstrom Bezeichner.
-   Der Auswahl Status der einzelnen Datenströme (ausgewählt oder deaktiviert).

Im Hinblick auf die Media Foundation Architektur enthält der Präsentations Deskriptor einen oder mehrere *streamdeskriptoren*. Jeder Datenstrom Deskriptor enthält einen *Medientyp Handler*, mit dem Medientypen im Stream abgerufen oder festgelegt werden. Media Foundation stellt Aktien Implementierungen für den Präsentations Deskriptor und den Datenstrom Deskriptor bereit. Diese sind für die meisten Medienquellen geeignet.

Um einen Präsentations Deskriptor zu erstellen, führen Sie die folgenden Schritte aus:

1.  Für jeden Stream:
    1.  Geben Sie eine Datenstrom-ID und ein Array möglicher Medientypen an. Wenn der Stream mehr als einen Medientyp unterstützt, ordnen Sie die Liste der Medientypen ggf. nach Belieben zu. (Geben Sie zuerst den optimalen Typ und den am wenigsten optimalen Typ an.)
    2.  Rufen Sie [**mfkreatestreamdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) auf, um den Datenstrom Deskriptor zu erstellen.
    3.  Aufrufen von [**imfstreamdescriptor:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) für den neu erstellten streamdeskriptor.
    4.  Um das Standardformat für den Stream festzulegen, können Sie [**imfmediatypeer Handler:: setcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) aufrufen. Wenn mehr als ein Medientyp vorhanden ist, sollten Sie in der Regel den ersten Typ in der Liste festlegen.
2.  Aufrufen von [**mfkreatepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) und übergeben des Arrays von streamdeskriptorzeigern.
3.  Für jeden Stream wird [**imfpresentationdescriptor:: selectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) oder [**deselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) aufgerufen, um den Standardauswahl Status festzulegen. Wenn mehr als ein Datenstrom desselben Typs (Audiodatei oder Video) vorhanden ist, sollte standardmäßig nur eine ausgewählt werden.

Das- `MPEG1Source` Objekt erstellt den Präsentations Deskriptor in der- `InitPresentationDescriptor` Methode:


```C++
HRESULT MPEG1Source::InitPresentationDescriptor()
{
    HRESULT hr = S_OK;
    DWORD cStreams = 0;

    assert(m_pPresentationDescriptor == NULL);
    assert(m_state == STATE_OPENING);

    if (m_pHeader == NULL)
    {
        return E_FAIL;
    }

    // Get the number of streams, as declared in the MPEG-1 header, skipping
    // any streams with an unsupported format.
    for (DWORD i = 0; i < m_pHeader->cStreams; i++)
    {
        if (IsStreamTypeSupported(m_pHeader->streams[i].type))
        {
            cStreams++;
        }
    }

    // How many streams do we actually have?
    if (cStreams > m_streams.GetCount())
    {
        // Keep reading data until we have seen a packet for each stream.
        return S_OK;
    }

    // We should never create a stream we don't support.
    assert(cStreams == m_streams.GetCount());

    // Ready to create the presentation descriptor.

    // Create an array of IMFStreamDescriptor pointers.
    IMFStreamDescriptor **ppSD =
            new (std::nothrow) IMFStreamDescriptor*[cStreams];

    if (ppSD == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    ZeroMemory(ppSD, cStreams * sizeof(IMFStreamDescriptor*));

    // Fill the array by getting the stream descriptors from the streams.
    for (DWORD i = 0; i < cStreams; i++)
    {
        hr = m_streams[i]->GetStreamDescriptor(&ppSD[i]);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the presentation descriptor.
    hr = MFCreatePresentationDescriptor(cStreams, ppSD,
        &m_pPresentationDescriptor);

    if (FAILED(hr))
    {
        goto done;
    }

    // Select the first video stream (if any).
    for (DWORD i = 0; i < cStreams; i++)
    {
        GUID majorType = GUID_NULL;

        hr = GetStreamMajorType(ppSD[i], &majorType);
        if (FAILED(hr))
        {
            goto done;
        }

        if (majorType == MFMediaType_Video)
        {
            hr = m_pPresentationDescriptor->SelectStream(i);
            if (FAILED(hr))
            {
                goto done;
            }
            break;
        }
    }

    // Switch state from "opening" to stopped.
    m_state = STATE_STOPPED;

    // Invoke the async callback to complete the BeginOpen operation.
    hr = CompleteOpen(S_OK);

done:
    // clean up:
    if (ppSD)
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            SafeRelease(&ppSD[i]);
        }
        delete [] ppSD;
    }
    return hr;
}
```



Die Anwendung ruft den Präsentations Deskriptor durch Aufrufen von [**imfmediasource:: createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)ab. Diese Methode erstellt eine flache Kopie des Präsentations Deskriptors, indem [**imfpresentationdescriptor:: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone)aufgerufen wird. (Die Kopie enthält Zeiger auf die ursprünglichen streamdeskriptoren.) Die Anwendung kann den präsentationdeskriptor verwenden, um den Medientyp festzulegen, einen Stream auszuwählen oder einen Stream zu deaktivieren.

Optional können Präsentations Deskriptoren und streamdeskriptoren Attribute enthalten, die zusätzliche Informationen über die Quelle enthalten. Eine Liste solcher Attribute finden Sie in den folgenden Themen:

-   [Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
-   [Streamdeskriptorattribute](stream-descriptor-attributes.md)

Ein Attribut verdient besondere Erwähnung: das [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) -Attribut enthält die Gesamtdauer der Quelle. Legen Sie dieses Attribut fest, wenn Sie die Dauer im Voraus kennen. die Dauer kann z. b. in den Datei Headern angegeben werden, abhängig vom Dateiformat. Die Anwendung kann diesen Wert anzeigen oder verwenden, um eine Statusanzeige oder eine Suchleiste festzulegen.

## <a name="streaming-states"></a>Streamingzustände

Eine Medienquelle definiert die folgenden Zustände:



| State    | BESCHREIBUNG                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| Gestartet  | Die Quelle akzeptiert und verarbeitet Beispiel Anforderungen.                                                               |
| Angehalten   | Die Quelle akzeptiert Beispiel Anforderungen, verarbeitet sie aber nicht. Anforderungen werden in die Warteschlange eingereiht, bis die Quelle gestartet wurde. |
| Beendet. | Die Quelle lehnt Beispiel Anforderungen ab.                                                                             |



 

### <a name="start"></a>Start

Die [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode startet die Medienquelle. Hierfür werden die folgenden Parameter verwendet:

-   Ein Präsentations Deskriptor.
-   Eine Zeitformat-GUID.
-   Eine Startposition.

Die Anwendung muss den Präsentations Deskriptor abrufen, indem [**createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) für die Quelle aufgerufen wird. Es ist kein definierter Mechanismus zum Validieren eines Präsentations Deskriptors vorhanden. Wenn die Anwendung den falschen Präsentations Deskriptor angibt, sind die Ergebnisse nicht definiert.

Die Zeitformat-GUID gibt an, wie die Anfangsposition interpretiert werden soll. Das Standardformat ist 100-Nanosecond (NS)-Einheiten, die durch GUID NULL angegeben werden \_ . Jede Medienquelle muss 100-ns-Einheiten unterstützen. Optional kann eine Quelle auch andere Zeiteinheiten unterstützen, z. b. Frame Nummer oder Zeit Code. Es gibt jedoch keine Standardmethode, um eine Medienquelle nach der Liste der unterstützten Zeitformate abzufragen.

Die Startposition wird als **PROPVARIANT** angegeben und ermöglicht je nach Zeitformat unterschiedliche Datentypen. Bei 100-ns ist der **PROPVARIANT** -Typ entweder **VT \_ I8** oder **VT \_ empty**. Wenn **VT \_ I8**, enthält die **PROPVARIANT** die Startposition in 100-ns-Einheiten. Der Wert **VT \_ empty** hat die besondere Bedeutung "Start an der aktuellen Position".

Implementieren Sie die [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode wie folgt:

1.  Parameter und Status überprüfen:
    -   Suchen Sie nach **null** -Parametern.
    -   Überprüfen Sie die Zeitformat-GUID. Wenn der Wert ungültig ist, wird das von **MF \_ E \_ nicht unterstützte \_ Zeit \_ Format** zurückgegeben.
    -   Überprüfen Sie den Datentyp von **PROPVARIANT** , der die Anfangsposition enthält.
    -   Überprüfen Sie die Startposition. Wenn ungültig, wird " **MF \_ E \_ invalidrequest**" zurückgegeben.
    -   Wenn die Quelle heruntergefahren wurde, wird das **\_ \_ Herunterfahren von MF E** zurückgegeben.
2.  Wenn in Schritt 1 kein Fehler auftritt, stellen Sie einen asynchronen Vorgang in die Warteschlange. Alles nach diesem Schritt tritt in einem Arbeitswarteschlangen-Thread auf.
3.  Für jeden Stream:
    1.  Überprüfen Sie, ob der Stream bereits aus einer vorherigen [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Anforderung aktiv ist.
    2.  Aufrufen von [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) , um zu überprüfen, ob die Anwendung den Stream ausgewählt oder deaktiviert hat.
    3.  Wenn ein zuvor ausgewählter Stream jetzt deaktiviert ist, leeren Sie alle nicht übermittelten Beispiele für diesen Stream.
    4.  Wenn der Stream aktiv ist, sendet die Medienquelle (nicht der Stream) eines der folgenden Ereignisse:
        -   Er sendet [meupdatedstream](meupdatedstream.md) , wenn der Stream zuvor aktiv war.
        -   Andernfalls wird [menewstream](menewstream.md)gesendet.

        Bei beiden Ereignissen handelt es sich bei den Ereignisdaten um den [**IMF Media Stream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) -Zeiger für den Datenstrom.
    5.  Wenn die Quelle vom angehaltenen Zustand neu gestartet wird, sind möglicherweise ausstehende Beispiel Anforderungen vorhanden. Wenn dies der Fall ist, übermitteln Sie diese jetzt.
    6.  Wenn die Quelle eine neue Position sucht, sendet jedes Stream-Objekt ein [mestreamseeked](mestreamseeked.md) -Ereignis. Andernfalls sendet jeder Stream ein [mestreamstarted](mestreamstarted.md) -Ereignis.
4.  Wenn die Quelle eine neue Position sucht, sendet die Medienquelle ein [mesourceseeked](mesourceseeked.md) -Ereignis. Andernfalls wird ein [mesourcestarted](mesourcestarted.md) -Ereignis gesendet.

Wenn zu einem beliebigen Zeitpunkt nach Schritt 2 ein Fehler auftritt, sendet die Quelle ein [mesourcestarted](mesourcestarted.md) -Ereignis mit einem Fehlercode. Dadurch wird die Anwendung benachrichtigt, dass die [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Methode asynchron fehlgeschlagen ist.

Der folgende Code zeigt die Schritte 1 – 2:


```C++
HRESULT MPEG1Source::Start(
        IMFPresentationDescriptor* pPresentationDescriptor,
        const GUID* pguidTimeFormat,
        const PROPVARIANT* pvarStartPos
    )
{

    HRESULT hr = S_OK;
    SourceOp *pAsyncOp = NULL;

    // Check parameters.

    // Start position and presentation descriptor cannot be NULL.
    if (pvarStartPos == NULL || pPresentationDescriptor == NULL)
    {
        return E_INVALIDARG;
    }

    // Check the time format.
    if ((pguidTimeFormat != NULL) && (*pguidTimeFormat != GUID_NULL))
    {
        // Unrecognized time format GUID.
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    // Check the data type of the start position.
    if ((pvarStartPos->vt != VT_I8) && (pvarStartPos->vt != VT_EMPTY))
    {
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    EnterCriticalSection(&m_critSec);

    // Check if this is a seek request. This sample does not support seeking.

    if (pvarStartPos->vt == VT_I8)
    {
        // If the current state is STOPPED, then position 0 is valid.
        // Otherwise, the start position must be VT_EMPTY (current position).

        if ((m_state != STATE_STOPPED) || (pvarStartPos->hVal.QuadPart != 0))
        {
            hr = MF_E_INVALIDREQUEST;
            goto done;
        }
    }

    // Fail if the source is shut down.
    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Fail if the source was not initialized yet.
    hr = IsInitialized();
    if (FAILED(hr))
    {
        goto done;
    }

    // Perform a basic check on the caller's presentation descriptor.
    hr = ValidatePresentationDescriptor(pPresentationDescriptor);
    if (FAILED(hr))
    {
        goto done;
    }

    // The operation looks OK. Complete the operation asynchronously.
    hr = SourceOp::CreateStartOp(pPresentationDescriptor, &pAsyncOp);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAsyncOp->SetData(*pvarStartPos);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = QueueOperation(pAsyncOp);

done:
    SafeRelease(&pAsyncOp);
    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



Die restlichen Schritte werden im folgenden Beispiel gezeigt:


```C++
HRESULT MPEG1Source::DoStart(StartOp *pOp)
{
    assert(pOp->Op() == SourceOp::OP_START);

    IMFPresentationDescriptor *pPD = NULL;
    IMFMediaEvent  *pEvent = NULL;

    HRESULT     hr = S_OK;
    LONGLONG    llStartOffset = 0;
    BOOL        bRestartFromCurrentPosition = FALSE;
    BOOL        bSentEvents = FALSE;

    hr = BeginAsyncOp(pOp);

    // Get the presentation descriptor from the SourceOp object.
    // This is the PD that the caller passed into the Start() method.
    // The PD has already been validated.
    if (SUCCEEDED(hr))
    {
        hr = pOp->GetPresentationDescriptor(&pPD);
    }

    // Because this sample does not support seeking, the start
    // position must be 0 (from stopped) or "current position."

    // If the sample supported seeking, we would need to get the
    // start position from the PROPVARIANT data contained in pOp.

    if (SUCCEEDED(hr))
    {
        // Select/deselect streams, based on what the caller set in the PD.
        // This method also sends the MENewStream/MEUpdatedStream events.
        hr = SelectStreams(pPD, pOp->Data());
    }

    if (SUCCEEDED(hr))
    {
        m_state = STATE_STARTED;

        // Queue the "started" event. The event data is the start position.
        hr = m_pEventQueue->QueueEventParamVar(
            MESourceStarted,
            GUID_NULL,
            S_OK,
            &pOp->Data()
            );
    }

    if (FAILED(hr))
    {
        // Failure. Send the error code to the application.

        // Note: It's possible that QueueEvent itself failed, in which case it
        // is likely to fail again. But there is no good way to recover in
        // that case.

        (void)m_pEventQueue->QueueEventParamVar(
            MESourceStarted, GUID_NULL, hr, NULL);
    }

    CompleteAsyncOp(pOp);

    SafeRelease(&pEvent);
    SafeRelease(&pPD);
    return hr;
}
```



### <a name="pause"></a>Anhalten

Die [**imfmediasource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) -Methode hält die Medienquelle an. Implementieren Sie diese Methode wie folgt:

1.  Einen asynchronen Vorgang in die Warteschlange stellen.
2.  Jeder aktive Stream sendet ein [mestreampaused](mestreampaused.md) -Ereignis.
3.  Die Medienquelle sendet ein [mesourcepaused](mesourcepaused.md) -Ereignis.

Bei angehaltenen Warteschlangen werden die Quell-in die Warteschlange eingereiht (Siehe [Beispiel Anforderungen](#sample-requests).)

### <a name="stop"></a>Stop

Die [**imfmediasource:: Stopp**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) -Methode beendet die Medienquelle. Implementieren Sie diese Methode wie folgt:

1.  Einen asynchronen Vorgang in die Warteschlange stellen.
2.  Jeder aktive Stream sendet ein [mestreambeendeten](mestreamstopped.md) -Ereignis.
3.  Löschen Sie alle Beispiele und Beispiel Anforderungen in der Warteschlange.
4.  Die Medienquelle sendet ein [mesourcestpt](mesourcestopped.md) -Ereignis.

Obwohl die Quelle beendet ist, lehnt sie alle Anforderungen für Stichproben ab.

Wenn die Quelle beendet wird, während eine e/a-Anforderung ausgeführt wird, kann die e/a-Anforderung abgeschlossen werden, nachdem die Quelle in den Zustand "beendet" wechselt. In diesem Fall sollte die Quelle das Ergebnis dieser e/a-Anforderung verwerfen.

## <a name="sample-requests"></a>Beispielanforderungen

Media Foundation ein *Pull* -Modell verwenden, bei dem die Pipeline Stichproben aus der Medienquelle anfordert. Dies unterscheidet sich von dem von DirectShow verwendeten Modell, in dem die Quellen "Push"-Beispiele verwendet werden.

Um ein neues Beispiel anzufordern, ruft die Media Foundation Pipeline [**imfmediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)auf. Diese Methode nimmt einen **IUnknown** -Zeiger an, der ein *Tokenobjekt* darstellt. Die Implementierung des Tokenobjekts liegt dem Aufrufer. Er bietet dem Aufrufer einfach die Möglichkeit, Beispiel Anforderungen zu verfolgen. Der tokenparameter kann auch **null** sein.

Angenommen, die Quelle verwendet asynchrone e/a-Anforderungen zum Lesen von Daten, wird die Beispiel Generierung nicht mit Beispiel Anforderungen synchronisiert. Zum Synchronisieren von Beispiel Anforderungen mit der Beispiel Generierung führt eine Medienquelle Folgendes aus:

1.  Anforderungs Token werden in einer Warteschlange abgelegt.
2.  Wenn Beispiele generiert werden, werden Sie in einer zweiten Warteschlange platziert.
3.  Die Medienquelle schließt eine Beispiel Anforderung ab, indem ein Anforderungs Token aus der ersten Warteschlange und ein Beispiel aus der zweiten Warteschlange abgerufen wird.
4.  Die Medienquelle sendet ein memediasample-Ereignis. Das Ereignis enthält einen Zeiger auf das Beispiel, und das Beispiel enthält einen Zeiger auf das Token.

Das folgende Diagramm zeigt die Beziehung zwischen dem [memediasample](memediasample.md) -Ereignis, dem Beispiel und dem Anforderungs Token.

![das Diagramm zeigt "memediasample" und eine Beispiel Warteschlange, die auf imfsample verweist. imfsample und die Anforderungs Warteschlange zeigen auf IUnknown.](images/mediasourceimpl01.png)

Die Beispiel-MPEG-1-Quelle implementiert diesen Prozess wie folgt:

1.  Die [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode stellt die Anforderung in eine FIFO-Warteschlange.
2.  Wenn e/a-Anforderungen abgeschlossen sind, erstellt die Medienquelle neue Beispiele und versetzt Sie in eine zweite FIFO-Warteschlange. (Diese Warteschlange verfügt über eine maximale Größe, um zu verhindern, dass die Quelle zu weit vorangeht.)
3.  Wenn beide Warteschlangen mindestens ein Element (eine Anforderung und ein Beispiel) enthalten, vervollständigt die Medienquelle die erste Anforderung aus der Anforderungs Warteschlange, indem das erste Beispiel aus der Beispiel Warteschlange gesendet wird.
4.  Um ein Beispiel zu liefern, sendet das Stream-Objekt (nicht das Quell Objekt) ein [memediasample](memediasample.md) -Ereignis.
    -   Die Ereignisdaten sind ein Zeiger auf die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle des Beispiels.
    -   Wenn die Anforderung ein Token enthielt, fügen Sie das Token an das Beispiel an, indem Sie das [**mfsampleextension- \_ tokenattribut**](mfsampleextension-token-attribute.md) für das Beispiel festlegen.

Zu diesem Zeitpunkt gibt es drei Möglichkeiten:

-   Es gibt ein weiteres Beispiel in der Beispiel Warteschlange, aber keine übereinstimmende Anforderung.
-   Es gibt eine Anforderung, aber keine Stichprobe.
-   Beide Warteschlangen sind leer. Es sind keine Beispiele und keine Anforderungen vorhanden.

Wenn die Beispiel Warteschlange leer ist, überprüft die Quelle das Ende des Streams (siehe das [Ende des Streams](#end-of-stream)). Andernfalls wird eine weitere e/a-Anforderung für Daten gestartet. Wenn während dieses Vorgangs ein Fehler auftritt, sendet der Stream ein [meerror](meerror.md) -Ereignis.

Der folgende Code implementiert die [**IMF Mediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode:


```C++
HRESULT MPEG1Stream::RequestSample(IUnknown* pToken)
{
    HRESULT hr = S_OK;
    IMFMediaSource *pSource = NULL;

    // Hold the media source object's critical section.
    SourceLock lock(m_pSource);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_state == STATE_STOPPED)
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (!m_bActive)
    {
        // If the stream is not active, it should not get sample requests.
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (m_bEOS && m_Samples.IsEmpty())
    {
        // This stream has already reached the end of the stream, and the
        // sample queue is empty.
        hr = MF_E_END_OF_STREAM;
        goto done;
    }

    hr = m_Requests.InsertBack(pToken);
    if (FAILED(hr))
    {
        goto done;
    }

    // Dispatch the request.
    hr = DispatchSamples();
    if (FAILED(hr))
    {
        goto done;
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        hr = m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }
    return hr;
}
```



Die `DispatchSamples` -Methode ruft Beispiele aus der Beispiel Warteschlange ab, gleicht Sie mit ausstehenden Beispiel Anforderungen und Warteschlangen [memediasample](memediasample.md) -Ereignissen ab:


```C++
HRESULT MPEG1Stream::DispatchSamples()
{
    HRESULT hr = S_OK;
    BOOL bNeedData = FALSE;
    BOOL bEOS = FALSE;

    SourceLock lock(m_pSource);

    // An I/O request can complete after the source is paused, stopped, or
    // shut down. Do not deliver samples unless the source is running.
    if (m_state != STATE_STARTED)
    {
        return S_OK;
    }

    IMFSample *pSample = NULL;
    IUnknown  *pToken = NULL;

    // Deliver as many samples as we can.
    while (!m_Samples.IsEmpty() && !m_Requests.IsEmpty())
    {
        // Pull the next sample from the queue.
        hr = m_Samples.RemoveFront(&pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Pull the next request token from the queue. Tokens can be NULL.
        hr = m_Requests.RemoveFront(&pToken);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pToken)
        {
            // Set the token on the sample.
            hr = pSample->SetUnknown(MFSampleExtension_Token, pToken);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Send an MEMediaSample event with the sample.
        hr = m_pEventQueue->QueueEventParamUnk(
            MEMediaSample, GUID_NULL, S_OK, pSample);

        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pSample);
        SafeRelease(&pToken);
    }

    if (m_Samples.IsEmpty() && m_bEOS)
    {
        // The sample queue is empty AND we have reached the end of the source
        // stream. Notify the pipeline by sending the end-of-stream event.

        hr = m_pEventQueue->QueueEventParamVar(
            MEEndOfStream, GUID_NULL, S_OK, NULL);

        if (FAILED(hr))
        {
            goto done;
        }

        // Notify the source. It will send the end-of-presentation event.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_END_OF_STREAM);
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (NeedsData())
    {
        // The sample queue is empty; the request queue is not empty; and we
        // have not reached the end of the stream. Ask for more data.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_REQUEST_DATA);
        if (FAILED(hr))
        {
            goto done;
        }
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }

    SafeRelease(&pSample);
    SafeRelease(&pToken);
    return S_OK;
}
```



Die- `DispatchSamples` Methode wird in den folgenden Situationen aufgerufen:

-   Innerhalb der [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode.
-   Wenn die Medienquelle vom angehaltenen Zustand neu gestartet wird.
-   Wenn eine e/a-Anforderung abgeschlossen ist.

## <a name="end-of-stream"></a>Ende des Streams

Wenn ein Stream keine weiteren Daten enthält und alle Beispiele für diesen Stream übermittelt wurden, sendet die Streamobjekte ein [meendof Stream](meendofstream.md) -Ereignis.

Wenn alle aktiven Streams abgeschlossen sind, sendet die Medienquelle ein [meendof Presentation](meendofpresentation.md) -Ereignis.

## <a name="asynchronous-operations"></a>Asynchrone Vorgänge

Der vielleicht schwierigste Teil beim Schreiben einer Medienquelle ist das Verständnis des Media Foundation asynchronen Modells.

Alle Methoden in einer Medienquelle, die das Streaming steuern, sind asynchron. In jedem Fall führt die-Methode eine anfängliche Validierung aus, z. b. das Überprüfen von Parametern. Die Quelle sendet dann den Rest der Arbeit an eine Arbeits Warteschlange. Nachdem der Vorgang abgeschlossen ist, sendet die Medienquelle ein Ereignis zurück an den Aufrufer über die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle der Medienquelle. Daher ist es wichtig, dass Sie die Arbeits Warteschlangen verstehen.

Wenn Sie ein Element in einer Arbeits Warteschlange platzieren möchten, können Sie entweder [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) oder [**mfputworkitemex**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex)abrufen. Die MPEG-1-Quelle verwendet " **mfputworkitem**", aber die beiden Funktionen führen dasselbe aus. Die **mfputworkitem** -Funktion übernimmt die folgenden Parameter:

-   Ein **DWORD** -Wert, der die Arbeits Warteschlange identifiziert. Sie können eine private Arbeits Warteschlange erstellen oder den **mfasync- \_ Rückruf \_ Warteschlangen- \_ Standard** verwenden.
-   Ein Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle. Diese Rückruf Schnittstelle wird aufgerufen, um die Arbeit auszuführen.
-   Ein optionales Zustands Objekt, das **IUnknown** implementieren muss.

Die Arbeits Warteschlange wird von mindestens einem Arbeitsthread gewartet, der fortlaufend das nächste Arbeits Element aus der Warteschlange abruft und die [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Methode der Rückruf Schnittstelle aufruft.

Es ist nicht garantiert, dass Arbeitselemente in derselben Reihenfolge ausgeführt werden, in der Sie Sie in der Warteschlange ablegen. Beachten Sie, dass mehr als ein Thread dieselbe Arbeits Warteschlange verarbeiten kann. Daher können [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Aufrufe überlappen oder nicht in der richtigen Reihenfolge auftreten. Daher liegt es an der Medienquelle, den korrekten internen Zustand beizubehalten, indem Arbeits Warteschlangen Elemente in der richtigen Reihenfolge übermittelt werden. Erst wenn der vorherige Vorgang beendet ist, startet die Quelle den nächsten Vorgang.

Zur Darstellung von ausstehenden Vorgängen definiert die MPEG-1-Quelle eine Klasse mit dem Namen `SourceOp` :


```C++
// Represents a request for an asynchronous operation.

class SourceOp : public IUnknown
{
public:

    enum Operation
    {
        OP_START,
        OP_PAUSE,
        OP_STOP,
        OP_REQUEST_DATA,
        OP_END_OF_STREAM
    };

    static HRESULT CreateOp(Operation op, SourceOp **ppOp);
    static HRESULT CreateStartOp(IMFPresentationDescriptor *pPD, SourceOp **ppOp);

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    SourceOp(Operation op);
    virtual ~SourceOp();

    HRESULT SetData(const PROPVARIANT& var);

    Operation Op() const { return m_op; }
    const PROPVARIANT& Data() { return m_data;}

protected:
    long        m_cRef;     // Reference count.
    Operation   m_op;
    PROPVARIANT m_data;     // Data for the operation.
};
```



Die- `Operation` Enumeration identifiziert den ausstehenden Vorgang. Die-Klasse enthält auch eine **PROPVARIANT** , um alle zusätzlichen Daten für den Vorgang zu übermitteln.

### <a name="operation-queue"></a>Vorgangs Warteschlange

Zum Serialisieren von Vorgängen verwaltet die Medienquelle eine Warteschlange von `SourceOp` Objekten. Er verwendet eine Hilfsklasse, um die Warteschlange zu verwalten:


```C++
template <class OP_TYPE>
class OpQueue : public IUnknown
{
public:

    typedef ComPtrList<OP_TYPE>   OpList;

    HRESULT QueueOperation(OP_TYPE *pOp);

protected:

    HRESULT ProcessQueue();
    HRESULT ProcessQueueAsync(IMFAsyncResult *pResult);

    virtual HRESULT DispatchOperation(OP_TYPE *pOp) = 0;
    virtual HRESULT ValidateOperation(OP_TYPE *pOp) = 0;

    OpQueue(CRITICAL_SECTION& critsec)
        : m_OnProcessQueue(this, &OpQueue::ProcessQueueAsync),
          m_critsec(critsec)
    {
    }

    virtual ~OpQueue()
    {
    }

protected:
    OpList                  m_OpQueue;         // Queue of operations.
    CRITICAL_SECTION&       m_critsec;         // Protects the queue state.
    AsyncCallback<OpQueue>  m_OnProcessQueue;  // ProcessQueueAsync callback.
};
```



Die- `OpQueue` Klasse ist so konzipiert, dass Sie von der Komponente geerbt wird, die asynchrone Arbeitsaufgaben ausführt. Der *\_ typvorlagen Parameter op* ist der Objekttyp, der zum Darstellen von Arbeits Elementen in der Warteschlange verwendet wird – in diesem Fall ist der *op- \_ Typ* `SourceOp` . Die- `OpQueue` Klasse implementiert die folgenden Methoden:

-   `QueueOperation` Fügt ein neues Element in die Warteschlange ein.
-   `ProcessQueue` sendet den nächsten Vorgang aus der Warteschlange. Diese Methode ist asynchron.
-   `ProcessQueueAsync` schließt die asynchrone- `ProcessQueue` Methode ab.

Zwei weitere Methoden müssen von der abgeleiteten Klasse implementiert werden:

-   `ValidateOperation` überprüft, ob ein angegebener Vorgang aufgrund des aktuellen Status der Medienquelle gültig ist.
-   `DispatchOperation` führt die asynchrone Arbeitsaufgabe aus.

Die Vorgangs Warteschlange wird wie folgt verwendet:

1.  Die Media Foundation Pipeline Ruft eine asynchrone Methode für die Medienquelle auf, z. b. [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).
2.  Die asynchrone-Methode ruft `QueueOperation` auf, wodurch der [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Vorgang in die Warteschlange versetzt und `ProcessQueue` (in Form eines- `SourceOp` Objekts) aufgerufen wird.
3.  `ProcessQueue` Ruft das [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem)-Element auf.
4.  Der Arbeits Warteschlangen Thread ruft auf `ProcessQueueAsync` .
5.  Die `ProcessQueueAsync` -Methode ruft `ValidateOperation` und auf `DispatchOperation` .

Der folgende Code fügt einen neuen Vorgang für die MPEG-1-Quelle in die Warteschlange ein:


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::QueueOperation(OP_TYPE *pOp)
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_critsec);

    hr = m_OpQueue.InsertBack(pOp);
    if (SUCCEEDED(hr))
    {
        hr = ProcessQueue();
    }

    LeaveCriticalSection(&m_critsec);
    return hr;
}
```



Der folgende Code verarbeitet die Warteschlange:


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::ProcessQueue()
{
    HRESULT hr = S_OK;
    if (m_OpQueue.GetCount() > 0)
    {
        hr = MFPutWorkItem(
            MFASYNC_CALLBACK_QUEUE_STANDARD,    // Use the standard work queue.
            &m_OnProcessQueue,                  // Callback method.
            NULL                                // State object.
            );
    }
    return hr;
}
```



Die `ValidateOperation` -Methode überprüft, ob die MPEG-1-Quelle den nächsten Vorgang in der Warteschlange senden kann. Wenn ein anderer Vorgang ausgeführt wird, wird von `ValidateOperation` **MF \_ E \_ notakzeptierte** zurückgegeben. Dadurch wird sichergestellt, dass `DispatchOperation` nicht aufgerufen wird, während ein anderer Vorgang aussteht.


```C++
HRESULT MPEG1Source::ValidateOperation(SourceOp *pOp)
{
    if (m_pCurrentOp != NULL)
    {
        return MF_E_NOTACCEPTING;
    }
    return S_OK;
}
```



Die DispatchOperation-Methode schaltet den Vorgangstyp ein:


```C++
//-------------------------------------------------------------------
// DispatchOperation
//
// Performs the asynchronous operation indicated by pOp.
//
// NOTE:
// This method implements the pure-virtual OpQueue::DispatchOperation
// method. It is always called from a work-queue thread.
//-------------------------------------------------------------------

HRESULT MPEG1Source::DispatchOperation(SourceOp *pOp)
{
    EnterCriticalSection(&m_critSec);

    HRESULT hr = S_OK;

    if (m_state == STATE_SHUTDOWN)
    {
        LeaveCriticalSection(&m_critSec);

        return S_OK; // Already shut down, ignore the request.
    }

    switch (pOp->Op())
    {

    // IMFMediaSource methods:

    case SourceOp::OP_START:
        hr = DoStart((StartOp*)pOp);
        break;

    case SourceOp::OP_STOP:
        hr = DoStop(pOp);
        break;

    case SourceOp::OP_PAUSE:
        hr = DoPause(pOp);
        break;

    // Operations requested by the streams:

    case SourceOp::OP_REQUEST_DATA:
        hr = OnStreamRequestSample(pOp);
        break;

    case SourceOp::OP_END_OF_STREAM:
        hr = OnEndOfStream(pOp);
        break;

    default:
        hr = E_UNEXPECTED;
    }

    if (FAILED(hr))
    {
        StreamingError(hr);
    }

    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



Zusammenfassung:

1.  Die Pipeline Ruft eine asynchrone Methode auf, z. b. [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).
2.  Die asynchrone-Methode ruft `OpQueue::QueueOperation` auf und übergibt einen Zeiger auf ein- `SourceOp` Objekt.
3.  `QueueOperation`Mit der-Methode wird der-Vorgang in der Warteschlangen-Warteschlange von *m \_* angezeigt `OpQueue::ProcessQueue` .
4.  Die- `ProcessQueue` Methode ruft das [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem)-Element auf. An diesem Punkt geschieht alles in einem Media Foundation Arbeits Warteschlangen Thread. Die asynchrone Methode kehrt zum Aufrufer zurück.
5.  Der Arbeits Warteschlangen Thread ruft die- `OpQueue::ProcessQueueAsync` Methode auf.
6.  Die `ProcessQueueAsync` Methode ruft `MPEG1Source:ValidateOperation` auf, um den Vorgang zu überprüfen.
7.  Die- `ProcessQueueAsync` Methode ruft `MPEG1Source::DispatchOperation` auf, um den Vorgang zu verarbeiten.

Dieser Entwurf bietet mehrere Vorteile:

-   Methoden sind asynchron, sodass Sie den Thread der aufrufenden Anwendung nicht blockieren.
-   Vorgänge werden an einen Media Foundation Arbeits Warteschlangen Thread gesendet, der von Pipeline Komponenten gemeinsam genutzt wird. Daher erstellt die Medienquelle keinen eigenen Thread und verringert so die Gesamtzahl der erstellten Threads.
-   Die Medienquelle wird nicht blockiert, während auf den Abschluss des Vorgangs gewartet wird. Dadurch wird die Wahrscheinlichkeit verringert, dass eine Medienquelle versehentlich einen Deadlock auslöst und den Kontextwechsel reduziert.
-   Die Medienquelle kann asynchrone e/a-Vorgänge verwenden, um die Quelldatei zu lesen (durch Aufrufen von [**imfbytestream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)). Die Medienquelle muss beim Warten auf den Abschluss einer e/a-Routine nicht blockiert werden.

Wenn Sie das im SDK-Beispiel gezeigte Muster befolgen, können Sie sich auf bestimmte Details der Medienquelle konzentrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienquellen](media-sources.md)
</dt> <dt>

[Schreiben einer benutzerdefinierten Medienquelle](writing-a-custom-media-source.md)
</dt> </dl>

 

 



