---
description: Fast alle Anwendungen verwenden den Bildschirm, um die Daten anzuzeigen, die Sie bearbeiten.
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: Informationen zum Zeichnen und zeichnen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993862"
---
# <a name="about-painting-and-drawing"></a>Informationen zum Zeichnen und zeichnen

Fast alle Anwendungen verwenden den Bildschirm, um die Daten anzuzeigen, die Sie bearbeiten. Eine Anwendung zeichnet Bilder, zeichnet Abbildungen und schreibt Text, sodass der Benutzerdaten anzeigen kann, während er erstellt, bearbeitet und gedruckt wird. Microsoft Windows bietet umfassende Unterstützung für das Zeichnen und zeichnen, aber aufgrund der Art der Multitasking-Betriebssysteme müssen Anwendungen beim Zugriff auf den Bildschirm miteinander zusammenarbeiten.

Damit alle Anwendungen reibungslos und kooperativ funktionieren, verwaltet das System alle Ausgaben auf dem Bildschirm. Anwendungen verwenden Windows als das primäre Ausgabegerät anstelle des Bildschirms. Die System Bereitstellung zeigt Geräte Kontexte an, die den Fenstern eindeutig entsprechen. Anwendungen verwenden Anzeigegeräte Kontexte, um die Ausgabe an die angegebenen Fenster weiterzuleiten. Das Zeichnen in einem Fenster (Weiterleiten der Ausgabe) hindert eine Anwendung daran, die Ausgabe anderer Anwendungen zu beeinträchtigen, und ermöglicht es, Anwendungen untereinander zu koexistieren, während die Grafikfunktionen des Systems weiterhin vollständig genutzt werden.

-   [Wann in einem Fenster gezeichnet werden soll](when-to-draw-in-a-window.md)
-   [Die WM-Zeichnungs \_ Meldung](the-wm-paint-message.md)
-   [Zeichnen ohne die WM-Zeichnungs \_ Nachricht](drawing-without-the-wm-paint-message.md)
-   [Fenster Koordinaten System](window-coordinate-system.md)
-   [Fensterbereiche](window-regions.md)
-   [Fenster Hintergrund](window-background.md)
-   [Minimierte Fenster](minimized-windows.md)
-   [Fenstergröße geändert](resized-windows.md)
-   [Nicht-Client Bereich](nonclient-area.md)
-   [Aktualisierungs Bereich des untergeordneten Fensters](child-window-update-region.md)
-   [Geräte anzeigen](display-devices.md)
-   [Fenster Update Sperre](window-update-lock.md)
-   [Akkumuliertes Rechteck](accumulated-bounding-rectangle.md)

 

 



