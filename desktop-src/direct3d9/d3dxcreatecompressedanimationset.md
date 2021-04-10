---
description: Erstellt eine ID3DXCompressedAnimationSet Key-Animation-Schnittstelle, die Keyframe-Daten in einem komprimierten Format speichert.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: D3DXCreateCompressedAnimationSet-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8aab23466cecf43a50a4136eb0b3d93a271dcb0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961630"
---
# <a name="d3dxcreatecompressedanimationset-function"></a><span data-ttu-id="46c11-103">D3DXCreateCompressedAnimationSet-Funktion</span><span class="sxs-lookup"><span data-stu-id="46c11-103">D3DXCreateCompressedAnimationSet function</span></span>

<span data-ttu-id="46c11-104">Erstellt eine [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) Key-Animation-Schnittstelle, die Keyframe-Daten in einem komprimierten Format speichert.</span><span class="sxs-lookup"><span data-stu-id="46c11-104">Creates a [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) key framed animation set interface that stores key frame data in a compressed format.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c11-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46c11-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="46c11-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46c11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46c11-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c11-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c11-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46c11-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46c11-109">Zeiger auf den Namen des Animations Satzes.</span><span class="sxs-lookup"><span data-stu-id="46c11-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="46c11-110">*TicksPerSecond* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c11-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c11-111">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46c11-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46c11-112">Anzahl der Keyframe-Ticks, die pro Sekunde verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="46c11-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="46c11-113">*Wiedergabe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c11-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c11-114">Type: **[ **D3DXPLAYBACK- \_ Typ**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="46c11-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="46c11-115">Der Typ der Wiedergabe Schleife für Animations Sätze.</span><span class="sxs-lookup"><span data-stu-id="46c11-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="46c11-116">Siehe [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="46c11-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="46c11-117">*pcompresseddata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c11-117">*pCompressedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c11-118">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="46c11-118">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="46c11-119">Zeiger auf den [**ID3DXBuffer**](id3dxbuffer.md) -Puffer, in dem der Animations Satz als komprimierte Daten gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="46c11-119">Pointer to the [**ID3DXBuffer**](id3dxbuffer.md) buffer that stores the animation set as compressed data.</span></span>

</dd> <dt>

<span data-ttu-id="46c11-120">*Numcallbackkeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c11-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c11-121">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46c11-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46c11-122">Anzahl von Rückruf Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="46c11-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="46c11-123">*pcallkeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c11-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c11-124">Typ: **Konstanten [**LPD3DXKEY \_ Rückruf**](d3dxkey-callback.md) \***</span><span class="sxs-lookup"><span data-stu-id="46c11-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="46c11-125">Zeiger auf eine [**D3DXKEY- \_ Rückruf**](d3dxkey-callback.md) Struktur, die Benutzer Rückruf Daten speichert.</span><span class="sxs-lookup"><span data-stu-id="46c11-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="46c11-126">*ppanimationset* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="46c11-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46c11-127">Typ: **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="46c11-127">Type: **[**LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span></span>

<span data-ttu-id="46c11-128">Adresse eines Zeigers auf die [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) -Schnittstelle, in der die Daten der keysetanimation in einem komprimierten Format gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="46c11-128">Address of a pointer to the [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) interface that stores key framed animation set data in a compressed format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46c11-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46c11-129">Return value</span></span>

<span data-ttu-id="46c11-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46c11-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46c11-131">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="46c11-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="46c11-132">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="46c11-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="46c11-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46c11-133">Requirements</span></span>



| <span data-ttu-id="46c11-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46c11-134">Requirement</span></span> | <span data-ttu-id="46c11-135">Wert</span><span class="sxs-lookup"><span data-stu-id="46c11-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46c11-136">Header</span><span class="sxs-lookup"><span data-stu-id="46c11-136">Header</span></span><br/>  | <dl> <span data-ttu-id="46c11-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="46c11-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="46c11-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="46c11-138">Library</span></span><br/> | <dl> <span data-ttu-id="46c11-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46c11-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="46c11-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46c11-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46c11-141">Animations Funktionen</span><span class="sxs-lookup"><span data-stu-id="46c11-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
