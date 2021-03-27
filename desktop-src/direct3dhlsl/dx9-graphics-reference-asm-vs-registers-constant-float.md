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
# <a name="constant-float-register-hlsl-vs-reference"></a><span data-ttu-id="9fa0a-104">Konstantes float-Register (HLSL vs-Referenz)</span><span class="sxs-lookup"><span data-stu-id="9fa0a-104">Constant float register (HLSL VS reference)</span></span>

<span data-ttu-id="9fa0a-105">Vertex-Shader-Eingabe Register für eine Gleit Komma Konstante mit vier Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-105">Vertex shader input register for a four component floating-point constant.</span></span> <span data-ttu-id="9fa0a-106">Legen Sie ein konstantes Register entweder mit [DEF-vs](def---vs.md) oder [**setvertexshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)fest.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-106">Set a constant register with either [def - vs](def---vs.md) or [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).</span></span>

<span data-ttu-id="9fa0a-107">Die Konstante Register Datei ist aus der Perspektive des Vertex-Shaders schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-107">The constant register file is read-only from the perspective of the vertex shader.</span></span> <span data-ttu-id="9fa0a-108">Jede einzelne Anweisung kann nur auf ein konstantes Register zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-108">Any single instruction may access only one constant register.</span></span> <span data-ttu-id="9fa0a-109">Jede Quelle in dieser Anweisung kann den Vektor jedoch unabhängig voneinander wischen, wenn er gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-109">However, each source in that instruction may independently swizzle and negate that vector as it is read.</span></span>

<span data-ttu-id="9fa0a-110">Das Verhalten der shaderkonstanten wurde zwischen Direct3D 8 und Direct3D 9 geändert.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-110">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="9fa0a-111">Bei Direct3D 9 weisen Konstanten, die mit defx festgelegt sind, dem Shader-konstantenbereich Werte zu.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-111">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="9fa0a-112">Die Lebensdauer einer mit defx deklarierten Konstante ist nur auf die Ausführung dieses Shaders beschränkt.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-112">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="9fa0a-113">Umgekehrt werden Konstanten, die mithilfe der APIs setxxxshaderconstantx festgelegt wurden, Konstanten im globalen Raum initialisieren.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-113">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="9fa0a-114">Konstanten im globalen Raum werden erst in den lokalen Bereich (sichtbar für den Shader) kopiert, bis setxxxshaderconstants aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-114">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="9fa0a-115">Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt sind, dem Shader-konstantenbereich Werte zu.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-115">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="9fa0a-116">Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von dem Verfahren, mit dem Sie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-116">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

<span data-ttu-id="9fa0a-117">Ein konstantes Register ist entweder absolut oder relativ:</span><span class="sxs-lookup"><span data-stu-id="9fa0a-117">A constant register is designated as either absolute or relative:</span></span>


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



<span data-ttu-id="9fa0a-118">Das Konstante Register kann daher entweder mit einem absoluten Index oder mit einem relativen Index aus einem Adressregister gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-118">The constant register can be read, therefore, either by using an absolute index or with a relative index from an address register.</span></span> <span data-ttu-id="9fa0a-119">Lesevorgänge aus außerhalb des gültigen Bereichs werden zurückgegeben (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="9fa0a-119">Reads from out-of-range registers return (0.0, 0.0, 0.0, 0.0).</span></span>

## <a name="examples"></a><span data-ttu-id="9fa0a-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fa0a-120">Examples</span></span>

<span data-ttu-id="9fa0a-121">Im folgenden finden Sie ein Beispiel für das Deklarieren von zwei Gleit Komma Konstanten innerhalb eines Shaders.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-121">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="9fa0a-122">Diese Konstanten werden jedes Mal geladen, wenn [**setvertexshader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-122">These constants are loaded every time [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) is called.</span></span>

<span data-ttu-id="9fa0a-123">Im folgenden finden Sie ein Beispiel für die Verwendung der API.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-123">Here is an example using the API.</span></span>


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



<span data-ttu-id="9fa0a-124">Wenn Sie Konstante Werte mit der API festlegen, ist keine Shader-Deklaration erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9fa0a-124">If you are setting constant values with the API, there is no shader declaration required.</span></span>



| <span data-ttu-id="9fa0a-125">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="9fa0a-125">Vertex shader versions</span></span> | <span data-ttu-id="9fa0a-126">1\_1</span><span class="sxs-lookup"><span data-stu-id="9fa0a-126">1\_1</span></span> | <span data-ttu-id="9fa0a-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9fa0a-127">2\_0</span></span> | <span data-ttu-id="9fa0a-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9fa0a-128">2\_sw</span></span> | <span data-ttu-id="9fa0a-129">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9fa0a-129">2\_x</span></span> | <span data-ttu-id="9fa0a-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9fa0a-130">3\_0</span></span> | <span data-ttu-id="9fa0a-131">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9fa0a-131">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="9fa0a-132">Konstantes Register</span><span class="sxs-lookup"><span data-stu-id="9fa0a-132">Constant Register</span></span>      | <span data-ttu-id="9fa0a-133">x</span><span class="sxs-lookup"><span data-stu-id="9fa0a-133">x</span></span>    | <span data-ttu-id="9fa0a-134">x</span><span class="sxs-lookup"><span data-stu-id="9fa0a-134">x</span></span>    | <span data-ttu-id="9fa0a-135">x</span><span class="sxs-lookup"><span data-stu-id="9fa0a-135">x</span></span>     | <span data-ttu-id="9fa0a-136">x</span><span class="sxs-lookup"><span data-stu-id="9fa0a-136">x</span></span>    | <span data-ttu-id="9fa0a-137">x</span><span class="sxs-lookup"><span data-stu-id="9fa0a-137">x</span></span>    | <span data-ttu-id="9fa0a-138">x</span><span class="sxs-lookup"><span data-stu-id="9fa0a-138">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="9fa0a-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9fa0a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fa0a-140">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="9fa0a-140">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 