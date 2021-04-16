---
description: 'Die IDirect3DDevice9:: SetStreamSource-Methode bindet einen Scheitelpunkt Puffer an einen Gerätedaten Strom, wobei eine Zuordnung zwischen den Scheitelpunkt Daten und einem von mehreren datenstreamports erstellt wird, die die primitiven Verarbeitungsfunktionen übertragen.'
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Festlegen der Streamquelle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d0c296b79d258be6eee2d683979081673d5d04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521912"
---
# <a name="setting-the-stream-source-direct3d-9"></a>Festlegen der Streamquelle (Direct3D 9)

Die [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) -Methode bindet einen Scheitelpunkt Puffer an einen Gerätedaten Strom, wobei eine Zuordnung zwischen den Scheitelpunkt Daten und einem von mehreren datenstreamports erstellt wird, die die primitiven Verarbeitungsfunktionen übertragen. Die tatsächlichen Verweise auf die Streamdaten treten erst auf, wenn eine Zeichnungs Methode, z. b. [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), aufgerufen wird.

Ein Datenstrom ist als einheitliches Array von Komponenten Daten definiert, wobei jede Komponente aus mindestens einem Element besteht, das eine einzelne Entität, z. b. Position, normal, Farbe usw., darstellt. Der Stride-Parameter gibt die Größe der Komponente in Bytes an.

Der folgende Code veranschaulicht das Festlegen der Streamquelle und das Zeichnen Ihres Inhalts. Die Variable "g \_ PVB" ist eine LPDIRECT3DVERTEXBUFFER9, die Scheitelpunkt Daten enthält.


```
if( SUCCEEDED( g_pd3dDevice->BeginScene() ) )
{
    // Setup the world, view, and projection matrices
    SetupMatrices();

    // Render the vertex buffer contents
    g_pd3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
    g_pd3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
    g_pd3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 1 );

    // End the scene
    g_pd3dDevice->EndScene();
}
```



Weitere Informationen zu diesem Code finden Sie im folgenden Tutorial: [Tutorial 3: Verwenden von Matrizen](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern von primitiven](rendering-primitives.md)
</dt> </dl>

 

 
