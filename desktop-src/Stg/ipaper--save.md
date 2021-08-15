---
title: IPaper Save
description: Der Hauptfokus in diesem Beispielcode liegt darauf, wie COPaper seine Papierdaten in Verbunddateien laden und speichern kann. Die Implementierungen der IPaper-, Load- und Save-Methode werden ausführlich erläutert.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52772002fe8f0ed234a4f430eaff4328f96f9d1ef151e83da3f4aa3e255dba09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961370"
---
# <a name="ipapersave"></a>IPaper::Save

Der Hauptfokus in diesem Beispielcode liegt darauf, wie COPaper seine Papierdaten in Verbunddateien laden und speichern kann. Die Implementierungen der [**IPaper-,**](ipaper-methods.md) [**Load-**](ipaper--load.md)und **Save-Methode** werden ausführlich erläutert.

Es folgt die **IPaper::Save-Methode** aus Paper.cpp.


```C++
STDMETHODIMP COPaper::CImpIPaper::Save(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    ULONG ulToWrite, ulWritten;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
        // Use the COM service to mark this compound file as one 
        // that is handled by our server component, DllPaper.
        WriteClassStg(pIStorage, CLSID_DllPaper);

        // Use the COM Service to write user-readable clipboard 
        // format into the compound file.
        WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, 
                            TEXT(CLIPBDFMT_STR));

        // Create the stream to be used for the actual paper data.
        // Call it "PAPERDATA".
        hr = pIStorage->CreateStream(
               STREAM_PAPERDATA_USTR,
        STGM_CREATE | STGM_WRITE | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained a stream. Write data to it.
          // First, write PAPER_PROPERTIES structure.
          m_PaperProperties.lInkArraySize = m_lInkDataEnd+1;
          m_PaperProperties.crWinColor = m_crWinColor;
          m_PaperProperties.WinRect.right = m_WinRect.right;
          m_PaperProperties.WinRect.bottom = m_WinRect.bottom;
          ulToWrite = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Write(&m_Paper_Properties, ulToWrite, 
                               &ulWritten);
          if (SUCCEEDED(hr) && ulToWrite != ulWritten)
            hr = STG_E_CANTSAVE;
          if (SUCCEEDED(hr))
          {
            // Now, write the complete array of Ink Data.
            ulToWrite = m_PaperProperties.lInkArraySize * 
                                                     sizeof(INKDATA);
            hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
            if (SUCCEEDED(hr) && ulToWrite != ulWritten)
              hr = STG_E_CANTSAVE;
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify all other connected clients that Paper is now saved.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_SAVED, 0, 0, 0, 0);

    return hr;
  }
```



In dieser Client- und Serverbeziehung erstellt COPaper nicht die Verbunddatei, die zum Speichern von Papierdaten verwendet wird. Für die Methoden **Save** und [**Load**](ipaper--load.md) übergibt der Client einen [**IStorage-Schnittstellenzeiger**](/windows/desktop/api/Objidl/nn-objidl-istorage) für eine vorhandene Verbunddatei. Anschließend wird **IStorage** verwendet, um Daten in dieser Verbunddatei zu schreiben und zu lesen. In **IPaper::Save** oben werden mehrere Datentypen gespeichert.

Die CLSID für DllPaper, CLSID \_ DllPaper, wird serialisiert und in einem speziellen COM-gesteuerten Stream innerhalb des Speicherobjekts namens \\ "001CompObj" gespeichert. Die [**WriteClassStg-Dienstfunktion**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) führt diesen Speicher aus. Diese gespeicherten CLSID-Daten können verwendet werden, um den Speicherinhalt der dllPaper-Komponente zuzuordnen, die erstellt wurde und sie interpretieren kann. In diesem Beispiel wird der Stammspeicher von **StoClien** übergeben, und daher wird die gesamte Verbunddatei der DllPaper-Komponente zugeordnet. Diese CLSID-Daten können später mit einem Aufruf der [**ReadClassStg-Dienstfunktion**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) abgerufen werden.

