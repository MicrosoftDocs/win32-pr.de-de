---
description: Standardmäßig ist es dem Direct3D-System gestattet, in den tiefen Puffer zu schreiben. Bei den meisten Anwendungen wird das Schreiben in den tiefen Puffer aktiviert, aber Sie können einige besondere Effekte erzielen, indem Sie dem Direct3D-System nicht gestatten, in den tiefen Puffer zu schreiben.
ms.assetid: d426ebff-bfce-4e5b-a97b-7b2539b4a9de
title: Ändern des Schreibzugriffs auf den Lesezugriff (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a261c4d30c9d0bd9edfbf07f765b2037e8195
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339688"
---
# <a name="changing-depth-buffer-write-access-direct3d-9"></a><span data-ttu-id="c426d-104">Ändern des Schreibzugriffs auf den Lesezugriff (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c426d-104">Changing Depth Buffer Write Access (Direct3D 9)</span></span>

<span data-ttu-id="c426d-105">Standardmäßig ist es dem Direct3D-System gestattet, in den tiefen Puffer zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c426d-105">By default, the Direct3D system is allowed to write to the depth buffer.</span></span> <span data-ttu-id="c426d-106">Bei den meisten Anwendungen wird das Schreiben in den tiefen Puffer aktiviert, aber Sie können einige besondere Effekte erzielen, indem Sie dem Direct3D-System nicht gestatten, in den tiefen Puffer zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c426d-106">Most applications leave writing to the depth buffer enabled, but you can achieve some special effects by not allowing the Direct3D system to write to the depth buffer.</span></span>

<span data-ttu-id="c426d-107">Sie können tiefe Puffer Schreibvorgänge in C++ deaktivieren, indem Sie die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode aufrufen, wobei der State-Parameter auf D3DRS \_ zbeschreib teenable und der value-Parameter auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c426d-107">You can disable depth buffer writes in C++ by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method with the State parameter set to D3DRS\_ZWRITEENABLE and the Value parameter set to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c426d-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c426d-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c426d-109">Tiefen Puffer</span><span class="sxs-lookup"><span data-stu-id="c426d-109">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
