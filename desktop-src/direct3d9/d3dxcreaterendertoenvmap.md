---
description: Erstellt eine Rendering-Umgebungs Zuordnung.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: D3DXCreateRenderToEnvMap-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050856"
---
# <a name="d3dxcreaterendertoenvmap-function"></a><span data-ttu-id="0dc57-103">D3DXCreateRenderToEnvMap-Funktion</span><span class="sxs-lookup"><span data-stu-id="0dc57-103">D3DXCreateRenderToEnvMap function</span></span>

<span data-ttu-id="0dc57-104">Erstellt eine Rendering-Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="0dc57-104">Creates a render environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc57-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dc57-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a><span data-ttu-id="0dc57-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0dc57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc57-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0dc57-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc57-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0dc57-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0dc57-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät ist, das der Renderoberfläche zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0dc57-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, which is the device to associate with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="0dc57-110">*Größe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0dc57-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc57-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dc57-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0dc57-112">Größe der Renderoberfläche.</span><span class="sxs-lookup"><span data-stu-id="0dc57-112">Size of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="0dc57-113">*Miplevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0dc57-113">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc57-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dc57-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0dc57-115">Die Anzahl von MipMap-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="0dc57-115">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="0dc57-116">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0dc57-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc57-117">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0dc57-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="0dc57-118">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Pixel Format der Umgebungs Zuordnung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0dc57-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the pixel format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="0dc57-119">*Depthstencil* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0dc57-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc57-120">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dc57-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0dc57-121">**True** gibt an, dass die Renderoberfläche eine tiefen Schablone unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0dc57-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="0dc57-122">Andernfalls ist dieser Member auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0dc57-122">Otherwise, this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0dc57-123">*Depthstencilformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0dc57-123">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc57-124">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="0dc57-124">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="0dc57-125">Wenn depthstencil auf **true** festgelegt ist, ist dieser Parameter ein Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das tiefen Schablone-Format der Umgebungs Zuordnung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0dc57-125">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the depth-stencil format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="0dc57-126">*pprenderumenvmap* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0dc57-126">*ppRenderToEnvMap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc57-127">Typ: **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span><span class="sxs-lookup"><span data-stu-id="0dc57-127">Type: **[**LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span></span>

<span data-ttu-id="0dc57-128">Adresse eines Zeigers auf eine [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) -Schnittstelle, die die erstellte Rendering-Umgebungs Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="0dc57-128">Address of a pointer to an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) interface that represents the created render environment map.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dc57-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0dc57-129">Return value</span></span>

<span data-ttu-id="0dc57-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0dc57-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0dc57-131">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0dc57-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0dc57-132">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="0dc57-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc57-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dc57-133">Requirements</span></span>



| <span data-ttu-id="0dc57-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0dc57-134">Requirement</span></span> | <span data-ttu-id="0dc57-135">Wert</span><span class="sxs-lookup"><span data-stu-id="0dc57-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc57-136">Header</span><span class="sxs-lookup"><span data-stu-id="0dc57-136">Header</span></span><br/>  | <dl> <span data-ttu-id="0dc57-137"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dc57-137"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0dc57-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0dc57-138">Library</span></span><br/> | <dl> <span data-ttu-id="0dc57-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0dc57-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0dc57-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dc57-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc57-141">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="0dc57-141">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
