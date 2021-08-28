---
title: Erste Schritte mit DirectX für Windows
description: Das Erstellen eines Microsoft DirectX-Spiels für Windows ist eine Herausforderung für einen neuen Entwickler. Hier sehen wir uns schnell die beteiligten Konzepte und die Schritte an, die Sie ausführen müssen, um mit der Entwicklung eines Spiels mit DirectX und C++ zu beginnen.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c93944b29546746f88b3edcacaefeeeacde0784e51f82c74f4cd462bc62025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987000"
---
# <a name="get-started-with-directx-for-windows"></a>Erste Schritte mit DirectX für Windows

Das Erstellen eines Microsoft DirectX-Spiels für Windows ist eine Herausforderung für einen neuen Entwickler. Hier sehen wir uns schnell die beteiligten Konzepte und die Schritte an, die Sie ausführen müssen, um mit der Entwicklung eines Spiels mit DirectX und C++ zu beginnen.

Fangen wir also an.

## <a name="what-skills-do-you-need"></a>Welche Qualifikationen benötigen Sie?

Um ein Spiel in DirectX für Windows entwickeln zu können, müssen Sie über einige Grundkenntnisse verfügen. Insbesondere müssen Folgendes möglich sein:

-   Lesen und Schreiben von modernem C++-Code (C++11 hilft am meisten) und Vertrautheit mit grundlegenden C++-Entwurfsprinzipien und -Mustern wie Vorlagen und dem Factorymodell. Sie müssen auch mit allgemeinen C++-Bibliotheken wie der Standardvorlagenbibliothek und insbesondere mit den Umwandlungsoperatoren, Zeigertypen und den Standardvorlagenbibliothek-Datenstrukturen (z. B. std::vector) vertraut sein.
-   Grundlegendes zur Geometrie, Trigonometrie und linearen Algebra. Ein Großteil des Codes, den Sie in den Beispielen finden, setzt voraus, dass Sie diese Formen der Mathematik und ihre allgemeinen Regeln verstehen.
-   Vertrautheit mit COM– insbesondere [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (intelligenter Zeiger).
-   Machen Sie sich mit den Grundlagen der Grafik- und Grafiktechnologie, insbesondere 3D-Grafiken, aus. Obwohl DirectX selbst über eine eigene Terminologie verfügt, baut es immer noch auf einem fundierten Verständnis allgemeiner 3D-Grafikprinzipien auf.
-   Verstehen Sie das Konzept einer Nachrichtenschleife, da Sie eine Schleife implementieren, die auf das Windows Betriebssystem lauscht.

## <a name="and-were-off"></a>Und wir sind los!

Bist du bereit? Sehen wir uns dies noch einmal an. Sie haben:

-   Eine aktualisierte und funktionierende Installation von Windows 8.1.
-   Eine Installation von [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).
-   Ein unerschrockener Spieler und der Wunsch, mehr über die Entwicklung von DirectX-Spielen zu erfahren!

## <a name="next-steps"></a>Nächste Schritte



| Thema                                                                                                   | Beschreibung                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Arbeiten mit DirectX-Geräteressourcen](work-with-dxgi.md)                                           | Erfahren Sie, wie Sie DXGI verwenden, um ein virtualisiertes Grafikgerät zu erstellen und eine Swapkette zu erstellen und zu konfigurieren.     |
| [Grundlegendes zur Direct3D 11-Renderingpipeline](understand-the-directx-11-2-graphics-pipeline.md) | Erfahren Sie, wie Sie die DirectX-Geräteressourcenklasse verknüpfen und mithilfe der Direct3D-Grafikpipeline zeichnen. |
| [Arbeiten mit Shadern und Shaderressourcen](work-with-shaders-and-shader-resources.md)               | Erfahren Sie, wie Sie HLSL-Shaderprogramme für Direct3D-Grafikpipelinestufen schreiben.                            |



 

 

 