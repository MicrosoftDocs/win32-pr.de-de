---
description: Holen Sie sich den Effekt Zustands-Manager.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'ID3DXEffect:: GetStatus Manager-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 293b642dfecfa4cc14426addf2567d43dffa7233
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371898"
---
# <a name="id3dxeffectgetstatemanager-method"></a><span data-ttu-id="20575-103">ID3DXEffect:: GetStatus Manager-Methode</span><span class="sxs-lookup"><span data-stu-id="20575-103">ID3DXEffect::GetStateManager method</span></span>

<span data-ttu-id="20575-104">Holen Sie sich den Effekt Zustands-Manager.</span><span class="sxs-lookup"><span data-stu-id="20575-104">Get the effect state manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="20575-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20575-105">Syntax</span></span>


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="20575-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20575-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20575-107">*ppManager* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="20575-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20575-108">Typ: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***</span><span class="sxs-lookup"><span data-stu-id="20575-108">Type: **[**LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***</span></span>

<span data-ttu-id="20575-109">Gibt einen Zeiger auf den Zustands-Manager zurück.</span><span class="sxs-lookup"><span data-stu-id="20575-109">Returns a pointer to the state manager.</span></span> <span data-ttu-id="20575-110">Siehe [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="20575-110">See [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20575-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20575-111">Return value</span></span>

<span data-ttu-id="20575-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="20575-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="20575-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20575-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="20575-114">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="20575-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="20575-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20575-115">Remarks</span></span>

<span data-ttu-id="20575-116">[**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) ist eine vom Benutzer implementierte Schnittstelle, die Rückrufe in eine Anwendung eingibt, um den Gerätezustand von einem Effekt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="20575-116">The [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) is a user-implemented interface that furnishes callbacks into an application for setting device state from an effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="20575-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20575-117">Requirements</span></span>



| <span data-ttu-id="20575-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20575-118">Requirement</span></span> | <span data-ttu-id="20575-119">Wert</span><span class="sxs-lookup"><span data-stu-id="20575-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20575-120">Header</span><span class="sxs-lookup"><span data-stu-id="20575-120">Header</span></span><br/>  | <dl> <span data-ttu-id="20575-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="20575-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="20575-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="20575-122">Library</span></span><br/> | <dl> <span data-ttu-id="20575-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20575-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="20575-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20575-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20575-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="20575-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="20575-126">**ID3DXEffect:: SetStatus Manager**</span><span class="sxs-lookup"><span data-stu-id="20575-126">**ID3DXEffect::SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




