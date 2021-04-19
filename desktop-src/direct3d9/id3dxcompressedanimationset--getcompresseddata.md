---
description: Ruft den Datenpuffer ab, in dem komprimierte Keyframe-Animationsdaten gespeichert werden.
ms.assetid: cb42a4c8-6420-4694-9921-0d36cfe960e5
title: 'ID3DXCompressedAnimationSet:: getcompresseddata-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCompressedData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7907daf5db2d03afca310a630f6aeb2dc16c4f22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370434"
---
# <a name="id3dxcompressedanimationsetgetcompresseddata-method"></a><span data-ttu-id="e53af-103">ID3DXCompressedAnimationSet:: getcompresseddata-Methode</span><span class="sxs-lookup"><span data-stu-id="e53af-103">ID3DXCompressedAnimationSet::GetCompressedData method</span></span>

<span data-ttu-id="e53af-104">Ruft den Datenpuffer ab, in dem komprimierte Keyframe-Animationsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e53af-104">Gets the data buffer that stores compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e53af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e53af-105">Syntax</span></span>


```C++
HRESULT GetCompressedData(
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="e53af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e53af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e53af-107">*ppcompresseddata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e53af-107">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e53af-108">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e53af-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e53af-109">Adresse eines Zeigers auf den [**ID3DXBuffer**](id3dxbuffer.md) -Datenpuffer, der komprimierte Keyframe-Animationsdaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="e53af-109">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) data buffer that receives compressed key frame animation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e53af-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e53af-110">Return value</span></span>

<span data-ttu-id="e53af-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e53af-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e53af-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e53af-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e53af-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="e53af-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e53af-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e53af-114">Requirements</span></span>



| <span data-ttu-id="e53af-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e53af-115">Requirement</span></span> | <span data-ttu-id="e53af-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e53af-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e53af-117">Header</span><span class="sxs-lookup"><span data-stu-id="e53af-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e53af-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e53af-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e53af-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e53af-119">Library</span></span><br/> | <dl> <span data-ttu-id="e53af-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e53af-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e53af-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e53af-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e53af-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="e53af-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 




