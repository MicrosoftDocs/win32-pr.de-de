---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht festzulegen.
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: 'ID3DXEffectStateManager:: setlight-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1306283b098922706f39abc7ffe2514d2fba0e5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353375"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a><span data-ttu-id="0e57b-103">ID3DXEffectStateManager:: setlight-Methode</span><span class="sxs-lookup"><span data-stu-id="0e57b-103">ID3DXEffectStateManager::SetLight method</span></span>

<span data-ttu-id="0e57b-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0e57b-104">A callback function that must be implemented by a user to set a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e57b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e57b-105">Syntax</span></span>


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a><span data-ttu-id="0e57b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e57b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e57b-107">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e57b-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e57b-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e57b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e57b-109">Der null basierte Index des Lichts.</span><span class="sxs-lookup"><span data-stu-id="0e57b-109">The zero-based index of the light.</span></span> <span data-ttu-id="0e57b-110">Dies ist derselbe Index in [**IDirect3DDevice9:: setlight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span><span class="sxs-lookup"><span data-stu-id="0e57b-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="0e57b-111">*Notlage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e57b-111">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e57b-112">Typ: **Konstanten [**D3DLight9**](d3dlight9.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e57b-112">Type: **const [**D3DLight9**](d3dlight9.md)\***</span></span>

<span data-ttu-id="0e57b-113">Das Light-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0e57b-113">The light object.</span></span> <span data-ttu-id="0e57b-114">Siehe [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="0e57b-114">See [**D3DLIGHT9**](d3dlight9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e57b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e57b-115">Return value</span></span>

<span data-ttu-id="0e57b-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e57b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e57b-117">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0e57b-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="0e57b-118">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="0e57b-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="0e57b-119">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="0e57b-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="0e57b-120">Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: setlight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="0e57b-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e57b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e57b-121">Requirements</span></span>



| <span data-ttu-id="0e57b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e57b-122">Requirement</span></span> | <span data-ttu-id="0e57b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0e57b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e57b-124">Header</span><span class="sxs-lookup"><span data-stu-id="0e57b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0e57b-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e57b-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0e57b-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e57b-126">Library</span></span><br/> | <dl> <span data-ttu-id="0e57b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e57b-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0e57b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e57b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e57b-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="0e57b-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
