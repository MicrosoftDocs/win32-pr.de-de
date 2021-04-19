---
description: Ein Zustands Block kann verwendet werden, um nur den Scheitelpunkt Zustand zu erfassen (siehe Status Blöcke speichern und Wiederherstellen (Direct3D 9)).
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: Speichern von Scheitelpunkt Zuständen mit einem stateblock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c6bc7fd291a2609ef60709f05a04fe8d27f8eb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342970"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a>Speichern von Scheitelpunkt Zuständen mit einem stateblock (Direct3D 9)

Ein Zustands Block kann verwendet werden, um nur den Scheitelpunkt Zustand zu erfassen (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)). Der folgende Zustand ist der Scheitelpunkt Status:

-   Vertex-Rendering-Zustand (siehe [vertexpipeline: Rendering State](#vertex-pipeline-render-state)).
-   Vertex-samplerstatus (siehe [Scheitelpunkt Pipeline: samplerzustand](#vertex-pipeline-sampler-state)).
-   Vertextexturzustand (siehe [vertexpipeline: Textur Zustand](#vertex-pipeline-texture-state)).
-   Die npatchmodussegmente aus [**IDirect3DDevice9:: setnpatchmode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).
-   Jedes Licht aus [**IDirect3DDevice9:: setlight**](/windows/desktop/api), und gibt an, ob das Licht mit [**IDirect3DDevice9:: lightenable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)aktiviert ist.
-   Der aktuelle Scheitelpunkt-Shader und jede der Vertex-shaderkonstanten.
-   Speichern Sie für jeden Vertex-Stream den unter Teiler-Wert von [**IDirect3DDevice9:: setstreamsourcefreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Die aktuelle Scheitelpunkt Deklaration.

Um den Scheitelpunkt Zustand mit einem Zustands Block zu erfassen, geben Sie D3DSBT \_ vertexstate beim Aufrufen von [**IDirect3DDevice9:: createstateblock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)an.

## <a name="vertex-pipeline-render-state"></a>Scheitelpunkt Pipeline: Rendering-Status

Renderzustände von Geräten wirken sich auf das Verhalten von fast jedem Teil der Pipeline aus. Renderzustände werden durch Aufrufen von [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)festgelegt.

In der folgenden Tabelle sind alle Rendering-Zustände enthalten, die den Scheitelpunkt Status einrichten:



| Rendering-Zustände                           | Standardwert          |
|-----------------------------------------|------------------------|
| D3DRS \_ CullMode                         | D3DCULL \_ CCW           |
| D3DRS \_ fogcolor                         | 0                      |
| D3DRS \_ fogtablemode                     | D3DFOG \_ None           |
| D3DRS \_ fogstart                         | 0                      |
| D3DRS \_ fogend                           | 1                      |
| D3DRS- \_ fogdensity                       | 1                      |
| D3DRS \_ RANGEFOGENABLE                   | **FALSE**              |
| D3DRS \_ AMBIENT                          | 0                      |
| D3DRS \_ ColorVertex                      | **TRUE**               |
| D3DRS \_ fogvertexmode                    | D3DFOG \_ None           |
| D3DRS \_ Clipping                         | **TRUE**               |
| D3DRS- \_ Beleuchtung                         | **TRUE**               |
| D3DRS \_ localviewer                      | **TRUE**               |
| D3DRS \_ emissivematerialsource           | D3DMCS \_ Material       |
| D3DRS \_ AmbientMaterialSource            | D3DMCS \_ Material       |
| D3DRS \_ DiffuseMaterialSource            | D3DMCS \_ COLOR1         |
| D3DRS \_ SpecularMaterialSource           | D3DMCS \_ COLOR2         |
| D3DRS \_ vertexblend                      | D3DVBF \_ Deaktivieren        |
| D3DRS \_ clipplaneenable                  | 0                      |
| D3DRS \_ pointsize                        | Treiber abhängig       |
| D3DRS \_ pointsize \_ Min                   | 1                      |
| D3DRS \_ pointspriteenable                | **FALSE**              |
| D3DRS \_ pointscaleenable                 | **FALSE**              |
| D3DRS \_ pointscale \_ A                    | 1                      |
| D3DRS \_ pointscale \_ B                    | 0                      |
| D3DRS \_ pointscale \_ C                    | 0                      |
| D3DRS \_ multisampleantialias             | **TRUE**               |
| D3DRS \_ multisamplemask                  | 0xFFFFFFFF             |
| D3DRS \_ patchedgestyle                   | D3DPATCHEDGE \_ diskret |
| D3DRS \_ pointsize \_ Max                   | 1                      |
| D3DRS \_ indexedvertexblendenable         | **FALSE**              |
| D3DRS \_ tweumfactor                      | 0                      |
| D3DRS \_ positiondegree                   | D3DDEGREE \_ kubisch       |
| D3DRS \_ normaldegree                     | D3DDEGREE \_ linear      |
| D3DRS \_ mintmeellationlevel             | 1                      |
| D3DRS \_ maxtmeellationlevel             | 1                      |
| D3DRS \_ adaptivetess \_ X                  | 0                      |
| D3DRS \_ adaptivetess \_ Y                  | 0                      |
| D3DRS \_ adaptivetess \_ Z                  | 1                      |
| D3DRS \_ adaptivetess \_ W                  | 0                      |
| D3DRS \_ enableadaptivetess-"/> | **FALSE**              |



 

## <a name="vertex-pipeline-sampler-state"></a>Scheitelpunkt Pipeline: samplerstatus

Samplerzustände Steuern samplingbezogene Themen, wie z. b. das Filtern, das ticken und den textemodi Verwenden Sie [**IDirect3DDevice9:: setsamplerstate, um den samplerzustand**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) einzurichten (einschließlich der in der Mosaik Einheit zum Beispiel für Verschiebungs Zuordnungen verwendeten). Die samplerzustände wurden mit dem \_ Präfix "D3DSAMP" umbenannt, um die Kompilierzeit-Fehlererkennung beim Portieren aus DirectX 8 zu aktivieren.

In der folgenden Tabelle sind alle samplerzustände enthalten, die den Scheitelpunkt Status einrichten:



| Samplerzustände      | Standardwert |
|---------------------|---------------|
| D3DSAMP \_ dmapoffset | 256           |



 

## <a name="vertex-pipeline-texture-state"></a>Scheitelpunkt Pipeline: Textur Zustand

Textur Zustände steuern Textur Mischungs Vorgänge des Multitextur-Blender. Verwenden Sie [**IDirect3DDevice9:: settexturestagestate**](/windows/desktop/api) zum Einrichten von Textur Zuständen. Verwenden Sie [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) , um eine Textur einer Samplingphase zuzuordnen.

In der folgenden Tabelle sind alle Textur Zustände enthalten, die den Scheitelpunkt Status einrichten:



| Textur Zustände                | Standardwert    |
|-------------------------------|------------------|
| D3DTSS \_ texcoordindex         | 0                |
| D3DTSS \_ texturetransformflags | D3DTTFF \_ Deaktivieren |



 

D3DTSS \_ texcoordindex ist ein Status der Vertex-Verarbeitung fester Funktionen. Wenn ein programmierbarer Vertex-Shader verwendet wird, wird dieser Zustand ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Status Blöcke speichern und Wiederherstellen](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
