---
title: Komponenten
description: Komponenten
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL on Windows,components
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11c8d23130393102f39b716e16c0a6433a40122ad176a525b40e2e1a21b0360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868780"
---
# <a name="components"></a>Komponenten

Die Microsoft-Implementierung von OpenGL in Windows umfasst die folgenden Komponenten:

-   Der vollständige Satz der aktuellen OpenGL-Befehle

    OpenGL enthält eine Bibliothek mit Kernfunktionen für 3D-Grafikvorgänge. Diese grundlegenden Funktionen werden verwendet, um Objektformbeschreibungen, Matrixtransformationen, Beleuchtung, Farben, Textur, Clipping, Bitmaps, Klammern und Antialiasing zu verwalten. Die Namen für diese Kernfunktionen haben das Präfix "gl".

    Viele der OpenGL-Befehle verfügen über mehrere Varianten, die sich in Anzahl und Typ ihrer Parameter unterscheiden. Wenn sie alle Varianten zählen, gibt es mehr als 300 OpenGL-Befehle.

-   Die OpenGL-Hilfsprogrammbibliothek (GLU)

    Diese Bibliothek von Hilfsfunktionen ergänzt die wichtigsten OpenGL-Funktionen. Die Befehle verwalten Texturunterstützung, Koordinatentransformation, Polygontessellation, Rendering-Kugeln, Zylinder und Datenträger, NURBS-Kurven (Non-Uniform Rational B-Spline) und Oberflächen sowie die Fehlerbehandlung.

-   Hilfsbibliothek zum OpenGL-Programmierhandbuch

    Dies ist eine einfache, plattformunabhängige Bibliothek von Funktionen zum Verwalten von Fenstern, Verarbeiten von Eingabeereignissen, Zeichnen klassischer 3D-Objekte, Verwalten eines Hintergrundprozesses und Ausführen eines Programms. Die Fensterverwaltungs- und Eingaberoutinen bieten eine Basisfunktionalität, mit der Sie schnell mit der Programmierung in OpenGL beginnen können.

    Verwenden Sie sie jedoch nicht in einer Produktionsanwendung. Dies sind einige Gründe für diese Warnung:

    -   Die Meldungsschleife befindet sich im Bibliothekscode.
    -   Es gibt keine Möglichkeit, Handler für zusätzliche WM-Meldungen \* hinzuzufügen.
    -   Logische Paletten werden nur sehr wenig unterstützt.

    Die Bibliothek wird im *OpenGL-Programmierhandbuch beschrieben und verwendet.*

-   Die WGL-Funktionen

    Dieser Funktionssatz verbindet OpenGL mit dem Windows Fenstersystem. Die Funktionen verwalten Renderingkontexte, Anzeigelisten, Erweiterungsfunktionen und Schriftartbitmaps. Die WGL-Funktionen sind analog zu den GLX-Erweiterungen, die OpenGL mit dem X Window System verbinden. Die Namen für diese Funktionen haben das Präfix "wgl".

-   Neue Windows für Pixelformate und doppelte Pufferung

    Diese Funktionen unterstützen Pixelformate pro Fenster und doppelte Pufferung (für reibungslose Bildänderungen) von Fenstern. Diese neuen Funktionen gelten nur für OpenGL-Grafikfenster.

 

 




