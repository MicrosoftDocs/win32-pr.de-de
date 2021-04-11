---
title: Portieren von Feedback Funktionen
description: Mit Iris GL unterscheidet sich die Art und Weise, wie Feedback behandelt wird, abhängig vom Computer, auf dem IRIS GL ausgeführt wird.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- IRIS GL Porting, Feedback
- Portieren von IRIS GL, Feedback
- Portieren auf OpenGL von IRIS GL, Feedback
- OpenGL-Portierung von IRIS GL, Feedback
- feedback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a04bcfe2c1d914a178ad7ad0dca95fb85d86bbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207152"
---
# <a name="porting-feedback-functions"></a>Portieren von Feedback Funktionen

Mit Iris GL unterscheidet sich die Art und Weise, wie Feedback behandelt wird, abhängig vom Computer, auf dem IRIS GL ausgeführt wird. OpenGL vereinheitlicht die Feedback Funktionen, sodass Sie sich auf ein konsistentes Feedback zwischen verschiedenen Hardwareplattformen verlassen können. In der folgenden Tabelle werden die-Feedback Funktionen von IRIS GL und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion | OpenGL-Funktion                                                                                            | Bedeutung                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| **Backs**     | [**glrendermode**](glrendermode.md) (GL- \_ Feedback)                                                      | Wechselt in den Feedback Modus.                    |
| **endfeedback**  | [**glrendermode**](glrendermode.md) (GL- \_ Rendering)[**glfeedbackbuffer**](glfeedbackbuffer.md)<br/> | Wechselt in den Renderingmodus.                   |
| **Passthrough**  | [**glpassthrough**](glpassthrough.md)                                                                     | Platziert einen tokenmarker im Feedback Puffer. |



 

 

 





