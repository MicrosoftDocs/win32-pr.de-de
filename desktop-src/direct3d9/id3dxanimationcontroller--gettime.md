---
description: Ruft die globale Animations Zeit ab.
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: 'ID3DXAnimationController:: getTime-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bfc3c2c1d5bb0bbbb3c364b47f22f0790f8d102
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355030"
---
# <a name="id3dxanimationcontrollergettime-method"></a><span data-ttu-id="3293b-103">ID3DXAnimationController:: getTime-Methode</span><span class="sxs-lookup"><span data-stu-id="3293b-103">ID3DXAnimationController::GetTime method</span></span>

<span data-ttu-id="3293b-104">Ruft die globale Animations Zeit ab.</span><span class="sxs-lookup"><span data-stu-id="3293b-104">Gets the global animation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="3293b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3293b-105">Syntax</span></span>


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a><span data-ttu-id="3293b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3293b-106">Parameters</span></span>

<span data-ttu-id="3293b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3293b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3293b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3293b-108">Return value</span></span>

<span data-ttu-id="3293b-109">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3293b-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3293b-110">Gibt die globale Animations Zeit zurück.</span><span class="sxs-lookup"><span data-stu-id="3293b-110">Returns the global animation time.</span></span>

## <a name="remarks"></a><span data-ttu-id="3293b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3293b-111">Remarks</span></span>

<span data-ttu-id="3293b-112">Animationen werden mithilfe einer lokalen Animations Zeit entwickelt und in der globalen Zeit mit [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)gemischt.</span><span class="sxs-lookup"><span data-stu-id="3293b-112">Animations are designed using a local animation time and mixed into global time with [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3293b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3293b-113">Requirements</span></span>



| <span data-ttu-id="3293b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3293b-114">Requirement</span></span> | <span data-ttu-id="3293b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3293b-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3293b-116">Header</span><span class="sxs-lookup"><span data-stu-id="3293b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3293b-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3293b-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3293b-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3293b-118">Library</span></span><br/> | <dl> <span data-ttu-id="3293b-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3293b-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3293b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3293b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3293b-121">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="3293b-121">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
