---
description: Ihre Anwendung bearbeitet Ressourcen, um eine Szene zu rendern.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Bearbeiten von Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0a9cf2ee85b2f8e86077eb525acffb914e60cba84082c9d610e10da9f5fa02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069050"
---
# <a name="manipulating-resources-direct3d-9"></a>Bearbeiten von Ressourcen (Direct3D 9)

Ihre Anwendung bearbeitet Ressourcen, um eine Szene zu rendern. Zunächst muss eine Anwendung eine Texturressource mit einer der folgenden Methoden erstellen:

-   [**IDirect3DDevice9::CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

Stattdessen kann eine Texturressource mit einer der Texturfunktionen D3DXCreatexxx erstellt werden.

Die Texturobjekte, die von den Texturerstellungsmethoden zurückgegeben werden, sind Container für Oberflächen oder Volumes. Diese Container werden allgemein als Puffer bezeichnet. Die Puffer im Besitz der Ressource erben die Verwendung, das Format und den Pool der Ressource, haben jedoch einen eigenen Typ. Weitere Informationen finden Sie unter [Ressourceneigenschaften (Direct3D 9).](resource-properties.md)

Die Anwendung erhält Zugriff auf die enthaltenen Oberflächen, um Grafiken zu laden, indem sie die folgenden Methoden aufruft. Weitere Informationen finden Sie unter [Sperren von Ressourcen (Direct3D 9).](locking-resources.md)

-   [**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [**IDirect3DVolumeTexture9::LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

Die Lock-Methoden verwenden Argumente, die die enthaltene Oberfläche (z. B. die Unterebene der Mipmap oder das Würfelgesicht der Textur) nennen, und geben Zeiger auf die Pixel zurück. Die typische Anwendung verwendet nie direkt ein Surface-Objekt.

Erstellen Sie geometry-orientierte Ressourcen, indem [**Sie IDirect3DDevice9::CreateIndexBuffer**](/windows/desktop/api) oder [**IDirect3DDevice9::CreateVertexBuffer aufrufen.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)

Sperren und füllen Sie die Pufferressourcen, indem Sie je nach Ressource [**entweder IDirect3DIndexBuffer9::Lock**](/windows/desktop/api) oder [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)aufrufen.

Bei verwalteten Texturressourcen endet der Ressourcenerstellungsprozess hier. Bei nicht verwalteten Texturressourcen werden Systemspeicherressourcen von einer Anwendung durch Aufrufen von [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)auf Geräteressourcen (für die Hardwarebeschleunigung) hochstürbt.

Um von Ressourcen gerenderte Bilder zu präsentieren, benötigt die Anwendung auch Farb- und Tiefen-Schablonenpuffer. Bei typischen Anwendungen befindet sich der Farbpuffer im Besitz der Austauschkette des Geräts, bei der es sich um eine Sammlung von Hintergrundpufferoberflächen handelt, und wird implizit mit dem Gerät erstellt. Tiefen-Schablonenoberflächen können implizit oder explizit mithilfe der [**IDirect3DDevice9::CreateDepthStencilSurface-Methode**](/windows/desktop/api) erstellt werden. Die Anwendung ordnet ein Gerät und seinen Tiefen- und Farbpuffer einem Aufruf von [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) oder [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface)zu.

Weitere Informationen zur Darstellung des endgültigen Bilds finden Sie unter [Presenting a Scene (Direct3D 9) (Präsentieren einer Szene (Direct3D 9)).](presenting-a-scene.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Ressourcen](direct3d-resources.md)
</dt> </dl>

 

 
