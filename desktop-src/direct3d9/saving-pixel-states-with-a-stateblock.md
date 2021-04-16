---
description: Ein Zustands Block kann verwendet werden, um nur den Pixel Zustand zu erfassen (siehe Status Blöcke speichern und Wiederherstellen (Direct3D 9)).
ms.assetid: 30624c0a-e30f-4383-bc0c-b43f42403e72
title: Speichern des Pixel Zustands mit einem stateblock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80741d9f17939d5795163a3e84c58bcdb9003c70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522387"
---
# <a name="saving-pixel-state-with-a-stateblock-direct3d-9"></a>Speichern des Pixel Zustands mit einem stateblock (Direct3D 9)

Ein Zustands Block kann verwendet werden, um nur den Pixel Zustand zu erfassen (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)). Der folgende Zustand ist Pixel Status:

-   Pixelrenderzustand (siehe [Pixel Pipeline: renderzustand](#pixel-pipeline-render-state)).
-   Pixel Textur Zustand (siehe [Pixel Pipeline: Textur Zustand](#pixel-pipeline-texture-state)).
-   Status des Pixel Samplers (siehe [Pixel Pipeline: samplerstatus](#pixel-pipeline-sampler-state)).
-   Der aktuelle Pixelshader und jede der Pixel-Shader-Konstanten.

Um den Pixel Zustand mit einem Zustands Block zu erfassen, geben Sie D3DSBT \_ pixelstate beim Aufrufen von [**IDirect3DDevice9:: createstateblock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)an.

## <a name="pixel-pipeline-render-state"></a>Pixel Pipeline: renderzustand

Renderzustände von Geräten wirken sich auf das Verhalten von fast jedem Teil der Pipeline aus. Renderzustände werden durch Aufrufen von [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)festgelegt.

In der folgenden Tabelle sind alle renderzustände enthalten, die den Pixel Status einrichten:



| Rendering-Zustände                              | Standardwert      |
|--------------------------------------------|--------------------|
| D3DRS \_ zenable                             | D3DZB \_ false       |
| D3DRS \_ specularenable                      | **FALSE**          |
| [**D3DFILLMODE**](./d3dfillmode.md)   | D3DFILL \_ Solid     |
| [**D3DSHADEMODE**](./d3dshademode.md) | D3DSHADE- \_ Gouraud  |
| D3DRS \_ zbeschreib teenable                        | **TRUE**           |
| D3DRS \_ Alpha atestenable                     | **FALSE**          |
| D3DRS \_ lastpixel                           | **TRUE**           |
| D3DRS \_ srcblend                            | D3DBLEND \_      |
| D3DRS \_ destblend                           | D3DBLEND \_ 0     |
| D3DRS \_ zfunc                               | D3DCMP \_ lessequal  |
| D3DRS \_ Alpha Aref                            | 0                  |
| D3DRS \_ alphafunc                           | D3DCMP \_ immer     |
| D3DRS \_ ditherenable                        | **FALSE**          |
| D3DRS \_ fogstart                            | 0                  |
| D3DRS \_ fogend                              | 1                  |
| D3DRS- \_ fogdensity                          | 1                  |
| D3DRS \_ AlphaBlendEnable                    | **FALSE**          |
| D3DRS \_ depthbias                           | 0                  |
| D3DRS \_ Schablone                       | **FALSE**          |
| D3DRS \_ stencilfail                         | D3DSTENCILOP \_ beibehalten |
| D3DRS \_ stencilzfail                        | D3DSTENCILOP \_ beibehalten |
| D3DRS \_ stencilpass                         | D3DSTENCILOP \_ beibehalten |
| D3DRS \_ stencilfunc                         | D3DCMP \_ immer     |
| D3DRS \_ stencilref                          | 0                  |
| D3DRS \_ stencilmask                         | 0xFFFFFFFF         |
| D3DRS \_ stencilschreitefrage                    | 0xFFFFFFFF         |
| D3DRS \_ TextureFactor                       | 0xFFFFFFFF         |
| D3DRS \_ WRAP0                               | 0                  |
| D3DRS \_ WRAP1                               | 0                  |
| D3DRS \_ WRAP2                               | 0                  |
| D3DRS \_ WRAP3                               | 0                  |
| D3DRS \_ WRAP4                               | 0                  |
| D3DRS \_ WRAP5                               | 0                  |
| D3DRS \_ WRAP6                               | 0                  |
| D3DRS \_ WRAP7                               | 0                  |
| D3DRS \_ WRAP8                               | 0                  |
| D3DRS \_ WRAP9                               | 0                  |
| D3DRS \_ WRAP10                              | 0                  |
| D3DRS \_ WRAP11                              | 0                  |
| D3DRS \_ WRAP12                              | 0                  |
| D3DRS \_ WRAP13                              | 0                  |
| D3DRS \_ WRAP14                              | 0                  |
| D3DRS \_ WRAP15                              | 0                  |
| D3DRS \_ localviewer                         | **TRUE**           |
| D3DRS \_ emissivematerialsource              | D3DMCS \_ Material   |
| D3DRS \_ AmbientMaterialSource               | D3DMCS \_ Material   |
| D3DRS \_ DiffuseMaterialSource               | D3DMCS \_ COLOR1     |
| D3DRS \_ SpecularMaterialSource              | D3DMCS \_ COLOR2     |
| D3DRS \_ colorschreiteenable                    | 0x0000000f         |
| [**D3DBLENDOP**](./d3dblendop.md)     | D3DBLENDOP \_ Hinzufügen    |
| D3DRS \_ scissortestenable                   | **FALSE**          |
| D3DRS \_ slopescaledepthbias                 | 0                  |
| D3DRS \_ antialiasedlineenable               | **FALSE**          |
| D3DRS \_ twosidedstencilmode                 | **FALSE**          |
| D3DRS \_ CCW \_ stencilfail                    | D3DSTENCILOP \_ beibehalten |
| D3DRS \_ CCW \_ stencilzfail                   | D3DSTENCILOP \_ beibehalten |
| D3DRS \_ CCW \_ stencilpass                    | D3DSTENCILOP \_ beibehalten |
| D3DRS \_ CCW \_ stencilfunc                    | D3DCMP \_ immer     |
| D3DRS \_ COLORWRITEENABLE1                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE2                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE3                   | 0x0000000f         |
| D3DRS \_ blendfactor                         | 0xFFFFFFFF         |
| D3DRS \_ srgbschreiteenable                     | 0                  |
| D3DRS \_ separatealphablendenable            | **FALSE**          |
| D3DRS \_ srcblendalpha                       | D3DBLEND \_      |
| D3DRS \_ destblendalpha                      | D3DBLEND \_ 0     |
| D3DRS \_ blendopalpha                        | D3DBLENDOP \_ Hinzufügen    |



 

## <a name="pixel-pipeline-sampler-state"></a>Pixel Pipeline: samplerstatus

Samplerzustände Steuern samplingbezogene Themen, wie z. b. das Filtern, das ticken und den textemodi Verwenden Sie [**IDirect3DDevice9:: setsamplerstate, um den samplerzustand**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) einzurichten (einschließlich der in der Mosaik Einheit zum Beispiel für Verschiebungs Zuordnungen verwendeten). Die samplerzustände wurden mit dem \_ Präfix "D3DSAMP" umbenannt, um die Kompilierzeit-Fehlererkennung beim Portieren aus DirectX 8 zu aktivieren.

In der folgenden Tabelle sind alle samplerzustände enthalten, die den Pixel Status einrichten:



| Samplerzustände         | Standardwert     |
|------------------------|-------------------|
| D3DSAMP \_ adressu      | D3DTADDRESS \_ Wrap |
| D3DSAMP \_ adressssv      | D3DTADDRESS \_ Wrap |
| D3DSAMP \_ AddressW      | D3DTADDRESS \_ Wrap |
| D3DSAMP \_ BorderColor   | 0x00000000        |
| D3DSAMP- \_ MagFilter     | D3DTEXF \_ Punkt    |
| D3DSAMP \_ MinFilter     | D3DTEXF \_ Punkt    |
| D3DSAMP \_ MipFilter     | D3DTEXF \_ None     |
| D3DSAMP \_ mipmaplodbias | 0                 |
| D3DSAMP \_ MaxMipLevel   | 0                 |
| D3DSAMP \_ MaxAnisotropy | 1                 |
| D3DSAMP \_ srgbtexture   | 0                 |
| D3DSAMP \_ Elementindex  | 0                 |



 

## <a name="pixel-pipeline-texture-state"></a>Pixel Pipeline: Textur Zustand

Textur Zustände steuern Textur Mischungs Vorgänge des Multitextur-Blender. Verwenden Sie [**IDirect3DDevice9:: settexturestagestate**](/windows/desktop/api) zum Einrichten von Textur Stufen Zuständen. Verwenden Sie [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) , um eine Textur einer Samplingphase zuzuordnen.

In der folgenden Tabelle sind alle Textur Zustände enthalten, die den Pixel Status einrichten:



| Textur Zustände                | Standardwert    |
|-------------------------------|------------------|
| D3DTSS \_ colorop               | D3DTOP \_ Deaktivieren  |
| D3DTSS \_ COLORARG1             | D3DTA- \_ Textur   |
| D3DTSS \_ COLORARG2             | D3DTA \_ aktuell   |
| D3DTSS \_ alphaop               | D3DTOP \_ Deaktivieren  |
| D3DTSS \_ ALPHAARG1             | D3DTA- \_ Textur   |
| D3DTSS \_ ALPHAARG2             | D3DTA \_ aktuell   |
| D3DTSS \_ BUMPENVMAT00          | 0                |
| D3DTSS \_ BUMPENVMAT01          | 0                |
| D3DTSS \_ BUMPENVMAT10          | 0                |
| D3DTSS \_ BUMPENVMAT11          | 0                |
| D3DTSS \_ texcoordindex         | 0                |
| D3DTSS \_ bumpendvlscale         | 0                |
| D3DTSS \_ bumpenvloffset        | 0                |
| D3DTSS \_ texturetransformflags | D3DTTFF \_ Deaktivieren |
| D3DTSS \_ COLORARG0             | D3DTA \_ aktuell   |
| D3DTSS \_ ALPHAARG0             | D3DTA \_ aktuell   |
| D3DTSS \_ resultarg             | D3DTA \_ aktuell   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Status Blöcke speichern und Wiederherstellen](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