Da DllPaper bearbeitbare Daten verarbeitet, ist es auch sinnvoll, ein Zwischenablageformat im Speicher aufzuzeichnen. Die [**WriteFmtUserTypeStg-Dienstfunktion**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) wird aufgerufen, um sowohl eine Formatbezeichnung in der Zwischenablage als auch einen benutzerlesbaren Namen für das Format zu speichern. Der benutzerlesbare Name ist für die GUI-Anzeige in Auswahllisten vorgesehen. Der oben übergebene Name verwendet das Makro CLIPBDFMT \_ STR, das in Paper.h als "DllPaper 1.0" definiert ist. Diese gespeicherten Zwischenablagedaten können später mit einem Aufruf der Dienstfunktion [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg)abgerufen werden. Diese Funktion gibt einen Zeichenfolgenwert zurück, der mithilfe der Taskspeicherzuweisung zugeordnet wird. Der Aufrufer ist für das Freigeben der Zeichenfolge verantwortlich.

**Speichern** erstellt als Nächstes einen Stream im Speicher für die COPaper-Papierdaten. Der Stream wird als "PAPERDATA" bezeichnet und mithilfe des STREAM \_ PAPERDATA \_ USTR-Makros übergeben. Die [**IStorage::CreateStream-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) erfordert, dass diese Zeichenfolge in Unicode enthalten ist. Da die Zeichenfolge zur Kompilierzeit festgelegt ist, wird das Makro in Paper.h als Unicode definiert.

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

Das "L" vor der Zeichenfolge, das LONG angibt, erreicht dies.

Die [**CreateStream-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) erstellt und öffnet einen Stream innerhalb des angegebenen Speichers. Ein [](/windows/desktop/api/Objidl/nn-objidl-istream) IStream-Schnittstellenzeiger für den neuen Stream wird in einer Aufruferschnittstellenzeigervariablen übergeben. AddRef wird für diesen Schnittstellenzeiger in **CreateStream** aufgerufen, und der Aufrufer muss diesen Zeiger nach der Verwendung freigeben. Der **CreateStream-Methode** werden wie folgt zahlreiche Zugriffsmodusflags übergeben.

STGM \_ CREATE \| STGM \_ WRITE \| STGM \_ DIRECT \| STGM \_ SHARE \_ EXCLUSIVE

[**STGM \_ CREATE**](stgm-constants.md) erstellt einen neuen Stream oder überschreibt einen vorhandenen mit dem gleichen Namen. [**STGM \_ WRITE**](stgm-constants.md) öffnet den Stream mit Schreibberechtigung. [**STGM \_ DIRECT**](stgm-constants.md) öffnet den Stream für den direkten Zugriff und nicht für den transaktiven Zugriff. [**STGM \_ SHARE \_ EXCLUSIVE**](stgm-constants.md) öffnet die Datei für die exklusive, nicht freigegebene Verwendung durch den Aufrufer.

Nachdem der PAPERDATA-Stream erfolgreich erstellt wurde, wird die [**IStream-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istream) verwendet, um in den Stream zu schreiben. Die **IStream::Write-Methode** wird verwendet, um zuerst den Inhalt der PAPER \_ PROPERTIES-Struktur zu speichern. Dies ist im Wesentlichen ein Eigenschaftenheader am Anfang des Streams. Da die Versionsnummer der erste Punkt in der Datei ist, kann sie unabhängig gelesen werden, um zu bestimmen, wie mit den folgenden Daten umgegangen wird. Wenn die tatsächlich geschriebene Datenmenge nicht der angeforderten Menge entspricht, wird die Save-Methode abgebrochen und STG \_ E \_ CANTSAVE zurückgegeben.

Das Speichern des gesamten Arrays von Ink-Daten im Stream ist einfach.


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



Da die [**IStream::Write-Methode**](/windows/desktop/api/Objidl/nn-objidl-istream) für ein Bytearray verwendet wird, wird die Anzahl der Bytes der gespeicherten Freihanddaten im Array berechnet, und der Schreibvorgang beginnt am Anfang des Arrays. Wenn die tatsächlich geschriebene Datenmenge nicht mit der angeforderten Menge identisch ist, gibt die **Save-Methode** STG \_ E \_ CANTSAVE zurück.

Nachdem der Stream geschrieben wurde, gibt die **IPaper::Save-Methode** den [**verwendeten IStream-Zeiger**](/windows/desktop/api/Objidl/nn-objidl-istream) frei.

Die **Save-Methode** ruft auch den Client [**IPaperSink**](ipapersink-methods.md) (in der internen NotifySinks-Methode von COPaper) auf, um den Client zu benachrichtigen, dass der Speichervorgang abgeschlossen ist. An diesem Punkt kehrt die **Save-Methode** zum aufrufenden Client zurück, der in der Regel den [**IStorage-Zeiger**](/windows/desktop/api/Objidl/nn-objidl-istorage) freigibt.

 

 




