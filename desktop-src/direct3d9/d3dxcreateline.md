---
description: Verwendet ein Links händiges Koordinatensystem, um eine Linie zu erstellen.
ms.assetid: 0d2ef331-9edf-4b0a-ace4-ecb8bb2f7352
title: D3DXCreateLine-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cf7d75ca63d64be39733b36a1b7d7a1b464238e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350674"
---
# <a name="d3dxcreateline-function"></a><span data-ttu-id="713c3-103">D3DXCreateLine-Funktion</span><span class="sxs-lookup"><span data-stu-id="713c3-103">D3DXCreateLine function</span></span>

<span data-ttu-id="713c3-104">Verwendet ein Links händiges Koordinatensystem, um eine Linie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="713c3-104">Uses a left-handed coordinate system to create a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="713c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="713c3-105">Syntax</span></span>


```C++
HRESULT D3DXCreateLine(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXLINE        *ppLine
);
```



## <a name="parameters"></a><span data-ttu-id="713c3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="713c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="713c3-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="713c3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713c3-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="713c3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="713c3-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das dem erstellten Box-Mesh zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="713c3-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="713c3-110">*ppline* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="713c3-110">*ppLine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="713c3-111">Typ: **[ **LPD3DXLINE**](id3dxline.md)\***</span><span class="sxs-lookup"><span data-stu-id="713c3-111">Type: **[**LPD3DXLINE**](id3dxline.md)\***</span></span>

<span data-ttu-id="713c3-112">Zeiger auf eine [**ID3DXLine**](id3dxline.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="713c3-112">Pointer to an [**ID3DXLine**](id3dxline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="713c3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="713c3-113">Return value</span></span>

<span data-ttu-id="713c3-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="713c3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="713c3-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="713c3-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="713c3-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="713c3-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="713c3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="713c3-117">Remarks</span></span>

<span data-ttu-id="713c3-118">Diese Funktion erstellt ein Mesh mit der D3DXMESH \_ Managed Creation-Option und [D3DFVF \_ XYZ \| D3DFVF \_ Normal](d3dfvf.md) flexibles Scheitelpunkt Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="713c3-118">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) Flexible Vertex Format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="713c3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="713c3-119">Requirements</span></span>



| <span data-ttu-id="713c3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="713c3-120">Requirement</span></span> | <span data-ttu-id="713c3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="713c3-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="713c3-122">Header</span><span class="sxs-lookup"><span data-stu-id="713c3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="713c3-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="713c3-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="713c3-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="713c3-124">Library</span></span><br/> | <dl> <span data-ttu-id="713c3-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="713c3-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="713c3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="713c3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="713c3-127">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="713c3-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
