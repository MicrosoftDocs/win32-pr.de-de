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
# <a name="inkstart-method"></a><span data-ttu-id="81127-103">Inkstart-Methode</span><span class="sxs-lookup"><span data-stu-id="81127-103">InkStart Method</span></span>

<span data-ttu-id="81127-104">Die Methoden **inkstart**, [**inkdraw**](inkdraw-method.md)und [**inkstoppt**](cguipaper-methods.md) verwenden alle Win32-GUI-Konstrukte wie z. b. Geräte Kontexte und Stift Objekte.</span><span class="sxs-lookup"><span data-stu-id="81127-104">**InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods all use Win32 GUI constructs such as device contexts and pen objects.</span></span> <span data-ttu-id="81127-105">Dies veranschaulicht, warum cguipaper als separate Ebene der Kapselung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="81127-105">This illustrates why CGuiPaper is needed as a separate level of encapsulation.</span></span> <span data-ttu-id="81127-106">Die GUI-Aspekte des Zeichnungs Papiers werden in cguipaper behandelt.</span><span class="sxs-lookup"><span data-stu-id="81127-106">The GUI aspects of the drawing paper are handled in CGuiPaper.</span></span> <span data-ttu-id="81127-107">Das copaper-Objekt wird nur frei Hand Daten gesendet.</span><span class="sxs-lookup"><span data-stu-id="81127-107">The COPaper object is sent only ink data.</span></span>

