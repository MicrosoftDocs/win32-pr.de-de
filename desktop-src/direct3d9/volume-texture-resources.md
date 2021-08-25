---
description: Volumentexturen sind dreidimensionale Sammlungen von Pixeln (Texel), die verwendet werden können, um ein zweidimensionales Primitiv wie ein Dreieck oder eine Linie zu zeichnen.
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: Volumetexturressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17e72448fd1fd4856cf81a344f5c176fdb6272546468126975edbff8b20218d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984355"
---
# <a name="volume-texture-resources-direct3d-9"></a>Volumetexturressourcen (Direct3D 9)

Volumentexturen sind dreidimensionale Sammlungen von Pixeln (Texel), die verwendet werden können, um ein zweidimensionales Primitiv wie ein Dreieck oder eine Linie zu zeichnen. Für jeden Scheitelpunkt eines Primitiven, der mit einem Volume texturiert werden soll, sind Texturkoordinaten mit drei Elementen erforderlich. Beim Zeichnen des Primitivs wird jedes enthaltene Pixel mit dem Farbwert von einem Pixel innerhalb des Volumes gefüllt, entsprechend den Regeln, die dem zweidimensionalen Texturfall entsprechen. Volumes werden nicht direkt gerendert, da es keine dreidimensionalen Primitive gibt, die mit ihnen gezeichnet werden können.

Sie können Volumentexturen für sonderliche Effekte wie patchige Oberflächen, Explosionen usw. verwenden.

Volumes sind in Slices organisiert und können als Breite x Höhe 2D-Oberflächen gestapelt angesehen werden, um eine Breite x Höhe x Tiefenvolumen zu erstellen. Jeder Slice ist eine einzelne Zeile. Volumes können nachfolgende Ebenen aufweisen, in denen die Dimensionen der einzelnen Ebenen auf die Hälfte der Dimensionen der vorherigen Ebene abgeschnitten werden. Das folgende Diagramm zeigt, wie eine Volumentextur mit mehreren Ebenen aussieht.

![Diagramm einer Volumetextur mit 8x2x4-, 4x1x2- und 2x1x1-Cubedarstellungen](images/level123.png)

## <a name="creating-a-volume-texture"></a>Erstellen einer Volumetextur

Die folgenden Codebeispiele zeigen die Schritte, die für die Verwendung einer Volumentextur erforderlich sind.

Geben Sie zunächst einen benutzerdefinierten Scheitelpunkttyp an, der über drei Texturkoordinaten für jeden Scheitelpunkt verfügt, wie in diesem Codebeispiel gezeigt.


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



Füllen Sie als Nächstes die Scheitelpunkte mit Daten aus.


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



Erstellen Sie nun einen Scheitelpunktpuffer, und füllen Sie ihn mit Daten aus den Scheitelpunkten aus.

Der nächste Schritt besteht darin, die [**IDirect3DDevice9::CreateVolumeTexture-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) zu verwenden, um eine Volumetextur zu erstellen, wie in diesem Codebeispiel gezeigt.


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



Legen Sie vor dem Rendern des Primitiven die aktuelle Textur auf die oben erstellte Volumetextur fest. Das folgende Codebeispiel zeigt den gesamten Renderingprozess für einen Dreiecksstreifen.


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

 

 
