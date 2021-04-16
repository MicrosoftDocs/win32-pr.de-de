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
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a>Erstellen von kubischen Umgebungs Zuordnungs Oberflächen (Direct3D 9)

Sie erstellen eine kubische Umgebungskarten Textur, indem Sie die [**createcubetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) -Methode aufrufen. Die Karten Texturen der kubischen Umgebung müssen quadratisch sein und zwei Dimensionen aufweisen.

Im folgenden Codebeispiel wird gezeigt, wie Ihre C++-Anwendung eine einfache kubische Umgebungs Zuordnung erstellen kann.


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a>Zugreifen auf die Flächen der kubischen Umgebung

Sie können mithilfe der [**getcubemapsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) -Methode zwischen Flächen einer kubischen Umgebungs Zuordnung navigieren.

Im folgenden Codebeispiel wird [**getcubemapsurface verwendet, um die cubemapoberfläche**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) abzurufen, die für die positive y-Seite verwendet wird (Face 2).


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



Der erste Parameter, den [**getcubemapsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) annimmt, ist ein [**D3DCUBEMAP \_ Gesichter**](./d3dcubemap-faces.md) -Enumerationswert, der die angefügte Oberfläche beschreibt, die die Methode abrufen soll. Der zweite Parameter teilt Direct3D, welche Ebene einer mipzugeordneten cubetextur abgerufen werden soll. Der dritte akzeptierte Parameter ist die Adresse der [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle, die die zurückgegebene cubetexturoberfläche darstellt. Da diese cubemap nicht falsch zugeordnet ist, wird hier 0 verwendet.

> [!Note]
>
> Nach dem Aufrufen dieser Methode wird der interne Verweis Zähler in der [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle erweitert. Wenn Sie diese Oberfläche verwenden, stellen Sie sicher, dass Sie die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methode auf dieser **IDirect3DSurface9** -Schnittstelle aufzurufen, oder Sie erhalten einen Speicherplatz.

 

## <a name="rendering-to-cubic-environment-maps"></a>Rendering in kubische Umgebungs Zuordnungen

Sie können Bilder in die einzelnen Flächen der cubemap kopieren, ebenso wie jedes andere Textur-oder Oberflächen Objekt. Vor dem Rendern in eine Oberfläche müssen die Transformations Matrizen so festgelegt werden, dass die Kamera ordnungsgemäß positioniert ist, und in der richtigen Richtung auf die Vorderseite zeigt: vorwärts (+ z), rückwärts (-z), Links (-x), rechts (+ x), nach oben (+ y) oder nach unten (-y).

Im folgenden C++-Codebeispiel wird eine Ansichts Matrix vorbereitet und entsprechend der geenderten Fläche festgelegt.


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



Beachten Sie, dass jedes Gesicht einer kubischen Umgebungs Zuordnung ein 90-Grad-Feld der Sicht darstellt. Es sei denn, für Ihre Anwendung ist ein anderes Feld mit Ansichts Winkel erforderlich. für besondere Effekte sollten Sie z. b. darauf achten, die Projektions Matrix entsprechend festzulegen.

In diesem Codebeispiel wird eine Projektions Matrix für den gängigsten Fall erstellt und festgelegt.


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



Wenn sich die Kamera in der Position befindet und die Projektions Matrix festgelegt ist, können Sie die Szene renden. Jedes Objekt in der Szene sollte so positioniert werden, wie Sie es normalerweise positionieren würden. Das folgende Codebeispiel, das aus Gründen der Vollständigkeit bereitgestellt wird, skizziert diese Aufgabe.


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



Beachten Sie den aufzurufenden aufzurufenden Befehl [**der Methode "**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) " Beim Rendern in den cubezuordnungs Flächen müssen Sie die Vorderseite als aktuelle Renderziel-Oberfläche zuweisen. Anwendungen, die tiefen Puffer verwenden, können explizit einen tiefen Puffer für das Renderziel erstellen oder einen vorhandenen tiefen Puffer der renderzieloberfläche neu zuweisen. Im obigen Codebeispiel wird der letztere Ansatz verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kubische Umgebungs Zuordnung](cubic-environment-mapping.md)
</dt> </dl>

 

 
