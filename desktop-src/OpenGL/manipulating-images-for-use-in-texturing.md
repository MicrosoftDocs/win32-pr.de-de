---
title: Bearbeiten von Bildern für die Verwendung in der Texturierung
description: Die OpenGL Utility Library (GLU) bietet Bildskalierung und automatische Mipmapping-Funktionen, um die Spezifikation von Textur Bildern zu vereinfachen.
ms.assetid: 20edf665-1fed-4761-b8b1-beee02c78b0d
keywords:
- OpenGL-Hilfsprogramm (GLU), Bildskalierung
- GLU (OpenGL-Hilfsprogramm), Bildskalierung
- OpenGL-Hilfsprogramm (GLU), automatisches Mipmapping
- GLU (OpenGL-Hilfsprogramm), automatische Mipmapping
- OpenGL-Hilfsprogramm (GLU), Textur Bilder
- GLU (OpenGL-Hilfsprogramm), Textur Bilder
- Glu-Bibliothek, Textur Bilder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16726493bbcb6e0116e4c158e470029f34f5b652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309795"
---
# <a name="manipulating-images-for-use-in-texturing"></a>Bearbeiten von Bildern für die Verwendung in der Texturierung

Die OpenGL Utility Library (GLU) bietet Bildskalierung und automatische Mipmapping-Funktionen, um die Spezifikation von Textur Bildern zu vereinfachen. Die Funktion " [**gluscaleimage**](gluscaleimage.md) " skaliert ein angegebenes Bild auf eine akzeptierte Textur Größe. Sie können das resultierende Bild als Textur an OpenGL übergeben. Die automatischen Mipmapping-Funktionen, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) und [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), erstellen mipzugeordnete Textur Bilder aus einem angegebenen Bild und übergeben Sie an [**glTexImage1D**](glteximage1d.md) bzw. [**glTexImage2D**](glteximage2d.md).

 

 




