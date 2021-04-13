---
description: Direct3D verwaltet eine Liste mit bis zu acht aktuellen Texturen. Diese Texturen werden in alle primitiven, die gerendert werden, kombiniert. Nur Texturen, die als Textur Schnittstellen Zeiger erstellt wurden, können im Satz der aktuellen Texturen verwendet werden.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Zuweisen der aktuellen Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7ae6d603d9547841628f9395889095533cf3e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483982"
---
# <a name="assigning-the-current-textures-direct3d-9"></a><span data-ttu-id="ede33-105">Zuweisen der aktuellen Texturen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ede33-105">Assigning the Current Textures (Direct3D 9)</span></span>

<span data-ttu-id="ede33-106">Direct3D verwaltet eine Liste mit bis zu acht aktuellen Texturen.</span><span class="sxs-lookup"><span data-stu-id="ede33-106">Direct3D maintains a list of up to eight current textures.</span></span> <span data-ttu-id="ede33-107">Diese Texturen werden in alle primitiven, die gerendert werden, kombiniert.</span><span class="sxs-lookup"><span data-stu-id="ede33-107">It blends these textures onto all the primitive it renders.</span></span> <span data-ttu-id="ede33-108">Nur Texturen, die als Textur Schnittstellen Zeiger erstellt wurden, können im Satz der aktuellen Texturen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ede33-108">Only textures created as texture interface pointers can be used in the set of current textures.</span></span>

<span data-ttu-id="ede33-109">Anwendungen aufrufen die [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -Methode, um Texturen dem Satz der aktuellen Texturen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ede33-109">Applications call the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method to assign textures into the set of current textures.</span></span> <span data-ttu-id="ede33-110">Der erste Parameter muss eine Zahl im Bereich von 0-7 (einschließlich) sein.</span><span class="sxs-lookup"><span data-stu-id="ede33-110">The first parameter must be a number in the range of 0-7, inclusive.</span></span> <span data-ttu-id="ede33-111">Übergeben Sie den Textur Schnittstellen Zeiger als zweiten Parameter.</span><span class="sxs-lookup"><span data-stu-id="ede33-111">Pass the texture interface pointer as the second parameter.</span></span>

<span data-ttu-id="ede33-112">Im folgenden C++-Codebeispiel wird veranschaulicht, wie eine Textur dem Satz aktueller Texturen zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ede33-112">The following C++ code example demonstrates how a texture can be assigned to the set of current textures.</span></span>


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> <span data-ttu-id="ede33-113">Software Geräte unterstützen das Zuweisen einer Textur zu mehr als einer Textur Phase nicht gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="ede33-113">Software devices do not support assigning a texture to more than one texture stage at a time.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ede33-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ede33-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ede33-115">Textur Mischung</span><span class="sxs-lookup"><span data-stu-id="ede33-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
