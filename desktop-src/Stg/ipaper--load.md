---
title: IPaper laden
description: Der folgende C++-Beispielcode zeigt, wie der vorhandene Stream im Speicher geöffnet wird, welche neuen Papiereigenschaften in gelesen werden und wie die aktuellen Werte für copaper festgelegt werden.
ms.assetid: a1559d97-387f-4d1a-8a9d-fa5c27abd545
keywords:
- IPaper laden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b5f16b8fe649d08226b2cff5a4b1a5234bddb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947952"
---
# <a name="ipaperload"></a>IPaper:: Load

Der folgende C++-Beispielcode zeigt, wie der vorhandene Stream im Speicher geöffnet wird, welche neuen Papiereigenschaften in gelesen werden und wie die aktuellen Werte für copaper festgelegt werden.

Im folgenden finden Sie die **iPaper:: Load** -Methode von Paper. cpp.


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



Nun wird die [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) -Methode aufgerufen, um den vorhandenen Datenstrom im Speicher zu öffnen, der als "Taschen Daten" bezeichnet wird. Zugriffsmodus-Flags sind für einen schreibgeschützten, direkten und nicht freigegebenen exklusiven Zugriff vorgesehen. Wenn der Stream geöffnet ist, wird die [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) -Methode aufgerufen, um die Papier \_ Eigenschafts Struktur zu lesen. Wenn der tatsächlich gelesene Betrag nicht gleich dem angeforderten Betrag ist, wird der Ladevorgang abgebrochen, und E \_ FAIL wird zurückgegeben. Wenn die Format Version in den neu gelesenen Papier \_ Eigenschaften nicht erkannt wird, wird der Ladevorgang abgebrochen, und **Load** gibt den Wert E \_ Fail zurück.

Bei einer gültigen Freihand-Datenformat Version wird die Größe des neuen frei Hand Daten Arrays aus den \_ gelesenen Papiereigenschaften verwendet, um ein neues frei Hand Daten Array mit der erforderlichen Größe zuzuweisen. Die vorhandenen frei Hand Daten werden gelöscht, und die Daten gehen verloren. Wenn diese Daten wertvoll waren, sollten Sie vor dem Aufrufen des **Lade** vorrufs gespeichert worden sein. Nachdem das neue Array zugewiesen wurde, wird [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) erneut aufgerufen, um die Daten aus dem Stream in das Array zu lesen. Wenn dieser Vorgang erfolgreich ist, werden die Werte in den neu gelesenen Papiereigenschaften als aktuelle Werte für copaper angenommen.

Während dieses Ladevorgangs wurde eine temporäre Papier \_ Eigenschafts Struktur (NewProperties) zum Speichern der neuen Eigenschaften verwendet, die gelesen wurden. Wenn alle mit der Last erfolgreich sind, werden NewProperties in die Papier \_ Eigenschafts Struktur "m \_ paperproperties" kopiert. Wie zuvor wird der **IStream** -Zeiger freigegeben, nachdem der Ladevorgang abgeschlossen und der [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) nicht mehr benötigt wird.

Wenn am Ende der **Last** ein Fehler auftritt, wird das frei Hand Daten Array gelöscht, da es möglicherweise beschädigte Daten enthält.

Wenn am Ende der **Auslastung** kein Fehler auftritt, wird die Client [**itaschen Sink:: Loaded**](ipapersink-methods.md) -Methode in der internen copaper-Methode aufgerufen, um den Client zu benachrichtigen, dass der Ladevorgang abgeschlossen ist. Dies ist eine wichtige Benachrichtigung für den Client, weil diese neuen geladenen frei Hand Daten angezeigt werden muss. Diese Benachrichtigung nutzt die Verbindungs fähigen-Objektfunktionen in copaper erheblich.

 

 




