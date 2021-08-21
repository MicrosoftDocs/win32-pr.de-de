---
description: Der Begriff blit ist eine Kurzform für &\# 0034;Bitblockübertragung,&0034; d. h. \# das Übertragen von Datenblöcken von einer Stelle im Arbeitsspeicher an eine andere.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Kopieren von Oberflächen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d31d897bcb9e1a8fefa45a7770959ecb4121f807e4ca51d26ca7da5b5f5f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123377"
---
# <a name="copying-surfaces-direct3d-9"></a>Kopieren von Oberflächen (Direct3D 9)

Der Begriff BLIT ist die Kurzform für "Bitblockübertragung". Dabei handelt es sich um den Prozess der Übertragung von Datenblöcken von einer Stelle im Arbeitsspeicher an eine andere. Die Blitting device driver interface (DDI) wird weiterhin in Direct3D 9 als primärer Mechanismus zum Verschieben großer Rechtecke von Pixeln pro Frame verwendet, dem Mechanismus hinter der kopierorientierten [**IDirect3DDevice9::P resent-Methode.**](/windows/desktop/api) Der Transport von Grafiken im BLIT-Vorgang wird von der [**IDirect3DDevice9::UpdateTexture-Methode**](/windows/desktop/api) ausgeführt. Grafiken können auch in Direct3D 9 mithilfe der [**IDirect3DDevice9::UpdateSurface-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) kopiert werden, die eine rechteckige Teilmenge von Pixeln kopiert.

> [!Note]  
> Direct3D 9 bietet D3DX-Funktionen, mit denen Sie Grafiken aus Dateien laden, Farbkonvertierungen anwenden und die Größe von Grafiken ändern können. Weitere Informationen zu den verfügbaren Funktionen finden Sie unter [Texturfunktionen in D3DX 9.](dx9-graphics-reference-d3dx-functions-texture.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

**IDirect3DDevice9::StretchRect**
</dt> </dl>

 

 
