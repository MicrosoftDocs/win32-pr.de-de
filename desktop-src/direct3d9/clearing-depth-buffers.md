---
description: Viele C++-Anwendungen löschen den tiefen Puffer, bevor Sie jeden neuen Frame rendern.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Löschen von tiefen Puffern (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ad415b5c92e62da4f64eb590a0e202ffa3e0c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344827"
---
# <a name="clearing-depth-buffers-direct3d-9"></a><span data-ttu-id="ace8a-103">Löschen von tiefen Puffern (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ace8a-103">Clearing Depth Buffers (Direct3D 9)</span></span>

<span data-ttu-id="ace8a-104">Viele C++-Anwendungen löschen den tiefen Puffer, bevor Sie jeden neuen Frame rendern.</span><span class="sxs-lookup"><span data-stu-id="ace8a-104">Many C++ applications clear the depth buffer before rendering each new frame.</span></span> <span data-ttu-id="ace8a-105">Sie können den tiefen Puffer über Direct3D explizit löschen, indem Sie [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) aufrufen und D3DCLEAR \_ ZBuffer für den flags-Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="ace8a-105">You can explicitly clear the depth buffer through Direct3D by calling [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) and specifying D3DCLEAR\_ZBUFFER for the Flags parameter.</span></span> <span data-ttu-id="ace8a-106">Mit der **IDirect3DDevice9:: Clear** -Methode können Sie einen beliebigen tiefen Wert im Z-Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="ace8a-106">The **IDirect3DDevice9::Clear** method allows you to specify an arbitrary depth value in the Z parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ace8a-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ace8a-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ace8a-108">Tiefen Puffer</span><span class="sxs-lookup"><span data-stu-id="ace8a-108">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
