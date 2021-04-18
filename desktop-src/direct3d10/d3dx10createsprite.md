---
description: Erstellen Sie ein Sprite zum Zeichnen einer 2D-Textur. Beachten Sie, dass Sie anstelle dieser Funktion die Verwendung von Direct2D und der directxtk-Bibliothek, SpriteBatch Class, empfehlen.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: D3DX10CreateSprite-Funktion (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365299"
---
# <a name="d3dx10createsprite-function"></a><span data-ttu-id="1a182-103">D3DX10CreateSprite-Funktion</span><span class="sxs-lookup"><span data-stu-id="1a182-103">D3DX10CreateSprite function</span></span>

<span data-ttu-id="1a182-104">Erstellen Sie ein Sprite zum Zeichnen einer 2D-Textur.</span><span class="sxs-lookup"><span data-stu-id="1a182-104">Create a sprite for drawing a 2D texture.</span></span>

> [!Note]  
> <span data-ttu-id="1a182-105">Anstatt diese Funktion zu verwenden, empfehlen wir die Verwendung von [Direct2D](../direct2d/direct2d-portal.md) und der [directxtk](https://github.com/Microsoft/DirectXTK) -Bibliothek, **SpriteBatch** Class.</span><span class="sxs-lookup"><span data-stu-id="1a182-105">Instead of using this function, we recommend that you use [Direct2D](../direct2d/direct2d-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteBatch** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1a182-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a182-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="1a182-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a182-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a182-108">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a182-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a182-109">Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="1a182-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="1a182-110">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), mit dem das Sprite gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1a182-110">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will draw the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="1a182-111">*cdevicebuffersize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a182-111">*cDeviceBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a182-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a182-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a182-113">Die Größe des Scheitelpunkt Puffers (in Anzahl von Sprites), die an das Gerät gesendet wird, wenn [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) oder [**ID3DX10Sprite::D rawspritesimvermittler**](id3dx10sprite-drawspritesimmediate.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1a182-113">The size of the vertex buffer, in number of sprites, that will be sent to the device when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) or [**ID3DX10Sprite::DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md) is called.</span></span> <span data-ttu-id="1a182-114">Dies sollte eine kleine Zahl sein, wenn Sie wissen, dass Sie jeweils nur eine kleine Anzahl von Sprites Rendern (um Speicherplatz zu sparen), und eine große Zahl, wenn Sie wissen, dass Sie eine große Anzahl von Sprites gleichzeitig rendern werden.</span><span class="sxs-lookup"><span data-stu-id="1a182-114">This should be a small number if you know you will be rendering a small number of sprites at a time (to save memory) and a large number if you know you will be rendering a large number of sprites at a time.</span></span> <span data-ttu-id="1a182-115">Der Höchstwert ist 4096.</span><span class="sxs-lookup"><span data-stu-id="1a182-115">The maximum value is 4096.</span></span> <span data-ttu-id="1a182-116">Wenn 0 angegeben wird, wird die Vertex-Puffergröße automatisch auf 4096 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1a182-116">If 0 is specified, the vertex buffer size will automatically be set to 4096.</span></span>

</dd> <dt>

<span data-ttu-id="1a182-117">*ppsprite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1a182-117">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a182-118">Typ: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a182-118">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)\***</span></span>

<span data-ttu-id="1a182-119">Die Adresse eines Zeigers auf eine Sprite-Schnittstelle (siehe [**ID3DX10Sprite-Schnittstelle**](id3dx10sprite.md)).</span><span class="sxs-lookup"><span data-stu-id="1a182-119">The address of a pointer to a sprite interface (see [**ID3DX10Sprite Interface**](id3dx10sprite.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a182-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a182-120">Return value</span></span>

<span data-ttu-id="1a182-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1a182-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1a182-122">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1a182-122">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1a182-123">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="1a182-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a182-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a182-124">Requirements</span></span>



| <span data-ttu-id="1a182-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a182-125">Requirement</span></span> | <span data-ttu-id="1a182-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1a182-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a182-127">Header</span><span class="sxs-lookup"><span data-stu-id="1a182-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1a182-128"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a182-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a182-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a182-129">Library</span></span><br/> | <dl> <span data-ttu-id="1a182-130"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a182-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a182-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a182-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a182-132">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="1a182-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
