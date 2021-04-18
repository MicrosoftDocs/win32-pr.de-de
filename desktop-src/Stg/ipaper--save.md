---
title: IPaper speichern
description: Der wichtigste Schwerpunkt in diesem Beispielcode ist, wie copaper seine Papier Daten in Verbund Dateien laden und speichern kann. Die iPaper-, Load-und Save-Methoden Implementierungen werden ausführlich erläutert.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ea49f194e64ab3f0cfd78569b1e6ff9ddee577
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340233"
---
# <a name="ipapersave"></a>IPaper:: Save

Der wichtigste Schwerpunkt in diesem Beispielcode ist, wie copaper seine Papier Daten in Verbund Dateien laden und speichern kann. Die [**iPaper**](ipaper-methods.md)-, [**Load**](ipaper--load.md)-und **Save** -Methoden Implementierungen werden ausführlich erläutert.

Im folgenden finden Sie die **iPaper:: Save** -Methode von Paper. cpp.


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



In dieser Client-und Server Beziehung erstellt copaper nicht die Verbund Datei, mit der Papier Daten gespeichert werden. Sowohl für die **Save** -als auch die [**Load**](ipaper--load.md) -Methode übergibt der Client einen [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstellen Zeiger für eine vorhandene Verbund Datei. Anschließend wird der **IStorage** zum Schreiben und Lesen von Daten in dieser Verbund Datei verwendet. In **iPaper:: Save** oberhalb werden mehrere Datentypen gespeichert.

Die CLSID für dllpaper, CLSID \_ dllpaper, wird serialisiert und in einem speziellen com-gesteuerten Stream im Speicher Objekt mit dem Namen " \\ 001compobj" gespeichert. Die Funktion " [**Write Service classstg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) " führt diesen Speicher aus. Diese gespeicherten CLSID-Daten können verwendet werden, um die Speicherinhalte der dllpaper-Komponente zuzuordnen, die Sie erstellt hat und interpretieren kann. In diesem Beispiel wird der Stamm Speicher von **stoclien** übergeben, und daher ist die gesamte Verbund Datei der Komponente dllpaper zugeordnet. Diese CLSID-Daten können später mit einem Rückruf der Dienstfunktion " [**leserclassg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) " abgerufen werden.

Da in dllpaper bearbeitbare Daten behandelt werden, ist es auch sinnvoll, ein Zwischenablage Format im Speicher aufzuzeichnen. Die Funktion " [**schreitefmtusertypestg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) " wird aufgerufen, um sowohl eine Format Bezeichnung für die Zwischenablage als auch einen Benutzer lesbaren Namen für das Format zu speichern. Der für den Benutzer lesbare Name ist für die GUI-Anzeige in Auswahllisten bestimmt. Der oben weiter gegebene Name verwendet das-Makro clipbdfmt \_ Str, das in Paper. h als "dllpaper 1,0" definiert ist. Diese gespeicherten Zwischenablage Daten können später mit einem Aufrufen der Dienstfunktion " [**leserfmtusertypestg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg)" abgerufen werden. Diese Funktion gibt einen Zeichen folgen Wert zurück, der mithilfe der Arbeitsspeicher Zuweisung zugeordnet wird. Der Aufrufer ist für das Freigeben der Zeichenfolge verantwortlich.

Beim nächsten **Speichern** wird ein Stream im Speicher für die copaper-Papier Daten erstellt. Der Stream wird als "Taschen Daten" bezeichnet und mithilfe des Stream \_ Taschen \_ datentops "USTR" übermittelt. Die [**IStorage:: foratestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) -Methode erfordert, dass diese Zeichenfolge in Unicode enthalten ist. Da die Zeichenfolge zur Kompilierzeit festgelegt ist, wird das Makro in Paper. h als Unicode definiert.

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

Das "L" vor der Zeichenfolge, das Long angibt, erreicht dies.

Die Methode " [**kreatestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) " erstellt und öffnet einen Stream innerhalb des angegebenen Speichers. Ein [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstellen Zeiger für den neuen Stream wird in der Zeiger Variablen der aufrufenden Schnittstelle übergeben. Die adressf wird für diesen Schnittstellen Zeiger innerhalb von " **kreatestream**" aufgerufen, und der Aufrufer muss diesen Zeiger nach der Verwendung freigeben. Der Methode " **kreatestream** " werden wie folgt zahlreiche zugriffsmodusflags übergeben.

STGM \_ Create \| STGM \_ Write \| STGM \_ Direct \| STGM \_ share \_ exklusiv

[**STGM \_ Create**](stgm-constants.md) erstellt einen neuen Stream oder überschreibt einen vorhandenen Namen. [**STGM \_ Write**](stgm-constants.md) öffnet den Stream mit Schreib Berechtigung. [**STGM \_ Direkt**](stgm-constants.md) öffnet den Stream für den direkten Zugriff im Gegensatz zum transaktiven Zugriff. [**STGM \_ Freigabe \_ exklusiv**](stgm-constants.md) öffnet die Datei für den exklusiven, nicht freigegebenen Gebrauch durch den Aufrufer.

Nachdem der Taschen Datenstrom erfolgreich erstellt wurde, wird die [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstelle verwendet, um in den Stream zu schreiben. Die **IStream:: Write** -Methode wird verwendet, um zuerst den Inhalt der Papier \_ Eigenschafts Struktur zu speichern. Dabei handelt es sich im Wesentlichen um einen Eigenschaften Header am Anfang des Streams. Da die Versionsnummer das erste Ergebnis in der Datei ist, kann Sie unabhängig voneinander gelesen werden, um zu bestimmen, wie die folgenden Daten behandelt werden. Wenn die tatsächlich geschriebene Datenmenge nicht mit der angeforderten Menge übereinstimmt, wird die Save-Methode abgebrochen und gibt STG \_ E \_ kansave zurück.

Es ist einfach, das gesamte Array von frei Hand Daten in den Stream zu speichern.


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



Da die [**IStream:: Write**](/windows/desktop/api/Objidl/nn-objidl-istream) -Methode mit einem Bytearray arbeitet, wird die Anzahl der Bytes gespeicherter frei Hand Daten im Array berechnet, und der Schreibvorgang beginnt am Anfang des Arrays. Wenn die tatsächlich geschriebene Datenmenge nicht mit der angeforderten Menge übereinstimmt, gibt die **Save** -Methode STG \_ E \_ kansave zurück.

Nachdem der Stream geschrieben wurde, gibt die **iPaper:: Save** -Methode den verwendeten [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Zeiger frei.

Die **Save** -Methode ruft auch den Client [**itaschen Sink**](ipapersink-methods.md) (in der internen Methode "copaper-notifysinks") auf, um den Client zu benachrichtigen, dass der Speichervorgang beendet wurde. An diesem Punkt wird die **Save** -Methode an den aufrufenden Client zurückgegeben, der in der Regel den [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Zeiger freigibt.

 

 




