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
# <a name="vertex-alpha-direct3d-9"></a><span data-ttu-id="4a086-104">Vertex Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4a086-104">Vertex Alpha (Direct3D 9)</span></span>

<span data-ttu-id="4a086-105">Alpha Daten können in den Scheitelpunkt Daten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4a086-105">Alpha data can be supplied in the vertex data.</span></span> <span data-ttu-id="4a086-106">Legen Sie zum Aktivieren von Vertex Alpha die D3DRS \_ DiffuseMaterialSource auf D3DMCS COLOR1 fest, \_ damit die Direct3D-Laufzeit den diffusen Wert aus der diffusen Farbe und nicht aus dem Material einnimmt.</span><span class="sxs-lookup"><span data-stu-id="4a086-106">To enable vertex alpha, set the D3DRS\_DIFFUSEMATERIALSOURCE to D3DMCS\_COLOR1 so that the Direct3D runtime takes the diffuse value from the diffuse color rather than the material.</span></span>


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE,  
                                D3DMCS_COLOR1 );
```



<span data-ttu-id="4a086-107">Geben Sie dann Alpha Werte in der diffusen Farbe an.</span><span class="sxs-lookup"><span data-stu-id="4a086-107">Then, provide alpha values in the diffuse color.</span></span> <span data-ttu-id="4a086-108">Die addalphatoasphere-Funktion fügt Alpha den Scheitel Punkten einer Kugel hinzu.</span><span class="sxs-lookup"><span data-stu-id="4a086-108">The AddAlphaToASphere function, adds alpha to the vertices of a sphere.</span></span> <span data-ttu-id="4a086-109">Im folgenden finden Sie ein Beispiel für die Bereitstellung der Alpha Informationen für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="4a086-109">Here's an example of how to provide the alpha information to the function.</span></span>


```
AddAlphaToASphere( m_pObstacleVertices, 12,  
                    D3DRGBA(light.dcvDiffuse.r, light.dcvDiffuse.g, 
                            light.dcvDiffuse.b, vAlpha ));
```



<span data-ttu-id="4a086-110">Dies ist die Funktion, wie Sie aussieht.</span><span class="sxs-lookup"><span data-stu-id="4a086-110">This is what the function looks like.</span></span>


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



<span data-ttu-id="4a086-111">Addalphatoasphere ändert einfach den farbmember der einzelnen Scheitel Punkte vom Typ D3DLVERTEX, um die Alpha Informationen einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4a086-111">AddAlphaToASphere simply modifies the color member of each vertex, which are of type D3DLVERTEX, to include the alpha information.</span></span>

<span data-ttu-id="4a086-112">D3DLVERTEX sieht wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="4a086-112">D3DLVERTEX looks like this.</span></span>


```
 
// Lit vertex
typedef struct {
    D3DVALUE x, y, z;
    DWORD dwReserved;
    D3DCOLOR color, specular;
    D3DVALUE tu, tv;
} D3DLVERTEX, *LPD3DLVERTEX;
```



<span data-ttu-id="4a086-113">Zeichnen der Kugel,</span><span class="sxs-lookup"><span data-stu-id="4a086-113">Drawing the sphere,</span></span>


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

//...

// Draw the lit sphere
m_pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, D3DFVF_LVERTEX,
                                    m_pObstacleVertices, m_dwNumObstacleVertices,
                                    m_pObstacleIndices,  m_dwNumObstacleIndices, 0 );
```



<span data-ttu-id="4a086-114">ergibt eine transparente Kugel mithilfe von Scheitelpunkt alpha.</span><span class="sxs-lookup"><span data-stu-id="4a086-114">results in a transparent sphere using vertex alpha.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a086-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a086-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a086-116">Alpha Blending</span><span class="sxs-lookup"><span data-stu-id="4a086-116">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



