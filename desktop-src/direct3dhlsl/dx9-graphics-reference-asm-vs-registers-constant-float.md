---
title: Constant float register (HLSL VS-Referenz)
description: Vertex-Shader-Eingaberegister für eine Gleitkommakonstierte mit vier Komponenten. Legen Sie ein Konstantenregister entweder mit def - vs oder SetVertexShaderConstantF fest.
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c81cc05a40ebb7ede53fb14c957584f289a14a15045a2b69f557072c6885c9ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949930"
---
# <a name="constant-float-register-hlsl-vs-reference"></a>Constant float register (HLSL VS-Referenz)

Vertex-Shader-Eingaberegister für eine Gleitkommakonstierte mit vier Komponenten. Legen Sie ein Konstantenregister entweder [mit def - vs](def---vs.md) oder [**SetVertexShaderConstantF fest.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)

Die konstante Registerdatei ist aus Sicht des Vertex-Shaders schreibgeschützt. Jede einzelne Anweisung kann nur auf ein konstantes Register zugreifen. Jede Quelle in dieser Anweisung kann jedoch unabhängig voneinander schwanken und diesen Vektor beim Lesen negieren.

Das Verhalten von Shaderkonst constants hat sich zwischen Direct3D 8 und Direct3D 9 geändert.

-   Bei Direct3D 9 weisen konstanten Konstanten, die mit defx festgelegt wurden, Werte dem konstanten Shaderraum zu. Die Lebensdauer einer mit defx deklarierten Konstante ist auf die Ausführung dieses Shaders beschränkt. Umgekehrt initialisieren Konstanten, die mithilfe der APIs SetXXXShaderConstantX festgelegt werden, Konstanten im globalen Raum. Konstanten im globalen Raum werden erst dann in den lokalen Raum kopiert (für den Shader sichtbar), wenn SetxxxShaderConstants aufgerufen wird.
-   Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt wurden, Werte dem konstanten Shaderraum zu. Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von der Technik, mit der sie festgelegt wurden.

Ein Konstantenregister wird entweder als absolut oder relativ festgelegt:


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



Das Konstantenregister kann daher entweder mithilfe eines absoluten Indexes oder mit einem relativen Index aus einem Adressregister gelesen werden. Liest aus Out-of-Range-Registern, die zurückgeben (0.0, 0.0, 0.0, 0.0).

## <a name="examples"></a>Beispiele

Hier ist ein Beispiel, in dem zwei Gleitkommakonst constants innerhalb eines Shaders deklariert werden.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Diese Konstanten werden jedes Mal geladen, wenn [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) aufgerufen wird.

Hier ist ein Beispiel für die Verwendung der API.


```
    // Set up the vertex shader constants.
    {
        D3DXMATRIXA16 mat;
        D3DXMatrixMultiply( &mat, &m_matView, &m_matProj );
        D3DXMatrixTranspose( &mat, &mat );

        D3DXVECTOR4 vA( sinf(m_fTime)*15.0f, 0.0f, 0.5f, 1.0f );
        D3DXVECTOR4 vD( D3DX_PI, 1.0f/(2.0f*D3DX_PI), 2.0f*D3DX_PI, 0.05f );

        // Taylor series coefficients for sin and cos.
        D3DXVECTOR4 vSin( 1.0f, -1.0f/6.0f, 1.0f/120.0f, -1.0f/5040.0f );
        D3DXVECTOR4 vCos( 1.0f, -1.0f/2.0f, 1.0f/ 24.0f, -1.0f/ 720.0f );

        m_pd3dDevice->SetVertexShaderConstantF(  0, (float*)&mat,  4 );
        m_pd3dDevice->SetVertexShaderConstantF(  4, (float*)&vA,   1 );
        m_pd3dDevice->SetVertexShaderConstantF(  7, (float*)&vD,   1 );
        m_pd3dDevice->SetVertexShaderConstantF( 10, (float*)&vSin, 1 );
        m_pd3dDevice->SetVertexShaderConstantF( 11, (float*)&vCos, 1 );
    }
```



Wenn Sie konstante Werte mit der API festlegen, ist keine Shaderdeklaration erforderlich.



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Konstantes Register      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 