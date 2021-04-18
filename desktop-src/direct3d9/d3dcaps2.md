---
description: Treiberfunktionsflags.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953e73c0ea6b079a6b8f0658790c749b4f30a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343610"
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
<td>#definieren</td>
<td>Wert</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANAUTOGENMIPMAP</td>
<td>0x40000000l</td>
<td>Der Treiber kann automatisch Mipmaps erstellen. Weitere Informationen finden Sie unter <a href="automatic-generation-of-mipmaps.md">Automatische Generierung von Mipmaps (Direct3D 9)</a>.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_CANCALIBRATEGAMMA</td>
<td>0x00100000l</td>
<td>Das System verfügt über einen installierten kalierer, der die Gamma-Rampe automatisch anpassen kann, sodass das Ergebnis auf allen Systemen mit einem kalikalierer identisch ist. Wenn Sie den kalierer beim Festlegen neuer Gamma Ebenen aufrufen möchten, verwenden Sie das D3DSGR_CALIBRATE-Flag beim Aufrufen von <a href="/windows/desktop/api"><strong>setgammaramp</strong></a>. Die Kalibrierung von Gamma Rampen verursacht einen gewissen Verarbeitungsaufwand und sollte nicht häufig verwendet werden.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANSHARERESOURCE</td>
<td>0x80000000l</td>
<td>Das Gerät kann freileg Bare Ressourcen erstellen. Methoden, die Ressourcen erstellen, können Werte ungleich NULL für Ihre <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>psharedhandle</strong></a> -Parameter festlegen. 
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
<td>0x10000000l</td>
<td>Der Treiber kann Ressourcen verwalten. Bei solchen Treibern werden D3DPOOL_MANAGED Ressourcen vom Treiber verwaltet. Um Direct3D den Treiber außer Kraft zu setzen, damit Direct3D Ressourcen verwaltet, verwenden Sie das D3DCREATE_DISABLE_DRIVER_MANAGEMENT-Flag beim Aufrufen von <a href="/windows/desktop/api"><strong>createdevice</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_DYNAMICTEXTURES</td>
<td>0x20000000l</td>
<td>Der Treiber unterstützt dynamische Texturen.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_FULLSCREENGAMMA</td>
<td>0x00020000l</td>
<td>Der Treiber unterstützt die dynamische Gamma Rampen Anpassung im Vollbildmodus.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_RESERVED</td>
<td>0x02000000l</td>
<td>Bleiben nicht verwendet.</td>
</tr>
</tbody>
</table>



 

Diese Konstanten werden vom D3CAPS2-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
