---
title: Matrixtransformationen
description: Scheitelungen und Normals werden von den Matrizen modelview und projection transformiert, bevor sie zum Erstellen eines Bilds im Framepuffer verwendet werden.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- OpenGL-Verarbeitungspipeline,Matrizen
- Matrizen OpenGL
- ModelView-Matrix
- Projektionsmatrix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e3c88ffcfebc989400cfa9a85c16f355c0a7090ff4d16531cf03c3697ee869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937319"
---
# <a name="matrix-transformations"></a>Matrixtransformationen

Scheitelungen und Normals werden von den Matrizen modelview und projection transformiert, bevor sie zum Erstellen eines Bilds im Framepuffer verwendet werden. Verwenden Sie Funktionen wie [**glMatrixMode,**](glmatrixmode.md) [ * *glMultMatrix \** _](glmultmatrix.md), [_*glRotate, \**_](glrotate.md) [_*glTranslate \**_](gltranslate.md)und [_*glScale, \**_](glscale.md) um die gewünschten Transformationen zu erstellen. Oder geben Sie Matrizen direkt mit [_*glLoadMatrix \**_](glloadmatrix.md) und [_ *glLoadIdentity an.* *](glloadidentity.md) Verwenden [**Sie glPushMatrix**](glpushmatrix.md) und [**glPopMatrix,**](glpopmatrix.md) um Modellansichts- und Projektionsmatrizen auf ihren jeweiligen Stapeln zu speichern und wiederherzustellen.

 

 




