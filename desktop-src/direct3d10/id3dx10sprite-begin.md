---
description: Bereiten Sie ein Gerät zum Zeichnen von Sprites vor.
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: 'ID3DX10Sprite:: Begin-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Begin
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ede2995f72eb1200e68f035119643a362e15701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219606"
---
# <a name="id3dx10spritebegin-method"></a><span data-ttu-id="b8066-103">ID3DX10Sprite:: Begin-Methode</span><span class="sxs-lookup"><span data-stu-id="b8066-103">ID3DX10Sprite::Begin method</span></span>

<span data-ttu-id="b8066-104">Bereiten Sie ein Gerät zum Zeichnen von Sprites vor.</span><span class="sxs-lookup"><span data-stu-id="b8066-104">Prepare a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8066-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8066-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a><span data-ttu-id="b8066-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8066-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8066-107">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8066-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8066-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8066-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8066-109">Flags, die Steuern, wie die Sprites gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b8066-109">Flags that control how the sprites will be drawn.</span></span> <span data-ttu-id="b8066-110">Siehe [**d3dx10 \_ Sprite- \_ Flag**](d3dx10-sprite-flag.md).</span><span class="sxs-lookup"><span data-stu-id="b8066-110">See [**D3DX10\_SPRITE\_FLAG**](d3dx10-sprite-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8066-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8066-111">Return value</span></span>

<span data-ttu-id="b8066-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8066-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8066-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b8066-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b8066-114">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DERR \_ ouesfvideomemory, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="b8066-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8066-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8066-115">Remarks</span></span>

<span data-ttu-id="b8066-116">Alle Aufrufe von Begin müssen mit einem [**ID3DX10Sprite:: End**](id3dx10sprite-end.md)-Befehl abgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="b8066-116">Every call to Begin must be matched with a call to [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8066-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8066-117">Requirements</span></span>



| <span data-ttu-id="b8066-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8066-118">Requirement</span></span> | <span data-ttu-id="b8066-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b8066-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8066-120">Header</span><span class="sxs-lookup"><span data-stu-id="b8066-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b8066-121"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8066-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8066-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b8066-122">Library</span></span><br/> | <dl> <span data-ttu-id="b8066-123"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8066-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8066-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8066-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8066-125">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="b8066-125">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="b8066-126">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b8066-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
