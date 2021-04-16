---
description: Sie erstellen eine kubische Umgebungskarten Textur, indem Sie die createcubetexture-Methode aufrufen. Die Karten Texturen der kubischen Umgebung müssen quadratisch sein und zwei Dimensionen aufweisen.
ms.assetid: 3879d215-064b-4d7d-afae-2ed46569c8bf
title: Erstellen von kubischen Umgebungs Zuordnungs Oberflächen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36be3067c6a5f21c39cfed7cab731ca875b70799
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523835"
---
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a><span data-ttu-id="40ab6-104">Erstellen von kubischen Umgebungs Zuordnungs Oberflächen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="40ab6-104">Creating Cubic Environment Map Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="40ab6-105">Sie erstellen eine kubische Umgebungskarten Textur, indem Sie die [**createcubetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="40ab6-105">You create a cubic environment map texture by calling the [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) method.</span></span> <span data-ttu-id="40ab6-106">Die Karten Texturen der kubischen Umgebung müssen quadratisch sein und zwei Dimensionen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="40ab6-106">Cubic environment map textures must be square, with dimensions that are a power of two.</span></span>

<span data-ttu-id="40ab6-107">Im folgenden Codebeispiel wird gezeigt, wie Ihre C++-Anwendung eine einfache kubische Umgebungs Zuordnung erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="40ab6-107">The following code example shows how your C++ application might create a simple cubic environment map.</span></span>


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a><span data-ttu-id="40ab6-108">Zugreifen auf die Flächen der kubischen Umgebung</span><span class="sxs-lookup"><span data-stu-id="40ab6-108">Accessing Cubic Environment Map Faces</span></span>

<span data-ttu-id="40ab6-109">Sie können mithilfe der [**getcubemapsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) -Methode zwischen Flächen einer kubischen Umgebungs Zuordnung navigieren.</span><span class="sxs-lookup"><span data-stu-id="40ab6-109">You can navigate between faces of a cubic environment map by using the [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) method.</span></span>

<span data-ttu-id="40ab6-110">Im folgenden Codebeispiel wird [**getcubemapsurface verwendet, um die cubemapoberfläche**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) abzurufen, die für die positive y-Seite verwendet wird (Face 2).</span><span class="sxs-lookup"><span data-stu-id="40ab6-110">The following code example uses [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) to retrieve the cube-map surface used for the positive y-face (face 2).</span></span>


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



<span data-ttu-id="40ab6-111">Der erste Parameter, den [**getcubemapsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) annimmt, ist ein [**D3DCUBEMAP \_ Gesichter**](./d3dcubemap-faces.md) -Enumerationswert, der die angefügte Oberfläche beschreibt, die die Methode abrufen soll.</span><span class="sxs-lookup"><span data-stu-id="40ab6-111">The first parameter that [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) accepts is a [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md) enumerated value that describes the attached surface that the method should retrieve.</span></span> <span data-ttu-id="40ab6-112">Der zweite Parameter teilt Direct3D, welche Ebene einer mipzugeordneten cubetextur abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="40ab6-112">The second parameter tells Direct3D which level of a mipmapped cube texture to retrieve.</span></span> <span data-ttu-id="40ab6-113">Der dritte akzeptierte Parameter ist die Adresse der [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle, die die zurückgegebene cubetexturoberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="40ab6-113">The third parameter accepted is the address of the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the returned cube texture surface.</span></span> <span data-ttu-id="40ab6-114">Da diese cubemap nicht falsch zugeordnet ist, wird hier 0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="40ab6-114">Because this cube-map is not mipmapped, 0 is used here.</span></span>

> [!Note]
>
> <span data-ttu-id="40ab6-115">Nach dem Aufrufen dieser Methode wird der interne Verweis Zähler in der [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle erweitert.</span><span class="sxs-lookup"><span data-stu-id="40ab6-115">After calling this method, the internal reference count on the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface is increased.</span></span> <span data-ttu-id="40ab6-116">Wenn Sie diese Oberfläche verwenden, stellen Sie sicher, dass Sie die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methode auf dieser **IDirect3DSurface9** -Schnittstelle aufzurufen, oder Sie erhalten einen Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="40ab6-116">When you are done using this surface, be sure to call the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method on this **IDirect3DSurface9** interface or you will have a memory leak.</span></span>

 

## <a name="rendering-to-cubic-environment-maps"></a><span data-ttu-id="40ab6-117">Rendering in kubische Umgebungs Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="40ab6-117">Rendering to Cubic Environment Maps</span></span>

<span data-ttu-id="40ab6-118">Sie können Bilder in die einzelnen Flächen der cubemap kopieren, ebenso wie jedes andere Textur-oder Oberflächen Objekt.</span><span class="sxs-lookup"><span data-stu-id="40ab6-118">You can copy images to the individual faces of the cube map just like you would any other texture or surface object.</span></span> <span data-ttu-id="40ab6-119">Vor dem Rendern in eine Oberfläche müssen die Transformations Matrizen so festgelegt werden, dass die Kamera ordnungsgemäß positioniert ist, und in der richtigen Richtung auf die Vorderseite zeigt: vorwärts (+ z), rückwärts (-z), Links (-x), rechts (+ x), nach oben (+ y) oder nach unten (-y).</span><span class="sxs-lookup"><span data-stu-id="40ab6-119">The most important thing to do before rendering to a face is set the transformation matrices so that the camera is positioned properly and points in the proper direction for that face: forward (+z), backward (-z), left (-x), right (+x), up (+y), or down (-y).</span></span>

<span data-ttu-id="40ab6-120">Im folgenden C++-Codebeispiel wird eine Ansichts Matrix vorbereitet und entsprechend der geenderten Fläche festgelegt.</span><span class="sxs-lookup"><span data-stu-id="40ab6-120">The following C++ code example prepares and sets a view matrix according to the face being rendered.</span></span>


```
// Init pCubeMap to point to an IDirect3DCubeTexture9 interface
// Init d3dDevice to point to an IDirect3DDevice9 interface

void RenderFaces()
{
    // Save transformation matrices of the device
    D3DXMATRIX matProjSave, matViewSave;
    d3dDevice->GetTransform(D3DTS_VIEW,       &matViewSave ;
    d3dDevice->GetTransform(D3DTS_PROJECTION, &matProjSave);

    // Store the current back buffer and z-buffer
    LPDIRECT3DSURFACE9 pBackBuffer, pZBuffer;
    d3dDevice->GetRenderTarget(&pBackBuffer);
    d3dDevice->GetDepthStencilSurface(&pZBuffer);
```



<span data-ttu-id="40ab6-121">Beachten Sie, dass jedes Gesicht einer kubischen Umgebungs Zuordnung ein 90-Grad-Feld der Sicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="40ab6-121">Remember, each face of a cubic environment map represents a 90-degree field of view.</span></span> <span data-ttu-id="40ab6-122">Es sei denn, für Ihre Anwendung ist ein anderes Feld mit Ansichts Winkel erforderlich. für besondere Effekte sollten Sie z. b. darauf achten, die Projektions Matrix entsprechend festzulegen.</span><span class="sxs-lookup"><span data-stu-id="40ab6-122">Unless your application requires a different field of view angle - for special effects, for example - take care to set the projection matrix accordingly.</span></span>

<span data-ttu-id="40ab6-123">In diesem Codebeispiel wird eine Projektions Matrix für den gängigsten Fall erstellt und festgelegt.</span><span class="sxs-lookup"><span data-stu-id="40ab6-123">This code example creates and sets a projection matrix for the most common case.</span></span>


```
    // Use 90-degree field of view in the projection
    D3DMATRIX matProj;
    D3DXMatrixPerspectiveFovLH(matProj, D3DX_PI/2, 1.0f, 0.5f, 1000.0f);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProj);

    // Loop through the six faces of the cube map
    for(DWORD i=0; i<6; i++)
    {
        // Standard view that will be overridden below
        D3DVECTOR vEnvEyePt = D3DVECTOR(0.0f, 0.0f, 0.0f);
        D3DVECTOR vLookatPt, vUpVec;

        switch(i)
        {
            case D3DCUBEMAP_FACE_POSITIVE_X:
                vLookatPt = D3DVECTOR(1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_X:
                vLookatPt = D3DVECTOR(-1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Y:
                vLookatPt = D3DVECTOR(0.0f, 1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f,-1.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Y:
                vLookatPt = D3DVECTOR(0.0f,-1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f, 1.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Z:
                vLookatPt = D3DVECTOR( 0.0f, 0.0f, 1.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Z:
                vLookatPt = D3DVECTOR(0.0f, 0.0f,-1.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
        }

         D3DMATRIX matView;
         D3DXMatrixLookAtLH(matView, vEnvEyePt, vLookatPt, vUpVec);
         d3dDevice->SetTransform(D3DTS_VIEW, &matView);
```



<span data-ttu-id="40ab6-124">Wenn sich die Kamera in der Position befindet und die Projektions Matrix festgelegt ist, können Sie die Szene renden.</span><span class="sxs-lookup"><span data-stu-id="40ab6-124">When the camera is in position and the projection matrix set, you can render the scene.</span></span> <span data-ttu-id="40ab6-125">Jedes Objekt in der Szene sollte so positioniert werden, wie Sie es normalerweise positionieren würden.</span><span class="sxs-lookup"><span data-stu-id="40ab6-125">Each object in the scene should be positioned as you would normally position them.</span></span> <span data-ttu-id="40ab6-126">Das folgende Codebeispiel, das aus Gründen der Vollständigkeit bereitgestellt wird, skizziert diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="40ab6-126">The following code example, provided for completeness, outlines this task.</span></span>


```
        // Get pointer to surface in order to render to it
        LPDIRECT3DSURFACE9 pFace;
        pCubeMap->GetCubeMapSurface((D3DCUBEMAP_FACES)i, 0, &pFace);
        d3dDevice->SetRenderTarget (pFace , pZBuffer);
        SAFE_RELEASE(pFace);

        d3dDevice->BeginScene();
        // Render scene here
        ...
        d3dDevice->EndScene();
    }

    // Change the render target back to the main back buffer.
    d3dDevice->SetRenderTarget(pBackBuffer, pZBuffer);
    SAFE_RELEASE(pBackBuffer);
    SAFE_RELEASE(pZBuffer);

    // Restore the original transformation matrices
    d3dDevice->SetTransform(D3DTS_VIEW,       &matViewSave);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProjSave);
}
```



<span data-ttu-id="40ab6-127">Beachten Sie den aufzurufenden aufzurufenden Befehl [**der Methode "**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) "</span><span class="sxs-lookup"><span data-stu-id="40ab6-127">Note the call to the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="40ab6-128">Beim Rendern in den cubezuordnungs Flächen müssen Sie die Vorderseite als aktuelle Renderziel-Oberfläche zuweisen.</span><span class="sxs-lookup"><span data-stu-id="40ab6-128">When rendering to the cube map faces, you must assign the face as the current render-target surface.</span></span> <span data-ttu-id="40ab6-129">Anwendungen, die tiefen Puffer verwenden, können explizit einen tiefen Puffer für das Renderziel erstellen oder einen vorhandenen tiefen Puffer der renderzieloberfläche neu zuweisen.</span><span class="sxs-lookup"><span data-stu-id="40ab6-129">Applications that use depth buffers can explicitly create a depth-buffer for the render-target, or reassign an existing depth-buffer to the render-target surface.</span></span> <span data-ttu-id="40ab6-130">Im obigen Codebeispiel wird der letztere Ansatz verwendet.</span><span class="sxs-lookup"><span data-stu-id="40ab6-130">The code sample above uses the latter approach.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40ab6-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40ab6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40ab6-132">Kubische Umgebungs Zuordnung</span><span class="sxs-lookup"><span data-stu-id="40ab6-132">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
