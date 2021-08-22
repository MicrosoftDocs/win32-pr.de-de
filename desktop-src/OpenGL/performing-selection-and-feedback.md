---
title: Durchführen von Auswahl und Feedback
description: Durchführen von Auswahl und Feedback
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL,Auswahl
- OpenGL,Feedback
- OpenGL,Rendering
- Auswahlmodus OpenGL
- Feedbackmodus OpenGL
- Renderingmodus OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95efe3f07e86056cd0364daaed1e6a9c0ef402afc18b14d74cca313c9835479f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936285"
---
# <a name="performing-selection-and-feedback"></a>Durchführen von Auswahl und Feedback

Auswahl, Feedback und Rendering schließen sich gegenseitig aus. Rendering ist der normale Standardmodus, in dem Fragmente durch Rasterung erzeugt werden.

Im Auswahl- und Feedbackmodus werden keine Fragmente erzeugt. daher findet keine Framebuffer-Änderung statt. Im Auswahlmodus können Sie bestimmen, welche Primitive in einen Bereich eines Fensters gezeichnet werden. Im Feedbackmodus werden Informationen zu Primitiven, die rastert werden, an die Anwendung zurückgeführt.

Sie wählen mit [**glRenderMode**](glrendermode.md)einen dieser drei Modi aus.

-   [Auswahl](selection.md)
-   [Feedback](feedback.md)
-   [Referenz zu Auswahl und Feedback](selection-and-feedback-reference.md)

 

 




