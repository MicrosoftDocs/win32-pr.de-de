---
description: Schaltet alle D3DX-Debugausgaben ein bzw. aus.
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: D3DXDebugMute-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDebugMute
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9259fa43a6a64829e42cbaa661aa7223a958f22d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219519"
---
# <a name="d3dxdebugmute-function"></a><span data-ttu-id="bca75-103">D3DXDebugMute-Funktion</span><span class="sxs-lookup"><span data-stu-id="bca75-103">D3DXDebugMute function</span></span>

<span data-ttu-id="bca75-104">Schaltet alle D3DX-Debugausgaben ein bzw. aus.</span><span class="sxs-lookup"><span data-stu-id="bca75-104">Turns on or off all D3DX debug output.</span></span>

## <a name="syntax"></a><span data-ttu-id="bca75-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bca75-105">Syntax</span></span>


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="bca75-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bca75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bca75-107">*Stumm schalten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bca75-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bca75-108">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bca75-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bca75-109">**True** gibt an, dass die Debugger-Ausgabe angehalten wird. **false** gibt an, dass die Debugausgabe aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bca75-109">If **TRUE**, debugger output is halted; if **FALSE**, debug output is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bca75-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bca75-110">Return value</span></span>

<span data-ttu-id="bca75-111">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bca75-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bca75-112">Gibt den vorherigen Wert von "stumm" zurück.</span><span class="sxs-lookup"><span data-stu-id="bca75-112">Returns the previous value of Mute.</span></span>

## <a name="requirements"></a><span data-ttu-id="bca75-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bca75-113">Requirements</span></span>



| <span data-ttu-id="bca75-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bca75-114">Requirement</span></span> | <span data-ttu-id="bca75-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bca75-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bca75-116">Header</span><span class="sxs-lookup"><span data-stu-id="bca75-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bca75-117"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="bca75-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="bca75-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bca75-118">Library</span></span><br/> | <dl> <span data-ttu-id="bca75-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bca75-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bca75-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bca75-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bca75-121">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="bca75-121">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
