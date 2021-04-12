---
description: Erstellen Sie einen Effekt Pool. Ein Pool wird verwendet, um Parameter zwischen Effekten gemeinsam zu nutzen.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: D3DXCreateEffectPool-Funktion (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219668"
---
# <a name="d3dxcreateeffectpool-function"></a><span data-ttu-id="50b45-104">D3DXCreateEffectPool-Funktion</span><span class="sxs-lookup"><span data-stu-id="50b45-104">D3DXCreateEffectPool function</span></span>

<span data-ttu-id="50b45-105">Erstellen Sie einen Effekt Pool.</span><span class="sxs-lookup"><span data-stu-id="50b45-105">Create an effect pool.</span></span> <span data-ttu-id="50b45-106">Ein Pool wird verwendet, um Parameter zwischen Effekten gemeinsam zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="50b45-106">A pool is used to share parameters between effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b45-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="50b45-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="50b45-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="50b45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50b45-109">*pppool* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="50b45-109">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50b45-110">Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="50b45-110">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="50b45-111">Gibt einen Zeiger auf den erstellten Pool zurück.</span><span class="sxs-lookup"><span data-stu-id="50b45-111">Returns a pointer to the created pool.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50b45-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50b45-112">Return value</span></span>

<span data-ttu-id="50b45-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="50b45-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="50b45-114">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="50b45-114">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="50b45-115">Wenn die Argumente ungültig sind, gibt die Methode D3DERR \_ invalidcallzurück.</span><span class="sxs-lookup"><span data-stu-id="50b45-115">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="50b45-116">Wenn die Methode fehlschlägt, lautet der Rückgabewert E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="50b45-116">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="50b45-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50b45-117">Remarks</span></span>

<span data-ttu-id="50b45-118">Für Effekte innerhalb eines Pools werden freigegebene Parameter mit dem gleichen Namen gemeinsam verwendet.</span><span class="sxs-lookup"><span data-stu-id="50b45-118">For effects within a pool, shared parameters with the same name share values.</span></span>

## <a name="requirements"></a><span data-ttu-id="50b45-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50b45-119">Requirements</span></span>



| <span data-ttu-id="50b45-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50b45-120">Requirement</span></span> | <span data-ttu-id="50b45-121">Wert</span><span class="sxs-lookup"><span data-stu-id="50b45-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b45-122">Header</span><span class="sxs-lookup"><span data-stu-id="50b45-122">Header</span></span><br/>  | <dl> <span data-ttu-id="50b45-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="50b45-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="50b45-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="50b45-124">Library</span></span><br/> | <dl> <span data-ttu-id="50b45-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50b45-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="50b45-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50b45-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b45-127">Effekt Funktionen</span><span class="sxs-lookup"><span data-stu-id="50b45-127">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




