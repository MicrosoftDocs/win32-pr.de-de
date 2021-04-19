---
description: Gibt die Anzahl von Animations Sätzen zurück, die derzeit im Animations Controller registriert sind.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'ID3DXAnimationController:: getnumanimationsets-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5baedb0ea30d51cbd659e597cb000a434ec1632
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367345"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a><span data-ttu-id="92281-103">ID3DXAnimationController:: getnumanimationsets-Methode</span><span class="sxs-lookup"><span data-stu-id="92281-103">ID3DXAnimationController::GetNumAnimationSets method</span></span>

<span data-ttu-id="92281-104">Gibt die Anzahl von Animations Sätzen zurück, die derzeit im Animations Controller registriert sind.</span><span class="sxs-lookup"><span data-stu-id="92281-104">Returns the number of animation sets currently registered in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="92281-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="92281-105">Syntax</span></span>


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a><span data-ttu-id="92281-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="92281-106">Parameters</span></span>

<span data-ttu-id="92281-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="92281-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92281-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92281-108">Return value</span></span>

<span data-ttu-id="92281-109">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92281-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92281-110">Anzahl der Animations Sätze.</span><span class="sxs-lookup"><span data-stu-id="92281-110">Number of animation sets.</span></span>

## <a name="remarks"></a><span data-ttu-id="92281-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92281-111">Remarks</span></span>

<span data-ttu-id="92281-112">Der Controller enthält eine beliebige Anzahl von Animations Sätzen und-Spuren.</span><span class="sxs-lookup"><span data-stu-id="92281-112">The controller contains any number of animations sets and tracks.</span></span> <span data-ttu-id="92281-113">Animations Sätze können mit [**registeranimationoutput**](id3dxanimationcontroller--registeranimationoutput.md)registriert werden.</span><span class="sxs-lookup"><span data-stu-id="92281-113">Animation sets can be registered with [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md).</span></span> <span data-ttu-id="92281-114">Ein Animations Controller, der durch einen [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) -Aufrufvorgang erstellt wird, registriert geladene Animations Sätze automatisch.</span><span class="sxs-lookup"><span data-stu-id="92281-114">An animation controller created by a call to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) will automatically register loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="92281-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92281-115">Requirements</span></span>



| <span data-ttu-id="92281-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92281-116">Requirement</span></span> | <span data-ttu-id="92281-117">Wert</span><span class="sxs-lookup"><span data-stu-id="92281-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92281-118">Header</span><span class="sxs-lookup"><span data-stu-id="92281-118">Header</span></span><br/>  | <dl> <span data-ttu-id="92281-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="92281-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="92281-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="92281-120">Library</span></span><br/> | <dl> <span data-ttu-id="92281-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92281-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="92281-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92281-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92281-123">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="92281-123">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
