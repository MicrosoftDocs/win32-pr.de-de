---
description: Erstellt eine Instanz der ID3DXMATRIXStack-Schnittstelle.
ms.assetid: bb067b38-efc6-4ed8-9eef-14b3cc70660f
title: D3DXCreateMatrixStack-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 08e1ac23d5f6bcd874b1d5bd7f60313a232b0563
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373537"
---
# <a name="d3dxcreatematrixstack-function-d3dx9mathh"></a><span data-ttu-id="f6682-103">D3DXCreateMatrixStack-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f6682-103">D3DXCreateMatrixStack function (D3dx9math.h)</span></span>

<span data-ttu-id="f6682-104">Erstellt eine Instanz der [**ID3DXMATRIXStack**](id3dxmatrixstack.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f6682-104">Creates an instance of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6682-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6682-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  DWORD             Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a><span data-ttu-id="f6682-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6682-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6682-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="f6682-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6682-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6682-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6682-109">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="f6682-109">Not implemented.</span></span> <span data-ttu-id="f6682-110">Geben Sie NULL an.</span><span class="sxs-lookup"><span data-stu-id="f6682-110">Specify zero.</span></span>

</dd> <dt>

<span data-ttu-id="f6682-111">*ppstack* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f6682-111">*ppStack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6682-112">Typ: **LPD3DXMATRIXSTACK \***</span><span class="sxs-lookup"><span data-stu-id="f6682-112">Type: **LPD3DXMATRIXSTACK\***</span></span>

<span data-ttu-id="f6682-113">Adresse eines Zeigers, der mit einem [**ID3DXMATRIXStack**](id3dxmatrixstack.md) -Schnittstellen Zeiger gefüllt wird, wenn die Funktion erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6682-113">Address of a pointer filled with an [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface pointer if the function succeeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6682-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6682-114">Return value</span></span>

<span data-ttu-id="f6682-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f6682-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f6682-116">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f6682-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f6682-117">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="f6682-117">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6682-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6682-118">Requirements</span></span>



| <span data-ttu-id="f6682-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6682-119">Requirement</span></span> | <span data-ttu-id="f6682-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f6682-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6682-121">Header</span><span class="sxs-lookup"><span data-stu-id="f6682-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f6682-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6682-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f6682-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f6682-123">Library</span></span><br/> | <dl> <span data-ttu-id="f6682-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6682-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f6682-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6682-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6682-126">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f6682-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
