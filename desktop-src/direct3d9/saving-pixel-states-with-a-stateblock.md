---
description: Ein Zustandsblock kann verwendet werden, um nur den Pixelzustand zu erfassen (siehe Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9)).
ms.assetid: 30624c0a-e30f-4383-bc0c-b43f42403e72
title: Speichern des Pixelzustands mit einem StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebc7cc408fe919b1569d51f5cdd4e3e5916968d05b90557a17a22377673fdfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797917"
---
# <a name="saving-pixel-state-with-a-stateblock-direct3d-9"></a>Speichern des Pixelzustands mit einem StateBlock (Direct3D 9)

Ein Zustandsblock kann verwendet werden, um nur den Pixelzustand zu erfassen (siehe [Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9)](state-blocks-save-and-restore-state.md)). Der folgende Zustand ist der Pixelzustand:

-   Pixelrenderzustand (siehe [Pixelpipeline: Renderzustand](#pixel-pipeline-render-state)).
-   Pixeltexturzustand (siehe [Pixelpipeline: Texturzustand](#pixel-pipeline-texture-state)).
-   Pixel-Samplerzustand (siehe [Pixelpipeline: Samplerzustand](#pixel-pipeline-sampler-state)).
-   Der aktuelle Pixelshader und jede der Pixelshaderkonstanten.

Um den Pixelzustand mit einem Zustandsblock zu erfassen, geben Sie D3DSBT \_ PIXELSTATE beim Aufrufen von [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)an.

## <a name="pixel-pipeline-render-state"></a>Pixelpipeline: Renderzustand

Geräterenderingzustände wirken sich auf das Verhalten von fast jedem Teil der Pipeline aus. Renderzustände werden durch Aufrufen von [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)festgelegt.

Die folgende Tabelle enthält alle Renderzustände, die den Pixelzustand einrichten:



| Renderzustände                              | Standardwert      |
|--------------------------------------------|--------------------|
| D3DRS \_ ZENABLE                             | D3D \_ FALSE       |
| D3DRS \_ SPECULARENABLE                      | **FALSE**          |
| [**D3DFILLMODE**](./d3dfillmode.md)   | D3DFILL \_ SOLID     |
| [**D3DSHADEMODE**](./d3dshademode.md) | D3DSHADE \_ GOURAUD  |
| D3DRS \_ ZWRITEENABLE                        | **TRUE**           |
| D3DRS \_ ALPHATESTENABLE                     | **FALSE**          |
| D3DRS \_ LASTPIXEL                           | **TRUE**           |
| D3DRS \_ SRCBLEND                            | D3DBLEND \_ ONE      |
| D3DRS \_ DESTBLEND                           | D3DBLEND \_ ZERO     |
| \_D3DRS–MARKEUNC                               | D3DCMP \_ LESSEQUAL  |
| D3DRS \_ ALPHAREF                            | 0                  |
| D3DRS \_ ALPHAFUNC                           | D3DCMP \_ ALWAYS     |
| D3DRS \_ DITHERENABLE                        | **FALSE**          |
| D3DRS- \_ UND -START                            | 0                  |
| D3DRS- \_ UND -END                              | 1                  |
| \_D3DRS-EMPFINDLICHKEIT                          | 1                  |
| D3DRS \_ ALPHABLENDENABLE                    | **FALSE**          |
| D3DRS \_ DEPTHBIAS                           | 0                  |
| D3DRS \_ STENCILENABLE                       | **FALSE**          |
| D3DRS \_ STENCILFAIL                         | D3DSTENCILOP \_ KEEP |
| D3DRS \_ STENCILZFAIL                        | D3DSTENCILOP \_ KEEP |
| D3DRS \_ STENCILPASS                         | D3DSTENCILOP \_ KEEP |
| D3DRS \_ STENCILFUNC                         | D3DCMP \_ ALWAYS     |
| D3DRS \_ STENCILREF                          | 0                  |
| D3DRS \_ STENCILMASK                         | 0xffffffff         |
| D3DRS \_ STENCILWRITEMASK                    | 0xffffffff         |
| D3DRS \_ TEXTUREFACTOR                       | 0xffffffff         |
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
| D3DRS \_ LOCALVIEWER                         | **TRUE**           |
| D3DRS \_ EMISSIVEMATERIALSOURCE              | D3DMCS \_ MATERIAL   |
| D3DRS \_ AMBIENTMATERIALSOURCE               | D3DMCS \_ MATERIAL   |
| D3DRS \_ DIFFUSEMATERIALSOURCE               | D3DMCS \_ COLOR1     |
| D3DRS \_ SPECULARMATERIALSOURCE              | D3DMCS \_ COLOR2     |
| D3DRS \_ COLORWRITEENABLE                    | 0x0000000f         |
| [**D3DBLENDOP**](./d3dblendop.md)     | D3DBLENDOP \_ ADD    |
| D3DRS \_ SCISSORTESTENABLE                   | **FALSE**          |
| D3DRS \_ IM 3DRS-REGLERCALEDEPTHBIAS                 | 0                  |
| D3DRS \_ ANTIALIASEDLINEENABLE               | **FALSE**          |
| D3DRS \_ TWOSIDEDSTENCILMODE                 | **FALSE**          |
| D3DRS \_ CCW \_ STENCILFAIL                    | D3DSTENCILOP \_ KEEP |
| D3DRS \_ CCW \_ STENCILZFAIL                   | D3DSTENCILOP \_ KEEP |
| D3DRS \_ CCW \_ STENCILPASS                    | D3DSTENCILOP \_ KEEP |
| D3DRS \_ CCW \_ STENCILFUNC                    | D3DCMP \_ ALWAYS     |
| D3DRS \_ COLORWRITEENABLE1                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE2                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE3                   | 0x0000000f         |
| D3DRS \_ BLENDFACTOR                         | 0xffffffff         |
| D3DRS \_ SRGBWRITEENABLE                     | 0                  |
| D3DRS \_ SEPARATEALPHABLENDENABLE            | **FALSE**          |
| D3DRS \_ SRCBLENDALPHA                       | D3DBLEND \_ ONE      |
| D3DRS \_ DESTBLENDALPHA                      | D3DBLEND \_ ZERO     |
| D3DRS \_ BLENDOPALPHA                        | D3DBLENDOP \_ ADD    |



 

## <a name="pixel-pipeline-sampler-state"></a>Pixelpipeline: Samplerzustand

Samplerzustände steuern Themen im Zusammenhang mit der Stichprobenentnahme, z. B. Filterung, Kacheln und Adressmodi für Texturkoordinaten. Verwenden Sie [**IDirect3DDevice9::SetSamplerState,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) um den Samplerzustand einzurichten (einschließlich des Zustands, der in der Mosaikeinheit verwendet wird, um Verschiebungszuordnungen zu untersuchen). Die Samplerzustände wurden mit dem Präfix "D3DSAMP" \_ umbenannt, um die Erkennung von Kompilierzeitfehlern beim Portieren von DirectX 8 zu ermöglichen.

Die folgende Tabelle enthält alle Samplerzustände, die den Pixelzustand einrichten:



| Samplerzustände         | Standardwert     |
|------------------------|-------------------|
| D3DSAMP \_ ADDRESSU      | D3DTADDRESS \_ WRAP |
| D3DSAMP \_ ADDRESSV      | D3DTADDRESS \_ WRAP |
| D3DSAMP \_ ADDRESSW      | D3DTADDRESS \_ WRAP |
| D3DSAMP \_ BORDERCOLOR   | 0x00000000        |
| D3DSAMP \_ MAGFILTER     | D3DTEXF \_ POINT    |
| D3DSAMP \_ MINFILTER     | D3DTEXF \_ POINT    |
| D3DSAMP \_ MIPFILTER     | D3DTEXF \_ NONE     |
| D3DSAMP \_ MIPMAPLODBIAS | 0                 |
| D3DSAMP \_ MAXMIPLEVEL   | 0                 |
| D3DSAMP \_ MAXANISOTROPY | 1                 |
| D3DSAMP \_ SRGBTEXTURE   | 0                 |
| D3DSAMP \_ ELEMENTINDEX  | 0                 |



 

## <a name="pixel-pipeline-texture-state"></a>Pixelpipeline: Texturzustand

Texturzustände steuern Texturmischungsvorgänge des Multitexturblenders. Verwenden Sie [**IDirect3DDevice9::SetTextureStageState,**](/windows/desktop/api) um Texturphasenzustände einzurichten. Verwenden Sie [**IDirect3DDevice9::SetTexture,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) um eine Textur einer Samplerphase zuzuordnen.

Die folgende Tabelle enthält alle Texturzustände, die den Pixelzustand einrichten:



| Texturzustände                | Standardwert    |
|-------------------------------|------------------|
| D3DTSS \_ COLOROP               | D3DTOP \_ DISABLE  |
| D3DTSS \_ COLORARG1             | D3DTA \_ TEXTURE   |
| D3DTSS \_ COLORARG2             | D3DTA \_ CURRENT   |
| D3DTSS \_ ALPHAOP               | D3DTOP \_ DISABLE  |
| D3DTSS \_ ALPHAARG1             | D3DTA \_ TEXTURE   |
| D3DTSS \_ ALPHAARG2             | D3DTA \_ CURRENT   |
| D3DTSS \_ BUMPENVMAT00          | 0                |
| D3DTSS \_ BUMPENVMAT01          | 0                |
| D3DTSS \_ BUMPENVMAT10          | 0                |
| D3DTSS \_ BUMPENVMAT11          | 0                |
| D3DTSS \_ TEXCOORDINDEX         | 0                |
| D3DTSS \_ BUMPENVLSCALE         | 0                |
| D3DTSS \_ BUMPENVLOFFSET        | 0                |
| D3DTSS \_ TEXTURETRANSFORMFLAGS | D3DTTFF \_ DISABLE |
| D3DTSS \_ COLORARG0             | D3DTA \_ CURRENT   |
| D3DTSS \_ ALPHAARG0             | D3DTA \_ CURRENT   |
| D3DTSS \_ RESULTARG             | D3DTA \_ CURRENT   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zustandsblöcke Speichern und Wiederherstellen des Zustands](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
