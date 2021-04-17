---
description: Volumetexturen sind dreidimensionale Auflistungen von Pixeln (texeln), mit denen ein zweidimensionales primitiv gezeichnet werden kann, z. b. ein Dreieck oder eine Linie.
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: Volumetextur-Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c66ff97d04e3c7c6c0a032f9a230dfd511b38c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104557716"
---
# <a name="volume-texture-resources-direct3d-9"></a>Volumetextur-Ressourcen (Direct3D 9)

Volumetexturen sind dreidimensionale Auflistungen von Pixeln (texeln), mit denen ein zweidimensionales primitiv gezeichnet werden kann, z. b. ein Dreieck oder eine Linie. Für jeden Scheitelpunkt eines primitiven, der mit einem Volume strukturiert werden soll, sind drei-Element-Texturkoordinaten erforderlich. Wenn das primitive gezeichnet wird, wird jedes enthaltene Pixel mit dem Farbwert von einem Pixel innerhalb des Volumes gefüllt, und zwar entsprechend den Regeln der zweidimensionalen Textur. Volumes werden nicht direkt gerendert, da keine dreidimensionalen primitiven vorhanden sind, die mit Ihnen gezeichnet werden können.

Volumetexturen können für besondere Effekte verwendet werden, z. b. für den Nebel, die Explosionen usw.

Volumes sind in Slices angeordnet und können als Breite x Höhe 2D-Oberflächen gestapelt werden, um eine Breite x-Tiefe von Höhen zu bilden. Jeder Slice ist eine einzelne Zeile. Volumes können nachfolgende Ebenen aufweisen, bei denen die Dimensionen der einzelnen Ebenen auf die Hälfte der Dimensionen der vorherigen Ebene gekürzt werden. Das folgende Diagramm zeigt, wie eine volumetextur mit mehreren Ebenen aussieht.

![Diagramm einer volumetextur mit 8x2x4, 4x1x2 und 2x1x1-cubedarstellungen](images/level123.png)

## <a name="creating-a-volume-texture"></a>Erstellen einer volumetextur

Die folgenden Codebeispiele zeigen die Schritte, die für die Verwendung einer Volumestruktur erforderlich sind.

Geben Sie zunächst einen benutzerdefinierten Scheitelpunkt mit drei Texturkoordinaten für jeden Scheitelpunkt an, wie in diesem Codebeispiel dargestellt.


```
struct VOLUMEVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu, tv, tw;
};

#define D3DFVF_VOLUMEVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|
                             D3DFVF_TEX1|D3DFVF_TEXCOORDSIZE3(0))
```



Füllen Sie als nächstes die Scheitel Punkte mit Daten.


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



Erstellen Sie nun einen Scheitelpunkt Puffer, und füllen Sie ihn mit Daten aus den Scheitel Punkten aus.

Der nächste Schritt besteht in der Verwendung der [**IDirect3DDevice9:: kreatevolumetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) -Methode zum Erstellen einer Volumestruktur, wie in diesem Codebeispiel gezeigt.


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



Legen Sie vor dem Rendern des primitiven die aktuelle Textur auf die oben erstellte volumetextur fest. Das folgende Codebeispiel zeigt den gesamten Renderingprozess für einen Dreiecke.


```
if( SUCCEEDED( d3dDevice->BeginScene() ) )
{
    // Draw the quad, with the volume texture.
    d3dDevice->SetTexture( 0, pVolumeTexture );
    d3dDevice->SetFVF( D3DFVF_VOLUMEVERTEX );
    d3dDevice->SetStreamSource( 0, pVB, sizeof(VOLUMEVERTEX) );
    d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 2);

   // End the scene.
   d3dDevice->EndScene();
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
