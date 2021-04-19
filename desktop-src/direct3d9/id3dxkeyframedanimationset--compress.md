---
description: Wandelt Animationen in einem Animations Satz in ein komprimiertes Format um und gibt einen Zeiger auf den Puffer zurück, in dem die komprimierten Daten gespeichert werden.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'ID3DXKeyframedAnimationSet:: compress-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd3a278760f2598df52d251a9e3558a72f954ceb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370469"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a><span data-ttu-id="0223f-103">ID3DXKeyframedAnimationSet:: compress-Methode</span><span class="sxs-lookup"><span data-stu-id="0223f-103">ID3DXKeyframedAnimationSet::Compress method</span></span>

<span data-ttu-id="0223f-104">Wandelt Animationen in einem Animations Satz in ein komprimiertes Format um und gibt einen Zeiger auf den Puffer zurück, in dem die komprimierten Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0223f-104">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0223f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0223f-105">Syntax</span></span>


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="0223f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0223f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0223f-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="0223f-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0223f-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0223f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0223f-109">Einer der [**D3DXCOMPRESSION \_ Flags**](./d3dxcompression-flags.md) -Werte, die den Komprimierungs Modus definieren, der zum Speichern komprimierter Animations Satz Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0223f-109">One of the [**D3DXCOMPRESSION\_FLAGS**](./d3dxcompression-flags.md) values that define the compression mode used for storing compressed animation set data.</span></span> <span data-ttu-id="0223f-110">D3DXCOMPRESS \_ Default ist der einzige derzeit unterstützte Wert.</span><span class="sxs-lookup"><span data-stu-id="0223f-110">D3DXCOMPRESS\_DEFAULT is the only value currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="0223f-111">*Verlust* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0223f-111">*Lossiness* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0223f-112">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0223f-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0223f-113">Das Verhältnis der gewünschten Komprimierungs Verluste liegt im Bereich von 0 bis 1.</span><span class="sxs-lookup"><span data-stu-id="0223f-113">Desired compression loss ratio, in the range from 0 to 1.</span></span>

</dd> <dt>

<span data-ttu-id="0223f-114">*phierarchie* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0223f-114">*pHierarchy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0223f-115">Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="0223f-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="0223f-116">Zeiger auf eine [**D3DXFRAME**](d3dxframe.md) -Transformations Frame Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="0223f-116">Pointer to a [**D3DXFRAME**](d3dxframe.md) transformation frame hierarchy.</span></span> <span data-ttu-id="0223f-117">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0223f-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0223f-118">*ppcompresseddata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0223f-118">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0223f-119">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0223f-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0223f-120">Adresse eines Zeigers auf den komprimierten [**ID3DXBuffer**](id3dxbuffer.md) -Animations Satz.</span><span class="sxs-lookup"><span data-stu-id="0223f-120">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) compressed animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0223f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0223f-121">Return value</span></span>

<span data-ttu-id="0223f-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0223f-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0223f-123">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0223f-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0223f-124">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="0223f-124">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0223f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0223f-125">Requirements</span></span>



| <span data-ttu-id="0223f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0223f-126">Requirement</span></span> | <span data-ttu-id="0223f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0223f-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0223f-128">Header</span><span class="sxs-lookup"><span data-stu-id="0223f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0223f-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0223f-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0223f-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0223f-130">Library</span></span><br/> | <dl> <span data-ttu-id="0223f-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0223f-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0223f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0223f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0223f-133">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="0223f-133">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