<span data-ttu-id="81127-108">Ein weiterer Entwurfs Grund für die cguipaper-Ebene der Kapselung ist die duale Art der **inkstart**-, [**inkdraw**](inkdraw-method.md)-und [**inkstopmethode**](cguipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="81127-108">Another design reason for the CGuiPaper level of encapsulation is the dual nature of its **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods.</span></span> <span data-ttu-id="81127-109">Sie werden nicht nur für copaper aufgerufen, um die frei Hand Daten aufzuzeichnen, während Sie auftreten, sondern zeichnen auch ein visuelles Bild der Zeichnung auf.</span><span class="sxs-lookup"><span data-stu-id="81127-109">They not only call on COPaper to record the ink data as it occurs, they also paint a visual image of the drawing as it occurs.</span></span> <span data-ttu-id="81127-110">Cguipaper behält ein m- \_ binksave-Flag bei, um diese duale Art zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="81127-110">CGuiPaper keeps an m\_bInkSaving flag to manage this dual nature.</span></span> <span data-ttu-id="81127-111">Wenn "m \_ binksave" den Wert "false" hat, wird das Bild auf dem Bildschirm gezeichnet, aber die Daten werden nicht zur Aufzeichnung an copaper gesendet.</span><span class="sxs-lookup"><span data-stu-id="81127-111">When m\_bInkSaving is FALSE, the image is drawn on screen but the data is not sent to COPaper for recording.</span></span>

<span data-ttu-id="81127-112">Dieses Schema wird beim Neuzeichnen verwendet, wenn der Benutzer die Maus nicht bewegt, aber die frei Hand Daten des Kopierers für das automatische Neuzeichnen an cguipaper erneut gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="81127-112">This scheme is used in repainting when the user is not moving the mouse but COPaper's ink data is being resent to CGuiPaper for automatic repainting.</span></span> <span data-ttu-id="81127-113">Cguipaper kann angewiesen werden, das m \_ binksave-Flag durch Aufrufen der [**inksave**](cguipaper-methods.md) -Methode festzulegen.</span><span class="sxs-lookup"><span data-stu-id="81127-113">CGuiPaper can be told to set the m\_bInkSaving flag by calling its [**InkSaving**](cguipaper-methods.md) method.</span></span>

<span data-ttu-id="81127-114">Die folgenden Beispielcode Ausschnitte veranschaulichen die **inkstart** -Methoden von guipaper. cpp und Senke. CPP.</span><span class="sxs-lookup"><span data-stu-id="81127-114">The following sample code snippets illustrate the **InkStart** methods of GUIPAPER.CPP AND SINK.CPP.</span></span>

## <a name="inkstart-method-guipapercpp"></a><span data-ttu-id="81127-115">Inkstart-Methode (guipaper). CPP</span><span class="sxs-lookup"><span data-stu-id="81127-115">InkStart Method (GUIPAPER.CPP)</span></span>


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



## <a name="inkstart-method-sinkcpp"></a><span data-ttu-id="81127-116">Inkstart-Methode (Senke). CPP</span><span class="sxs-lookup"><span data-stu-id="81127-116">InkStart Method (SINK.CPP)</span></span>

<span data-ttu-id="81127-117">**Stoclien** empfängt die Zeichnungsdaten in Form von Aufrufen der verbundenen **itaschen Sink** -Schnittstelle in Ihrem copapersink-Objekt.</span><span class="sxs-lookup"><span data-stu-id="81127-117">**StoClien** receives the drawing data in the form of calls to the connected **IPaperSink** interface in its COPaperSink object.</span></span> <span data-ttu-id="81127-118">Diese Methoden entsprechen den ähnlichen Methoden **inkstart**, [**inkdraw**](inkdraw-method.md)und [**inkstopps**](cguipaper-methods.md) in cguipaper.</span><span class="sxs-lookup"><span data-stu-id="81127-118">These methods correspond to the similar **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods in CGuiPaper.</span></span>


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



<span data-ttu-id="81127-119">Wenn **inkstart** in der Senke aufgerufen wird, wird cguipaper aufgerufen, um das Speichern von frei Hand Eingaben auf copaper zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="81127-119">When **InkStart** is called in the sink, it calls CGuiPaper to turn off ink saving to COPaper.</span></span> <span data-ttu-id="81127-120">Copaper muss keine Echo Kopie der gesendeten Daten empfangen.</span><span class="sxs-lookup"><span data-stu-id="81127-120">COPaper does not need to receive an echoed copy of the data it is sending.</span></span> <span data-ttu-id="81127-121">Wenn [**inkdraw**](inkdraw-method.md) in der Senke aufgerufen wird, übergibt es einfach den Aufruf an **cguipaper:: inkdraw**.</span><span class="sxs-lookup"><span data-stu-id="81127-121">When [**InkDraw**](inkdraw-method.md) is called in the sink, it simply passes the call on to **CGuiPaper::InkDraw**.</span></span> <span data-ttu-id="81127-122">Wenn [**inkend**](cguipaper-methods.md) in der Senke aufgerufen wird, wird cguipaper aufgerufen, um die frei Hand Speicherung wieder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="81127-122">When [**InkStop**](cguipaper-methods.md) is called in the sink, CGuiPaper is called to turn ink saving back on.</span></span> <span data-ttu-id="81127-123">Das Ergebnis ist eine Wiedergabe der frei Hand Daten von copaper an cguipaper zur Anzeige.</span><span class="sxs-lookup"><span data-stu-id="81127-123">The result is a playback of COPaper's ink data to CGuiPaper for display only.</span></span>

<span data-ttu-id="81127-124">Sie können das Verhalten von **stoclien** testen, wenn dessen **itaschen Sink** getrennt ist, indem Sie im Menü "Sink" die Auswahl Option trennen auswählen.</span><span class="sxs-lookup"><span data-stu-id="81127-124">You can test the behavior of **StoClien** when its **IPaperSink** is disconnected by choosing the Disconnect choice on the Sink menu.</span></span> <span data-ttu-id="81127-125">Nachdem Sie die Senke getrennt haben, wählen Sie als Experiment im Menü Hilfe die Option Info aus.</span><span class="sxs-lookup"><span data-stu-id="81127-125">As an experiment, after disconnecting the sink, choose About from the Help menu.</span></span> <span data-ttu-id="81127-126">Dadurch wird das Dialogfeld Info angezeigt, das einen Teil der **stoclien**-Zeichnung abdeckt.</span><span class="sxs-lookup"><span data-stu-id="81127-126">This will show the About dialog box, which will cover part of the **StoClien**'s drawing.</span></span> <span data-ttu-id="81127-127">Klicken Sie im Dialogfeld Info auf OK.</span><span class="sxs-lookup"><span data-stu-id="81127-127">Click OK in the About dialog box.</span></span> <span data-ttu-id="81127-128">Beachten Sie, dass der Teil der Zeichnung, der abgedeckt wurde, jetzt nicht mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="81127-128">Notice that the portion of the drawing that was covered is now gone.</span></span> <span data-ttu-id="81127-129">Die Zeichnungsdaten gehen nicht verloren, aber ein Teil des Bilds ist.</span><span class="sxs-lookup"><span data-stu-id="81127-129">The drawing data is not lost, but part of the image is.</span></span> <span data-ttu-id="81127-130">Der Client hat die WM \_ -Zeichnungs Nachricht empfangen und die [**iPaper:: Redraw**](ipaper--redraw.md) -Methode ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="81127-130">The client received the WM\_PAINT message and issued the [**IPaper::Redraw**](ipaper--redraw.md) method.</span></span> <span data-ttu-id="81127-131">Da die Senke jedoch nicht verbunden war, erhielt sie nicht die **ipapersink** -Aufrufe, um die Zeichnung neu zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="81127-131">But because the sink was not connected, it did not receive the **IPaperSink** calls to repaint the drawing.</span></span>

<span data-ttu-id="81127-132">Sie können dieses Verhalten auch testen, indem Sie die **stoclien** minimieren und dann wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="81127-132">You can also test this behavior by minimizing **StoClien** and then restoring it.</span></span> <span data-ttu-id="81127-133">In diesem Fall geht das gesamte Zeichnungsbild verloren und muss neu gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="81127-133">In this case, the entire drawing image is lost and needs repainting.</span></span> <span data-ttu-id="81127-134">Um das Zeichnungsbild nach einem dieser Tests neu zu zeichnen, verwenden Sie das Menü Sink, um die Verbindung wiederherzustellen, und wählen Sie dann im Menü Zeichnen die Option [**neu zeichnen**](ipaper--redraw.md) aus.</span><span class="sxs-lookup"><span data-stu-id="81127-134">To repaint the drawing image after either of these tests, use the Sink menu to reconnect, and then choose [**Redraw**](ipaper--redraw.md) from the Draw menu.</span></span>

 

 




