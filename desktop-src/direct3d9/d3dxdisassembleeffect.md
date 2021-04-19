---
description: Disassemblieren eines Effekts.
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: D3DXDisassembleEffect-Funktion (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 945c30319d16264a2b7489d1dc0849a4678cbede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364365"
---
# <a name="d3dxdisassembleeffect-function"></a><span data-ttu-id="1d9a1-103">D3DXDisassembleEffect-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d9a1-103">D3DXDisassembleEffect function</span></span>

<span data-ttu-id="1d9a1-104">Disassemblieren eines Effekts.</span><span class="sxs-lookup"><span data-stu-id="1d9a1-104">Disassemble an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d9a1-105">Syntax</span></span>


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="1d9a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d9a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d9a1-107">*Peer-ect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d9a1-107">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d9a1-108">Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="1d9a1-108">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)**</span></span>

<span data-ttu-id="1d9a1-109">Zeiger auf eine [**ID3DXEffect**](id3dxeffect.md) -Schnittstelle, die den Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="1d9a1-109">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface that contains the effect.</span></span>

</dd> <dt>

<span data-ttu-id="1d9a1-110">*Enablecolorcode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d9a1-110">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d9a1-111">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d9a1-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d9a1-112">Aktivieren Sie die Farbcodierung, um die Disassembly leichter lesbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="1d9a1-112">Enable color coding to make the disassembly easier to read.</span></span>

</dd> <dt>

<span data-ttu-id="1d9a1-113">*ppdisassembly* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1d9a1-113">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d9a1-114">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d9a1-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1d9a1-115">Gibt einen Puffer zurück, der den disassemblierten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="1d9a1-115">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="1d9a1-116">Siehe [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="1d9a1-116">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d9a1-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d9a1-117">Return value</span></span>

<span data-ttu-id="1d9a1-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d9a1-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d9a1-119">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1d9a1-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1d9a1-120">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="1d9a1-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d9a1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d9a1-121">Requirements</span></span>



| <span data-ttu-id="1d9a1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d9a1-122">Requirement</span></span> | <span data-ttu-id="1d9a1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1d9a1-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d9a1-124">Header</span><span class="sxs-lookup"><span data-stu-id="1d9a1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1d9a1-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d9a1-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1d9a1-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1d9a1-126">Library</span></span><br/> | <dl> <span data-ttu-id="1d9a1-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d9a1-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1d9a1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d9a1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d9a1-129">Effekt Funktionen</span><span class="sxs-lookup"><span data-stu-id="1d9a1-129">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 
