---
description: Mithilfe von Effekt Zuständen werden Pipeline Zustände als Vorbereitung für die Vertex-und Pixel Verarbeitung initialisiert.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Effekt Zustände (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e208c0c7c14564a9967562ff2fd04a400cb7901
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314763"
---
# <a name="effect-states-direct3d-9"></a>Effekt Zustände (Direct3D 9)

Mithilfe von Effekt Zuständen werden Pipeline Zustände als Vorbereitung für die Vertex-und Pixel Verarbeitung initialisiert.


```
effect state [ [index] ] = expression;
```



Hierbei gilt:

-   Effekt Zustand: vergleichbar mit den herkömmlichen Pipeline Zuständen fester Funktionen. Eine komplette Liste der Zustände finden Sie unten.
-   \[\[ \] Index \] -Optionaler ganzzahliger Index. Der Index identifiziert einen bestimmten Zustand innerhalb eines Arrays von Effekt Zuständen. Die äußeren Klammern zeigen an, dass ein Index optional ist. Wenn ein Index verwendet wird, achten Sie darauf, die inneren Klammern zu verwenden.
-   Ausdrucks Zustands Zuweisungs Ausdruck. Weitere Informationen finden Sie unter [Ausdrücke (Direct3D 9)](expressions.md).

Jeder Status weist einen systemeigenen Datentyp auf. Dies ist der Datentyp, in dem der Zustand Werte erwartet, wenn der Effekt Sie zuweist. Die Datentypen, die von den einzelnen Zuständen erwartet werden, sind unten aufgeführt.

Beachten Sie, dass die Effect-Schnittstelle versucht, Werte so früh wie möglich in den entsprechenden Typ umzuwandeln. Literalwerte können zur Kompilierzeit umgewandelt werden. Nicht Literale (d. h. reguläre Variablen) müssen umgewandelt werden, wenn die entsprechenden Set-Methoden aufgerufen werden. Beispielsweise wandelt die Effect-Schnittstelle Werte um, die bei Bedarf mithilfe von [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md)und anderen ähnlichen Funktionen festgelegt werden. Um eine bessere Leistung zu erzielen, stellen Sie sicher, dass die an die Effekt Schnittstelle über gebenden Werte bereits den richtigen Typ haben und keine Umwandlung benötigen. Wenn die Laufzeit einen Wert nicht umwandeln kann, wird ein Fehler zurückgegeben.

Die Auswirkung der Zustände kann in die folgenden Kategorien unterteilt werden:

-   [Helle Zustände](#light-states)
-   [Material Zustände](#material-states)
-   [Rendering-Zustände](#render-states)
    -   [Pixelpipe-renderzustände](#pixel-pipe-render-states)
    -   [Vertexpipe-Rendering-Zustände](#vertex-pipe-render-states)
-   [Samplerzustände](#sampler-states)
-   [Sampler-Phasen Status](#sampler-stage-states)
-   [Shader-Zustände](#shader-states)
-   [Shader-konstantenzustände](#shader-constant-states)
-   [Textur Zustände](#texture-states)
-   [Textur Stufen Zustände](#texture-stage-states)
-   [Transformations Zustände](#transform-states)

## <a name="light-states"></a>Helle Zustände

Um die beste Leistung für das Anwenden eines Effekts zu ermöglichen, sollten alle Komponenten eines Lichts oder eines Materials in der Effekt Datei angegeben werden. Wenn Sie nicht deklarieren, werden Sie auf einen Standardwert festgelegt, da Direct3D keine Möglichkeit hat, helle Zustände einzeln festzulegen.



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| Heller Zustand            | type   | Werte                                                                                                              |
| Lightambient \[ n\]      | float4 | Siehe Ambient-Member von [**D3DLIGHT9**](d3dlight9.md).                                                           |
| LightAttenuation0 \[ n\] | float  | Weitere Informationen finden Sie unter Attenuation0-Member von [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightAttenuation1 \[ n\] | float  | Weitere Informationen finden Sie unter Attenuation1-Member von [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightAttenuation2 \[ n\] | float  | Weitere Informationen finden Sie unter Attenuation2-Member von [**D3DLIGHT9**](d3dlight9.md).                                                      |
| Lightdiffuse \[ n\]      | float4 | Siehe den diffusen Member von [**D3DLIGHT9**](d3dlight9.md).                                                           |
| Lightdirection \[ n\]    | float3 | Weitere Informationen finden Sie in der Direction-Member von [**D3DLIGHT9**](d3dlight9.md).                                                         |
| Lightenable \[ n\]       | bool   | **True** oder **false**. Siehe das benable-Argument in [**lightenable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).            |
| Lightf-Zuweisung \[ n\]      | float  | [**D3DCOLORVALUE**](d3dcolorvalue.md). Siehe den fzuweisung-Member von [**D3DLIGHT9**](d3dlight9.md).                   |
| Lightphi \[ n\]          | float  | Siehe den Phi-Member von [**D3DLIGHT9**](d3dlight9.md).                                                               |
| Lightposition \[ n\]     | float3 | Siehe Positions Element von [**D3DLIGHT9**](d3dlight9.md).                                                          |
| Lightrange \[ n\]        | float  | Siehe den Range-Member von [**D3DLIGHT9**](d3dlight9.md).                                                             |
| Lightspecarität \[ n\]     | float4 | Weitere Informationen finden Sie unter dem Glanz Element von [**D3DLIGHT9**](d3dlight9.md).                                                          |
| Lighttheita \[ n\]        | float  | Weitere Informationen finden Sie unter der [**D3DLIGHT9**](d3dlight9.md)-Member.                                                             |
| LightType \[ n\]         | dword  | Gleicher Wert wie das Array von bis zu n [**D3DLIGHTTYPE**](./d3dlighttype.md) -Werten ohne das D3DLIGHT- \_ Präfix. |



 

Beispiel:


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



Dadurch wird die Beleuchtung aktiviert, Punktbeleuchtung durch den Typ festgelegt, die helle Position auf float3<10.0 f, 1.0 f, 23,0 f> festgelegt und die Umgebungs Farbe auf float4<0,7 f, 0,0 f, 0,0 f, 1.0 f> festgelegt.

## <a name="material-states"></a>Material Zustände

Wenn Sie nicht deklarieren, werden Sie auf einen Standardwert festgelegt, da Direct3D keine Möglichkeit hat, Materialzustände einzeln festzulegen.



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| Material Zustand   | type   | Werte                                         |
| Optionen materialambient  | float4 | Gleicher Wert wie [ **Ambient**](d3dmaterial9.md)  |
| Material diffuse  | float4 | Gleicher Wert wie [ **diffuses**](d3dmaterial9.md)  |
| MaterialEmissive | float4 | Gleicher Wert wie [ **emissive**](d3dmaterial9.md) |
| Materialpower    | float  | Gleicher Wert wie [ **Power**](d3dmaterial9.md)    |
| MaterialSpecular | float4 | Gleicher [  Wert wie Glanz](d3dmaterial9.md) |



 

Beispiel:


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



Dadurch wird die diffuse Farbe auf float4<0,7 f, 0,0 f, 0,0 f, 1.0 f> festgelegt und die Leistungsfähigkeit der Materialien 3.0 f festgelegt.

## <a name="render-states"></a>Rendering-Zustände

Es gibt zwei Arten von Rendering-Zuständen:

-   [Pixelpipe-renderzustände](#pixel-pipe-render-states)
-   [Vertexpipe-Rendering-Zustände](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a>Pixelpipe-renderzustände

Der Effekt von Datei-gerenderzuständen hat ähnliche Namen wie die Status der Fixed-Funktions Pipeline, häufig wird das Präfix entfernt.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Rendering-Zustand</td>
<td>type</td>
<td>Werte</td>
</tr>
<tr class="even">
<td>AlphaBlendEnable</td>
<td>bool</td>
<td>Richtig oder falsch: Die gleichen Werte wie D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</td>
</tr>
<tr class="odd">
<td>Alphafunc</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> ohne das Präfix D3DCMP_. Siehe D3DRS_ALPHAFUNC.</td>
</tr>
<tr class="even">
<td>Alpha Aref</td>
<td>dword</td>
<td>Die gleichen Werte wie D3DRS_ALPHAREF.</td>
</tr>
<tr class="odd">
<td>Alpha atestenable</td>
<td>dword</td>
<td>Richtig oder falsch: Siehe D3DRS_ALPHATESTENABLE.</td>
</tr>
<tr class="even">
<td>Blendop</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> ohne das Präfix D3DBLENDOP_.</td>
</tr>
<tr class="odd">
<td>Colorschreiteenable</td>
<td>dword</td>
<td>Bitweise Kombination von rot | Grün | Blau | Alpha. Siehe D3DRS_COLORWRITEENABLE.</td>
</tr>
<tr class="even">
<td>Depthbias</td>
<td>float</td>
<td>Die gleichen Werte wie D3DRS_DEPTHBIAS.</td>
</tr>
<tr class="odd">
<td>Destblend</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> ohne das Präfix D3DBLEND_.</td>
</tr>
<tr class="even">
<td>Ditherenable</td>
<td>bool</td>
<td>Richtig oder falsch: Die gleichen Werte wie D3DRS_DITHERENABLE.</td>
</tr>
<tr class="odd">
<td>FillMode</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> ohne das Präfix D3DFILL_.</td>
</tr>
<tr class="even">
<td>Lastpixel</td>
<td>dword</td>
<td>Richtig oder falsch: Siehe D3DRS_LASTPIXEL.</td>
</tr>
<tr class="odd">
<td>SHADEMODE</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> ohne das Präfix D3DSHADE_.</td>
</tr>
<tr class="even">
<td>Slopescaledepthbias</td>
<td>float</td>
<td>Die gleichen Werte wie D3DRS_SLOPESCALEDEPTHBIAS.</td>
</tr>
<tr class="odd">
<td>Srcblend</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> ohne das Präfix D3DBLEND_.</td>
</tr>
<tr class="even">
<td>Srgbschreiteenable</td>
<td>bool</td>
<td>Richtig oder falsch: Die gleichen Werte wie D3DRS_SRGBWRITEENABLE.</td>
</tr>
<tr class="odd">
<td>Schablone möglich</td>
<td>bool</td>
<td>Richtig oder falsch: Die gleichen Werte wie D3DRS_STENCILENABLE.</td>
</tr>
<tr class="even">
<td>Stencilfail</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> ohne das Präfix D3DSTENCILCAP_. Siehe D3DRS_STENCILFAIL.</td>
</tr>
<tr class="odd">
<td>Schablone Func</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> ohne das Präfix D3DCMP_. Siehe D3DRS_STENCILFUNC.</td>
</tr>
<tr class="even">
<td>Schablone Mask</td>
<td>dword</td>
<td>Die gleichen Werte wie D3DRS_STENCILMASK.</td>
</tr>
<tr class="odd">
<td>Schablone-Pass</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> ohne das Präfix D3DSTENCILCAP_. Siehe D3DRS_STENCILPASS.</td>
</tr>
<tr class="even">
<td>Schablone Ref</td>
<td>INT</td>
<td>Die gleichen Werte wie D3DRS_STENCILREF.</td>
</tr>
<tr class="odd">
<td>Schablone</td>
<td>dword</td>
<td>Die gleichen Werte wie D3DRS_STENCILWRITEMASK.</td>
</tr>
<tr class="even">
<td>Stencilzfail</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> ohne das Präfix D3DSTENCILCAP_. Siehe D3DRS_STENCILZFAIL.</td>
</tr>
<tr class="odd">
<td>TextureFactor</td>
<td>dword</td>
<td>Dieselben Werte wie <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>. Die gleichen Werte wie D3DRS_TEXTUREFACTOR.</td>
</tr>
<tr class="even">
<td>Wrap0 - Wrap15</td>
<td>dword</td>
<td>Werte sind identisch mit den Werten, die von D3DRS_WRAP0 verwendet werden. Gültige Werte sind:
<ul>
<li>COORD0 (entspricht D3DWRAPCOORD_0)</li>
<li>COORD1 (entspricht D3DWRAPCOORD_1)</li>
<li>COORD2 (entspricht D3DWRAPCOORD_2)</li>
<li>COORD3 (entspricht D3DWRAPCOORD_3)</li>
<li>U (entspricht D3DWRAP_U)</li>
<li>V (entspricht D3DWRAP_V)</li>
<li>W (entspricht D3DWRAP_W)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zenzierbar</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> ohne das Präfix D3DZB_.</td>
</tr>
<tr class="even">
<td>Zfunc</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> ohne das Präfix D3DCMP_. Siehe D3DRS_ZFUNC.</td>
</tr>
<tr class="odd">
<td>Zbeschreib teenable</td>
<td>bool</td>
<td>Richtig oder falsch: Siehe D3DRS_ZWRITEENABLE.</td>
</tr>
</tbody>
</table>



 

Beispiel:


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



Dadurch wird die Alpha Mischung aktiviert, und alle Geometrien werden im Wireframe dargestellt.

### <a name="vertex-pipe-render-states"></a>Vertexpipe-Rendering-Zustände

Der Effekt von Datei-gerenderzuständen hat ähnliche Namen wie die Status der Fixed-Funktions Pipeline, häufig wird das Präfix entfernt.



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Rendering-Zustand             | type   | Werte                                                                                                                                        |
| Umgebend                  | float4 | Dieselben Werte wie D3DRS \_ AMBIENT.                                                                                                                |
| AmbientMaterialSource    | dword  | Dieselben Werte wie [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) ohne das D3DMCS- \_ Präfix. Weitere Informationen finden Sie unter D3DRS \_ AmbientMaterialSource.  |
| Freistellen                 | bool   | Richtig oder falsch: Die gleichen Werte wie D3DRS \_ Clipping.                                                                                                |
| Clipplaneenable          | dword  | Bitweise Kombination von D3DCLIPPLANE0-D3DCLIPPLANE5-Makros. Weitere Informationen finden Sie unter [**D3DCLIPPLANEn**](d3dclipplanen.md) und D3DRS \_ clipplaneenable.           |
| ColorVertex              | bool   | Richtig oder falsch: Die gleichen Werte wie D3DRS \_ ColorVertex.                                                                                             |
| CullMode                 | dword  | Dieselben Werte wie [**D3DCULL**](./d3dcull.md) ohne das D3DCULL- \_ Präfix.                                                                 |
| DiffuseMaterialSource    | dword  | Dieselben Werte wie [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) ohne das D3DMCS- \_ Präfix. Weitere Informationen finden Sie unter D3DRS \_ DiffuseMaterialSource.  |
| Emissivematerialsource   | dword  | Dieselben Werte wie [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) ohne das D3DMCS- \_ Präfix. Siehe D3DRS \_ emissivematerialsource. |
| Fogcolor                 | dword  | Dieselben Werte wie [**D3DCOLOR**](d3dcolor.md). Siehe D3DRS \_ fogcolor.                                                                             |
| Fogdensity               | float  | Die gleichen Werte wie D3DRS \_ fogdensity.                                                                                                             |
| Fogenable                | bool   | Richtig oder falsch: Die gleichen Werte wie D3DRS \_ fogenable.                                                                                               |
| Fogend                   | float  | Die gleichen Werte wie D3DRS \_ fogend.                                                                                                                 |
| Fogstart                 | float  | Die gleichen Werte wie D3DRS \_ fogstart.                                                                                                               |
| Fogtablemode             | dword  | Dieselben Werte wie [**D3DFOGMODE**](./d3dfogmode.md). Weitere Informationen finden Sie \_ unter D3DRS fogtablemode in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).     |
| Fogvertexmode            | dword  | Dieselben Werte wie [**D3DFOGMODE**](./d3dfogmode.md) ohne das D3DFOG- \_ Präfix.                                                            |
| Indexedvertexblendenable | bool   | Richtig oder falsch: Dieselben Werte wie D3DRS \_ indexedvertexblendenable.                                                                                |
| Beleuchtung                 | bool   | Richtig oder falsch: Die gleichen Werte wie die D3DRS- \_ Beleuchtung.                                                                                                |
| Localviewer              | bool   | Richtig oder falsch: Die gleichen Werte wie D3DRS \_ localviewer.                                                                                             |
| Multisampleantialias     | bool   | Dieselben Werte wie D3DRS \_ multisampleantialias.                                                                                                   |
| Multisamplemask          | dword  | Dieselben Werte wie D3DRS \_ multisamplemask.                                                                                                        |
| Normalizenormals         | bool   | Richtig oder falsch: Dieselben Werte wie D3DRS \_ normalizenormals.                                                                                        |
| Patchsegmente            | float  | Die gleichen Werte wie nsegmente im [**setnpatchmode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).                                                         |
| Pointscale \_ A            | float  | Die gleichen Werte wie D3DRS \_ pointscale \_ A.                                                                                                          |
| Pointscale \_ B            | float  | Dieselben Werte wie D3DRS \_ pointscale \_ B.                                                                                                          |
| Pointscale \_ C            | float  | Dieselben Werte wie D3DRS \_ pointscale \_ C.                                                                                                          |
| Pointscaleenable         | bool   | Dieselben Werte wie D3DRS \_ pointscaleenable.                                                                                                       |
| PointSize                | float  | Die gleichen Werte wie D3DRS \_ pointsize.                                                                                                              |
| Pointsize (min.) \_           | float  | Dieselben Werte wie D3DRS \_ pointsize \_ Min.                                                                                                         |
| Pointsize- \_ Maximalwert           | float  | Die gleichen Werte wie D3DRS \_ pointsize \_ Max ohne das D3DRS- \_ Präfix.                                                                              |
| Pointspriteenable        | bool   | Richtig oder falsch: Dieselben Werte wie D3DRS \_ pointspriteenable.                                                                                       |
| RangeFogEnable           | bool   | Richtig oder falsch: Dieselben Werte wie D3DRS \_ RANGEFOGENABLE.                                                                                          |
| Specularenable           | bool   | Richtig oder falsch: Dieselben Werte wie D3DRS \_ specularenable.                                                                                          |
| SpecularMaterialSource   | dword  | Dieselben Werte wie [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) ohne das D3DMCS- \_ Präfix. Siehe D3DRS \_ SpecularMaterialSource. |
| Tweumfactor              | float  | Dieselben Werte wie D3DRS \_ tweumfactor.                                                                                                            |
| Vertexblend              | dword  | Dieselben Werte wie [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) ohne das D3DVBF- \_ Präfix. Weitere Informationen finden Sie unter D3DRS \_ vertexblend.                  |



 

Beispiel:


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



Dadurch wird die Ambient-Farbe float4<0,7 f, 0,0 f, 0,0 f, 1.0 f>, der Modus für die Hintergrund Erkennung wird gegen den Uhrzeigersinn festgelegt, und die Nebelfarbe wird auf Rot festgelegt.

## <a name="sampler-states"></a>Samplerzustände

Ein samplerzustand stellt ein Sampler-Objekt dar.



|         |         |                                     |
|---------|---------|-------------------------------------|
| State   | type    | Werte                              |
| Sampler | Sammel | **Null** oder ein samplerstatusblock. |



 

## <a name="sampler-stage-states"></a>Sampler-Phasen Status

Samplingstufen Zustände werden zum Beispiel für Texturen verwendet. Der samplerzustand bestimmt Filterungs-und Darstellungsmodi.



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Samplerstatus       | type                         | Werte                                                                                                                            |
| Adresssu \[ 16\]      | dword                        | Dieselben Werte wie [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) ohne das D3DTADDRESS- \_ Präfix. Weitere Informationen finden Sie unter D3DSAMP \_ adressssu.      |
| Adressssv \[ 16\]      | dword                        | Dieselben Werte wie [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) ohne das D3DTADDRESS- \_ Präfix. Siehe D3DSAMP \_ adressssv.      |
| AddressW \[ 16\]      | dword                        | Dieselben Werte wie [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) ohne das D3DTADDRESS- \_ Präfix. Siehe D3DSAMP \_ AddressW.      |
| BorderColor \[ 16\]   | [**D3DCOLOR**](d3dcolor.md) | Dieselben Werte wie [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) ohne das D3DTEXF- \_ Präfix. Siehe D3DSAMP \_ BorderColor. |
| MagFilter \[ 16\]     | dword                        | Dieselben Werte wie [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) ohne das D3DTEXF- \_ Präfix. Siehe D3DSAMP \_ MagFilter.   |
| MaxAnisotropy \[ 16\] | dword                        | Dieselben Werte wie D3DSAMP \_ MaxAnisotropy ohne das D3DSAMP- \_ Präfix.                                                               |
| MaxMipLevel \[ 16\]   | INT                          | Dieselben Werte wie D3DSAMP \_ MaxMipLevel ohne das D3DSAMP- \_ Präfix.                                                                 |
| MinFilter \[ 16\]     | dword                        | Dieselben Werte wie D3DSAMP \_ MinFilter ohne das D3DSAMP- \_ Präfix.                                                                   |
| MipFilter \[ 16\]     | dword                        | Dieselben Werte wie D3DSAMP \_ MipFilter ohne das D3DSAMP- \_ Präfix.                                                                   |
| Mipmaplodbias \[ 16\] | float                        | Dieselben Werte wie D3DSAMP \_ mipmaplodbias ohne das D3DSAMP- \_ Präfix.                                                               |
| Srgbtexture         | bool                         | Gleicher Wert wie D3DSAMP \_ srgbtexture ohne das D3DSAMP- \_ Präfix.                                                                   |



 

Beispiel:


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



Dadurch werden UVW-Werte auf einen Wert zwischen 0 und 1 Klammern.

## <a name="shader-states"></a>Shader-Zustände

Es gibt nur zwei Effekt-shaderzustände: eine, die einem Vertex-Shader-Objekt zugeordnet ist, und die andere, die einem Pixel-Shader-Objekt zugeordnet ist.



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| Shader-Status | type         | Werte                                                                      |
| Pixelshader  | Pixelshader  | **Null**, ein assemblyblock, ein Kompilierungs Ziel oder ein Pixel-Shader-Parameter. |
| Titellink | Titellink | **Null**, ein assemblyblock, ein Kompilierungs Ziel oder ein Pixel-Shader-Parameter. |



 

Beispiel:


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



Hierdurch wird vstexture, ein weiter oben in der FX-Datei definiertes Vertex-Shader, mit der Vertex-Shader-Version 1,1 kompiliert und dann als Vertexshader für den kompilierten Shader festgelegt. Der Pixelshader wird **null** zugewiesen.

## <a name="shader-constant-states"></a>Shader-konstantenzustände

Shaderkonstantenzustände werden verwendet, um auf Shader-Konstante Parameter zuzugreifen.



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| Shader-konstantenzustand | type            | Werte                                       |
| Pixelshaderconstant   | float \[ m \[ n\]\] | m x n Array von Gleit Komma Zahlen; m und n sind optional. |
| PixelShaderConstant1  | float4          | Ein 4D-float-Wert.                                |
| PixelShaderConstant2  | float4x2        | Zwei 4D-Gleit Komma Zahlen.                               |
| PixelShaderConstant3  | float4x3        | Drei 4D-Gleit Komma Zahlen.                             |
| PixelShaderConstant4  | float4x4        | Vier 4D-Gleit Komma Zahlen.                              |
| Pixelshaderconstantb  | Boolescher \[ m \[ n\]\]  | m x n Array von bools; m und n sind optional.  |
| Pixelshaderconstanti  | int \[ m \[ n\]\]   | m x n Array von int. m und n sind optional.   |
| Pixelshaderconstantf  | float \[ m \[ n\]\] | m x n Array von Gleit Komma Zahlen. m und n sind optional. |
| Vertexshaderconstant  | float \[ m \[ n\]\] | m x n Array von Gleit Komma Zahlen. m und n sind optional. |
| VertexShaderConstant1 | float4          | Ein 4D-float-Wert.                                |
| VertexShaderConstant2 | float4x2        | Zwei 4D-Gleit Komma Zahlen.                               |
| VertexShaderConstant3 | float4x3        | Drei 4D-Gleit Komma Zahlen.                             |
| VertexShaderConstant4 | float4x4        | Vier 4D-Gleit Komma Zahlen.                              |
| Vertexshaderconstantb | Boolescher \[ m \[ n\]\]  | m x n Array von bools. m und n sind optional.  |
| Vertexshaderconstanti | int \[ m \[ n\]\]   | m x n Array von int. m und n sind optional.   |
| Vertexshaderconstantf | float \[ m \[ n\]\] | m x n Array von Gleit Komma Zahlen. m und n sind optional. |



 

## <a name="texture-states"></a>Textur Zustände

Textur Zustände initialisieren Texturen, die vom Multitextur-Blender verwendet werden.



|               |         |                                   |
|---------------|---------|-----------------------------------|
| Textur Zustand | type    | Werte                            |
| Textur \[ 8\]  | Struktur | **Null** oder ein Textur Parameter. |



 

## <a name="texture-stage-states"></a>Textur Stufen Zustände

Textur Stufen Zustände richten Texturen und die Textur Stufen im Multitextur-Blender ein.



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Textur Phasen Status        | type  | Werte                                                                                                                                                    |
| Alphaop \[ 8\]               | dword | Identisch mit [**D3DTEXTUREOP**](./d3dtextureop.md) ohne das D3DTOP- \_ Präfix. Siehe D3DTSS \_ alphaop.                                                      |
| AlphaArg0 \[ 8\]             | dword | Identisch mit [D3DTA](d3dta.md) ohne das D3DTA- \_ Präfix. Siehe D3DTSS \_ ALPHAARG0.                                                                             |
| AlphaArg1 \[ 8\]             | dword | Identisch mit [D3DTA](d3dta.md) ohne das D3DTA- \_ Präfix. Siehe D3DTSS \_ ALPHAARG1.                                                                             |
| AlphaArg2 \[ 8\]             | dword | Identisch mit [D3DTA](d3dta.md) ohne das D3DTA- \_ Präfix. Siehe D3DTSS \_ ALPHAARG2.                                                                             |
| ColorArg0 \[ 8\]             | dword | Identisch mit [D3DTA](d3dta.md) ohne das D3DTA- \_ Präfix. Siehe D3DTSS \_ COLORARG0.                                                                             |
| ColorArg1 \[ 8\]             | dword | Identisch mit [D3DTA](d3dta.md) ohne das D3DTA- \_ Präfix. Siehe D3DTSS \_ COLORARG1.                                                                             |
| ColorArg2 \[ 8\]             | dword | Identisch mit [D3DTA](d3dta.md) ohne das D3DTA- \_ Präfix. Siehe D3DTSS \_ COLORARG2.                                                                             |
| Colorop \[ 8\]               | dword | Identisch mit [**D3DTEXTUREOP**](./d3dtextureop.md) ohne das D3DTOP- \_ Präfix. Siehe D3DTSS \_ colorop.                                                      |
| Bumpendvlscale \[ 8\]         | float | Dieselben Werte wie D3DTSS \_ bumpeinvlscale ohne das D3DTSS \_ TCI-Präfix.                                                                                      |
| Bumpenvloffset \[ 8\]        | float | Die gleichen Werte wie D3DTSS \_ bumpenvloffset ohne das D3DTSS \_ TCI-Präfix.                                                                                     |
| BumpEnvMat00 \[ 8\]          | float | Dieselben Werte wie D3DTSS \_ BUMPENVMAT00.                                                                                                                      |
| BumpEnvMat01 \[ 8\]          | float | Dieselben Werte wie D3DTSS \_ BUMPENVMAT01.                                                                                                                      |
| BumpEnvMat10 \[ 8\]          | float | Dieselben Werte wie D3DTSS \_ BUMPENVMAT10.                                                                                                                      |
| BumpEnvMat11 \[ 8\]          | float | Dieselben Werte wie D3DTSS \_ BUMPENVMAT11.                                                                                                                      |
| Resultarg \[ 8\]             | dword | Identisch mit [D3DTA](d3dta.md) ohne das D3DTA- \_ Präfix. Siehe D3DTSS \_ resultarg.                                                                             |
| Texcoordindex \[ 8\]         | dword | Dieselben Werte wie D3DTSS \_ texcoordindex ohne das D3DTSS \_ TCI-Präfix.                                                                                      |
| Texturetransformflags \[ 8\] | dword | Die gleichen Werte wie [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) -Werte ohne das D3DTTFF- \_ Präfix. Weitere Informationen finden Sie unter D3DTSS \_ texturetransformflags. |



 

## <a name="transform-states"></a>Transformations Zustände

Legen Sie Transformations Zustände fest, um Transformations Matrizen zu initialisieren. Effekte verwenden für die Effizienz die Umsetzung von Matrizen. Sie können die bereitgestellten Matrizen für einen Effekt bereitstellen, oder die Matrizen werden von einem Effekt automatisch ausgetauscht, bevor Sie verwendet werden.



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Transformations Status       | type     | Werte                                                                                                                          |
| Projectiontransform   | float4x4 | Eine 4 x 4-Matrix von Gleit Komma Zahlen. Die gleichen Werte wie \_ die D3DTS-Projektion ohne das D3DTS- \_ Präfix.                                            |
| TextureTransform \[ 8\] | float4x4 | Eine 4 x 4-Matrix von Gleit Komma Zahlen. Dieselben Werte wie [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) ohne das D3DTS- \_ Präfix. |
| ViewTransform         | float4x4 | Eine 4 x 4-Matrix von Gleit Komma Zahlen. Die gleichen Werte wie \_ die D3DTS View ohne das D3DTS- \_ Präfix.                                                  |
| Worldtransform        | float4x4 | Eine 4 x 4-Matrix von Gleit Komma Zahlen.                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Format](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
