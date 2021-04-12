---
description: Eine Mischungs Stufe ist ein Satz von Textur Vorgängen und ihren Argumenten, die definieren, wie Texturen gemischt werden.
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: Erstellen von Mischungs Stufen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126881"
---
# <a name="creating-blending-stages-direct3d-9"></a><span data-ttu-id="513d3-103">Erstellen von Mischungs Stufen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="513d3-103">Creating Blending Stages (Direct3D 9)</span></span>

<span data-ttu-id="513d3-104">Eine Mischungs Stufe ist ein Satz von Textur Vorgängen und ihren Argumenten, die definieren, wie Texturen gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="513d3-104">A blending stage is a set of texture operations and their arguments that define how textures are blended.</span></span> <span data-ttu-id="513d3-105">Beim Erstellen einer Mischungs Phase rufen C++-Anwendungen die [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="513d3-105">When making a blending stage, C++ applications invoke the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="513d3-106">Der erste-Befehl gibt den Vorgang an, der ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="513d3-106">The first call specifies the operation that is performed.</span></span> <span data-ttu-id="513d3-107">Zwei weitere Aufrufe definieren die Argumente, auf die der Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="513d3-107">Two additional invocations define the arguments to which the operation is applied.</span></span> <span data-ttu-id="513d3-108">Im folgenden Codebeispiel wird die Erstellung einer Mischungs Stufe veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="513d3-108">The following code example illustrates the creation of a blending stage.</span></span>


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



<span data-ttu-id="513d3-109">Texel-Daten in Texturen enthalten Farb-und Alpha Werte.</span><span class="sxs-lookup"><span data-stu-id="513d3-109">Texel data in textures contain color and alpha values.</span></span> <span data-ttu-id="513d3-110">Anwendungen können separate Vorgänge für Farb-und Alpha Werte in einer einzelnen Mischungs Stufe definieren.</span><span class="sxs-lookup"><span data-stu-id="513d3-110">Applications can define separate operations for both color and alpha values in a single blending stage.</span></span> <span data-ttu-id="513d3-111">Jeder Vorgang, jede Farbe und jedes Alpha hat seine eigenen Argumente.</span><span class="sxs-lookup"><span data-stu-id="513d3-111">Each operation, color, and alpha, has its own arguments.</span></span> <span data-ttu-id="513d3-112">Weitere Informationen finden Sie unter [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span><span class="sxs-lookup"><span data-stu-id="513d3-112">For details, see [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

<span data-ttu-id="513d3-113">Obwohl Sie nicht Teil der Direct3D-API sind, können Sie die folgenden Makros in Ihre Anwendung einfügen, um den Code abzukürzen, der zum Erstellen von Textur Mischungs Stufen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="513d3-113">Although not part of the Direct3D API, you can insert the following macros into your application to abbreviate the code required for creating texture blending stages.</span></span>


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a><span data-ttu-id="513d3-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="513d3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="513d3-115">Textur Mischung</span><span class="sxs-lookup"><span data-stu-id="513d3-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
