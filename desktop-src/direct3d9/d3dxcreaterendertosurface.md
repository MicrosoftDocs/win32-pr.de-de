---
description: Erstellt eine Renderoberfläche.
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: D3DXCreateRenderToSurface-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fc64cbc65d30838db2105e0458d3553247f1ab1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363140"
---
# <a name="d3dxcreaterendertosurface-function"></a><span data-ttu-id="1213f-103">D3DXCreateRenderToSurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="1213f-103">D3DXCreateRenderToSurface function</span></span>

<span data-ttu-id="1213f-104">Erstellt eine Renderoberfläche.</span><span class="sxs-lookup"><span data-stu-id="1213f-104">Creates a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1213f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1213f-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToSurface(
  _In_  LPDIRECT3DDEVICE9     pDevice,
  _In_  UINT                  Width,
  _In_  UINT                  Height,
  _In_  D3DFORMAT             Format,
  _In_  BOOL                  DepthStencil,
  _In_  D3DFORMAT             DepthStencilFormat,
  _Out_ LPD3DXRENDERTOSURFACE *ppRenderToSurface
);
```



## <a name="parameters"></a><span data-ttu-id="1213f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1213f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1213f-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1213f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1213f-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1213f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1213f-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das Gerät, das der Renderoberfläche zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1213f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="1213f-110">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1213f-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1213f-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1213f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1213f-112">Breite der Renderoberfläche in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1213f-112">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="1213f-113">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1213f-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1213f-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1213f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1213f-115">Höhe der Renderoberfläche in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1213f-115">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="1213f-116">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1213f-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1213f-117">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="1213f-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="1213f-118">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Pixel Format der Renderoberfläche beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1213f-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="1213f-119">*Depthstencil* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1213f-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1213f-120">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1213f-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1213f-121">**True** gibt an, dass die Renderoberfläche eine tiefen Schablone unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1213f-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="1213f-122">Andernfalls ist dieser Member auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1213f-122">Otherwise, this member is set to **FALSE**.</span></span> <span data-ttu-id="1213f-123">Mit dieser Funktion wird ein neuer tiefen Puffer erstellt.</span><span class="sxs-lookup"><span data-stu-id="1213f-123">This function will create a new depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1213f-124">*Depthstencilformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1213f-124">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1213f-125">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="1213f-125">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="1213f-126">Wenn *depthstencil* auf **true** festgelegt ist, ist dieser Parameter ein Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das tiefen Schablone-Format der Renderoberfläche beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1213f-126">If *DepthStencil* is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="1213f-127">*pprenderumsurface* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1213f-127">*ppRenderToSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1213f-128">Typ: **[ **LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span><span class="sxs-lookup"><span data-stu-id="1213f-128">Type: **[**LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span></span>

<span data-ttu-id="1213f-129">Adresse eines Zeigers auf eine [**ID3DXRenderToSurface**](id3dxrendertosurface.md) -Schnittstelle, die die erstellte Renderoberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="1213f-129">Address of a pointer to an [**ID3DXRenderToSurface**](id3dxrendertosurface.md) interface, representing the created render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1213f-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1213f-130">Return value</span></span>

<span data-ttu-id="1213f-131">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1213f-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1213f-132">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1213f-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1213f-133">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="1213f-133">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1213f-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1213f-134">Requirements</span></span>



| <span data-ttu-id="1213f-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1213f-135">Requirement</span></span> | <span data-ttu-id="1213f-136">Wert</span><span class="sxs-lookup"><span data-stu-id="1213f-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1213f-137">Header</span><span class="sxs-lookup"><span data-stu-id="1213f-137">Header</span></span><br/>  | <dl> <span data-ttu-id="1213f-138"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1213f-138"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="1213f-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1213f-139">Library</span></span><br/> | <dl> <span data-ttu-id="1213f-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1213f-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1213f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1213f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1213f-142">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="1213f-142">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
