---
title: Bearbeiten von Bildern zur Verwendung in der Texturierung
description: Die OpenGL Utility Library (GLU) bietet Bildskalierung und automatische mipmapping-Funktionen, um die Spezifikation von Texturbildern zu vereinfachen.
ms.assetid: 20edf665-1fed-4761-b8b1-beee02c78b0d
keywords:
- OpenGL Utility (GLU), Imageskalierung
- GLU (OpenGL Utility), Imageskalierung
- OpenGL Utility (GLU),automatische Mipmapping
- GLU (OpenGL Utility), automatische Mipmapping
- OpenGL Utility (GLU), Texturbilder
- GLU (OpenGL Utility), Texturbilder
- GLU-Bibliothek, Texturbilder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dbe948dc3dbe84c9c2e89e02a43b45cf22d34af0198e422a883afd8f3384606
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553910"
---
# <a name="manipulating-images-for-use-in-texturing"></a>Bearbeiten von Bildern zur Verwendung in der Texturierung

Die OpenGL Utility Library (GLU) bietet Bildskalierung und automatische mipmapping-Funktionen, um die Spezifikation von Texturbildern zu vereinfachen. Die [**funktion gluScaleImage**](gluscaleimage.md) skaliert ein angegebenes Bild auf eine akzeptierte Texturgröße. Sie können das resultierende Bild als Textur an OpenGL übergeben. Die automatischen mipmapping-Funktionen [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) und [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)erstellen mipmapped-Texturbilder aus einem angegebenen Bild und übergeben sie an [**glTexImage1D**](glteximage1d.md) bzw. [**glTexImage2D.**](glteximage2d.md)

 

 




