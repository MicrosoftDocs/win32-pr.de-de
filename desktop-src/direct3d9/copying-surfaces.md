---
description: Der Begriff Blit ist eine \# Kurznotiz für &0034, Bitblock Übertragung, &\# 0034. dabei handelt es sich um den Prozess, bei dem Datenblöcke von einem Speicherort im Arbeitsspeicher auf einen anderen übertragen werden.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Kopieren von Oberflächen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344372"
---
# <a name="copying-surfaces-direct3d-9"></a>Kopieren von Oberflächen (Direct3D 9)

Der Begriff Blit ist eine Kurznotiz für "Bitblock Übertragung", bei der es sich um den Prozess der Übertragung von Datenblöcken von einem Speicherort im Arbeitsspeicher auf einen anderen handelt. Die blitinggeräte Treiberschnittstelle (DDI) wird weiterhin in Direct3D 9 als primärer Mechanismus zum Verschieben großer Rechtecke von Pixeln pro Frame verwendet, der Mechanismus hinter der Kopier orientierten [**IDirect3DDevice9::P Resent**](/windows/desktop/api) -Methode. Der Transport von Grafiken im Blit-Vorgang wird von der [**IDirect3DDevice9:: UpdateTexture**](/windows/desktop/api) -Methode durchgeführt. Mithilfe der [**IDirect3DDevice9:: updatesurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) -Methode kann auch das Artwork in Direct3D 9 kopiert werden, das eine rechteckige Teilmenge von Pixeln kopiert.

> [!Note]  
> Direct3D 9 stellt D3DX-Funktionen bereit, mit denen Sie Grafiken aus Dateien laden, Farb Konvertierungen anwenden und die Größe von Grafiken ändern können. Weitere Informationen zu den verfügbaren Funktionen finden Sie unter [Textur Funktionen in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9:: stretchrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

**IDirect3DDevice9:: stretchrect**
</dt> </dl>

 

 
