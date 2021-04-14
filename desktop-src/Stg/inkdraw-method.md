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
# <a name="inkdraw-method"></a>Inkdraw-Methode

Cguipaper speichert auch ein m- \_ binking-Flag. [Inkstart](inkstart-method.md) legt ihn auf " **true** " fest, um zu signalisieren, dass eine Zeichnungs Sequenz gerade verarbeitet wird. Beispielsweise verwendet die inkdraw-Methode dieses Flag, um zu bestimmen, ob Sie frei Hand Daten zeichnen und speichern soll.

Im folgenden finden Sie die inkdraw-Methode von guipaper. CPP.


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



Diese Methode führt keine Aktion aus, wenn m- \_ binking **false** ist. Dies ist die Bedingung, wenn der Benutzer einfach den Mauszeiger über das Client Fenster bewegt, ohne die linke Maustaste zu drücken.

Inkdraw hat eine doppelte Verantwortung. Die Win32-Aufrufe "fivetoex" und "LineTo" werden zum Zeichnen von Linienbildern auf dem GUI-Bildschirm erstellt (mit dem Gerätekontext handle, das in m \_ hdc gespeichert ist). Die frei Hand Daten werden auch an das copaper-Objekt für die Aufzeichnung mithilfe der inkdraw-Methode der [iPaper](ipaper-methods.md) -Schnittstelle übermittelt. Wenn "m \_ binksave" den Wert " **false**" hat, zeichnet inkdraw das Linien Bild, speichert die Daten aber nicht in copaper. Diese Bedingung wird beim Neuzeichnen verwendet.

 

 




