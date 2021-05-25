---
title: Erste Schritte mit DirectX für Windows
description: Das Erstellen eines Microsoft DirectX-Spiels für Windows ist eine Herausforderung für einen neuen Entwickler. Hier sehen wir uns schnell die beteiligten Konzepte und die Schritte an, die Sie ausführen müssen, um mit der Entwicklung eines Spiels mit DirectX und C++ zu beginnen.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bac8ca2805fed9ec42faf9deda9ddd51da39685
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343585"
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
-   Verstehen Sie das Konzept einer Nachrichtenschleife, da Sie eine Schleife implementieren, die auf das Windows-Betriebssystem lauscht.

## <a name="and-were-off"></a>Und wir sind los!

Bist du bereit? Sehen wir uns dies noch einmal an. Sie haben:

-   Eine aktualisierte und funktionierende Installation von Windows 8.1.
-   Eine Installation von [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).
-   Ein unerschrockener Kasten und der Wunsch, mehr über die DirectX-Spieleentwicklung zu erfahren!

## <a name="next-steps"></a>Nächste Schritte



| Thema                                                                                                   | BESCHREIBUNG                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Arbeiten mit DirectX-Geräteressourcen](work-with-dxgi.md)                                           | Erfahren Sie, wie Sie DXGI verwenden, um ein virtualisiertes Grafikgerät zu erstellen und eine Austauschkette zu erstellen und zu konfigurieren.     |
| [Verstehen der Direct3D 11-Renderingpipeline](understand-the-directx-11-2-graphics-pipeline.md) | Erfahren Sie, wie Sie mithilfe der Direct3D-Grafikpipeline eine Verbindung mit der DirectX-Geräteressourcenklasse erstellen und zeichnen. |
| [Arbeiten mit Shadern und Shaderressourcen](work-with-shaders-and-shader-resources.md)               | Erfahren Sie, wie Sie HLSL-Shaderprogramme für Direct3D-Grafikpipelinestufen schreiben.                            |



 

 

 