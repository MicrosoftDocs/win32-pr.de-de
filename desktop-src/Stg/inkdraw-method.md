---
title: InkDraw-Methode
description: CGuiPaper behält auch ein m \_ bInking-Flag bei. InkStart legt ihn auf TRUE fest, um zu signalisieren, dass eine Zeichnungssequenz ausgeführt wird. Beispielsweise verwendet die InkDraw-Methode dieses Flag, um zu bestimmen, ob sie Ink-Daten zeichnen und speichern soll.
ms.assetid: 0fe9d029-1522-4caf-8efb-0a4eb2b59958
keywords:
- InkDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e146093d23fd16d122da1ea81d1c99bdf06ed926d5cb4dba2f1d77b747b2058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662760"
---
# <a name="inkdraw-method"></a>InkDraw-Methode

CGuiPaper behält auch ein m \_ bInking-Flag bei. [InkStart legt](inkstart-method.md) ihn auf **TRUE fest,** um zu signalisieren, dass eine Zeichnungssequenz ausgeführt wird. Beispielsweise verwendet die InkDraw-Methode dieses Flag, um zu bestimmen, ob sie Ink-Daten zeichnen und speichern soll.

Im Folgenden finden Sie die InkDraw-Methode von GUIPAPER. Cpp.


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



Diese Methode führt nichts aus, wenn m \_ bInking FALSE **ist.** Dies ist die Bedingung, wenn der Benutzer einfach den Mauszeiger über das Clientfenster bewegt, ohne die linke Maustaste zu drücken.

InkDraw hat eindeutig eine doppelte Verantwortung. Die Win32-Aufrufe MoveToEx und LineTo werden zum Zeichnen von Linienbildern auf dem GUI-Bildschirm (mithilfe des Gerätekontexthandlers in m \_ hDC) vorgenommen. Die Ink-Daten werden auch zur Aufzeichnung mithilfe der InkDraw-Methode der IPaper-Schnittstelle an das [COPaper-Objekt](ipaper-methods.md) übergeben. Wenn m \_ bInkSaving **FALSE ist,** zeichnet InkDraw das Linienbild, aber die Daten werden nicht in COPaper gespeichert. Diese Bedingung wird während des Neupaintings verwendet.

 

 




