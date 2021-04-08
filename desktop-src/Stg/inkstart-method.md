---
title: Inkstart-Methode
description: Die Methoden inkstart, inkdraw und inkstoppt verwenden alle Win32-GUI-Konstrukte wie z. b. Geräte Kontexte und Stift Objekte.
ms.assetid: a639e1d2-6d81-472b-b639-d237e202020f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e25d02c4490106180298b6977ec539bd96fd03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947953"
---
# <a name="inkstart-method"></a>Inkstart-Methode

Die Methoden **inkstart**, [**inkdraw**](inkdraw-method.md)und [**inkstoppt**](cguipaper-methods.md) verwenden alle Win32-GUI-Konstrukte wie z. b. Geräte Kontexte und Stift Objekte. Dies veranschaulicht, warum cguipaper als separate Ebene der Kapselung benötigt wird. Die GUI-Aspekte des Zeichnungs Papiers werden in cguipaper behandelt. Das copaper-Objekt wird nur frei Hand Daten gesendet.

Ein weiterer Entwurfs Grund für die cguipaper-Ebene der Kapselung ist die duale Art der **inkstart**-, [**inkdraw**](inkdraw-method.md)-und [**inkstopmethode**](cguipaper-methods.md) . Sie werden nicht nur für copaper aufgerufen, um die frei Hand Daten aufzuzeichnen, während Sie auftreten, sondern zeichnen auch ein visuelles Bild der Zeichnung auf. Cguipaper behält ein m- \_ binksave-Flag bei, um diese duale Art zu verwalten. Wenn "m \_ binksave" den Wert "false" hat, wird das Bild auf dem Bildschirm gezeichnet, aber die Daten werden nicht zur Aufzeichnung an copaper gesendet.

Dieses Schema wird beim Neuzeichnen verwendet, wenn der Benutzer die Maus nicht bewegt, aber die frei Hand Daten des Kopierers für das automatische Neuzeichnen an cguipaper erneut gesendet werden. Cguipaper kann angewiesen werden, das m \_ binksave-Flag durch Aufrufen der [**inksave**](cguipaper-methods.md) -Methode festzulegen.

Die folgenden Beispielcode Ausschnitte veranschaulichen die **inkstart** -Methoden von guipaper. cpp und Senke. CPP.

## <a name="inkstart-method-guipapercpp"></a>Inkstart-Methode (guipaper). CPP


```C++
HRESULT CGuiPaper::InkStart(
                       SHORT nX,
                       SHORT nY)
  {
    HRESULT hr = E_FAIL;

    if (m_nLockKey || (!m_nLockKey && !m_bInkSaving))
    {
      // Start an ink drawing sequence only if one is not in progress.
      if (!m_bInking)
      {
        // Remember start position.
        m_OldPos.x = nX;
        m_OldPos.y = nY;

        // Delete old pen.
        if (m_hPen)
          DeleteObject(m_hPen);

        // Create and select the new drawing pen.
        m_hPen = CreatePen(PS_SOLID, m_nInkWidth, m_crInkColor);
        SelectObject(m_hDC, m_hPen);

        hr = NOERROR;

        // Ask the Paper object to mark the start of the ink drawing
        // sequence in the current ink color.
        if (m_pIPaper && m_bInkSaving)
        {
          hr = m_pIPaper->InkStart(
                            m_nLockKey,
                            nX,
                            nY,
                            m_nInkWidth,
                            m_crInkColor);
          // Capture the Mouse.
          SetCapture(m_hWnd);

          // We've modified the ink data--it is now "dirty" with
          // respect to the compound file image. Set dirty flag.
          m_bDirty = TRUE;
        }

        // Set inking flag to TRUE.
        m_bInking = TRUE;
      }
    }

    return hr;
  }
```



## <a name="inkstart-method-sinkcpp"></a>Inkstart-Methode (Senke). CPP

**Stoclien** empfängt die Zeichnungsdaten in Form von Aufrufen der verbundenen **itaschen Sink** -Schnittstelle in Ihrem copapersink-Objekt. Diese Methoden entsprechen den ähnlichen Methoden **inkstart**, [**inkdraw**](inkdraw-method.md)und [**inkstopps**](cguipaper-methods.md) in cguipaper.


```C++
STDMETHODIMP COPaperSink::CImpIPaperSink::InkStart(
                                              SHORT nX,
                                              SHORT nY,
                                              SHORT nWidth,
                                              COLORREF crInkColor)
  {
    // Turn off ink saving to the COPaper object.
    m_pBackObj->m_pGuiPaper->InkSaving(FALSE);

    // Play the data back to the CGuiPaper for display only.
    m_pBackObj->m_pGuiPaper->InkWidth(nWidth);
    m_pBackObj->m_pGuiPaper->InkColor(crInkColor);
    m_pBackObj->m_pGuiPaper->InkStart(nX, nY);

    return NOERROR;
  }
```



Wenn **inkstart** in der Senke aufgerufen wird, wird cguipaper aufgerufen, um das Speichern von frei Hand Eingaben auf copaper zu deaktivieren. Copaper muss keine Echo Kopie der gesendeten Daten empfangen. Wenn [**inkdraw**](inkdraw-method.md) in der Senke aufgerufen wird, übergibt es einfach den Aufruf an **cguipaper:: inkdraw**. Wenn [**inkend**](cguipaper-methods.md) in der Senke aufgerufen wird, wird cguipaper aufgerufen, um die frei Hand Speicherung wieder zu aktivieren. Das Ergebnis ist eine Wiedergabe der frei Hand Daten von copaper an cguipaper zur Anzeige.

Sie können das Verhalten von **stoclien** testen, wenn dessen **itaschen Sink** getrennt ist, indem Sie im Menü "Sink" die Auswahl Option trennen auswählen. Nachdem Sie die Senke getrennt haben, wählen Sie als Experiment im Menü Hilfe die Option Info aus. Dadurch wird das Dialogfeld Info angezeigt, das einen Teil der **stoclien**-Zeichnung abdeckt. Klicken Sie im Dialogfeld Info auf OK. Beachten Sie, dass der Teil der Zeichnung, der abgedeckt wurde, jetzt nicht mehr vorhanden ist. Die Zeichnungsdaten gehen nicht verloren, aber ein Teil des Bilds ist. Der Client hat die WM \_ -Zeichnungs Nachricht empfangen und die [**iPaper:: Redraw**](ipaper--redraw.md) -Methode ausgegeben. Da die Senke jedoch nicht verbunden war, erhielt sie nicht die **ipapersink** -Aufrufe, um die Zeichnung neu zu zeichnen.

Sie können dieses Verhalten auch testen, indem Sie die **stoclien** minimieren und dann wiederherstellen. In diesem Fall geht das gesamte Zeichnungsbild verloren und muss neu gezeichnet werden. Um das Zeichnungsbild nach einem dieser Tests neu zu zeichnen, verwenden Sie das Menü Sink, um die Verbindung wiederherzustellen, und wählen Sie dann im Menü Zeichnen die Option [**neu zeichnen**](ipaper--redraw.md) aus.

 

 




