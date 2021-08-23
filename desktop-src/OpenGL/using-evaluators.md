---
title: Verwenden von Auswertungen
description: Verwenden von Auswertungen
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, Evaluators
- Evaluators OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4bb6808ad1898b0c98906a543291c700ee61257a35befa8886789f3f8b7e31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553490"
---
# <a name="using-evaluators"></a>Verwenden von Auswertungen

Mit den OpenGL-Auswertungsfunktionen können Sie eine polynomiale Zuordnung verwenden, um Scheitelpunkte, Normalwerte, Texturkoordinaten und Farben zu erzeugen. Diese berechneten Werte werden dann an die Verarbeitungspipeline übergeben, als wären sie direkt angegeben worden. Die Auswertungsfunktionen sind auch die Grundlage für die NURBS-Funktionen (Non-Uniform Rational B-Spline), mit denen Sie Kurven und Oberflächen definieren können, wie unter [OpenGL-Hilfsprogrammbibliothek](opengl-utility-library.md)beschrieben.

Der erste Schritt bei der Verwendung von Auswertungen besteht darin, die entsprechende ein- oder zweidimensionale polynomiale Zuordnung mithilfe von [**glMap \***](glmap1.md)zu definieren. Anschließend können Sie die Domänenwerte für diese Zuordnung auf zwei Arten angeben und auswerten:

-   Definieren Sie eine Reihe von Domänenwerten mit gleichmäßiger Leerzeichen, die mit [**glMapGrid**](glmapgrid-functions.md) zugeordnet werden sollen, und werten Sie dann eine rechteckige Teilmenge dieses Rasters mit [**glEvalMesh**](glevalmesh-functions.md)aus. Ein einzelner Punkt des Rasters kann mit [**glEvalPoint**](glevalpoint.md)ausgewertet werden.
-   Geben Sie explizit einen gewünschten Domänenwert als Argument an, das die Zuordnungen bei diesem Wert auswertet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auswertungsreferenz](evaluators-reference.md)
</dt> </dl>

 

 




