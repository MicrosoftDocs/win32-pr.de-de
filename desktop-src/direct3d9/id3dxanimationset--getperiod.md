---
description: Ruft den Zeitraum des Animations Satzes ab.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'ID3DXAnimationSet:: GetPeriod-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f6eafbfe802afc8ff3084c49acf31addca66cef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367494"
---
# <a name="id3dxanimationsetgetperiod-method"></a><span data-ttu-id="f350e-103">ID3DXAnimationSet:: GetPeriod-Methode</span><span class="sxs-lookup"><span data-stu-id="f350e-103">ID3DXAnimationSet::GetPeriod method</span></span>

<span data-ttu-id="f350e-104">Ruft den Zeitraum des Animations Satzes ab.</span><span class="sxs-lookup"><span data-stu-id="f350e-104">Gets the period of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="f350e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f350e-105">Syntax</span></span>


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a><span data-ttu-id="f350e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f350e-106">Parameters</span></span>

<span data-ttu-id="f350e-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f350e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f350e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f350e-108">Return value</span></span>

<span data-ttu-id="f350e-109">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f350e-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f350e-110">Zeitraum des Animations Satzes.</span><span class="sxs-lookup"><span data-stu-id="f350e-110">Period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="f350e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f350e-111">Remarks</span></span>

<span data-ttu-id="f350e-112">Der Zeitraum ist der Zeitraum, in dem die Animations Schlüsselframes gültig sind.</span><span class="sxs-lookup"><span data-stu-id="f350e-112">The period is the range of time that the animation key frames are valid.</span></span> <span data-ttu-id="f350e-113">Bei Schleifen Animationen ist dies der Zeitraum der Schleife.</span><span class="sxs-lookup"><span data-stu-id="f350e-113">For looping animations, this is the period of the loop.</span></span> <span data-ttu-id="f350e-114">Die Zeiteinheiten, in denen die Keyframes angegeben werden (z. b. Sekunden), werden von der Anwendung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f350e-114">The time units that the key frames are specified in (for example, seconds) is determined by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="f350e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f350e-115">Requirements</span></span>



| <span data-ttu-id="f350e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f350e-116">Requirement</span></span> | <span data-ttu-id="f350e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f350e-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f350e-118">Header</span><span class="sxs-lookup"><span data-stu-id="f350e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f350e-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f350e-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f350e-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f350e-120">Library</span></span><br/> | <dl> <span data-ttu-id="f350e-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f350e-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f350e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f350e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f350e-123">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="f350e-123">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
