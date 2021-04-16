---
description: Tiefen Puffer werden dem Gerät zugeordnet.
ms.assetid: c4faab8d-17cf-4202-9a39-c609fc975558
title: Bearbeiten des tiefen Puffers (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe32f950ec2897d0effb2dfbeded577158e4638b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520491"
---
# <a name="manipulating-the-depth-buffer-direct3d-9"></a><span data-ttu-id="84aa8-103">Bearbeiten des tiefen Puffers (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="84aa8-103">Manipulating the Depth Buffer (Direct3D 9)</span></span>

<span data-ttu-id="84aa8-104">Tiefen Puffer werden dem Gerät zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="84aa8-104">Depth buffers are associated with the device.</span></span> <span data-ttu-id="84aa8-105">Anwendungen müssen die tiefen Puffer verschieben, wenn Sie Renderziele festlegen.</span><span class="sxs-lookup"><span data-stu-id="84aa8-105">Applications are required to move the depth buffers when they set render targets.</span></span> <span data-ttu-id="84aa8-106">Die [**IDirect3DDevice9:: getdepthstencilsurface**](/windows/desktop/api) -Methode und die [**IDirect3DDevice9:: setdepthstencilsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) -Methode werden verwendet, um Tiefe Puffer zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="84aa8-106">The [**IDirect3DDevice9::GetDepthStencilSurface**](/windows/desktop/api) and [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) methods are used to manipulate depth buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84aa8-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="84aa8-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84aa8-108">Präsentieren einer Szene</span><span class="sxs-lookup"><span data-stu-id="84aa8-108">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 
