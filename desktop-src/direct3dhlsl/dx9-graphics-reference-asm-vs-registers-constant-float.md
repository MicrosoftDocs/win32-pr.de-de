---
title: Konstantes float-Register (HLSL vs-Referenz)
description: Vertex-Shader-Eingabe Register für eine Gleit Komma Konstante mit vier Komponenten. Legen Sie ein konstantes Register entweder mit DEF-vs oder setvertexshaderconstantf fest.
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 856c9567070a071a123b28279342fd9cbbb0f6af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390466"
---
# <a name="constant-float-register-hlsl-vs-reference"></a>Konstantes float-Register (HLSL vs-Referenz)

Vertex-Shader-Eingabe Register für eine Gleit Komma Konstante mit vier Komponenten. Legen Sie ein konstantes Register entweder mit [DEF-vs](def---vs.md) oder [**setvertexshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)fest.

Die Konstante Register Datei ist aus der Perspektive des Vertex-Shaders schreibgeschützt. Jede einzelne Anweisung kann nur auf ein konstantes Register zugreifen. Jede Quelle in dieser Anweisung kann den Vektor jedoch unabhängig voneinander wischen, wenn er gelesen wird.

Das Verhalten der shaderkonstanten wurde zwischen Direct3D 8 und Direct3D 9 geändert.

-   Bei Direct3D 9 weisen Konstanten, die mit defx festgelegt sind, dem Shader-konstantenbereich Werte zu. Die Lebensdauer einer mit defx deklarierten Konstante ist nur auf die Ausführung dieses Shaders beschränkt. Umgekehrt werden Konstanten, die mithilfe der APIs setxxxshaderconstantx festgelegt wurden, Konstanten im globalen Raum initialisieren. Konstanten im globalen Raum werden erst in den lokalen Bereich (sichtbar für den Shader) kopiert, bis setxxxshaderconstants aufgerufen wird.
-   Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt sind, dem Shader-konstantenbereich Werte zu. Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von dem Verfahren, mit dem Sie festgelegt werden.

Ein konstantes Register ist entweder absolut oder relativ:


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



Das Konstante Register kann daher entweder mit einem absoluten Index oder mit einem relativen Index aus einem Adressregister gelesen werden. Lesevorgänge aus außerhalb des gültigen Bereichs werden zurückgegeben (0,0, 0,0, 0,0, 0,0).

## <a name="examples"></a>Beispiele

Im folgenden finden Sie ein Beispiel für das Deklarieren von zwei Gleit Komma Konstanten innerhalb eines Shaders.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Diese Konstanten werden jedes Mal geladen, wenn [**setvertexshader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) aufgerufen wird.

Im folgenden finden Sie ein Beispiel für die Verwendung der API.


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



Wenn Sie Konstante Werte mit der API festlegen, ist keine Shader-Deklaration erforderlich.



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Konstantes Register      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 