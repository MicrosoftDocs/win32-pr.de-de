---
description: Eine Liste der D3DCAPS2-Treiberfunktionsflags finden Sie hier. Enthält die Definitionen, Werte und Beschreibungen mit Links zu APIs.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2266073c2d803f9bf11f4a3548078c0d34e5f78
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408293"
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
<td>Beschreibung</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANAUTOGENMIPMAP</td>
<td>0x40000000L</td>
<td>Der Treiber kann automatisch Mipmaps generieren. Weitere Informationen finden Sie unter <a href="automatic-generation-of-mipmaps.md">Automatische Generierung von Mipmaps (Direct3D 9).</a></td>
</tr>
<tr class="odd">
<td>D3DCAPS2_CANCALIBRATEGAMMA</td>
<td>0x00100000L</td>
<td>Das System verfügt über einen installierten Kalibrierer, der die Gamma-Rampe automatisch so anpassen kann, dass das Ergebnis auf allen Systemen identisch ist, die über einen Kalibrierer verfügen. Verwenden Sie zum Aufrufen des Kalibrierers beim Festlegen neuer Gammawerte das D3DSGR_CALIBRATE beim Aufrufen <a href="/windows/desktop/api"><strong>von SetGammaRamp</strong></a>. Das Kalibrieren von Gamma-Rampen verursacht verarbeitungsaufwand und sollte nicht häufig verwendet werden.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANSHARERESOURCE</td>
<td>0x80000000L</td>
<td>Das Gerät kann sharable-Ressourcen erstellen. Methoden, die Ressourcen erstellen, können Werte festlegen, die nicht NULL sind, für <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>ihre pSharedHandle-Parameter.</strong></a> 
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

 

 
