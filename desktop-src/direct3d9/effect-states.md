---
description: Effektzustände werden verwendet, um Pipelinezustände als Vorbereitung für die Scheitelpunkt- und Pixelverarbeitung zu initialisieren.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Effektzustände (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb7b00362520ed67203f5adf84f6c420e1e16fcb34dc741d2f3fdd303a2152d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986010"
---
# <a name="effect-states-direct3d-9"></a>Effektzustände (Direct3D 9)

Effektzustände werden verwendet, um Pipelinezustände als Vorbereitung für die Scheitelpunkt- und Pixelverarbeitung zu initialisieren.


```
effect state [ [index] ] = expression;
```



Hierbei gilt:

-   effect state: Ähnelt den herkömmlichen festen Funktionspipelinezuständen. Eine vollständige Liste der Zustände finden Sie unten.
-   \[\[ \] Index \] – Optionaler ganzzahliger Index. Der Index identifiziert einen bestimmten Zustand innerhalb eines Arrays von Effektzuständen. Die äußeren Klammern geben an, dass ein Index optional ist. Wenn ein Index verwendet wird, achten Sie darauf, die inneren Klammern zu verwenden.
-   expression: Zustandszuweisungsausdruck. Siehe [Ausdrücke (Direct3D 9).](expressions.md)

Jeder Zustand verfügt über einen nativen Datentyp. Dies ist der Datentyp, von dem der Zustand erwartet, dass werte in sind, wenn sie durch den Effekt zugewiesen werden. Die Datentypen, die von den einzelnen Bundesstaaten erwartet werden, sind unten aufgeführt.

Beachten Sie, dass die Effektschnittstelle versucht, Werte so früh wie möglich in den entsprechenden Typ zu casten. Literalwerte können zur Kompilierzeit castt werden. Nichtliterale (d. h. reguläre Variablen) müssen beim Aufgerufenen der entsprechenden Set-Methoden castiert werden. Beispielsweise werden von der Effektschnittstelle werte, die mit [**SetBool,**](id3dxbaseeffect--setbool.md) [**SetValue und**](id3dxbaseeffect--setvalue.md)anderen ähnlichen Funktionen festgelegt wurden, bei Bedarf um. Stellen Sie für eine bessere Leistung sicher, dass die an die Effektschnittstelle übergebenen Werte bereits den richtigen Typ haben und keine Umwandlung benötigen. Wenn die Runtime einen Wert nicht casten kann, wird ein Fehler zurückgegeben.

Auswirkungszustände können in die folgenden Kategorien unterteilt werden:

-   [Lichtzustände](#light-states)
-   [Materialzustände](#material-states)
-   [Renderzustände](#render-states)
    -   [Renderzustände der Pixelpipe](#pixel-pipe-render-states)
    -   [Vertexpipe-Renderzustände](#vertex-pipe-render-states)
-   [Samplerzustände](#sampler-states)
-   [Sampler-Phasenzustände](#sampler-stage-states)
-   [Shaderzustände](#shader-states)
-   [Shader-Konstantenzustände](#shader-constant-states)
-   [Texturzustände](#texture-states)
-   [Texturphasenzustände](#texture-stage-states)
-   [Transformationszustände](#transform-states)

## <a name="light-states"></a>Lichtzustände

Um die beste Leistung für das Anwenden eines Effekts zu erzielen, sollten alle Komponenten eines Lichts oder eines Materials in der Effektdatei angegeben werden. Zustände, die Sie nicht deklarieren können, werden auf einen Standardwert festgelegt, da Direct3D keine Möglichkeit hat, lichte Zustände einzeln zu setzen.



| Lichtzustand            | type   | Werte                                                                                                              |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| LightAmbient \[ n\]      | float4 | Weitere Informationen finden Sie im Ambient-Member [**von D3DLIGHT9.**](d3dlight9.md)                                                           |
| LightAttenuation0 \[ n\] | float  | Weitere Informationen finden Sie unter dem Attenuation0-Member von [**D3DLIGHT9.**](d3dlight9.md)                                                      |
| LightAttenuation1 \[ n\] | float  | Siehe attenuation1 member of D3DLIGHT9 (Attenuation1-Member [**von D3DLIGHT9).**](d3dlight9.md)                                                      |
| LightAttenuation2 \[ n\] | float  | Weitere Informationen finden Sie unter dem Attenuation2-Member von [**D3DLIGHT9.**](d3dlight9.md)                                                      |
| LightDiffuse \[ n\]      | float4 | Siehe diffuse Member von [**D3DLIGHT9.**](d3dlight9.md)                                                           |
| LightDirection \[ n\]    | float3 | Weitere Informationen finden Sie unter dem Direction-Member [**von D3DLIGHT9.**](d3dlight9.md)                                                         |
| LightEnable \[ n\]       | bool   | **TRUE** oder **FALSE**. Weitere Informationen finden Sie unter dem bEnable-Argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).            |
| LightFalloff \[ n\]      | float  | [**D3DCOLORVALUE**](d3dcolorvalue.md). Weitere Informationen finden Sie unter dem Falloff-Member [**von D3DLIGHT9.**](d3dlight9.md)                   |
| LightPhi \[ n\]          | float  | Weitere Informationen finden Sie unter dem Phi-Member [**von D3DLIGHT9.**](d3dlight9.md)                                                               |
| LightPosition \[ n\]     | float3 | Weitere Informationen finden Sie unter Dem Position-Member [**von D3DLIGHT9.**](d3dlight9.md)                                                          |
| LightRange \[ n\]        | float  | Weitere Informationen finden Sie unter Range member of [**D3DLIGHT9 (Range-Member von D3DLIGHT9).**](d3dlight9.md)                                                             |
| LightSpecular \[ n\]     | float4 | Siehe specular member of D3DLIGHT9 (Specular-Member [**von D3DLIGHT9).**](d3dlight9.md)                                                          |
| LightTheta \[ n\]        | float  | Weitere Informationen finden Sie im Theta-Member [**von D3DLIGHT9.**](d3dlight9.md)                                                             |
| LightType \[ n\]         | dword  | Der gleiche Wert wie das Array von bis zu n [**D3DLIGHTTYPE-Werten**](./d3dlighttype.md) ohne das Präfix D3DLIGHT. \_ |



 

Beispiel:


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



Dies ermöglicht die Beleuchtung, die Punktbeleuchtung des Typs, die Lichtposition auf float3<10.0f, 1.0f, 23.0f> und die Umgebungsfarbe auf float4<0,7f, 0,0f, 0,0f, 1,0f>.

## <a name="material-states"></a>Materialzustände

Zustände, die Sie nicht deklarieren können, werden auf einen Standardwert festgelegt, da Direct3D keine Möglichkeit hat, Materialzustände einzeln festlegen zu können.



| Materialstatus   | type   | Werte                                         |
|------------------|--------|------------------------------------------------|
| MaterialAmbient  | float4 | Identischer Wert wie [ **Ambient**](d3dmaterial9.md)  |
| MaterialDiffuse  | float4 | Identischer Wert wie [ **Diffuse**](d3dmaterial9.md)  |
| MaterialEmissive | float4 | Identischer Wert [ **wie Fürssive**](d3dmaterial9.md) |
| MaterialPower    | float  | Identischer Wert wie [ **Power**](d3dmaterial9.md)    |
| MaterialSpecular | float4 | Identischer Wert wie [ **Specular**](d3dmaterial9.md) |



 

Beispiel:


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



Dadurch wird die diffuse Farbe auf float4<0,7f, 0,0f, 0,0f, 1,0f> festgelegt und die Leistung des Materials auf 3,0f festgelegt.

## <a name="render-states"></a>Renderzustände

Es gibt zwei Arten von Renderzuständen:

-   [Renderzustände der Pixelpipe](#pixel-pipe-render-states)
-   [Vertexpipe-Renderzustände](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a>Renderzustände der Pixelpipe

Renderzustände von Effect-Dateien haben Namen, die den festen Funktionspipelinezuständen ähneln, häufig mit entferntem Präfix.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Renderzustand</td>
<td>type</td>
<td>Werte</td>
</tr>
<tr class="even">
<td>AlphaBlendEnable</td>
<td>bool</td>
<td>Richtig oder falsch. Die gleichen Werte wie D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</td>
</tr>
<tr class="odd">
<td>AlphaFunc</td>
<td>dword</td>
<td>Identische Werte <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>wie D3DCMPFUNC</strong></a> ohne D3DCMP_ Präfix. Siehe D3DRS_ALPHAFUNC.</td>
</tr>
<tr class="even">
<td>AlphaRef</td>
<td>dword</td>
<td>Die gleichen Werte wie D3DRS_ALPHAREF.</td>
</tr>
<tr class="odd">
<td>AlphaTestEnable</td>
<td>dword</td>
<td>Richtig oder falsch. Siehe D3DRS_ALPHATESTENABLE.</td>
</tr>
<tr class="even">
<td>BlendOp</td>
<td>dword</td>
<td>Identische Werte <a href="/windows/desktop/direct3d9/d3dblendop"><strong>wie D3DBLENDOP</strong></a> ohne D3DBLENDOP_ Präfix.</td>
</tr>
<tr class="odd">
<td>ColorWriteEnable</td>
<td>dword</td>
<td>Bitweise Kombination von RED| GREEN| BLUE| Alpha. Siehe D3DRS_COLORWRITEENABLE.</td>
</tr>
<tr class="even">
<td>DepthBias</td>
<td>float</td>
<td>Die gleichen Werte wie D3DRS_DEPTHBIAS.</td>
</tr>
<tr class="odd">
<td>DestBlend</td>
<td>dword</td>
<td>Identische Werte <a href="/windows/desktop/direct3d9/d3dblend"><strong>wie D3DBLEND</strong></a> ohne D3DBLEND_ Präfix.</td>
</tr>
<tr class="even">
<td>DitherEnable</td>
<td>bool</td>
<td>Richtig oder falsch. Die gleichen Werte wie D3DRS_DITHERENABLE.</td>
</tr>
<tr class="odd">
<td>Fillmode</td>
<td>dword</td>
<td>Identische Werte <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>wie D3DFILLMODE</strong></a> ohne D3DFILL_ Präfix.</td>
</tr>
<tr class="even">
<td>LastPixel</td>
<td>dword</td>
<td>Richtig oder falsch. Siehe D3DRS_LASTPIXEL.</td>
</tr>
<tr class="odd">
<td>ShadeMode</td>
<td>dword</td>
<td>Identische Werte <a href="/windows/desktop/direct3d9/d3dshademode"><strong>wie D3DSHADEMODE</strong></a> ohne D3DSHADE_ Präfix.</td>
</tr>
<tr class="even">
<td>SlopeScaleDepthBias</td>
<td>float</td>
<td>Die gleichen Werte wie D3DRS_SLOPESCALEDEPTHBIAS.</td>
</tr>
<tr class="odd">
<td>SrcBlend</td>
<td>dword</td>
<td>Identische Werte <a href="/windows/desktop/direct3d9/d3dblend"><strong>wie D3DBLEND</strong></a> ohne D3DBLEND_ Präfix.</td>
</tr>
<tr class="even">
<td>SRGBWriteEnable</td>
<td>bool</td>
<td>Richtig oder falsch. Die gleichen Werte wie D3DRS_SRGBWRITEENABLE.</td>
</tr>
<tr class="odd">
<td>StencilEnable</td>
<td>bool</td>
<td>Richtig oder falsch. Die gleichen Werte wie D3DRS_STENCILENABLE.</td>
</tr>
<tr class="even">
<td>StencilFail</td>
<td>dword</td>
<td>Dieselben Werte wie <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> ohne D3DSTENCILCAP_ Präfix. Siehe D3DRS_STENCILFAIL.</td>
</tr>
<tr class="odd">
<td>StencilFunc</td>
<td>dword</td>
<td>Identische Werte <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>wie D3DCMPFUNC</strong></a> ohne D3DCMP_ Präfix. Siehe D3DRS_STENCILFUNC.</td>
</tr>
<tr class="even">
<td>Schablonenmaske</td>
<td>dword</td>
<td>Die gleichen Werte wie D3DRS_STENCILMASK.</td>
</tr>
<tr class="odd">
<td>StencilPass</td>
<td>dword</td>
<td>Dieselben Werte wie <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> ohne D3DSTENCILCAP_ Präfix. Siehe D3DRS_STENCILPASS.</td>
</tr>
<tr class="even">
<td>StencilRef</td>
<td>INT</td>
<td>Die gleichen Werte wie D3DRS_STENCILREF.</td>
</tr>
<tr class="odd">
<td>StencilWriteMask</td>
<td>dword</td>
<td>Die gleichen Werte wie D3DRS_STENCILWRITEMASK.</td>
</tr>
<tr class="even">
<td>StencilZFail</td>
<td>dword</td>
<td>Dieselben Werte wie <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> ohne D3DSTENCILCAP_ Präfix. Siehe D3DRS_STENCILZFAIL.</td>
</tr>
<tr class="odd">
<td>TextureFactor</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="d3dcolor.md"><strong>D3DCOLOR.</strong></a> Die gleichen Werte wie D3DRS_TEXTUREFACTOR.</td>
</tr>
<tr class="even">
<td>Wrap0 – Wrap15</td>
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
<td>ZEnable</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DSILUFFERTYPE</strong></a> ohne das präfix D3DZB_.</td>
</tr>
<tr class="even">
<td>ZFunc</td>
<td>dword</td>
<td>Die gleichen Werte wie <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> ohne das präfix D3DCMP_. Weitere Informationen finden Sie unter D3DRS_ZFUNC.</td>
</tr>
<tr class="odd">
<td>ZWriteEnable</td>
<td>bool</td>
<td>Richtig oder falsch. Siehe D3DRS_ZWRITEENABLE.</td>
</tr>
</tbody>
</table>



 

Beispiel:


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



Dadurch wird die Alphamischung aktiviert, und alle Geometrien werden in Wireframe gerendert.

### <a name="vertex-pipe-render-states"></a>Vertexpipe-Renderzustände

Effect-Dateirenderzustände weisen Namen auf, die den festen Funktionspipelinezuständen ähneln, wobei das Präfix häufig entfernt wird.



| Renderzustand             | type   | Werte                                                                                                                                        |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Umgebend                  | float4 | Die gleichen Werte wie D3DRS \_ AMBIENT.                                                                                                                |
| AmbientMaterialSource    | dword  | Die gleichen Werte wie [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) ohne das \_ D3DMCS-Präfix. Weitere Informationen finden Sie unter D3DRS \_ AMBIENTMATERIALSOURCE.  |
| Freistellen                 | bool   | Richtig oder falsch. Die gleichen Werte wie D3DRS \_ CLIPPING.                                                                                                |
| ClipPlaneEnable          | dword  | Bitweise Kombination von D3DCLIPPLANE0 – D3DCLIPPLANE5-Makros. Weitere Informationen finden Sie unter [**D3DCLIPPLANEn**](d3dclipplanen.md) und D3DRS \_ CLIPPLANEENABLE.           |
| ColorVertex              | bool   | Richtig oder falsch. Die gleichen Werte wie D3DRS \_ COLORVERTEX.                                                                                             |
| CullMode                 | dword  | Die gleichen Werte wie [**D3DCULL**](./d3dcull.md) ohne das \_ Präfix D3DCULL.                                                                 |
| DiffuseMaterialSource    | dword  | Die gleichen Werte wie [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) ohne das \_ D3DMCS-Präfix. Siehe D3DRS \_ DIFFUSEMATERIALSOURCE.  |
| EmissiveMaterialSource   | dword  | Die gleichen Werte wie [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) ohne das \_ D3DMCS-Präfix. Siehe D3DRS \_ EMISSIVEMATERIALSOURCE. |
| ColorColor                 | dword  | Die gleichen Werte wie [**D3DCOLOR.**](d3dcolor.md) Weitere Informationen finden Sie unter \_ D3DRSCOLOR.                                                                             |
| Überdungsalität               | float  | Die gleichen Werte wie D3DRS- \_ UND -WERTE.                                                                                                             |
| Aufsträhbar                | bool   | Richtig oder falsch. Die gleichen Werte wie D3DRS, \_ DIE VERWERTBAR sind.                                                                                               |
| Dies ist ein vordinges                   | float  | Identische Werte wie D3DRS \_ MSIEND.                                                                                                                 |
| Überlaufstart                 | float  | Die gleichen Werte wie D3DRS, \_ DANNSTART.                                                                                                               |
| StandbyTableMode             | dword  | Die gleichen Werte wie [**D3DFOGMODE.**](./d3dfogmode.md) Weitere Informationen finden Sie unter D3DRSTABLEMODE \_ in [**D3DRENDERSTATETYPE.**](./d3drenderstatetype.md)     |
| TexVertexMode            | dword  | Die gleichen Werte wie [**D3DFOGMODE**](./d3dfogmode.md) ohne das \_ D3DFOG-Präfix.                                                            |
| IndexedVertexBlendEnable | bool   | Richtig oder falsch. Die gleichen Werte wie D3DRS \_ INDEXEDVERTEXBLENDENABLE.                                                                                |
| Beleuchtung                 | bool   | Richtig oder falsch. Die gleichen Werte wie D3DRS \_ LIGHTING.                                                                                                |
| LocalViewer              | bool   | Richtig oder falsch. Die gleichen Werte wie D3DRS \_ LOCALVIEWER.                                                                                             |
| MultiSampleAntialias     | bool   | Identische Werte wie D3DRS \_ MULTISAMPLEANTIALIAS.                                                                                                   |
| MultiSampleMask          | dword  | Identische Werte wie D3DRS \_ MULTISAMPLEMASK.                                                                                                        |
| NormalizeNormals         | bool   | Richtig oder falsch. Identische Werte wie D3DRS \_ NORMALIZENORMALS.                                                                                        |
| PatchSegments            | float  | Die gleichen Werte wie nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).                                                         |
| PointScale \_ A            | float  | Identische Werte wie D3DRS \_ POINTSCALE \_ A.                                                                                                          |
| PointScale \_ B            | float  | Identische Werte wie D3DRS \_ POINTSCALE \_ B.                                                                                                          |
| PointScale \_ C            | float  | Identische Werte wie D3DRS \_ POINTSCALE \_ C.                                                                                                          |
| PointScaleEnable         | bool   | Identische Werte wie D3DRS \_ POINTSCALEENABLE.                                                                                                       |
| PointSize                | float  | Dieselben Werte wie D3DRS \_ POINTSIZE.                                                                                                              |
| PointSize \_ Min           | float  | Identische Werte wie D3DRS \_ POINTSIZE \_ MIN.                                                                                                         |
| PointSize \_ Max           | float  | Dieselben Werte wie D3DRS \_ POINTSIZE \_ MAX ohne das D3DRS-Präfix. \_                                                                              |
| PointSpriteEnable        | bool   | Richtig oder falsch. Identische Werte wie D3DRS \_ POINTSPRITEENABLE.                                                                                       |
| RangeFogEnable           | bool   | Richtig oder falsch. Identische Werte wie D3DRS \_ RANGEFOGENABLE.                                                                                          |
| SpecularEnable           | bool   | Richtig oder falsch. Identische Werte wie D3DRS \_ SPECULARENABLE.                                                                                          |
| SpecularMaterialSource   | dword  | Dieselben Werte wie [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) ohne das Präfix D3DMCS. \_ Siehe D3DRS \_ SPECULARMATERIALSOURCE. |
| TweenFactor              | float  | Identische Werte wie D3DRS \_ TWEENFACTOR.                                                                                                            |
| VertexBlend              | dword  | Dieselben Werte wie [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) ohne das Präfix D3DVBF. \_ Siehe D3DRS \_ VERTEXBLEND.                  |



 

Beispiel:


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



Dadurch wird die Umgebungsfarbe float4<0,7f, 0,0f, 0,0f, 1,0f>, der Hinterface-Cullingmodus auf gegen den Uhrzeigersinn festgelegt und die Farbfarbe auf Rot festgelegt.

## <a name="sampler-states"></a>Samplerzustände

Ein Samplerzustand stellt ein Samplerobjekt dar.



| State   | type    | Werte                              |
|---------|---------|-------------------------------------|
| Sampler | Sampler | **NULL** oder ein Samplerzustandsblock. |



 

## <a name="sampler-stage-states"></a>Sampler-Phasenzustände

Sampler-Phasenzustände werden verwendet, um Texturen zu beproben. Der Zustand des Samplers bestimmt Filtertypen und Textur-Adressierungsmodi.



| Samplerzustand       | type                         | Werte                                                                                                                            |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| AddressU \[ 16\]      | dword                        | Identische Werte [**wie D3DTEXTUREADDRESS ohne**](./d3dtextureaddress.md) das Präfix D3DTADDRESS. \_ Siehe D3DSAMP \_ ADDRESSU.      |
| AddressV \[ 16\]      | dword                        | Identische Werte [**wie D3DTEXTUREADDRESS ohne**](./d3dtextureaddress.md) das Präfix D3DTADDRESS. \_ Siehe D3DSAMP \_ ADDRESSV.      |
| AddressW \[ 16\]      | dword                        | Identische Werte [**wie D3DTEXTUREADDRESS ohne**](./d3dtextureaddress.md) das Präfix D3DTADDRESS. \_ Siehe D3DSAMP \_ ADDRESSW.      |
| BorderColor \[ 16\]   | [**D3DCOLOR**](d3dcolor.md) | Dieselben Werte wie [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) ohne das Präfix D3DTEXF. \_ Siehe D3DSAMP \_ BORDERCOLOR. |
| MagFilter \[ 16\]     | dword                        | Dieselben Werte wie [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) ohne das Präfix D3DTEXF. \_ Siehe D3DSAMP \_ MAGFILTER.   |
| MaxAnisotropie \[ 16\] | dword                        | Identische Werte wie D3DSAMP \_ MAXANISOTROPY ohne das Präfix D3DSAMP. \_                                                               |
| MaxMipLevel \[ 16\]   | INT                          | Identische Werte wie D3DSAMP \_ MAXMIPLEVEL ohne das Präfix D3DSAMP. \_                                                                 |
| MinFilter \[ 16\]     | dword                        | Dieselben Werte wie D3DSAMP \_ MINFILTER ohne das Präfix D3DSAMP. \_                                                                   |
| MipFilter \[ 16\]     | dword                        | Identische Werte wie D3DSAMP \_ MIPFILTER ohne das Präfix D3DSAMP. \_                                                                   |
| MipMapLodBias \[ 16\] | float                        | Identische Werte wie D3DSAMP \_ MIPMAPLODBIAS ohne das Präfix D3DSAMP. \_                                                               |
| SRGBTexture         | bool                         | Der gleiche Wert wie D3DSAMP \_ SRGBTEXTURE ohne das Präfix D3DSAMP. \_                                                                   |



 

Beispiel:


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



Dies klammert UVW-Werte auf einen Wert zwischen 0 und 1.

## <a name="shader-states"></a>Shaderzustände

Es gibt nur zwei Effekt-Shaderzustände: einen, der einem Vertex-Shaderobjekt zugeordnet ist, und den anderen, der einem Pixel-Shaderobjekt zugeordnet ist.



| Shaderzustand | type         | Werte                                                                      |
|--------------|--------------|-----------------------------------------------------------------------------|
| Pixelshader  | Pixelshader  | **NULL,** ein Assemblyblock, ein Kompilierungsziel oder ein Shaderparameter für Pixel. |
| VertexShader | vertexshader | **NULL,** ein Assemblyblock, ein Kompilierungsziel oder ein Shaderparameter für Pixel. |



 

Beispiel:


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



Dadurch wird VSTexture, ein vertex-Shader, der zuvor in der FX-Datei definiert wurde, in die Vertex-Shaderversion 1.1 kompiliert und diesen kompilierten Shader dann als Vertex-Shader festgelegt. Der Pixel-Shader ist NULL **zugewiesen.**

## <a name="shader-constant-states"></a>Shader-Konstantenzustände

Shader-Konstantenzustände werden verwendet, um auf shader-Konstantenparameter zu zugreifen.



| Shaderkonst konstanter Zustand | type            | Werte                                       |
|-----------------------|-----------------|----------------------------------------------|
| PixelShaderConstant   | float \[ m \[ n\]\] | m x n Array von floats; m und n sind optional. |
| PixelShaderConstant1  | float4          | Ein 4D-Gleitkomma.                                |
| PixelShaderConstant2  | float4x2        | Zwei 4D-Gleitkommakomma-                               |
| PixelShaderConstant3  | float4x3        | Drei 4D-Gleitkommakomma-                             |
| PixelShaderConstant4  | float4x4        | Vier 4D-Gleitkommakomma-                              |
| PixelShaderConstantB  | bool \[ m \[ n\]\]  | m x n array of bools; m und n sind optional.  |
| PixelShaderConstantI  | int \[ m \[ n\]\]   | m x n Array von Ints. m und n sind optional.   |
| PixelShaderConstantF  | float \[ m \[ n\]\] | m x n Array von Floats. m und n sind optional. |
| VertexShaderConstant  | float \[ m \[ n\]\] | m x n Array von Floats. m und n sind optional. |
| VertexShaderConstant1 | float4          | Ein 4D-Gleitkomma.                                |
| VertexShaderConstant2 | float4x2        | Zwei 4D-Gleitkommakomma-                               |
| VertexShaderConstant3 | float4x3        | Drei 4D-Gleitkommakomma-                             |
| VertexShaderConstant4 | float4x4        | Vier 4D-Gleitkommakomma-                              |
| VertexShaderConstantB | bool \[ m \[ n\]\]  | m x n-Array mit booleschen Daten. m und n sind optional.  |
| VertexShaderConstantI | int \[ m \[ n\]\]   | m x n Array von Ints. m und n sind optional.   |
| VertexShaderConstantF | float \[ m \[ n\]\] | m x n Array von Floats. m und n sind optional. |



 

## <a name="texture-states"></a>Texturzustände

Texturzustände initialisieren Texturen, die vom Multitexture-Blender verwendet werden.



| Texturzustand | type    | Werte                            |
|---------------|---------|-----------------------------------|
| Textur \[ 8\]  | Struktur | **NULL** oder ein Texturparameter. |



 

## <a name="texture-stage-states"></a>Texturphasenzustände

Texturphasenzustände richten Texturen und die Texturstufen im Multitexture-Blender ein.



| Texturphasenzustand        | type  | Werte                                                                                                                                                    |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlphaOp \[ 8\]               | dword | Identisch mit [**D3DTEXTUREOP**](./d3dtextureop.md) ohne das Präfix D3DTOP. \_ Siehe D3DTSS \_ ALPHAOP.                                                      |
| AlphaArg0 \[ 8\]             | dword | Entspricht [D3DTA](d3dta.md) ohne das D3DTA-Präfix. \_ Siehe D3DTSS \_ ALPHAARG0.                                                                             |
| AlphaArg1 \[ 8\]             | dword | Entspricht [D3DTA](d3dta.md) ohne das D3DTA-Präfix. \_ Siehe D3DTSS \_ ALPHAARG1.                                                                             |
| AlphaArg2 \[ 8\]             | dword | Entspricht [D3DTA](d3dta.md) ohne das D3DTA-Präfix. \_ Siehe D3DTSS \_ ALPHAARG2.                                                                             |
| ColorArg0 \[ 8\]             | dword | Entspricht [D3DTA](d3dta.md) ohne das D3DTA-Präfix. \_ Siehe D3DTSS \_ COLORARG0.                                                                             |
| ColorArg1 \[ 8\]             | dword | Entspricht [D3DTA](d3dta.md) ohne das D3DTA-Präfix. \_ Siehe D3DTSS \_ COLORARG1.                                                                             |
| ColorArg2 \[ 8\]             | dword | Entspricht [D3DTA](d3dta.md) ohne das D3DTA-Präfix. \_ Siehe D3DTSS \_ COLORARG2.                                                                             |
| ColorOp \[ 8\]               | dword | Entspricht [**D3DTEXTUREOP**](./d3dtextureop.md) ohne das \_ Präfix D3DTOP. Weitere Informationen finden Sie unter D3DTSS \_ COLOROP.                                                      |
| BumpEnvLScale \[ 8\]         | float | Die gleichen Werte wie D3DTSS \_ BUMPENVLSCALE ohne das \_ TCI-Präfix D3DTSS.                                                                                      |
| BumpEnvLOffset \[ 8\]        | float | Die gleichen Werte wie D3DTSS \_ BUMPENVLOFFSET ohne das \_ TCI-Präfix D3DTSS.                                                                                     |
| BumpEnvMat00 \[ 8\]          | float | Die gleichen Werte wie D3DTSS \_ BUMPENVMAT00.                                                                                                                      |
| BumpEnvMat01 \[ 8\]          | float | Die gleichen Werte wie D3DTSS \_ BUMPENVMAT01.                                                                                                                      |
| BumpEnvMat10 \[ 8\]          | float | Die gleichen Werte wie D3DTSS \_ BUMPENVMAT10.                                                                                                                      |
| BumpEnvMat11 \[ 8\]          | float | Die gleichen Werte wie D3DTSS \_ BUMPENVMAT11.                                                                                                                      |
| ResultArg \[ 8\]             | dword | Entspricht [D3DTA](d3dta.md) ohne das D3DTA-Präfix. \_ Siehe D3DTSS \_ RESULTARG.                                                                             |
| TexCoordIndex \[ 8\]         | dword | Die gleichen Werte wie D3DTSS \_ TEXCOORDINDEX ohne das \_ TCI-Präfix D3DTSS.                                                                                      |
| TextureTransformFlags \[ 8\] | dword | Die gleichen Werte wie [**D3DTEXTURETRANSFORMFLAGS-Werte**](./d3dtexturetransformflags.md) ohne das \_ D3DTTFF-Präfix. Siehe D3DTSS \_ TEXTURETRANSFORMFLAGS. |



 

## <a name="transform-states"></a>Transformationszustände

Legen Sie Transformationszustände fest, um Transformationsmatrizen zu initialisieren. Effekte verwenden transponierte Matrizen zur Effizienz. Sie können transponierte Matrizen für einen Effekt bereitstellen, oder ein Effekt transponiert die Matrizen automatisch, bevor sie verwendet werden.



| Zustand transformieren       | type     | Werte                                                                                                                          |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| ProjectionTransform   | float4x4 | Eine 4x4-Matrix von Gleitkomma- Die gleichen Werte wie D3DTS \_ PROJECTION ohne das \_ D3DTS-Präfix.                                            |
| TextureTransform \[ 8\] | float4x4 | Eine 4x4-Matrix von Gleitkomma- Die gleichen Werte wie [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) ohne das \_ D3DTS-Präfix. |
| ViewTransform         | float4x4 | Eine 4x4-Matrix von Gleitkomma- Die gleichen Werte wie D3DTS \_ VIEW ohne das D3DTS-Präfix. \_                                                  |
| WorldTransform        | float4x4 | Eine 4x4-Matrix von Gleitkomma-                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektformat](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
