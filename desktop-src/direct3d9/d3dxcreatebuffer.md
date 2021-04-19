---
description: Erstellt ein Puffer Objekt.
ms.assetid: 6f44fe84-3e0b-4fb8-821a-c997944fed37
title: D3DXCreateBuffer-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc54813ea9947d263febcbe843702124c68ba747
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373544"
---
# <a name="d3dxcreatebuffer-function"></a><span data-ttu-id="ad13d-103">D3DXCreateBuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="ad13d-103">D3DXCreateBuffer function</span></span>

<span data-ttu-id="ad13d-104">Erstellt ein Puffer Objekt.</span><span class="sxs-lookup"><span data-stu-id="ad13d-104">Creates a buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad13d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad13d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBuffer(
  _In_  DWORD        NumBytes,
  _Out_ LPD3DXBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ad13d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad13d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad13d-107">*NumBytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad13d-107">*NumBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad13d-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad13d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad13d-109">Größe des zu erstellenden Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ad13d-109">Size of the buffer to create, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ad13d-110">*ppbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ad13d-110">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad13d-111">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad13d-111">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ad13d-112">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die das erstellte Puffer Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ad13d-112">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, representing the created buffer object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad13d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad13d-113">Return value</span></span>

<span data-ttu-id="ad13d-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad13d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad13d-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad13d-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ad13d-116">Wenn bei der Funktion ein Fehler auftritt, kann der Rückgabewert einer der folgenden sein: E \_ outo-Memory.</span><span class="sxs-lookup"><span data-stu-id="ad13d-116">If the function fails, the return value can be one of the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad13d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad13d-117">Requirements</span></span>



| <span data-ttu-id="ad13d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad13d-118">Requirement</span></span> | <span data-ttu-id="ad13d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ad13d-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad13d-120">Header</span><span class="sxs-lookup"><span data-stu-id="ad13d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ad13d-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad13d-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ad13d-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ad13d-122">Library</span></span><br/> | <dl> <span data-ttu-id="ad13d-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad13d-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad13d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad13d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad13d-125">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad13d-125">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
