---
description: Verschiedene primitive Treiberfunktionsflags.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ace0b9070d158769e22e02a759545b1bf7785
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343135"
---
# <a name="d3dpmisccaps"></a>D3DPMISCCAPS

Verschiedene primitive Treiberfunktionsflags.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definieren</td>
<td>Wert</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MASKZ</td>
<td>0x00000002L</td>
<td>Das Gerät kann die Änderung des Tiefenpuffers bei Pixelvorgängen aktivieren und deaktivieren.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLNONE</td>
<td>0x00000010L</td>
<td>Der Treiber führt kein Dreiecksculling aus. Dies entspricht dem D3DCULL_NONE Member des <a href="/windows/desktop/direct3d9/d3dcull"><strong>aufzählten D3DCULL-Typs.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CULLCW</td>
<td>0x00000020L</td>
<td>Der Treiber unterstützt im Uhrzeigersinn dreiecksweises Culling durch D3DRS_CULLMODE Zustand. (Dies gilt nur für Dreiecksprimitive.) Dieses Flag entspricht dem D3DCULL_CW Member des <a href="/windows/desktop/direct3d9/d3dcull"><strong>aufzählten D3DCULL-Typs.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLCCW</td>
<td>0x00000040L</td>
<td>Der Treiber unterstützt gegen den Uhrzeigersinn Culling durch den D3DRS_CULLMODE Zustand. (Dies gilt nur für Dreiecksprimitive.) Dieses Flag entspricht dem D3DCULL_CCW des <a href="/windows/desktop/direct3d9/d3dcull"><strong>aufzählten D3DCULL-Typs.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_COLORWRITEENABLE</td>
<td>0x00000100L</td>
<td>Das Gerät unterstützt kanalspezifische Schreibvorgänge für den Renderzielfarbpuffer über den D3DRS_COLORWRITEENABLE Zustand.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</td>
<td>0x00000200L</td>
<td>Das Gerät klammern skalierte Punkte mit einer Größe von mehr als 1,0 ordnungsgemäß in benutzerdefinierte Clippingebenen ein.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CLIPTLVERTS</td>
<td>0x00000200L</td>
<td>Geräteclips nachtransformationsbasierte Scheitelpunktprimitiven. Geben Sie D3DUSAGE_DONOTCLIP an, wenn die Pipeline keinen Clipping durchführen soll. In diesem Fall müssen möglicherweise zusätzliche Softwareclips zur Zeichnenzeit ausgeführt werden, sodass sich der Scheitelpunktpuffer im Systemspeicher befindet.<br/></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_TSSARGTEMP</td>
<td>0x00000400L</td>
<td>Das Gerät unterstützt <a href="d3dta.md">D3DTA</a> für die temporäre Registrierung.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_BLENDOP</td>
<td>0x00000800L</td>
<td>Das Gerät unterstützt andere Alphamischungsvorgänge als D3DBLENDOP_ADD.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_NULLREFERENCE</td>
<td>0x00000100L</td>
<td>Ein Verweisgerät, das nicht gerendert wird.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_INDEPENDENTWRITEMASKS</td>
<td>0x00004000L</td>
<td>Das Gerät unterstützt unabhängige Schreibmasken für mehrere Elementtexturen oder mehrere Renderziele.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_PERSTAGECONSTANT</td>
<td>0x00008000L</td>
<td>Das Gerät unterstützt phasenspezifische Konstanten. Siehe D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_POSTBLENDSRGBCONVERT</td>
<td>0x00200000L</td>
<td>Das Gerät unterstützt die Konvertierung in sRGB nach dem Mischen. 
<table>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> Dieses Flag ist nur in Direct3D 9Ex verfügbar.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGANDSPECULARALPHA</td>
<td>0x00010000L</td>
<td>Das Gerät unterstützt separates Und-Alpha. Viele Geräte verwenden den alphanularen Specular-Kanal, um den Faktor zu speichern.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_SEPARATEALPHABLEND</td>
<td>0x00020000L</td>
<td>Das Gerät unterstützt separate Blend-Einstellungen für den Alphakanal.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</td>
<td>0x00040000L</td>
<td>Das Gerät unterstützt unterschiedliche Bittiefen für mehrere Renderziele.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</td>
<td>0x00080000L</td>
<td>Das Gerät unterstützt Postpixel-Shadervorgänge für mehrere Renderziele.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGVERTEXCLAMPED</td>
<td>0x00100000L</td>
<td>Das Gerät verbindet den Blendfaktor pro Scheitelpunkt.</td>
</tr>
</tbody>
</table>



 

Diese Konstanten werden vom PrimitiveMiscCaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.

## <a name="constant-information"></a>Konstanteninformationen



| Anforderung                         |  Wert          |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
