---
title: Einstieg in DirectX für Windows
description: Das Erstellen eines Microsoft DirectX-Spiels für Windows stellt eine Herausforderung für einen neuen Entwickler dar. Hier überprüfen wir schnell die Konzepte und die Schritte, die Sie ausführen müssen, um mit der Entwicklung eines Spiels mit DirectX und C++ zu beginnen.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae09cd127a30401ae0493f5dd770fe1e67607b45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339279"
---
# <a name="get-started-with-directx-for-windows"></a>Einstieg in DirectX für Windows

Das Erstellen eines Microsoft DirectX-Spiels für Windows stellt eine Herausforderung für einen neuen Entwickler dar. Hier überprüfen wir schnell die Konzepte und die Schritte, die Sie ausführen müssen, um mit der Entwicklung eines Spiels mit DirectX und C++ zu beginnen.

Fangen wir also an.

## <a name="what-skills-do-you-need"></a>Welche Fähigkeiten benötigen Sie?

Um ein Spiel in DirectX für Windows zu entwickeln, müssen Sie über einige grundlegende Kenntnisse verfügen. Insbesondere müssen Sie in der Lage sein, Folgendes zu tun:

-   Lesen und Schreiben von modernem C++-Code (C++ 11 hilft am meisten) und ist mit grundlegenden C++-Entwurfs Prinzipien und-Mustern wie Vorlagen und dem Werk Modell vertraut. Sie müssen auch mit allgemeinen C++-Bibliotheken wie der Standardvorlagen Bibliothek und speziell mit den Typumwandlungs Operatoren, Zeiger Typen und den standardmäßigen Vorlagen Bibliotheksdaten Strukturen (z. b. Std:: Vector) vertraut sein.
-   Verstehen Sie grundlegende Geometrie, Trigonometry und lineare Algebra. Bei einem Großteil des Codes, den Sie in den Beispielen finden, wird davon ausgegangen, dass Sie diese Formen der Mathematik und ihrer allgemeinen Regeln verstehen.
-   Vertrautheit mit com – besonders [**Microsoft:: WRL:: comptr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (intelligenter Zeiger).
-   Lernen Sie die Grundlagen von Grafiken und Grafik Technologien kennen, insbesondere 3D-Grafiken. Obwohl DirectX selbst über eine eigene Terminologie verfügt, baut es immer noch auf ein gut erstelltes Verständnis allgemeiner 3D-Grafik Prinzipien auf.
-   Verstehen Sie das Konzept einer Nachrichten Schleife, da Sie eine Schleife implementieren, die auf das Windows-Betriebssystem lauscht.

## <a name="and-were-off"></a>Und wir sind los!

Bist du bereit? Schauen wir uns das einmal an. Sie haben:

-   Eine aktualisierte und funktionierende Installation von Windows 8.1.
-   Eine Installation von [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).
-   Ein unerschrockener-Geist und ein Wunsch, mehr über die Entwicklung von DirectX-spielen zu erfahren!

## <a name="next-steps"></a>Nächste Schritte



|                                                                                                    |                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Arbeiten mit DirectX-Geräte Ressourcen](work-with-dxgi.md)                                           | Erfahren Sie, wie Sie DXGI verwenden, um ein virtualisiertes Grafikgerät zu erstellen und eine SwapChain zu erstellen und zu konfigurieren.     |
| [Grundlegendes zur Direct3D 11-Renderingpipeline](understand-the-directx-11-2-graphics-pipeline.md) | Erfahren Sie, wie Sie sich mit der DirectX-Geräte Ressourcen Klasse verbinden und mithilfe der Direct3D-Grafik Pipeline zeichnen. |
| [Arbeiten mit Shader und Shaderressourcen](work-with-shaders-and-shader-resources.md)               | Erfahren Sie, wie Sie HLSL-Shader-Programme für Direct3D-Grafik Pipeline Stufen schreiben.                            |



 

 

 