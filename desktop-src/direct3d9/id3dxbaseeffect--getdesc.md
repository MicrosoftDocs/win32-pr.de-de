---
description: Ruft die Beschreibung des Effekts ab.
ms.assetid: 96b53b8a-0c20-4bfd-af45-626f6e0305d2
title: 'ID3DXBaseEffect:: getdesc-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 35fcb62e9461d419e6643c99c1879efa28fa78c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365133"
---
# <a name="id3dxbaseeffectgetdesc-method"></a><span data-ttu-id="6e1d6-103">ID3DXBaseEffect:: getdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="6e1d6-103">ID3DXBaseEffect::GetDesc method</span></span>

<span data-ttu-id="6e1d6-104">Ruft die Beschreibung des Effekts ab.</span><span class="sxs-lookup"><span data-stu-id="6e1d6-104">Gets the effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e1d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e1d6-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXEFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="6e1d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e1d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e1d6-107">*PDE SC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6e1d6-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e1d6-108">Typ: **[ **D3DXEFFECT \_ DESC**](d3dxeffect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e1d6-108">Type: **[**D3DXEFFECT\_DESC**](d3dxeffect-desc.md)\***</span></span>

<span data-ttu-id="6e1d6-109">Gibt eine Beschreibung des Effekts zurück.</span><span class="sxs-lookup"><span data-stu-id="6e1d6-109">Returns a description of the effect.</span></span> <span data-ttu-id="6e1d6-110">Weitere Informationen finden Sie unter [**D3DXEFFECT \_**](d3dxeffect-desc.md).</span><span class="sxs-lookup"><span data-stu-id="6e1d6-110">See [**D3DXEFFECT\_DESC**](d3dxeffect-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e1d6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e1d6-111">Return value</span></span>

<span data-ttu-id="6e1d6-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6e1d6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6e1d6-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6e1d6-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6e1d6-114">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="6e1d6-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e1d6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e1d6-115">Requirements</span></span>



| <span data-ttu-id="6e1d6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e1d6-116">Requirement</span></span> | <span data-ttu-id="6e1d6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6e1d6-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e1d6-118">Header</span><span class="sxs-lookup"><span data-stu-id="6e1d6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6e1d6-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e1d6-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6e1d6-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6e1d6-120">Library</span></span><br/> | <dl> <span data-ttu-id="6e1d6-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e1d6-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6e1d6-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e1d6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e1d6-123">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="6e1d6-123">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




