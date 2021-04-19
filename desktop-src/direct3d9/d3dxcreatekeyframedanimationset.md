---
description: Erstellt eine ID3DXKeyframedAnimationSet Key-Animation für Animations Sätze.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: D3DXCreateKeyframedAnimationSet-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f3eb45e999d25c776014c3df5824e0468d03ffd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363168"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a><span data-ttu-id="847a4-103">D3DXCreateKeyframedAnimationSet-Funktion</span><span class="sxs-lookup"><span data-stu-id="847a4-103">D3DXCreateKeyframedAnimationSet function</span></span>

<span data-ttu-id="847a4-104">Erstellt eine [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) Key-Animation für Animations Sätze.</span><span class="sxs-lookup"><span data-stu-id="847a4-104">Creates a [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="847a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="847a4-105">Syntax</span></span>


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="847a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="847a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="847a4-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="847a4-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="847a4-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="847a4-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="847a4-109">Zeiger auf den Namen des Animations Satzes.</span><span class="sxs-lookup"><span data-stu-id="847a4-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="847a4-110">*TicksPerSecond* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="847a4-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="847a4-111">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="847a4-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="847a4-112">Anzahl der Keyframe-Ticks, die pro Sekunde verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="847a4-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="847a4-113">*Wiedergabe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="847a4-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="847a4-114">Type: **[ **D3DXPLAYBACK- \_ Typ**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="847a4-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="847a4-115">Der Typ der Wiedergabe Schleife für Animations Sätze.</span><span class="sxs-lookup"><span data-stu-id="847a4-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="847a4-116">Siehe [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="847a4-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="847a4-117">*Numanimationen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="847a4-117">*NumAnimations* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="847a4-118">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="847a4-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="847a4-119">Anzahl der Skalierungs Gruppen für Skalierung, Drehung und Übersetzung (SRT).</span><span class="sxs-lookup"><span data-stu-id="847a4-119">Number of scale, rotate, and translate (SRT) animation sets.</span></span>

</dd> <dt>

<span data-ttu-id="847a4-120">*Numcallbackkeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="847a4-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="847a4-121">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="847a4-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="847a4-122">Anzahl von Rückruf Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="847a4-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="847a4-123">*pcallkeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="847a4-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="847a4-124">Typ: **Konstanten [**LPD3DXKEY \_ Rückruf**](d3dxkey-callback.md) \***</span><span class="sxs-lookup"><span data-stu-id="847a4-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="847a4-125">Zeiger auf eine [**D3DXKEY- \_ Rückruf**](d3dxkey-callback.md) Struktur, die Benutzer Rückruf Daten speichert.</span><span class="sxs-lookup"><span data-stu-id="847a4-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="847a4-126">*ppanimationset* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="847a4-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="847a4-127">Typ: **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="847a4-127">Type: **[**LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span></span>

<span data-ttu-id="847a4-128">Adresse eines Zeigers auf die [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) Key Framed Animation Set-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="847a4-128">Address of a pointer to the [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="847a4-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="847a4-129">Return value</span></span>

<span data-ttu-id="847a4-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="847a4-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="847a4-131">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="847a4-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="847a4-132">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="847a4-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="847a4-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="847a4-133">Requirements</span></span>



| <span data-ttu-id="847a4-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="847a4-134">Requirement</span></span> | <span data-ttu-id="847a4-135">Wert</span><span class="sxs-lookup"><span data-stu-id="847a4-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="847a4-136">Header</span><span class="sxs-lookup"><span data-stu-id="847a4-136">Header</span></span><br/>  | <dl> <span data-ttu-id="847a4-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="847a4-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="847a4-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="847a4-138">Library</span></span><br/> | <dl> <span data-ttu-id="847a4-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="847a4-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="847a4-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="847a4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="847a4-141">Animations Funktionen</span><span class="sxs-lookup"><span data-stu-id="847a4-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
