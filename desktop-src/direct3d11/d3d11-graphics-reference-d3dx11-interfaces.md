---
title: D3DX-Schnittstellen (Direct3D 11-Grafiken)
description: Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen (Component Object Model), die von der D3DX Utility Library bereitgestellt werden.
ms.assetid: 0d3be1e6-b558-4586-9440-251a5611d7cd
keywords:
- D3DX-Schnittstellen, Direct3D 11
- Schnittstellen, Direct3D 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da2890c3c55d1bac9eba09c046927e432b1a27f8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039927"
---
# <a name="d3dx-interfaces-direct3d-11-graphics"></a>D3DX-Schnittstellen (Direct3D 11-Grafiken)

Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen (Component Object Model), die von der D3DX Utility Library bereitgestellt werden.

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 


## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="id3dx11dataloader.md"><strong>ID3DX11DataLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Datenlade Objekt, das von der <a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump-Schnittstelle</strong></a> zum asynchronen Laden von Daten verwendet wird<br/></td>
</tr>
<tr class="even">
<td><a href="id3dx11dataprocessor.md"><strong>ID3DX11DataProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Datenverarbeitungs Objekt, das von der <a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump-Schnittstelle</strong></a> zum asynchronen Laden von Daten verwendet wird<br/></td>
</tr>
<tr class="odd">
<td><a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Ein Thread-Pump führt Aufgaben asynchron aus. Sie wird durch Aufrufen von <a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a>erstellt. Es gibt mehrere APIs, die ein optionales threadpump als Parameter akzeptieren, z. b. <a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a> und <a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a>. Wenn Sie eine Thread-Pump-Schnittstelle an diese APIs übergeben, werden die Funktionen asynchron in einem separaten Thread ausgeführt. Vor allem bei Multiprozessorcomputern kann ein Thread-Pump Ressourcen laden und Daten verarbeiten, ohne eine spürbare Leistungsminderung zu erzielen.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

 





