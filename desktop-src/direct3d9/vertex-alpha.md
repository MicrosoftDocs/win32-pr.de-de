---
description: Alpha Daten können in den Scheitelpunkt Daten bereitgestellt werden. Legen Sie zum Aktivieren von Vertex Alpha die D3DRS \_ DiffuseMaterialSource auf D3DMCS COLOR1 fest, \_ damit die Direct3D-Laufzeit den diffusen Wert aus der diffusen Farbe und nicht aus dem Material einnimmt.
ms.assetid: 2b0d842d-ee7d-4633-846d-96697153adc7
title: Vertex Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f661c013e324a0bf209b4faca41d1974a41e81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123998"
---
# <a name="vertex-alpha-direct3d-9"></a>Vertex Alpha (Direct3D 9)

Alpha Daten können in den Scheitelpunkt Daten bereitgestellt werden. Legen Sie zum Aktivieren von Vertex Alpha die D3DRS \_ DiffuseMaterialSource auf D3DMCS COLOR1 fest, \_ damit die Direct3D-Laufzeit den diffusen Wert aus der diffusen Farbe und nicht aus dem Material einnimmt.


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE,  
                                D3DMCS_COLOR1 );
```



Geben Sie dann Alpha Werte in der diffusen Farbe an. Die addalphatoasphere-Funktion fügt Alpha den Scheitel Punkten einer Kugel hinzu. Im folgenden finden Sie ein Beispiel für die Bereitstellung der Alpha Informationen für die Funktion.


```
AddAlphaToASphere( m_pObstacleVertices, 12,  
                    D3DRGBA(light.dcvDiffuse.r, light.dcvDiffuse.g, 
                            light.dcvDiffuse.b, vAlpha ));
```



Dies ist die Funktion, wie Sie aussieht.


```
 
void AddAlphaToASphere(D3DLVERTEX* pVertices, DWORD dwNumRings, D3DCOLOR lightcolor)
{
    WORD x, y;
    // rings around
    for( y=0; y < dwNumRings; y++ )
        for( x=0; x < (dwNumRings*2)+1; x++ )
            (pVertices++)->color = lightcolor;

    // top and bottom
    (pVertices++)->color = lightcolor;
    (pVertices++)->color = lightcolor;
}
```



Addalphatoasphere ändert einfach den farbmember der einzelnen Scheitel Punkte vom Typ D3DLVERTEX, um die Alpha Informationen einzuschließen.

D3DLVERTEX sieht wie folgt aus.


```
 
// Lit vertex
typedef struct {
    D3DVALUE x, y, z;
    DWORD dwReserved;
    D3DCOLOR color, specular;
    D3DVALUE tu, tv;
} D3DLVERTEX, *LPD3DLVERTEX;
```



Zeichnen der Kugel,


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

//...

// Draw the lit sphere
m_pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, D3DFVF_LVERTEX,
                                    m_pObstacleVertices, m_dwNumObstacleVertices,
                                    m_pObstacleIndices,  m_dwNumObstacleIndices, 0 );
```



ergibt eine transparente Kugel mithilfe von Scheitelpunkt alpha.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alpha Blending](alpha-blending.md)
</dt> </dl>

 

 



