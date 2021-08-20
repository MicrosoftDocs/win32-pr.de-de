---
title: D3DX-Schnittstellen (Direct3D 11-Grafiken)
description: Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen (Component Object Model), die von der D3DX-Hilfsprogrammbibliothek bereitgestellt werden.
ms.assetid: 0d3be1e6-b558-4586-9440-251a5611d7cd
keywords:
- D3DX-Schnittstellen, Direct3D 11
- Schnittstellen, Direct3D 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d746c02695860ecefda85b1d2700c718a65cdc657965af093c883c43914bbb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046628"
---
# <a name="d3dx-interfaces-direct3d-11-graphics"></a>D3DX-Schnittstellen (Direct3D 11-Grafiken)

Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen (Component Object Model), die von der D3DX-Hilfsprogrammbibliothek bereitgestellt werden.

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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="id3dx11dataloader.md"><strong>ID3DX11DataLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Datenladeobjekt, das von <a href="id3dx11threadpump.md"><strong>der ID3DX11ThreadPump-Schnittstelle</strong></a> zum asynchronen Laden von Daten verwendet wird.<br/></td>
</tr>
<tr class="even">
<td><a href="id3dx11dataprocessor.md"><strong>ID3DX11DataProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Datenverarbeitungsobjekt, das von <a href="id3dx11threadpump.md"><strong>der ID3DX11ThreadPump-Schnittstelle zum</strong></a> asynchronen Laden von Daten verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.
</blockquote>
<br/> Ein Threadpump führt Aufgaben asynchron aus. Sie wird durch Aufrufen von <a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump erstellt.</strong></a> Es gibt mehrere APIs, die eine optionale Threadpump als Parameter verwenden, z. B. <a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a> und <a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile;</strong></a> Wenn Sie eine Threadpumpschnittstelle an diese APIs übergeben, werden die Funktionen asynchron in einem separaten Thread ausgeführt. Insbesondere auf Multiprozessorcomputern kann eine Threadpump Ressourcen laden und Daten verarbeiten, ohne die Leistung merklich zu beeinträchtigen.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX 11-Referenz](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

 





