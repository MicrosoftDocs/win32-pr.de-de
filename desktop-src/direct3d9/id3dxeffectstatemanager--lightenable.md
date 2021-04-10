---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht zu aktivieren bzw. zu deaktivieren.
ms.assetid: 11522ca3-8a2f-4767-a6e6-4186cb4f3115
title: 'ID3DXEffectStateManager:: lightenable-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.LightEnable
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d065540eb036b26cdd19791dc393d32c5b45e3ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219598"
---
# <a name="id3dxeffectstatemanagerlightenable-method"></a><span data-ttu-id="79774-103">ID3DXEffectStateManager:: lightenable-Methode</span><span class="sxs-lookup"><span data-stu-id="79774-103">ID3DXEffectStateManager::LightEnable method</span></span>

<span data-ttu-id="79774-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht zu aktivieren bzw. zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="79774-104">A callback function that must be implemented by a user to enable/disable a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="79774-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79774-105">Syntax</span></span>


```C++
HRESULT LightEnable(
  [in] DWORD Index,
  [in] BOOL  Enable
);
```



## <a name="parameters"></a><span data-ttu-id="79774-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79774-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79774-107">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79774-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79774-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79774-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79774-109">Der null basierte Index des Lichts.</span><span class="sxs-lookup"><span data-stu-id="79774-109">The zero-based index of the light.</span></span> <span data-ttu-id="79774-110">Dies ist derselbe Index in [**IDirect3DDevice9:: setlight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span><span class="sxs-lookup"><span data-stu-id="79774-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="79774-111">*Aktivieren* \[ von in\]</span><span class="sxs-lookup"><span data-stu-id="79774-111">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79774-112">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79774-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79774-113">True, wenn das Licht aktiviert werden soll, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="79774-113">True to enable the light, false otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79774-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79774-114">Return value</span></span>

<span data-ttu-id="79774-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79774-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79774-116">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="79774-116">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="79774-117">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="79774-117">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="79774-118">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="79774-118">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="79774-119">Der Aufruf des dynamischen Effekts-Zustands (z. [**b. IDirect3DDevice9:: lightenable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="79774-119">The dynamic effect state call (such as [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="79774-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79774-120">Requirements</span></span>



| <span data-ttu-id="79774-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79774-121">Requirement</span></span> | <span data-ttu-id="79774-122">Wert</span><span class="sxs-lookup"><span data-stu-id="79774-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="79774-123">Header</span><span class="sxs-lookup"><span data-stu-id="79774-123">Header</span></span><br/>  | <dl> <span data-ttu-id="79774-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="79774-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="79774-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="79774-125">Library</span></span><br/> | <dl> <span data-ttu-id="79774-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79774-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="79774-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79774-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79774-128">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="79774-128">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
