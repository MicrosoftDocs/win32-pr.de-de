---
description: Anwendungen verwenden die ID3DXEffectPool-Schnittstelle, um Parameter zu identifizieren, die von den einzelnen Effekten gemeinsam genutzt werden. Weitere Informationen finden Sie unter Parameter Freigabe beim Klonen und freigeben (Direct3D 9). Diese Schnittstelle verfügt über keine Methoden.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: ID3DXEffectPool-Schnittstelle (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394070"
---
# <a name="id3dxeffectpool-interface"></a><span data-ttu-id="ae2a8-105">ID3DXEffectPool-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ae2a8-105">ID3DXEffectPool interface</span></span>

<span data-ttu-id="ae2a8-106">Anwendungen verwenden die **ID3DXEffectPool** -Schnittstelle, um Parameter zu identifizieren, die von den einzelnen Effekten gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="ae2a8-106">Applications use the **ID3DXEffectPool** interface to identify parameters that are going to be shared across effects.</span></span> <span data-ttu-id="ae2a8-107">Weitere Informationen finden Sie unter Parameter Freigabe beim [Klonen und freigeben (Direct3D 9)](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="ae2a8-107">See parameter sharing in [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span> <span data-ttu-id="ae2a8-108">Diese Schnittstelle verfügt über keine Methoden.</span><span class="sxs-lookup"><span data-stu-id="ae2a8-108">This interface has no methods.</span></span>

## <a name="members"></a><span data-ttu-id="ae2a8-109">Member</span><span class="sxs-lookup"><span data-stu-id="ae2a8-109">Members</span></span>

<span data-ttu-id="ae2a8-110">Die **ID3DXEffectPool** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="ae2a8-110">The **ID3DXEffectPool** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae2a8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae2a8-111">Remarks</span></span>

<span data-ttu-id="ae2a8-112">Die ID3DXEffectPool-Schnittstelle wird durch Aufrufen von [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ae2a8-112">The ID3DXEffectPool interface is obtained by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).</span></span>

<span data-ttu-id="ae2a8-113">Der LPD3DXEFFECTPOOL-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="ae2a8-113">The LPD3DXEFFECTPOOL type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a><span data-ttu-id="ae2a8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae2a8-114">Requirements</span></span>



| <span data-ttu-id="ae2a8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae2a8-115">Requirement</span></span> | <span data-ttu-id="ae2a8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ae2a8-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2a8-117">Header</span><span class="sxs-lookup"><span data-stu-id="ae2a8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ae2a8-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2a8-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="ae2a8-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ae2a8-119">Library</span></span><br/> | <dl> <span data-ttu-id="ae2a8-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae2a8-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ae2a8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae2a8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2a8-122">Effekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ae2a8-122">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
