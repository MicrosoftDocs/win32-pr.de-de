---
description: Eine Liste der Treiberfunktionsflags finden Sie hier. Enthält die Definitionen, Werte und Beschreibungen mit Links zu APIs.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f209e840450b834c3a69593d1297f2cba9ee43c0
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343375"
---
# <a name="d3dcaps2"></a>D3DCAPS2

Treiberfunktionsflags.



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
<td>D3DCAPS2_CANAUTOGENMIPMAP</td>
<td>0x40000000L</td>
<td>Der Treiber kann automatisch Mipmaps generieren. Weitere Informationen finden Sie unter <a href="automatic-generation-of-mipmaps.md">Automatische Generierung von Mipmaps (Direct3D 9).</a></td>
</tr>
<tr class="odd">
<td>D3DCAPS2_CANCALIBRATEGAMMA</td>
<td>0x00100000L</td>
<td>Auf dem System ist ein Kalibrierer installiert, mit dem die Gammaverlaufsverlauf automatisch angepasst werden kann, sodass das Ergebnis auf allen Systemen, die über einen Kalibrierer verfügen, identisch ist. Um den Kalibrierungsprozessor beim Festlegen neuer Gammawerte aufzurufen, verwenden Sie beim Aufrufen von <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>das flag D3DSGR_CALIBRATE . Das Kalibrieren von Gamma rampen verursacht einen gewissen Verarbeitungsaufwand und sollte nicht häufig verwendet werden.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANSHARERESOURCE</td>
<td>0x80000000L</td>
<td>Das Gerät kann sharable Ressourcen erstellen. Methoden, die Ressourcen erstellen, können Nicht-NULL-Werte für ihre <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle-Parameter</strong></a> festlegen. 
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
<td>D3DCAPS2_CANMANAGERESOURCE</td>
<td>0x10000000L</td>
<td>Der Treiber kann Ressourcen verwalten. Bei solchen Treibern D3DPOOL_MANAGED Ressourcen vom Treiber verwaltet. Damit Direct3D den Treiber überschreibt, sodass Direct3D Ressourcen verwaltet, verwenden Sie das D3DCREATE_DISABLE_DRIVER_MANAGEMENT-Flag, wenn <a href="/windows/desktop/api"><strong>Sie CreateDevice aufrufen.</strong></a></td>
</tr>
<tr class="even">
<td>D3DCAPS2_DYNAMICTEXTURES</td>
<td>0x20000000L</td>
<td>Der Treiber unterstützt dynamische Texturen.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_FULLSCREENGAMMA</td>
<td>0x00020000L</td>
<td>Der Treiber unterstützt die dynamische Gamma-Rampenanpassung im Vollbildmodus.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_RESERVED</td>
<td>0x02000000L</td>
<td>Reserviert; nicht verwendet.</td>
</tr>
</tbody>
</table>



 

Diese Konstanten werden vom D3CAPS2-Member von [**D3DCAPS9 verwendet.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Konstante Informationen



|  Anforderung                        | Wert           |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
