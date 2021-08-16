---
title: IPaper Load
description: Der folgende C++-Beispielcode zeigt, wie Sie den vorhandenen Stream im Speicher öffnen, neue Papiereigenschaften in lesen und diese dann als aktuelle Werte für COPaper festlegen.
ms.assetid: a1559d97-387f-4d1a-8a9d-fa5c27abd545
keywords:
- IPaper Load
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b592573f016018d359b5e3e35911d92371892b98ebea70338844b7f8ef4b1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961380"
---
# <a name="ipaperload"></a>IPaper::Load

Der folgende C++-Beispielcode zeigt, wie Sie den vorhandenen Stream im Speicher öffnen, neue Papiereigenschaften in lesen und diese dann als aktuelle Werte für COPaper festlegen.

Im Folgenden ist die **IPaper::Load-Methode** aus Paper.cpp.


```
STDMETHODIMP COPaper::CImpIPaper::Load(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    INKDATA* paInkData;
    ULONG ulToRead, ulReadIn;
    LONG lNewArraySize;
    PAPER_PROPERTIES NewProps;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
       // Open the "PAPERDATA" stream where the paper data is stored.
        hr = pIStorage->OpenStream(
               STREAM_PAPERDATA_USTR,
               0,
               STGM_READ | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained paper data stream. Read the Paper Properties.
          ulToRead = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Read(
                           &NewProps,
                           ulToRead,
                           &ulReadIn);
          if (SUCCEEDED(hr) && ulToRead != ulReadIn)
            hr = E_FAIL;
          if (SUCCEEDED(hr))
          {
            // Handle the different versions of ink data format.
            switch (NewProps.lInkDataVersion)
            {
              case INKDATA_VERSION10:
                // Allocate an ample-sized ink data array.
                lNewArraySize = NewProps.lInkArraySize + 
                                               INKDATA_ALLOC;
                paInkData = new INKDATA[(LONG) lNewArraySize];
                if (NULL != paInkData)
                {
                  // Delete the old ink data array.
                  delete [] m_paInkData;

                  // Assign the new array.
                  m_paInkData = paInkData;
                  m_lInkDataMax = lNewArraySize;

                  // Read the complete array of Ink Data.
                  ulToRead = NewProps.lInkArraySize * sizeof(INKDATA);
                  hr = pIStream->Read(m_paInkData, 
                                      ulToRead, &ulReadIn);
                  if (SUCCEEDED(hr) && ulToRead != ulReadIn)
                    hr = E_FAIL;
                  if (SUCCEEDED(hr))
                  {
                    // Set COPaper to use the new PAPER_PROPERTIES
                    // data.
                    m_lInkDataEnd = NewProps.lInkArraySize-1;
                    m_crWinColor = NewProps.crWinColor;
                    m_WinRect.right = NewProps.WinRect.right;
                    m_WinRect.bottom = NewProps.WinRect.bottom;

                    // Copy the new properties into current 
                    // properties.
                    memcpy(
                      &m_PaperProperties,
                      &NewProps,
                      sizeof(PAPER_PROPERTIES));
                  }
                }
                else
                  hr = E_OUTOFMEMORY;
                break;
              default:
                hr = E_FAIL;  // Bad version.
                break;
            }
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify other connected clients that Paper is now loaded.
    // If Paper not loaded, then erase to a safe, empty ink data 
    // array.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_LOADED, 0, 0, 0, 0);
    else
      Erase(nLockKey);

    return hr;
  }
```



Jetzt wird die [**IStorage::OpenStream-Methode**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) aufgerufen, um den vorhandenen Stream im Speicher mit dem Namen "PAPERDATA" zu öffnen. Zugriffsmodusflags sind für schreibgeschützten, direkten und nicht freigegebenen exklusiven Zugriff vorgesehen. Wenn der Stream geöffnet ist, wird die [**IStream::Read-Methode**](/windows/desktop/api/Objidl/nn-objidl-istream) aufgerufen, um die PAPER \_ PROPERTIES-Struktur zu lesen. Wenn der tatsächlich gelesene Betrag nicht dem angeforderten Betrag entspricht, wird der Ladevorgang abgebrochen, und E \_ FAIL wird zurückgegeben. Wenn die Formatversion in den neu gelesenen PAPER \_ PROPERTIES nicht erkannt wird, wird der Ladevorgang abgebrochen, und **Load** gibt E \_ FAIL zurück.

Bei einer gültigen Formatversion für Ink-Daten wird die Größe des neuen Ink-Datenarrays aus den \_ PAPER PROPERTIES verwendet, das eingelesen wurde, um ein neues Ink-Datenarray der erforderlichen Größe zuzuordnen. Die vorhandenen Ink-Daten werden gelöscht, und ihre Daten verloren. Wenn diese Daten nützlich waren, sollten sie gespeichert worden sein, bevor **Load** aufgerufen wurde. Nachdem das neue Array zugeordnet wurde, wird [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) erneut aufgerufen, um die Daten aus dem Stream in das Array zu lesen. Wenn dieser Aufruf erfolgreich ist, werden die Werte in den neu gelesenen Papiereigenschaften als aktuelle Werte für COPaper übernommen.

Während dieses Ladevorgangs wurde die temporäre PAPER \_ PROPERTIES-Struktur NewProps verwendet, um die neuen eingelesenen Eigenschaften zu speichern. Wenn alle beim Laden erfolgreich sind, wird NewProps in die PAPER \_ PROPERTIES-Struktur m \_ PaperProperties kopiert. Wie zuvor wird der [**IStream-Zeiger**](/windows/desktop/api/Objidl/nn-objidl-istream) freigegeben, nachdem das Laden abgeschlossen ist und der **IStream** nicht mehr benötigt wird.

Wenn am Ende von **Laden** ein Fehler auftritt, wird das Ink-Datenarray gelöscht, da es beschädigte Daten enthalten kann.

Wenn am Ende des **Ladevorgangs** kein Fehler auftritt, wird die [**IPaperSink::Loaded-Methode**](ipapersink-methods.md) des Clients in der internen NotifySinks-Methode von COPaper aufgerufen, um den Client zu benachrichtigen, dass der Ladevorgang abgeschlossen ist. Dies ist eine wichtige Benachrichtigung für den Client, da er diese neuen geladenen Ink-Daten anzeigen muss. Diese Benachrichtigung nutzt in COPaper erheblich die Features von miteinander verbundenen Objekten.

 

 




