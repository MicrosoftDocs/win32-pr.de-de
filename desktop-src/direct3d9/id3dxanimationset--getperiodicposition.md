---
description: Gibt die Uhrzeit Position im lokalen Zeitrahmen eines Animations Satzes zurück.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'ID3DXAnimationSet:: GetPeriodicPosition-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355936"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a><span data-ttu-id="dd2ad-103">ID3DXAnimationSet:: GetPeriodicPosition-Methode</span><span class="sxs-lookup"><span data-stu-id="dd2ad-103">ID3DXAnimationSet::GetPeriodicPosition method</span></span>

<span data-ttu-id="dd2ad-104">Gibt die Uhrzeit Position im lokalen Zeitrahmen eines Animations Satzes zurück.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-104">Returns time position in the local timeframe of an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd2ad-105">Syntax</span></span>


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a><span data-ttu-id="dd2ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd2ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd2ad-107">*Position* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd2ad-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2ad-108">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd2ad-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dd2ad-109">Lokale Zeit des Animations Satzes.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-109">Local time of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd2ad-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd2ad-110">Return value</span></span>

<span data-ttu-id="dd2ad-111">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd2ad-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dd2ad-112">Die Zeit Position, gemessen im Zeitrahmen des Animations Satzes.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-112">Time position as measured in the timeframe of the animation set.</span></span> <span data-ttu-id="dd2ad-113">Dieser Wert wird durch den Zeitraum des Animations Satzes begrenzt.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-113">This value will be bounded by the period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd2ad-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd2ad-114">Remarks</span></span>

<span data-ttu-id="dd2ad-115">Die von dieser Methode zurückgegebene Zeit Position kann als PeriodicPosition-Parameter von [**ID3DXAnimationSet:: gezrt**](id3dxanimationset--getsrt.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd2ad-115">The time position returned by this method can be used as the PeriodicPosition parameter of [**ID3DXAnimationSet::GetSRT**](id3dxanimationset--getsrt.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd2ad-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd2ad-116">Requirements</span></span>



| <span data-ttu-id="dd2ad-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd2ad-117">Requirement</span></span> | <span data-ttu-id="dd2ad-118">Wert</span><span class="sxs-lookup"><span data-stu-id="dd2ad-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2ad-119">Header</span><span class="sxs-lookup"><span data-stu-id="dd2ad-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dd2ad-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd2ad-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="dd2ad-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dd2ad-121">Library</span></span><br/> | <dl> <span data-ttu-id="dd2ad-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd2ad-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dd2ad-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd2ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2ad-124">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="dd2ad-124">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
