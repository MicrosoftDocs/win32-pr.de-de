---
title: Inkdraw-Methode
description: Cguipaper speichert auch ein m- \_ binking-Flag. Inkstart legt ihn auf "true" fest, um zu signalisieren, dass eine Zeichnungs Sequenz gerade verarbeitet wird. Beispielsweise verwendet die inkdraw-Methode dieses Flag, um zu bestimmen, ob Sie frei Hand Daten zeichnen und speichern soll.
ms.assetid: 0fe9d029-1522-4caf-8efb-0a4eb2b59958
keywords:
- Inkdraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41973d3f8560f25a81ac1deb782bada51b015239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388585"
---
# <a name="inkdraw-method"></a><span data-ttu-id="b8422-106">Inkdraw-Methode</span><span class="sxs-lookup"><span data-stu-id="b8422-106">InkDraw Method</span></span>

<span data-ttu-id="b8422-107">Cguipaper speichert auch ein m- \_ binking-Flag.</span><span class="sxs-lookup"><span data-stu-id="b8422-107">CGuiPaper also keeps an m\_bInking flag.</span></span> <span data-ttu-id="b8422-108">[Inkstart](inkstart-method.md) legt ihn auf " **true** " fest, um zu signalisieren, dass eine Zeichnungs Sequenz gerade verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b8422-108">[InkStart](inkstart-method.md) sets it to **TRUE** to signal that a drawing sequence is in process.</span></span> <span data-ttu-id="b8422-109">Beispielsweise verwendet die inkdraw-Methode dieses Flag, um zu bestimmen, ob Sie frei Hand Daten zeichnen und speichern soll.</span><span class="sxs-lookup"><span data-stu-id="b8422-109">For example, the InkDraw method uses this flag to determine whether it should paint and save ink data.</span></span>

<span data-ttu-id="b8422-110">Im folgenden finden Sie die inkdraw-Methode von guipaper. CPP.</span><span class="sxs-lookup"><span data-stu-id="b8422-110">The following is the InkDraw method from GUIPAPER.CPP.</span></span>


```C++
HRESULT CGuiPaper::InkDraw(
                       SHORT nX,
                       SHORT nY)
  {
    if (m_bInking)
    {
      // Start this ink line at previous old position.
      MoveToEx(m_hDC, m_OldPos.x, m_OldPos.y, NULL);

      // Assign new old position and draw the new line.
      LineTo(m_hDC, m_OldPos.x = nX, m_OldPos.y = nY);

      // Ask the Paper object to save this data.
      if (m_bInkSaving)
        m_pIPaper->InkDraw(m_nLockKey, nX, nY);
    }

    return NOERROR;
  }
```



<span data-ttu-id="b8422-111">Diese Methode führt keine Aktion aus, wenn m- \_ binking **false** ist.</span><span class="sxs-lookup"><span data-stu-id="b8422-111">This method does nothing if m\_bInking is **FALSE**.</span></span> <span data-ttu-id="b8422-112">Dies ist die Bedingung, wenn der Benutzer einfach den Mauszeiger über das Client Fenster bewegt, ohne die linke Maustaste zu drücken.</span><span class="sxs-lookup"><span data-stu-id="b8422-112">This is the condition when the user is simply moving the mouse over the client window without pressing the left mouse button.</span></span>

<span data-ttu-id="b8422-113">Inkdraw hat eine doppelte Verantwortung.</span><span class="sxs-lookup"><span data-stu-id="b8422-113">InkDraw clearly has a dual responsibility.</span></span> <span data-ttu-id="b8422-114">Die Win32-Aufrufe "fivetoex" und "LineTo" werden zum Zeichnen von Linienbildern auf dem GUI-Bildschirm erstellt (mit dem Gerätekontext handle, das in m \_ hdc gespeichert ist).</span><span class="sxs-lookup"><span data-stu-id="b8422-114">The Win32 MoveToEx and LineTo calls are made to draw line images on the GUI screen (using the device context handle kept in m\_hDC).</span></span> <span data-ttu-id="b8422-115">Die frei Hand Daten werden auch an das copaper-Objekt für die Aufzeichnung mithilfe der inkdraw-Methode der [iPaper](ipaper-methods.md) -Schnittstelle übermittelt.</span><span class="sxs-lookup"><span data-stu-id="b8422-115">The ink data is also passed to the COPaper object for recording using the [IPaper](ipaper-methods.md) interface's InkDraw method.</span></span> <span data-ttu-id="b8422-116">Wenn "m \_ binksave" den Wert " **false**" hat, zeichnet inkdraw das Linien Bild, speichert die Daten aber nicht in copaper.</span><span class="sxs-lookup"><span data-stu-id="b8422-116">When m\_bInkSaving is **FALSE**, InkDraw paints the line image but does not store the data in COPaper.</span></span> <span data-ttu-id="b8422-117">Diese Bedingung wird beim Neuzeichnen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8422-117">This condition is used during repainting.</span></span>

 

 




