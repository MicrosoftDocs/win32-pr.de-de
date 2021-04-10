---
description: Ruft einen Zeiger auf den Pool von freigegebenen Parametern ab.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: 'ID3DXEffect:: getpool-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetPool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 18a35e9bc0a596cb88da6d4c1faf10941fbce8a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961564"
---
# <a name="id3dxeffectgetpool-method"></a><span data-ttu-id="19082-103">ID3DXEffect:: getpool-Methode</span><span class="sxs-lookup"><span data-stu-id="19082-103">ID3DXEffect::GetPool method</span></span>

<span data-ttu-id="19082-104">Ruft einen Zeiger auf den Pool von freigegebenen Parametern ab.</span><span class="sxs-lookup"><span data-stu-id="19082-104">Gets a pointer to the pool of shared parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="19082-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19082-105">Syntax</span></span>


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="19082-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19082-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19082-107">*pppool* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="19082-107">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19082-108">Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="19082-108">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="19082-109">Zeiger auf ein [**ID3DXEffectPool**](id3dxeffectpool.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="19082-109">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19082-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19082-110">Return value</span></span>

<span data-ttu-id="19082-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19082-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19082-112">Diese Methode gibt immer den Wert S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="19082-112">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="19082-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19082-113">Remarks</span></span>

<span data-ttu-id="19082-114">Pools enthalten freigegebene Parameter zwischen Effekten.</span><span class="sxs-lookup"><span data-stu-id="19082-114">Pools contain shared parameters between effects.</span></span> <span data-ttu-id="19082-115">Weitere Informationen finden Sie unter [Klonen und freigeben (Direct3D 9)](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="19082-115">See [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19082-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19082-116">Requirements</span></span>



| <span data-ttu-id="19082-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19082-117">Requirement</span></span> | <span data-ttu-id="19082-118">Wert</span><span class="sxs-lookup"><span data-stu-id="19082-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19082-119">Header</span><span class="sxs-lookup"><span data-stu-id="19082-119">Header</span></span><br/>  | <dl> <span data-ttu-id="19082-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="19082-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="19082-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="19082-121">Library</span></span><br/> | <dl> <span data-ttu-id="19082-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19082-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="19082-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19082-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19082-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="19082-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




