---
description: Die IDirect3DDevice9::SetStreamSource-Methode bindet einen Scheitelpunktpuffer an einen Gerätedatenstrom und erstellt eine Zuordnung zwischen den Scheitelpunktdaten und einem von mehreren Datenstromports, die die primitiven Verarbeitungsfunktionen unterstützen.
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Festlegen der Streamquelle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91bd760b23204de2c6ccd313b164ac7536c7db2d3e2da26d7e40b7d98daa60a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044238"
---
# <a name="setting-the-stream-source-direct3d-9"></a>Festlegen der Streamquelle (Direct3D 9)

Die [**IDirect3DDevice9::SetStreamSource-Methode**](/windows/desktop/api) bindet einen Scheitelpunktpuffer an einen Gerätedatenstrom und erstellt eine Zuordnung zwischen den Scheitelpunktdaten und einem von mehreren Datenstromports, die die primitiven Verarbeitungsfunktionen unterstützen. Die tatsächlichen Verweise auf die Streamdaten treten erst auf, wenn eine Zeichnungsmethode wie [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)aufgerufen wird.

Ein Stream wird als einheitliches Array von Komponentendaten definiert, wobei jede Komponente aus mindestens einem Element besteht, das eine einzelne Entität darstellt, z. B. Position, Normal, Farbe usw. Der Stride-Parameter gibt die Größe der Komponente in Bytes an.

Der folgende Code veranschaulicht das Festlegen der Streamquelle und das Zeichnen ihres Inhalts. Die \_ g pVB-Variable ist eine LPDIRECT3DVERTEXBUFFER9, die Scheitelpunktdaten enthält.


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



Weitere Informationen zu diesem Code finden Sie im folgenden Tutorial: [Tutorial 3: Verwenden von Matrizen.](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern von Primitiven](rendering-primitives.md)
</dt> </dl>

 

 
