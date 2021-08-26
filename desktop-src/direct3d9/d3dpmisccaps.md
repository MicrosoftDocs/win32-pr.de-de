---
description: Verschiedene primitive Treiberfunktionsflags.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee88ba03b3c0a6d51c0100b20768df4cbf632d46
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624536"
---
# <a name="d3dpmisccaps"></a>D3DPMISCCAPS

Verschiedene primitive Treiberfunktionsflags.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definieren</td>
<td>Wert</td>
<td>Beschreibung</td>
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
<td>Das Gerät unterstützt Schreibvorgänge pro Kanal für den Renderziel-Farbpuffer durch D3DRS_COLORWRITEENABLE Zustand.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</td>
<td>0x00000200L</td>
<td>Das Gerät schneide ordnungsgemäß skalierte Punkte mit einer Größe größer als 1,0 auf benutzerdefinierte Clippingebenen.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CLIPTLVERTS</td>
<td>0x00000200L</td>
<td>Geräteclips nach transformierten Scheitelpunktprimitiven. Geben D3DUSAGE_DONOTCLIP an, wenn die Pipeline keine Beschneidungsausschneiden soll. In diesem Fall muss möglicherweise zur Zeichnen-Zeit zusätzliche Softwareclips ausgeführt werden, was erfordert, dass sich der Scheitelpunktpuffer im Systemspeicher befingt.<br/></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_TSSARGTEMP</td>
<td>0x00000400L</td>
<td>Das Gerät unterstützt <a href="d3dta.md">D3DTA für</a> die temporäre Registrierung.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_BLENDOP</td>
<td>0x00000800L</td>
<td>Das Gerät unterstützt alphablending-Vorgänge, die keine D3DBLENDOP_ADD.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_NULLREFERENCE</td>
<td>0x00000100L</td>
<td>Ein Referenzgerät, das nicht gerendert wird.</td>
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
<td>Das Gerät unterstützt Shadervorgänge nach Pixel für mehrere Renderziele.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGVERTEXCLAMPED</td>
<td>0x00100000L</td>
<td>Gerät klammert Blendfaktor pro Scheitelpunkt.</td>
</tr>
</tbody>
</table>



 

Diese Konstanten werden vom PrimitiveMiscCaps-Member von [**D3DCAPS9 verwendet.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Konstante Informationen



| Anforderung                         |  Wert          |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
