---
description: Das Rendern von Scheitelpunktdaten aus einem Scheitelpunktpuffer erfordert einige Schritte. Zunächst müssen Sie die Streamquelle festlegen, indem Sie die IDirect3DDevice9::SetStreamSource-Methode aufrufen, wie im folgenden Beispiel gezeigt.
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Rendern aus einem Scheitelpunktpuffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ee3d477fc812d2dabed765e28bb14452a6badf746a331a13283108ef46b47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520071"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a>Rendern aus einem Scheitelpunktpuffer (Direct3D 9)

Das Rendern von Scheitelpunktdaten aus einem Scheitelpunktpuffer erfordert einige Schritte. Zunächst müssen Sie die Streamquelle festlegen, indem Sie die [**IDirect3DDevice9::SetStreamSource-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) aufrufen, wie im folgenden Beispiel gezeigt.


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



Der erste Parameter von [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) teilt Direct3D die Quelle des Gerätedatenstroms mit. Der zweite Parameter ist der Scheitelpunktpuffer, der an den Datenstrom gebunden werden soll. Der dritte Parameter ist der Offset vom Anfang des Streams bis zum Anfang der Scheitelpunktdaten in Bytes. Der vierte Parameter ist der Schritt der Komponente in Bytes. Im obigen Beispielcode wird die Größe von CUSTOMVERTEX für den Schritt der Komponente verwendet.

Im nächsten Schritt wird Direct3D durch Aufrufen der [**IDirect3DDevice9::SetVertexShader-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) darüber informiert, welcher Vertexshader verwendet werden soll. Der folgende Beispielcode legt einen FVF-Code für den Vertex-Shader fest. Dadurch wird Direct3D über die Scheitelungstypen informiert, mit der es zu tun hat.


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



Nach dem Festlegen der Streamquelle und des Vertex-Shaders verwenden alle Draw-Methoden den Scheitelpunktpuffer. Das folgende Codebeispiel zeigt, wie Scheitelpunkte aus einem Scheitelpunktpuffer mit der [**IDirect3DDevice9::D rawPrimitive-Methode gerendert**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) werden.


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



Der zweite Parameter, den [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) akzeptiert, ist der Index des ersten zu ladenden Vektors im Scheitelpunktpuffer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunktpuffer](vertex-buffers.md)
</dt> <dt>

[Rendern von Scheitelpunkt- und Indexpuffern (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
