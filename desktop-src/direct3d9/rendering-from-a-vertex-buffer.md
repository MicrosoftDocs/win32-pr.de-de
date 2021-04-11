---
description: 'Zum Rendern von Scheitelpunkt Daten aus einem Vertex-Puffer sind einige Schritte erforderlich. Zuerst müssen Sie die Streamquelle festlegen, indem Sie die IDirect3DDevice9:: SetStreamSource-Methode aufrufen, wie im folgenden Beispiel gezeigt.'
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Rendering von einem Scheitelpunkt Puffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cebb68c5395a827a9aee4ea1f8465257c436bb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123428"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a>Rendering von einem Scheitelpunkt Puffer (Direct3D 9)

Zum Rendern von Scheitelpunkt Daten aus einem Vertex-Puffer sind einige Schritte erforderlich. Zuerst müssen Sie die Streamquelle festlegen, indem Sie die [**IDirect3DDevice9:: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) -Methode aufrufen, wie im folgenden Beispiel gezeigt.


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



Der erste Parameter von [**IDirect3DDevice9:: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) teilt Direct3D die Quelle des Datenstroms des Geräts. Der zweite Parameter ist der Vertex-Puffer, der an den Datenstream gebunden werden soll. Der dritte Parameter ist der Offset vom Anfang des Streams bis zum Anfang der Scheitelpunkt Daten (in Bytes). Der vierte Parameter ist der Schritt der Komponente (in Bytes). Im obigen Beispielcode wird die Größe eines CustomVertex für den Schritt der Komponente verwendet.

Der nächste Schritt besteht darin, den zu verwendenden Vertex-Shader zu informieren Direct3D indem Sie die [**IDirect3DDevice9:: setvertexshader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) -Methode aufrufen. Der folgende Beispielcode legt einen f-Code für den Vertex-Shader fest. Dies informiert Direct3D über die Typen der Scheitel Punkte, mit denen es umzugehen ist.


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



Nachdem Sie die Streamquelle und den Vertexshader festgelegt haben, verwenden alle Draw-Methoden den Vertex-Puffer. Im folgenden Codebeispiel wird gezeigt, wie Vertices aus einem Vertex-Puffer mit der [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Methode gerwiert werden.


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



Der zweite Parameter, den [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) akzeptiert, ist der Index des ersten Vektors im Vertex-Puffer, der geladen werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Puffer](vertex-buffers.md)
</dt> <dt>

[Rendering aus Scheitelpunkt-und Index Puffer (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
