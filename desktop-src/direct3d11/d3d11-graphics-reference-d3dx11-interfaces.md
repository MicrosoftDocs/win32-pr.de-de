---
title: D3DX-Schnittstellen (Direct3D 11-Grafiken)
description: Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen (Component Object Model), die von der D3DX-Hilfsprogrammbibliothek bereitgestellt werden.
ms.assetid: 0d3be1e6-b558-4586-9440-251a5611d7cd
keywords:
- D3DX-Schnittstellen, Direct3D 11
- Schnittstellen, Direct3D 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd67f82d3198ef25254b3a682c80dc98e0313321
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475737"
---
# <a name="d3dx-interfaces-direct3d-11-graphics"></a>D3DX-Schnittstellen (Direct3D 11-Grafiken)

Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen (Component Object Model), die von der D3DX-Hilfsprogrammbibliothek bereitgestellt werden.

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 


## <a name="in-this-section"></a>In diesem Abschnitt




| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="id3dx11dataloader.md"><strong>ID3DX11DataLoader</strong></a><br /> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Datenladeobjekt, das von <a href="id3dx11threadpump.md"><strong>der ID3DX11ThreadPump-Schnittstelle</strong></a> zum asynchronen Laden von Daten verwendet wird.<br /> | 
| <a href="id3dx11dataprocessor.md"><strong>ID3DX11DataProcessor</strong></a><br /> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Datenverarbeitungsobjekt, das von <a href="id3dx11threadpump.md"><strong>der ID3DX11ThreadPump-Schnittstelle zum</strong></a> asynchronen Laden von Daten verwendet wird.<br /> | 
| <a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump</strong></a><br /> | <blockquote>[!Note]<br />Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</blockquote><br /> Ein Threadpump führt Aufgaben asynchron aus. Sie wird durch Aufrufen von <a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump erstellt.</strong></a> Es gibt mehrere APIs, die eine optionale Threadpump als Parameter verwenden, z. B. <a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a> und <a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile;</strong></a> Wenn Sie eine Threadpumpschnittstelle an diese APIs übergeben, werden die Funktionen asynchron in einem separaten Thread ausgeführt. Insbesondere auf Multiprozessorcomputern kann eine Threadpump Ressourcen laden und Daten verarbeiten, ohne die Leistung merklich zu beeinträchtigen.<br /> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX 11-Referenz](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

 





