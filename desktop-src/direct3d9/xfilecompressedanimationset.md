---
description: Identifiziert komprimierte Keyframe-Animationsdaten.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: Xfilecompressedanimationset-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 240cac57c9c0d123203ee4599c14092df1327f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365075"
---
# <a name="xfilecompressedanimationset-structure"></a><span data-ttu-id="865a1-103">Xfilecompressedanimationset-Struktur</span><span class="sxs-lookup"><span data-stu-id="865a1-103">XFILECOMPRESSEDANIMATIONSET structure</span></span>

<span data-ttu-id="865a1-104">Identifiziert komprimierte Keyframe-Animationsdaten.</span><span class="sxs-lookup"><span data-stu-id="865a1-104">Identifies compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="865a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="865a1-105">Syntax</span></span>


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a><span data-ttu-id="865a1-106">Member</span><span class="sxs-lookup"><span data-stu-id="865a1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="865a1-107">**Compressedblocksize**</span><span class="sxs-lookup"><span data-stu-id="865a1-107">**CompressedBlockSize**</span></span>
</dt> <dd>

<span data-ttu-id="865a1-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="865a1-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="865a1-109">Gesamtgröße (in Bytes) der komprimierten Daten im komprimierten Keyframe-Animationsdaten Puffer.</span><span class="sxs-lookup"><span data-stu-id="865a1-109">Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>

</dd> <dt>

<span data-ttu-id="865a1-110">**Tickspersec**</span><span class="sxs-lookup"><span data-stu-id="865a1-110">**TicksPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="865a1-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="865a1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="865a1-112">Anzahl der Animations Tastatur-Frame Ticks, die pro Sekunde auftreten.</span><span class="sxs-lookup"><span data-stu-id="865a1-112">Number of animation key frame ticks that occur per second.</span></span>

</dd> <dt>

<span data-ttu-id="865a1-113">**Playbacktyp**</span><span class="sxs-lookup"><span data-stu-id="865a1-113">**PlaybackType**</span></span>
</dt> <dd>

<span data-ttu-id="865a1-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="865a1-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="865a1-115">Der Typ der Wiedergabe Schleife für Animations Sätze.</span><span class="sxs-lookup"><span data-stu-id="865a1-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="865a1-116">Siehe [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="865a1-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="865a1-117">**BufferLength**</span><span class="sxs-lookup"><span data-stu-id="865a1-117">**BufferLength**</span></span>
</dt> <dd>

<span data-ttu-id="865a1-118">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="865a1-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="865a1-119">Minimale Puffergröße in Bytes, die zum Speichern komprimierter Keyframe-Animationsdaten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="865a1-119">Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="865a1-120">Der Wert ist gleich ((compressedblocksize + 3)/4).</span><span class="sxs-lookup"><span data-stu-id="865a1-120">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="865a1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="865a1-121">Requirements</span></span>



| <span data-ttu-id="865a1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="865a1-122">Requirement</span></span> | <span data-ttu-id="865a1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="865a1-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="865a1-124">Header</span><span class="sxs-lookup"><span data-stu-id="865a1-124">Header</span></span><br/> | <dl> <span data-ttu-id="865a1-125"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="865a1-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="865a1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="865a1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="865a1-127">D3DX X-Dateistrukturen</span><span class="sxs-lookup"><span data-stu-id="865a1-127">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="865a1-128">**ID3DXCompressedAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="865a1-128">**ID3DXCompressedAnimationSet**</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
