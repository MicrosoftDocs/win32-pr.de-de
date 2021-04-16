---
description: Erstellen Sie einen Matrix Stapel.
ms.assetid: df0f3564-0226-44b8-b22b-4dd27905c44c
title: D3DXCreateMatrixStack-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b5799632f171d1b80f95f0f684bb22d24f741f6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394205"
---
# <a name="d3dxcreatematrixstack-function-d3dx10mathh"></a><span data-ttu-id="bb6a2-103">D3DXCreateMatrixStack-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="bb6a2-103">D3DXCreateMatrixStack function (D3DX10Math.h)</span></span>

<span data-ttu-id="bb6a2-104">Erstellen Sie einen Matrix Stapel.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-104">Create a matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb6a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb6a2-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  UINT              Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="bb6a2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb6a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb6a2-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="bb6a2-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb6a2-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb6a2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb6a2-109">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-109">Not implemented.</span></span> <span data-ttu-id="bb6a2-110">Geben Sie NULL an.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="bb6a2-111">*ppstack* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bb6a2-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb6a2-112">Typ: **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="bb6a2-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="bb6a2-113">Die Adresse eines Zeigers auf einen Matrix Stapel (siehe [**ID3DXMatrixStack-Schnittstelle**](d3d10-id3dxmatrixstack.md)).</span><span class="sxs-lookup"><span data-stu-id="bb6a2-113">The address of a pointer to a matrix stack (see [**ID3DXMatrixStack Interface**](d3d10-id3dxmatrixstack.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb6a2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb6a2-114">Return value</span></span>

<span data-ttu-id="bb6a2-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb6a2-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb6a2-116">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="bb6a2-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb6a2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb6a2-117">Requirements</span></span>



| <span data-ttu-id="bb6a2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb6a2-118">Requirement</span></span> | <span data-ttu-id="bb6a2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bb6a2-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb6a2-120">Header</span><span class="sxs-lookup"><span data-stu-id="bb6a2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bb6a2-121"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb6a2-121"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bb6a2-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb6a2-122">Library</span></span><br/> | <dl> <span data-ttu-id="bb6a2-123"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb6a2-123"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb6a2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb6a2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6a2-125">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="bb6a2-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
