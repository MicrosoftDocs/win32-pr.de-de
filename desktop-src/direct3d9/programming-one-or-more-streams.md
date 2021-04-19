---
description: In diesem Abschnitt werden Shader beschrieben, die für das programmierbare Streamingmodell verwendet werden können.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programmieren von mindestens einem Stream (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43210823911648ed11227faef44d980b60d0a335
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346194"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a><span data-ttu-id="349c7-103">Programmieren von mindestens einem Stream (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="349c7-103">Programming One or More Streams (Direct3D 9)</span></span>

<span data-ttu-id="349c7-104">In diesem Abschnitt werden Shader beschrieben, die für das programmierbare Streamingmodell verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="349c7-104">This section describes shaders that can be used for the programmable stream model.</span></span>

## <a name="using-streams"></a><span data-ttu-id="349c7-105">Verwenden von Streams</span><span class="sxs-lookup"><span data-stu-id="349c7-105">Using Streams</span></span>

<span data-ttu-id="349c7-106">In DirectX 8 wurde das Konzept eines Datenstroms eingeführt, um Daten an Eingabe Register zur Verwendung durch Shader zu binden.</span><span class="sxs-lookup"><span data-stu-id="349c7-106">DirectX 8 introduced the notion of a stream to bind data to input registers for use by shaders.</span></span> <span data-ttu-id="349c7-107">Ein Datenstrom ist ein einheitliches Array von Komponenten Daten, wobei jede Komponente aus mindestens einem Element besteht, das eine einzelne Entität (z. b. Position, normal, Farbe usw.) darstellt.</span><span class="sxs-lookup"><span data-stu-id="349c7-107">A stream is a uniform array of component data, where each component consists of one or more elements that represent a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="349c7-108">Mithilfe von Streams können Grafikchips einen direkten Speicherzugriff von mehreren Scheitelpunkt Puffern parallel ausführen und außerdem eine natürlichere Zuordnung von Anwendungsdaten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="349c7-108">Streams enable graphic chips to perform a direct memory access from multiple vertex buffers in parallel and also provide a more natural mapping from application data.</span></span> <span data-ttu-id="349c7-109">Außerdem ermöglichen Sie eine triviale Multitextur im Vergleich zu Multipass.</span><span class="sxs-lookup"><span data-stu-id="349c7-109">They also enable trivial multitexture versus multipass.</span></span> <span data-ttu-id="349c7-110">Sehen Sie sich dies wie folgt an:</span><span class="sxs-lookup"><span data-stu-id="349c7-110">Think of it like this:</span></span>

-   <span data-ttu-id="349c7-111">Ein Scheitelpunkt besteht aus n Streams.</span><span class="sxs-lookup"><span data-stu-id="349c7-111">A vertex is composed of n streams.</span></span>
-   <span data-ttu-id="349c7-112">Ein Stream besteht aus m-Elementen.</span><span class="sxs-lookup"><span data-stu-id="349c7-112">A stream is composed of m elements.</span></span>
-   <span data-ttu-id="349c7-113">Ein Element ist \[ Position, Farbe, normal, Textur Koordinate \] .</span><span class="sxs-lookup"><span data-stu-id="349c7-113">An element is \[position, color, normal, texture coordinate\].</span></span>

<span data-ttu-id="349c7-114">Die [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) -Methode bindet einen Scheitelpunkt Puffer an einen Gerätedaten Strom, wobei eine Zuordnung zwischen den Scheitelpunkt Daten und einem von mehreren datenstreamports erstellt wird, die die primitiven Verarbeitungsfunktionen übertragen.</span><span class="sxs-lookup"><span data-stu-id="349c7-114">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="349c7-115">Die tatsächlichen Verweise auf die Streamdaten treten erst auf, wenn eine Zeichnungs Methode, z. b. [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="349c7-115">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="349c7-116">Die Zuordnung der eingegebenen Scheitelpunkt Elemente zu den Vertex-Eingabe Registern für programmierbare Vertex-Shader wird in der Shader-Deklaration definiert, aber die eingegebenen Scheitelpunkt Elemente weisen keine bestimmte Semantik hinsichtlich ihrer Verwendung auf.</span><span class="sxs-lookup"><span data-stu-id="349c7-116">The mapping of the input vertex elements to the vertex input registers for programmable vertex shaders is defined in the shader declaration, but the input vertex elements do not have specific semantics about their use.</span></span> <span data-ttu-id="349c7-117">Die Interpretation der eingegebenen Scheitelpunkt Elemente wird mithilfe der shaderanweisungen programmiert.</span><span class="sxs-lookup"><span data-stu-id="349c7-117">The interpretation of the input vertex elements is programmed using the shader instructions.</span></span> <span data-ttu-id="349c7-118">Die Vertex-Shader-Funktion wird durch ein Array von Anweisungen definiert, die auf jeden Scheitelpunkt angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="349c7-118">The vertex shader function is defined by an array of instructions that are applied to each vertex.</span></span> <span data-ttu-id="349c7-119">Die Vertex-Ausgabe Register werden explizit mithilfe von Anweisungen in der Shader-Funktion in geschrieben.</span><span class="sxs-lookup"><span data-stu-id="349c7-119">The vertex output registers are explicitly written to, using instructions in the shader function.</span></span>

<span data-ttu-id="349c7-120">Für diese Erörterung sollten Sie jedoch weniger mit der semantischen Zuordnung von Elementen zu Registern und mehr über den Grund für die Verwendung von Streams und das Problem, das durch die Verwendung von Streams gelöst wird, befassen.</span><span class="sxs-lookup"><span data-stu-id="349c7-120">For this discussion, though, be less concerned with the semantic mapping of elements to registers and more concerned with the reason for using streams and what problem is solved by using streams.</span></span> <span data-ttu-id="349c7-121">Der Hauptvorteil von Streams besteht darin, dass Sie die Vertex-Datenkosten entfernen, die zuvor mit der multitexturierung verknüpft waren.</span><span class="sxs-lookup"><span data-stu-id="349c7-121">The main benefit of streams is that they remove the vertex data costs previously associated with multitexturing.</span></span> <span data-ttu-id="349c7-122">Vor Streams musste ein Benutzer entweder Vertex-Datasets duplizieren, um den Single-und Multitextur-Fall ohne nicht verwendete Datenelemente zu verarbeiten, oder es wurden keine Datenelemente übertragen, die mit Ausnahme des Multitextur-Falls nicht verwendet werden würden.</span><span class="sxs-lookup"><span data-stu-id="349c7-122">Before streams, a user had to either duplicate vertex data sets to handle the single and multitexture case with no unused data elements, or carry data elements that would be unused except in the multitexture case.</span></span>

<span data-ttu-id="349c7-123">Im folgenden finden Sie ein Beispiel für die Verwendung von zwei Sätzen von Vertex-Daten: eine für eine einzelne Textur und eine für die multitexturierung.</span><span class="sxs-lookup"><span data-stu-id="349c7-123">Here is an example of using two sets of vertex data, one for single texture and one for multitexturing.</span></span>


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="349c7-124">Die Alternative war, ein einzelnes Vertex-Element zu haben, das beide Sätze von Texturkoordinaten enthielt.</span><span class="sxs-lookup"><span data-stu-id="349c7-124">The alternative was to have a single vertex element that contained both sets of texture coordinates.</span></span>


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="349c7-125">Mit diesen Vertex-Daten wird nur eine Kopie der Positions-und Farbdaten in den Arbeitsspeicher übertragen. dabei werden beide Sätze von Texturkoordinaten für das Rendering selbst in der einzelnen Textur Groß-/Kleinschreibung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="349c7-125">With this vertex data, only one copy of the position and color data are carried in memory, at the expense of carrying both sets of texture coordinates around for rendering even in the single texture case.</span></span>

<span data-ttu-id="349c7-126">Nachdem der Kompromiss eindeutig ist, bieten Streams eine elegante Lösung für dieses Problem.</span><span class="sxs-lookup"><span data-stu-id="349c7-126">Now that the tradeoff is clear, streams provide an elegant fix to this dilemma.</span></span> <span data-ttu-id="349c7-127">Im folgenden finden Sie eine Reihe von Vertex-Definitionen zur Unterstützung von drei Streams: eine mit der Position und der Farbe, eine mit dem ersten Satz von Texturkoordinaten und eine mit dem zweiten Satz von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="349c7-127">Here is a set of vertex definitions to support three streams: one with position and color, one with the first set of texture coordinates, and one with the second set of texture coordinates.</span></span>


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



<span data-ttu-id="349c7-128">Die Vertex-Deklaration sieht folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="349c7-128">The vertex declaration would be as follows:</span></span>


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



<span data-ttu-id="349c7-129">Erstellen Sie nun das Vertex-Deklarations Objekt, und legen Sie es wie folgt fest:</span><span class="sxs-lookup"><span data-stu-id="349c7-129">Now create the vertex declaration object and set it as shown:</span></span>


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a><span data-ttu-id="349c7-130">Beispiele für Kombinationen</span><span class="sxs-lookup"><span data-stu-id="349c7-130">Examples of Combinations</span></span>

### <a name="one-stream-diffuse-color"></a><span data-ttu-id="349c7-131">Diffuse Farbe für einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="349c7-131">One Stream Diffuse Color</span></span>

<span data-ttu-id="349c7-132">Die Vertex-Deklaration und die streameinstellungen für das Rendering diffuses Farben würden wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="349c7-132">The vertex declaration and stream settings for diffuse color rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a><span data-ttu-id="349c7-133">Zwei Streams mit Farbe und Textur</span><span class="sxs-lookup"><span data-stu-id="349c7-133">Two Streams with Color and Texture</span></span>

<span data-ttu-id="349c7-134">Die Vertex-Deklaration und die streameinstellungen für ein einzelnes Textur Rendering würden wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="349c7-134">The vertex declaration and stream settings for single texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a><span data-ttu-id="349c7-135">Zwei Streams mit Farben und zwei Texturen</span><span class="sxs-lookup"><span data-stu-id="349c7-135">Two Streams with Color and two Textures</span></span>

<span data-ttu-id="349c7-136">Die Vertex-Deklaration und die streameinstellungen für das zwei-Textur-Rendering mit mehreren Texturen würden wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="349c7-136">The vertex declaration and stream settings for two-texture multi-texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



<span data-ttu-id="349c7-137">In jedem Fall genügt der folgende [**IDirect3DDevice9::D rawprimitiver**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) Aufruf.</span><span class="sxs-lookup"><span data-stu-id="349c7-137">In every case, the following [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) invocation suffices.</span></span>


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



<span data-ttu-id="349c7-138">Dies zeigt die Flexibilität von Datenströmen bei der Lösung des Problems bei der Datenübertragung über den Bus (d. h. zur Verschwendung von Bandbreite).</span><span class="sxs-lookup"><span data-stu-id="349c7-138">This shows the flexibility of streams in solving the problem of data duplication/redundant data transmission across the bus (that is, of wasting bandwidth).</span></span>

## <a name="related-topics"></a><span data-ttu-id="349c7-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="349c7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="349c7-140">Vertex-Deklaration</span><span class="sxs-lookup"><span data-stu-id="349c7-140">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
