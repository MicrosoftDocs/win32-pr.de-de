---
description: 'Sie erstellen ein Vertex-Puffer Objekt, indem Sie die IDirect3DDevice9:: createvertexbuffer-Methode aufrufen, die fünf Parameter akzeptiert.'
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Erstellen eines Scheitelpunkt Puffers (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc831ab508f14d61b8e42861f75422ff6a04bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343194"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="d0b0b-103">Erstellen eines Scheitelpunkt Puffers (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d0b0b-103">Creating a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="d0b0b-104">Sie erstellen ein Vertex-Puffer Objekt, indem Sie die [**IDirect3DDevice9:: createvertexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) -Methode aufrufen, die fünf Parameter akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-104">You create a vertex buffer object by calling the [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method, which accepts five parameters.</span></span> <span data-ttu-id="d0b0b-105">Der erste Parameter gibt die Vertex-Pufferlänge in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-105">The first parameter specifies the vertex buffer length, in bytes.</span></span> <span data-ttu-id="d0b0b-106">Verwenden Sie den sizeof-Operator, um die Größe eines Scheitelpunkt Formats in Bytes zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-106">Use the sizeof operator to determine the size of a vertex format, in bytes.</span></span> <span data-ttu-id="d0b0b-107">Beachten Sie das folgende benutzerdefinierte Scheitelpunkt Format.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-107">Consider the following custom vertex format.</span></span>


```
struct CUSTOMVERTEX {
        FLOAT x, y, z;
        FLOAT rhw;
        DWORD color;
        FLOAT tu, tv;   // Texture coordinates
};

// Custom flexible vertex format (FVF) describing the custom vertex structure
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)
```



<span data-ttu-id="d0b0b-108">Um einen Vertex-Puffer zum Speichern von vier CustomVertex-Strukturen zu erstellen, geben Sie \[ 4 \* sizeof (CustomVertex) \] für den *length* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-108">To create a vertex buffer to hold four CUSTOMVERTEX structures, specify \[4\*sizeof(CUSTOMVERTEX)\] for the *Length* parameter.</span></span>

<span data-ttu-id="d0b0b-109">Der zweite Parameter ist ein Satz von Verwendungs Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-109">The second parameter is a set of usage controls.</span></span> <span data-ttu-id="d0b0b-110">Unter anderem bestimmt der Wert, ob der Vertex-Puffer clippinginformationen in Form von Clip-Flags enthalten kann, die außerhalb des Anzeige Bereichs vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-110">Among other things, its value determines whether the vertex buffer is capable of containing clipping information - in the form of clip flags - for vertices that exist outside the viewing area.</span></span> <span data-ttu-id="d0b0b-111">Zum Erstellen eines Scheitelpunkt Puffers, der keine Clip-Flags enthalten kann, schließen Sie das D3DUSAGE \_ DoNotClip-Flag für den *Usage* -Parameter ein.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-111">To create a vertex buffer that cannot contain clip flags, include the D3DUSAGE\_DONOTCLIP flag for the *Usage* parameter.</span></span> <span data-ttu-id="d0b0b-112">Das \_ Flag D3DUSAGE DoNotClip wird nur angewendet, wenn Sie auch angeben, dass der Vertexpuffer transformierte Scheitel Punkte enthalten soll \_ . das Flag D3DFVF xyzrhw ist im Parameter " *f* ..." enthalten.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-112">The D3DUSAGE\_DONOTCLIP flag is applied only if you also indicate that the vertex buffer will contain transformed vertices - the D3DFVF\_XYZRHW flag is included in the *FVF* parameter.</span></span> <span data-ttu-id="d0b0b-113">Die [**IDirect3DDevice9:: samatevertexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) -Methode ignoriert das \_ Flag D3DUSAGE DoNotClip, wenn Sie angeben, dass der Puffer untransformierte Scheitel Punkte (das D3DFVF \_ XYZ-Flag) enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-113">The [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method ignores the D3DUSAGE\_DONOTCLIP flag if you indicate that the buffer will contain untransformed vertices (the D3DFVF\_XYZ flag).</span></span> <span data-ttu-id="d0b0b-114">Clippingflags belegen zusätzlichen Arbeitsspeicher, sodass ein Clipping-fähiger Vertex-Puffer etwas größer als ein Scheitelpunkt Puffer ist, der keine clippingflags enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-114">Clipping flags occupy additional memory, making a clipping-capable vertex buffer slightly larger than a vertex buffer incapable of containing clipping flags.</span></span> <span data-ttu-id="d0b0b-115">Da diese Ressourcen zugewiesen werden, wenn der Scheitelpunkt Puffer erstellt wird, müssen Sie im Voraus einen Clipping-fähigen Vertex-Puffer anfordern.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-115">Because these resources are allocated when the vertex buffer is created, you must request a clipping-capable vertex buffer ahead of time.</span></span>

<span data-ttu-id="d0b0b-116">Der dritte Parameter, " *f VF*", ist eine Kombination aus [D3DFVF](d3dfvf.md) , die das Scheitelpunkt Format des Scheitelpunkt Puffers beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-116">The third parameter, *FVF*, is a combination of [D3DFVF](d3dfvf.md) that describe the vertex format of the vertex buffer.</span></span> <span data-ttu-id="d0b0b-117">Wenn Sie für diesen Parameter den Wert 0 angeben, ist der Vertex-Puffer ein nicht-f-b-Puffer.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-117">If you specify 0 for this parameter, then the vertex buffer is a non-FVF vertex buffer.</span></span> <span data-ttu-id="d0b0b-118">Weitere Informationen finden Sie unter [f-Server-Vertex-Puffer (Direct3D 9)](fvf-vertex-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="d0b0b-118">For more information, see [FVF Vertex Buffers (Direct3D 9)](fvf-vertex-buffers.md).</span></span> <span data-ttu-id="d0b0b-119">Der vierte Parameter beschreibt die Speicher Klasse, in die der Scheitelpunkt Puffer platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-119">The fourth parameter describes the memory class into which to place the vertex buffer.</span></span>

<span data-ttu-id="d0b0b-120">Der letzte Parameter, den [**IDirect3DDevice9:: anatevertexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) akzeptiert, ist die Adresse einer Variablen, die mit einem Zeiger auf die neue [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) -Schnittstelle des Vertex-Puffer Objekts gefüllt wird, wenn der-Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-120">The final parameter that [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) accepts is the address of a variable that will be filled with a pointer to the new [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface of the vertex buffer object, if the call succeeds.</span></span>

<span data-ttu-id="d0b0b-121">Sie können keine Clip Flags für einen Vertex-Puffer erstellen, der ohne Unterstützung für Sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-121">You cannot produce clip flags for a vertex buffer that was created without support for them.</span></span>

<span data-ttu-id="d0b0b-122">Im folgenden C++-Codebeispiel wird gezeigt, wie das Erstellen eines Scheitelpunkt Puffers im Code aussehen könnte.</span><span class="sxs-lookup"><span data-stu-id="d0b0b-122">The following C++ code example shows what creating a vertex buffer might look like in code.</span></span>


```
   
// d3dDevice contains the address of an IDirect3DDevice9 interface
// g_pVB is a variable of type LPDIRECT3DVERTEXBUFFER9 

// The custom vertex type
struct CUSTOMVERTEX {
    FLOAT x, y, z;
    FLOAT rhw;
    DWORD color;
    FLOAT tu, tv;   // The texture coordinates
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)

// Create a clipping-capable vertex buffer. Allocate enough memory 
// in the default memory pool to hold three CUSTOMVERTEX 
// structures

    if( FAILED( d3dDevice->CreateVertexBuffer( 3*sizeof(CUSTOMVERTEX),
            0 /*Usage*/, D3DFVF_CUSTOMVERTEX, D3DPOOL_DEFAULT, &g_pVB, NULL ) ) )
        return E_FAIL;
```



## <a name="related-topics"></a><span data-ttu-id="d0b0b-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d0b0b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0b0b-124">Vertex-Puffer</span><span class="sxs-lookup"><span data-stu-id="d0b0b-124">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
