---
title: Komponenten
description: Komponenten
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL unter Windows, Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341468"
---
# <a name="components"></a>Komponenten

Die Microsoft-Implementierung von OpenGL in Windows umfasst die folgenden Komponenten:

-   Der vollständige Satz der aktuellen OpenGL-Befehle

    OpenGL enthält eine Bibliothek mit Kernfunktionen für 3D-Grafik Vorgänge. Diese grundlegenden Funktionen werden verwendet, um Objektform Beschreibung, Matrix Transformation, Beleuchtung, Färbung, Textur, Clipping, Bitmaps, Nebel und Antialiasing zu verwalten. Die Namen für diese Kernfunktionen haben das Präfix "GL".

    Viele der OpenGL-Befehle verfügen über mehrere Varianten, die sich von der Anzahl und dem Typ ihrer Parameter unterscheiden. Wenn alle Varianten gezählt werden, sind mehr als 300 OpenGL-Befehle vorhanden.

-   The OpenGL Utility (GLU) Library

    Diese Bibliothek von Hilfsfunktionen ergänzt die wichtigsten OpenGL-Funktionen. Die Befehle verwalten Textur Unterstützung, Koordinatentransformation, Polygon-Mosaik, renderingbereiche, Zylinder und Datenträger, NURBS (nicht einheitliche rationale B-Spline-Kurven und-Oberflächen) und Fehlerbehandlung.

-   Hilfsbibliothek für OpenGL-Programmier Handbuch

    Dies ist eine einfache, plattformunabhängige Funktionsbibliothek für die Verwaltung von Fenstern, das Behandeln von Eingabe Ereignissen, das Zeichnen klassischer 3D-Objekte, das Verwalten eines Hintergrund Prozesses und das Ausführen eines Programms. Die Fensterverwaltung und Eingabe Routinen stellen eine grundlegende Funktionalität bereit, mit der Sie schnell mit der Programmierung in OpenGL beginnen können.

    Verwenden Sie Sie jedoch nicht in einer Produktionsanwendung. Dies sind einige Gründe für diese Warnung:

    -   Die Nachrichten Schleife befindet sich im Bibliotheks Code.
    -   Es gibt keine Möglichkeit zum Hinzufügen von Handlern für zusätzliche WM- \* Nachrichten.
    -   Logische Paletten werden nur sehr unterstützt.

    Die Bibliothek wird im *OpenGL-Programmier Handbuch* beschrieben und verwendet.

-   Die WGL-Funktionen

    Dieser Funktions Satz verbindet OpenGL mit dem Windows-windowingsystem. Die Funktionen verwalten renderingkontexte, Anzeigelisten, Erweiterungsfunktionen und Schriftart Bitmaps. Die WGL-Funktionen entsprechen den glx-Erweiterungen, die OpenGL mit dem X-Fenster System verbinden. Die Namen für diese Funktionen haben das Präfix "WGL".

-   Neue Windows-Funktionen für Pixel Formate und doppelte Pufferung

    Diese Funktionen unterstützen Pixel Formate pro Fenster und doppelte Pufferung (für Smooth-Abbild Änderungen) von Fenstern. Diese neuen Funktionen gelten nur für OpenGL-Grafikfenster.

 

 




