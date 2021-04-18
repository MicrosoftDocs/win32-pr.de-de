---
title: Legen Sie den Gerätestatus für die Funktion "Shader" fest.
description: Dieser Abschnitt enthält die wichtigsten Unterschiede zwischen dem Festlegen des Geräte Zustands mit der Fixed-und der programmierbaren shaderpipeline.
ms.assetid: FF0F2A97-F75A-4AF0-8F5A-EA687523E753
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2d5c0e0ba9e1ac890468654d348b0f8b316f64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104214009"
---
# <a name="set-device-state-on-fixed-function-shader-pipelines"></a>Legen Sie den Gerätestatus für die Funktion "Shader" fest.

Dieser Abschnitt enthält die wichtigsten Unterschiede zwischen dem Festlegen des Geräte Zustands mit der Fixed-und der programmierbaren shaderpipeline.

Im folgenden sind die Gerätezustände aufgeführt, die Sie für eine Pipeline mit fester Funktionseinheit festlegen können:

-   Transform und Lighting der Fixed-Funktion [**: IDirect3DDevice9:: strenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) mit D3DRS \_ SHADEMODE, D3DRS \_ specularenable, D3DRS \_ Beleuchtung, D3DRS \_ AMBIENT, D3DRS \_ ColorVertex, D3DRS \_ localviewer, D3DRS \_ normalizenormals, D3DRS \_ DiffuseMaterialSource, D3DRS \_ SpecularMaterialSource, D3DRS \_ AmbientMaterialSource, D3DRS \_ emissivematerialsource, D3DRS \_ vertexblend, D3DRS \_ indexedvertexblendenable, D3DRS \_ tweenfactor, [**IDirect3DDevice9:: lightenable**](/windows/desktop/api), [**IDirect3DDevice9:: MultiplyTransform**](/windows/desktop/api), [**IDirect3DDevice9:: setfvf**](/windows/desktop/api), [**IDirect3DDevice9:: setlight**](/windows/desktop/api), [**IDirect3DDevice9:: setmaterial**](/windows/desktop/api), [**IDirect3DDevice9:: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
-   Fixed-Function Pixel Shader: [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) mit D3DRS \_ TextureFactor, [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
-   Nebel: [**IDirect3DDevice9:: strenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) mit D3DRS \_ fogenable, D3DRS \_ fogcolor, D3DRS \_ fogtablemode, D3DRS \_ fogstart, D3DRS \_ fogend, D3DRS \_ fogdensity, D3DRS \_ RANGEFOGENABLE, D3DRS \_ fogvertexmode

Im folgenden finden Sie die Geräte-renderzustände, die Sie mit [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) für sowohl eine Funktion mit fester Funktion als auch programmierbare Shader-Pipelines festlegen können:

-   Renderzielstatus: D3DRS \_ colorschreiteenable, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2, D3DRS \_ COLORWRITEENABLE3, D3DRS \_ srgbschreiteenable
-   Tiefen Status: D3DRS \_ zenable, D3DRS \_ zwrite teenable, D3DRS \_ zfunc, D3DRS \_ slopescaledepthbias, D3DRS \_ depthbias
-   Status der Schablone: D3DRS \_ stencilenable, D3DRS \_ stencilfail, D3DRS \_ stencilzfail, D3DRS \_ stencilpass, D3DRS \_ stencilfunc, D3DRS \_ stencilref, D3DRS \_ stencilmask, D3DRS \_ stencilschreitemask, D3DRS \_ twosidedstencilmode, D3DRS \_ CCW \_ stencilfail, D3DRS \_ CCW \_ stencilzfail, D3DRS \_ CCW \_ stencilpass, D3DRS \_ CCW \_ stencilfunc
-   Alpha Blending: D3DRS \_ srcblend, D3DRS \_ destblend, D3DRS \_ blendop, D3DRS \_ blendfactor, D3DRS \_ separatealphablendenable, D3DRS \_ srcblendalpha, D3DRS \_ destblendalpha, D3DRS \_ blendopalpha
-   Alpha Test: D3DRS \_ Alpha atestenable, D3DRS \_ Alpha Aref, D3DRS \_ alphafunc
-   Status des Rasterizers: D3DRS \_ FillMode, D3DRS \_ lastpixel, D3DRS \_ ditherenable (16-Bit-Oberflächen)
-   Cullinger: D3DRS \_ CullMode
-   Clipping: D3DRS \_ Clipping, D3DRS \_ clipplaneenable
-   Schere: D3DRS \_ scissortestenable
-   Textur Samplers: D3DRS \_ WRAP0, D3DRS \_ WRAP1, D3DRS \_ WRAP2, D3DRS \_ WRAP3, D3DRS \_ WRAP4, D3DRS \_ WRAP5, D3DRS \_ WRAP6, D3DRS \_ WRAP7, D3DRS \_ WRAP8, D3DRS \_ WRAP9, D3DRS \_ WRAP10, D3DRS \_ WRAP11, D3DRS \_ WRAP12, D3DRS \_ WRAP13, D3DRS \_ WRAP14, D3DRS \_ WRAP15
-   Antialiasing: D3DRS \_ multisampleantialias, D3DRS \_ multisamplemask, D3DRS \_ antialiasedlineenable
-   Punkt Sprites: D3DRS \_ pointsize, D3DRS \_ pointsize \_ Min, D3DRS \_ pointspriteenable, D3DRS \_ pointsize \_ MAXD3DRS \_ pointscaleenable, D3DRS \_ pointscale \_ A, D3DRS \_ pointscale \_ B, D3DRS \_ pointscale \_ C
-   N-Patches: D3DRS \_ patchedgestyle, D3DRS \_ positiondegree, D3DRS \_ normaldegree, D3DRS \_ mintessellationlevel, D3DRS \_ maxtessellationlevel, D3DRS \_ adaptivetess \_ X, D3DRS \_ adaptivetess \_ Y, D3DRS \_ adaptivetess \_ Z, D3DRS \_ adaptivetess \_ W, D3DRS \_ enableadaptivetessellation

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Themen](advanced-topics.md)
</dt> </dl>

 

 
