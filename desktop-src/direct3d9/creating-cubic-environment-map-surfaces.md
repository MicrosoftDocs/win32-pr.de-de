---
description: Sie erstellen eine kubische Umgebungszuordnungstextur, indem Sie die CreateCubeTexture-Methode aufrufen. Kubische Umgebungszuordnungstexturen müssen quadratisch sein, mit Dimensionen, die eine Zweierkraft haben.
ms.assetid: 3879d215-064b-4d7d-afae-2ed46569c8bf
title: Erstellen kubischer Umgebungszuordnungsoberflächen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b37321978a40170d47718318e4b3f6898ba04d5fa229e97ada47e08e589fdcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608020"
---
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a>Erstellen kubischer Umgebungszuordnungsoberflächen (Direct3D 9)

Sie erstellen eine kubische Umgebungszuordnungstextur, indem Sie [**die CreateCubeTexture-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) aufrufen. Kubische Umgebungszuordnungstexturen müssen quadratisch sein, mit Dimensionen, die eine Zweierkraft haben.

Das folgende Codebeispiel zeigt, wie Ihre C++-Anwendung eine einfache kubische Umgebungszuordnung erstellen kann.


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a>Zugreifen auf kubische Umgebungszuordnungsgesichter

Sie können mithilfe der [**GetCubeMapSurface-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) zwischen Gesichtern einer kubischen Umgebungskarte navigieren.

Im folgenden Codebeispiel wird [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) verwendet, um die Cubemapoberfläche abzurufen, die für das positive y-Gesicht (Gesicht 2) verwendet wird.


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



Der erste Parameter, den [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) akzeptiert, ist ein [**aufzählter D3DCUBEMAP \_ FACES-Wert,**](./d3dcubemap-faces.md) der die angefügte Oberfläche beschreibt, die die Methode abrufen soll. Der zweite Parameter teilt Direct3D mit, welche Ebene einer mipmappen Cubetextur abgerufen werden soll. Der dritte akzeptierte Parameter ist die Adresse der [**IDirect3DSurface9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) die die zurückgegebene Cubetexturoberfläche darstellt. Da diese Cubezuordnung nicht mipmapped ist, wird hier 0 verwendet.

> [!Note]
>
> Nach dem Aufruf dieser Methode wird die interne Verweisanzahl für die [**IDirect3DSurface9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) erhöht. Wenn Sie diese Oberfläche nicht mehr verwenden, rufen Sie unbedingt die [**IUnknown-Methode**](/windows/win32/api/unknwn/nn-unknwn-iunknown) auf dieser **IDirect3DSurface9-Schnittstelle** auf, da ein Arbeitsspeicherverlust vorlag.

 

## <a name="rendering-to-cubic-environment-maps"></a>Rendern in kubische Karten

Sie können Bilder auf die einzelnen Gesichter der Cube map kopieren, wie Sie es bei jedem anderen Textur- oder Oberflächenobjekt machen würden. Das Wichtigste vor dem Rendern in einem Gesicht ist, die Transformationsmatrizen so zu setzen, dass die Kamera ordnungsgemäß positioniert ist und in der richtigen Richtung für dieses Gesicht zeigt: vorwärts (+z), rückwärts (-z), links (-x), rechts (+x), nach oben (+y) oder nach unten (-y).

Im folgenden C++-Codebeispiel wird eine Ansichtsmatrix entsprechend dem gerenderten Gesicht vorbereitet und definiert.


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



Denken Sie daran, dass jedes Gesicht einer kubischen Umgebungskarte ein 90-Grad-Sichtfeld darstellt. Wenn Ihre Anwendung nicht einen anderen Sichtwinkel erfordert , z. B. für Sondereffekte, achten Sie darauf, die Projektionsmatrix entsprechend zu setzen.

In diesem Codebeispiel wird eine Projektionsmatrix für den gängigsten Fall erstellt und definiert.


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



Wenn sich die Kamera in Position befindet und die Projektionsmatrix festgelegt ist, können Sie die Szene rendern. Jedes Objekt in der Szene sollte so positioniert sein, wie Sie es normalerweise positionieren würden. Im folgenden Codebeispiel, das der Vollständigkeit halber bereitgestellt wird, wird diese Aufgabe beschrieben.


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



Beachten Sie den Aufruf der [**SetRenderTarget-Methode.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) Beim Rendern auf die Cubemapgesichter müssen Sie das Gesicht als aktuelle Renderzieloberfläche zuweisen. Anwendungen, die Tiefenpuffer verwenden, können explizit einen Tiefenpuffer für das Renderziel erstellen oder einen vorhandenen Tiefenpuffer der Renderzieloberfläche neu zuweisen. Im obigen Codebeispiel wird der zweite Ansatz verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kubische Umgebungszuordnung](cubic-environment-mapping.md)
</dt> </dl>

 

 
