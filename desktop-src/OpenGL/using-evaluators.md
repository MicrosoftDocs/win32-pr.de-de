---
title: Verwenden von Evaluatoren
description: Verwenden von Evaluatoren
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, Evaluators
- Evaluatoren OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1aef70a7a854e16cf4992d9dd44c4931ad4d044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309643"
---
# <a name="using-evaluators"></a>Verwenden von Evaluatoren

Mit den OpenGL-Auswertungsfunktionen können Sie eine polynomale Zuordnung verwenden, um Vertices, normale, Texturkoordinaten und Farben zu entwickeln. Diese berechneten Werte werden dann an die Verarbeitungs Pipeline weitergegeben, als würden Sie direkt angegeben. Die auswerterfunktionen sind auch die Grundlage für die NURBS-Funktionen (Non-Uniform Rational B-Spline), mit denen Sie Kurven und Oberflächen definieren können, wie unter [OpenGL Utility Library](opengl-utility-library.md)beschrieben.

Der erste Schritt bei der Verwendung von auswergratoren besteht darin, die entsprechende eindimensionale oder zweidimensionale polynomenzuordnung mithilfe von " [**glmap \***](glmap1.md)" zu definieren. Sie können dann die Domänen Werte für diese Zuordnung auf zwei Arten angeben und auswerten:

-   Definieren Sie eine Reihe von gleichmäßig zugeordneten Domänen Werten, die mithilfe von [**glmapgrid**](glmapgrid-functions.md) zugeordnet werden sollen, und evaluieren Sie dann eine rechteckige Teilmenge dieses Rasters mit [**glevalmesh**](glevalmesh-functions.md). Ein einzelner Punkt des Rasters kann mithilfe von [**glevalpoint**](glevalpoint.md)ausgewertet werden.
-   Geben Sie einen gewünschten Domänen Wert explizit als Argument an, das die Zuordnungen mit diesem Wert auswertet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Evaluatorreferenz](evaluators-reference.md)
</dt> </dl>

 

 




