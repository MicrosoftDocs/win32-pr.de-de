---
description: Ihre Anwendung bearbeitet Ressourcen, um eine Szene zu Rendering.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Bearbeiten von Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886dfee3af024d103dab8666687f1b053a5fb46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392329"
---
# <a name="manipulating-resources-direct3d-9"></a>Bearbeiten von Ressourcen (Direct3D 9)

Ihre Anwendung bearbeitet Ressourcen, um eine Szene zu Rendering. Zuerst muss eine Anwendung eine Textur Ressource mit einer der folgenden Methoden erstellen:

-   [**IDirect3DDevice9:: kreatecubetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**IDirect3DDevice9:: kreatetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**IDirect3DDevice9:: kreatevolumetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

Eine Textur Ressource kann stattdessen mit einer der D3DXCreatexxx Texturing-Funktionen erstellt werden.

Die Textur Objekte, die von den Textur Erstellungs Methoden zurückgegeben werden, sind Container für Oberflächen oder Volumes. Diese Container werden generisch als Puffer bezeichnet. Die Puffer, die sich im Besitz der Ressource befinden, erben die Verwendungen, das Format und den Pool der Ressource, haben aber ihren eigenen Typ. Weitere Informationen finden Sie unter [Ressourcen Eigenschaften (Direct3D 9)](resource-properties.md).

Die Anwendung erhält Zugriff auf die enthaltenen Oberflächen zum Zweck des Ladens von Grafiken durch Aufrufen der folgenden Methoden. Weitere Informationen finden Sie unter [Sperren von Ressourcen (Direct3D 9)](locking-resources.md).

-   [**IDirect3DCubeTexture9:: lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [**IDirect3DTexture9:: lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [**IDirect3DVolumeTexture9:: Lockbox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

Die Lock-Methoden verwenden Argumente, die die enthaltene Oberfläche anzeigen, z. b. die MipMap-Unterebene oder die cubeseite der Textur und geben Zeiger auf die Pixel zurück. Die typische Anwendung verwendet niemals direkt ein Surface-Objekt.

Erstellen Sie Geometrie orientierte Ressourcen durch Aufrufen von [**IDirect3DDevice9:: createindexbuffer**](/windows/desktop/api) oder [**IDirect3DDevice9:: createvertexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).

Sperren und füllen Sie die Puffer Ressourcen, indem Sie entweder [**IDirect3DIndexBuffer9:: Lock**](/windows/desktop/api) oder [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)aufrufen, abhängig von der Ressource.

Bei verwalteten Textur Ressourcen wird der Prozess der Ressourcen Erstellung hier beendet. Bei nicht verwalteten Textur Ressourcen stuft eine Anwendung Systemspeicher Ressourcen auf Geräte zugängliche Ressourcen (für die Hardwarebeschleunigung) durch Aufrufen von [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)herauf.

Zum Darstellen von Bildern, die aus Ressourcen gerendert werden, benötigt die Anwendung auch Farb-und tiefen Schablonen Puffer. Bei typischen Anwendungen gehört der Farb Puffer der Swapkette des Geräts an, bei der es sich um eine Sammlung von backpufferoberflächen handelt, die implizit mit dem Gerät erstellt wird. Tiefen Schablone können mithilfe der [**IDirect3DDevice9:: foatedepthstencilsurface**](/windows/desktop/api) -Methode implizit erstellt oder explizit erstellt werden. Die Anwendung ordnet ein Gerät und seine tiefe und ihren Farb Puffer einem [**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) -oder [**IDirect3DDevice9:: setdepthstencilsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface)-Befehl zu.

Ausführliche Informationen zur Darstellung des endgültigen Bilds finden Sie unter [präsentieren einer Szene (Direct3D 9)](presenting-a-scene.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Ressourcen](direct3d-resources.md)
</dt> </dl>

 

 
