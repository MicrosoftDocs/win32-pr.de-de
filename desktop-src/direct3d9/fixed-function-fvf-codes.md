---
description: Ein f-Code-Code beschreibt den Inhalt von Vertices, die in einem einzelnen Datenstrom verschachtelt werden.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Code der Fixed-Funktion (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346177"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a><span data-ttu-id="1f5eb-103">Code der Fixed-Funktion (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1f5eb-103">Fixed Function FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="1f5eb-104">Ein f-Code-Code beschreibt den Inhalt von Vertices, die in einem einzelnen Datenstrom verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-104">A FVF code describes the contents of vertices stored interleaved in a single data stream.</span></span> <span data-ttu-id="1f5eb-105">Im Allgemeinen werden die Daten angegeben, die von der Pipeline für die Verarbeitung fester Funktionen verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-105">It generally specifies data to be processed by the fixed function vertex processing pipeline.</span></span> <span data-ttu-id="1f5eb-106">Dies ist eine Scheitelpunkt Deklaration im älteren Stil. um den aktuellen Scheitelpunkt Deklarations Stil anzuzeigen, finden Sie weitere Informationen unter [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="1f5eb-106">This is an older-style vertex declaration; to see the current vertex declaration style, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="1f5eb-107">Direct3D-Anwendungen können Modell Vertices auf verschiedene Weise definieren.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-107">Direct3D applications can define model vertices in several different ways.</span></span> <span data-ttu-id="1f5eb-108">Die Unterstützung von flexiblen Scheitelpunkt Definitionen, auch als flexible Scheitelpunkt Formate oder flexible Scheitelpunkt Formate bezeichnet, ermöglicht es der Anwendung, nur die zu verwendenden Scheitelpunkt Komponenten zu verwenden, sodass die Komponenten, die nicht verwendet werden, ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-108">Support for flexible vertex definitions, also known as flexible vertex formats or flexible vertex format codes, makes it possible for your application to use only the vertex components it needs, eliminating those components that aren't used.</span></span> <span data-ttu-id="1f5eb-109">Wenn Sie nur die erforderlichen Scheitelpunkt Komponenten verwenden, kann Ihre Anwendung Arbeitsspeicher einsparen und die Verarbeitungs Bandbreite minimieren, die zum Rendering von Modellen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-109">By using only the needed vertex components, your application can conserve memory and minimize the processing bandwidth required to render models.</span></span> <span data-ttu-id="1f5eb-110">Sie beschreiben, wie die Vertices formatiert werden, indem Sie eine Kombination aus [D3DFVF](d3dfvf.md) Codes verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-110">You describe how your vertices are formatted by using a combination of [D3DFVF](d3dfvf.md) codes.</span></span>

<span data-ttu-id="1f5eb-111">Die Spezifikation "f VF" umfasst Formate für die Punktgröße, die durch D3DFVF \_ Psize angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-111">The FVF specification includes formats for point size, specified by D3DFVF\_PSIZE.</span></span> <span data-ttu-id="1f5eb-112">Diese Größe wird in Kamera Raumeinheiten für nicht transformierte und beleuchtete Scheitel Punkte (TL) und in Einheiten für die Speichereinheiten für TL-Scheitel Punkte ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-112">This size is expressed in camera space units for non-transformed and lit (TL) vertices, and in device-space units for TL vertices.</span></span>

<span data-ttu-id="1f5eb-113">Die Renderingmethoden der [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle stellen C++-Anwendungen Methoden bereit, die eine Kombination dieser Flags akzeptieren, und verwenden Sie, um zu bestimmen, wie primitive gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-113">The rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface provide C++ applications with methods that accept a combination of these flags, and use them to determine how to render primitives.</span></span> <span data-ttu-id="1f5eb-114">Im Grunde weisen diese Flags das System an, welche Scheitelpunkt Komponenten Positions-, Vertex-Mischungs Gewichtungen, normal, Farben und die Anzahl und das Format von Texturkoordinaten verwenden. Ihre Anwendung verwendet und, indirekt, welche Teile der Renderingpipeline, auf die Direct3D angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-114">Basically, these flags tell the system which vertex components - position, vertex blending weights, normal, colors, and the number and format of texture coordinates - your application uses and, indirectly, which parts of the rendering pipeline you want Direct3D to apply to them.</span></span> <span data-ttu-id="1f5eb-115">Außerdem kommuniziert das vorhanden sein oder Fehlen eines bestimmten Scheitelpunkt Formatflags mit dem System, welche vertexkomponentenfelder im Arbeitsspeicher vorhanden sind und welche ausgelassen wurden.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-115">In addition, the presence or absence of a particular vertex format flag communicates to the system which vertex component fields are present in memory and which you've omitted.</span></span>

<span data-ttu-id="1f5eb-116">Um die Geräte Einschränkungen zu ermitteln, können Sie ein Gerät nach den Werten von D3DFVFCAPS \_ donotstripelements und D3DFVFCAPS \_ texcoordrattmask im fvfcaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)Abfragen.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-116">To determine device limitations, you can query a device for the values of D3DFVFCAPS\_DONOTSTRIPELEMENTS and D3DFVFCAPS\_TEXCOORDCOUNTMASK in the FVFCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="1f5eb-117">Texturkoordinaten können in unterschiedlichen Formaten deklariert werden, sodass Texturen mit nur einer Koordinate oder bis zu vier Texturkoordinaten (bei 2D-projizierten Texturkoordinaten) adressiert werden können.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-117">Texture coordinates can be declared in different formats, allowing textures to be addressed using as few as one coordinate or as many as four texture coordinates (for 2D projected texture coordinates).</span></span> <span data-ttu-id="1f5eb-118">Weitere Informationen finden Sie unter [Texturkoordinaten Formate (Direct3D 9)](texture-coordinate-formats.md).</span><span class="sxs-lookup"><span data-stu-id="1f5eb-118">For more information, see [Texture Coordinate Formats (Direct3D 9)](texture-coordinate-formats.md).</span></span> <span data-ttu-id="1f5eb-119">Verwenden Sie den [**D3DFVF \_ texcoordsizen**](d3dfvf-texcoordsizen.md) -Satz von Makros, um Bitmuster zu erstellen, mit denen die Texturkoordinaten Formate identifiziert werden, die im Vertex-Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-119">Use the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros to create bit patterns that identify the texture coordinate formats that your vertex format uses.</span></span>

<span data-ttu-id="1f5eb-120">Jede-Komponente wird von keiner Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-120">No application will use every component.</span></span> <span data-ttu-id="1f5eb-121">Die normalen Felder "gegenseitige homogene W" und "Scheitelpunkt" schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-121">The reciprocal homogeneous W (RHW) and vertex normal fields are mutually exclusive.</span></span> <span data-ttu-id="1f5eb-122">Die meisten Anwendungen versuchen auch, alle acht Sätze von Texturkoordinaten zu verwenden, aber Direct3D hat diese Kapazität.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-122">Nor will most applications try to use all eight sets of texture coordinates, but Direct3D has this capacity.</span></span> <span data-ttu-id="1f5eb-123">Es gibt mehrere Einschränkungen hinsichtlich der Flags, die Sie mit anderen Flags verwenden können.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-123">There are several restrictions on which flags you can use with other flags.</span></span> <span data-ttu-id="1f5eb-124">Beispielsweise können Sie die \_ Flags D3DFVF XYZ und D3DFVF \_ xyzrhw nicht gleichzeitig verwenden, da dies darauf hindeuten würde, dass Ihre Anwendung die Position eines Scheitel Punkts mit nicht transformierten und transformierten Vertices beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-124">For example, you cannot use the D3DFVF\_XYZ and D3DFVF\_XYZRHW flags together, as this would indicate that your application is describing a vertex's position with both untransformed and transformed vertices.</span></span>

<span data-ttu-id="1f5eb-125">Um indizierte vertexmischungs Zeichen zu verwenden, sollte das D3DFVF \_ lastbeta \_ UBYTE4-Flag am Ende der FVF-Deklaration angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-125">To use indexed vertex blending, the D3DFVF\_LASTBETA\_UBYTE4 flag should appear at the end of the FVF declaration.</span></span> <span data-ttu-id="1f5eb-126">Das vorhanden sein dieses Flags gibt an, dass das fünfte Mischungs Gewicht als DWORD und nicht als float behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-126">The presence of this flag indicates that the fifth blending weight will be treated as a DWORD instead of float.</span></span> <span data-ttu-id="1f5eb-127">Weitere Informationen finden Sie unter [indiziertes Vertex-Blending (Direct3D 9)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="1f5eb-127">For more information, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span>

<span data-ttu-id="1f5eb-128">Die folgenden Codebeispiele zeigen den Unterschied zwischen einem f-Code, der das D3DFVF \_ lastbeta \_ UBYTE4-Flag verwendet, und einem, das nicht ist.</span><span class="sxs-lookup"><span data-stu-id="1f5eb-128">The following code samples shows the difference between an FVF code that uses the D3DFVF\_LASTBETA\_UBYTE4 flag and one that doesn't.</span></span> <span data-ttu-id="1f5eb-129">Das Flag D3DFVF \_ XYZB3 ist vorhanden, wenn vier Mischungs Indizes verwendet werden, weil Sie immer die Summe der ersten drei Werte von der Zahl 1 subtrahieren, um die vierte zu erhalten (Blend ₄ = 1-(Blend ₁ + Blend-Taste + Blend ₃)).</span><span class="sxs-lookup"><span data-stu-id="1f5eb-129">The flag D3DFVF\_XYZB3 is present when four blending indices are used because you always subtract the sum of the first three from the number one to obtain the fourth (blend₄ = 1 - (blend₁ + blend₂ + blend₃)).</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



<span data-ttu-id="1f5eb-130">Die unten definierte "f VF" verwendet das Flag "D3DFVF \_ Last \_ UBYTE4".</span><span class="sxs-lookup"><span data-stu-id="1f5eb-130">The FVF defined below uses the D3DFVF\_LAST\_UBYTE4 flag.</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a><span data-ttu-id="1f5eb-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1f5eb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f5eb-132">Vertex-Deklaration</span><span class="sxs-lookup"><span data-stu-id="1f5eb-132">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
