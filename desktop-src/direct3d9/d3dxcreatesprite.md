---
description: Erstellt ein Sprite-Objekt, das einem bestimmten Gerät zugeordnet ist. Sprite-Objekte werden verwendet, um 2D-Bilder auf den Bildschirm zu zeichnen.
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: D3DXCreateSprite-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSprite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e16feb2ff07f10703c5243ebeaaee3a2a15e7f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365092"
---
# <a name="d3dxcreatesprite-function"></a><span data-ttu-id="9fc60-104">D3DXCreateSprite-Funktion</span><span class="sxs-lookup"><span data-stu-id="9fc60-104">D3DXCreateSprite function</span></span>

<span data-ttu-id="9fc60-105">Erstellt ein Sprite-Objekt, das einem bestimmten Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9fc60-105">Creates a sprite object which is associated with a particular device.</span></span> <span data-ttu-id="9fc60-106">Sprite-Objekte werden verwendet, um 2D-Bilder auf den Bildschirm zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="9fc60-106">Sprite objects are used to draw 2D images to the screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc60-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fc60-107">Syntax</span></span>


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="9fc60-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fc60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc60-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fc60-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc60-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9fc60-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9fc60-111">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das Gerät, das dem Sprite zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fc60-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="9fc60-112">*ppsprite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9fc60-112">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc60-113">Typ: **[ **LPD3DXSPRITE**](id3dxsprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="9fc60-113">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)\***</span></span>

<span data-ttu-id="9fc60-114">Adresse eines Zeigers auf eine [**ID3DXSprite**](id3dxsprite.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9fc60-114">Address of a pointer to an [**ID3DXSprite**](id3dxsprite.md) interface.</span></span> <span data-ttu-id="9fc60-115">Diese Schnittstelle ermöglicht dem Benutzer den Zugriff auf Sprite-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9fc60-115">This interface allows the user to access sprite functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc60-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fc60-116">Return value</span></span>

<span data-ttu-id="9fc60-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9fc60-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9fc60-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9fc60-118">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9fc60-119">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="9fc60-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc60-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fc60-120">Remarks</span></span>

<span data-ttu-id="9fc60-121">Diese Schnittstelle kann verwendet werden, um zweidimensionale Bilder im Bildschirmbereich des zugeordneten Geräts zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="9fc60-121">This interface can be used to draw two dimensional images in screen space of the associated device.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc60-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fc60-122">Requirements</span></span>



| <span data-ttu-id="9fc60-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fc60-123">Requirement</span></span> | <span data-ttu-id="9fc60-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9fc60-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc60-125">Header</span><span class="sxs-lookup"><span data-stu-id="9fc60-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9fc60-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fc60-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9fc60-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9fc60-127">Library</span></span><br/> | <dl> <span data-ttu-id="9fc60-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fc60-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9fc60-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fc60-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc60-130">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="9fc60-130">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
