---
title: Matrix Transformationen
description: Vertices und normale werden von Modelview und Projektions Matrizen transformiert, bevor Sie zum Entwickeln eines Bilds im Framebuffer verwendet werden.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- OpenGL-Verarbeitungs Pipeline, Matrizen
- Matrizen OpenGL
- Modelview-Matrix
- Projektions Matrix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db0ebd8bd13b8d2cee32b8873f697ab073140bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206659"
---
# <a name="matrix-transformations"></a>Matrix Transformationen

Vertices und normale werden von Modelview und Projektions Matrizen transformiert, bevor Sie zum Entwickeln eines Bilds im Framebuffer verwendet werden. Verwenden Sie Funktionen wie z. b. [**glMatrixMode**](glmatrixmode.md) [**, \* glmultmatrix**](glmultmatrix.md), [**glrotation \***](glrotate.md), [**gltranslate \***](gltranslate.md)und [**glscale \***](glscale.md) , um die gewünschten Transformationen zu verfassen. Oder Sie geben Matrizen direkt mit " [**glloadmatrix \***](glloadmatrix.md) " und " [**glLoadIdentity**](glloadidentity.md)" an. Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und [**glPopMatrix**](glpopmatrix.md) , um Modelview-und Projektions Matrizen auf ihren jeweiligen Stapeln zu speichern und wiederherzustellen.

 

 




