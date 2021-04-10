---
title: Ausführen von Auswahl und Feedback
description: Ausführen von Auswahl und Feedback
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL, Auswahl
- OpenGL, Feedback
- OpenGL, Rendering
- Auswahlmodus OpenGL
- Feedback Modus OpenGL
- Renderingmodus OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310039"
---
# <a name="performing-selection-and-feedback"></a>Ausführen von Auswahl und Feedback

Auswahl, Feedback und Rendering sind sich gegenseitig ausschließende Betriebsmodi. Rendering ist der normale Standardmodus, in dem Fragmente durch rasterization erstellt werden.

Im Auswahl-und Feedback Modus werden keine Fragmente erzeugt. Daher findet keine Frame Puffer-Änderung statt. Im Auswahlmodus können Sie feststellen, welche primitiven in einem Fensterbereich gezeichnet werden. im Feedback Modus werden Informationen über primitive, die gerengt werden, an die Anwendung zurückgegeben.

Mit [**glrendermode**](glrendermode.md)wählen Sie zwischen diesen drei Modi aus.

-   [Auswahl](selection.md)
-   [Feedback](feedback.md)
-   [Auswahl-und Feedback Referenz](selection-and-feedback-reference.md)

 

 




