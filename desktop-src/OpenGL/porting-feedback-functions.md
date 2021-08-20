---
title: Portieren von Feedbackfunktionen
description: Bei IRIS GL unterscheidet sich die Art und Weise, wie Feedback verarbeitet wird, je nachdem, auf welchem Computer IRIS GL ausgeführt wird.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- IRIS GL-Portierung, Feedback
- Portieren von IRIS GL, Feedback
- Portieren von IRIS GL zu OpenGL, Feedback
- OpenGL-Portierung von IRIS GL,Feedback
- feedback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f4ab584dfbd9038d45e7d24c006857f278a9239fc6f9da4d38a75363f0d585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132632"
---
# <a name="porting-feedback-functions"></a>Portieren von Feedbackfunktionen

Bei IRIS GL unterscheidet sich die Art und Weise, wie Feedback verarbeitet wird, je nachdem, auf welchem Computer IRIS GL ausgeführt wird. OpenGL standardisiert Feedbackfunktionen, sodass Sie sich auf konsistentes Feedback zwischen verschiedenen Hardwareplattformen verlassen können. In der folgenden Tabelle sind die IRIS GL-Feedbackfunktionen und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion | OpenGL-Funktion                                                                                            | Bedeutung                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| **Feedback**     | [**glRenderMode**](glrendermode.md) ( GL \_ FEEDBACK )                                                      | Wechselt in den Feedbackmodus.                    |
| **endfeedback**  | [**glRenderMode**](glrendermode.md) ( GL \_ RENDER )[**glFeedbackBuffer**](glfeedbackbuffer.md)<br/> | Wechselt in den Renderingmodus.                   |
| **Passthrough**  | [**glPassThrough**](glpassthrough.md)                                                                     | Platziert einen Tokenmarker im Feedbackpuffer. |



 

 

 





