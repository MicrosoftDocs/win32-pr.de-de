---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Textur festzulegen.
ms.assetid: 971802f4-ea7a-4906-83b8-0cd83111716e
title: 'ID3DXEffectStateManager:: SetTexture-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b395c19b65bb39b8328da24f727292f7dbe2a0f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530974"
---
# <a name="id3dxeffectstatemanagersettexture-method"></a><span data-ttu-id="329b1-103">ID3DXEffectStateManager:: SetTexture-Methode</span><span class="sxs-lookup"><span data-stu-id="329b1-103">ID3DXEffectStateManager::SetTexture method</span></span>

<span data-ttu-id="329b1-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Textur festzulegen.</span><span class="sxs-lookup"><span data-stu-id="329b1-104">A callback function that must be implemented by a user to set a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="329b1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="329b1-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] DWORD                  Stage,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="329b1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="329b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="329b1-107">*Stage* \[in\]</span><span class="sxs-lookup"><span data-stu-id="329b1-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="329b1-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="329b1-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="329b1-109">Die Stufe, der die Textur zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="329b1-109">The stage to which the texture is assigned.</span></span> <span data-ttu-id="329b1-110">Dies ist der Indexwert in [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) oder [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="329b1-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="329b1-111">*ptexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="329b1-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="329b1-112">Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="329b1-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="329b1-113">Ein Zeiger auf das Textur Objekt.</span><span class="sxs-lookup"><span data-stu-id="329b1-113">A pointer to the texture object.</span></span> <span data-ttu-id="329b1-114">Dabei kann es sich um einen beliebigen Direct3D-Textur Typen (Cube, Volume usw.) handeln.</span><span class="sxs-lookup"><span data-stu-id="329b1-114">This can be any of the Direct3D texture types (cube, volume, etc.).</span></span> <span data-ttu-id="329b1-115">Siehe [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="329b1-115">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="329b1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="329b1-116">Return value</span></span>

<span data-ttu-id="329b1-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="329b1-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="329b1-118">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="329b1-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="329b1-119">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="329b1-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="329b1-120">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="329b1-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="329b1-121">Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="329b1-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="329b1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="329b1-122">Requirements</span></span>



| <span data-ttu-id="329b1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="329b1-123">Requirement</span></span> | <span data-ttu-id="329b1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="329b1-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="329b1-125">Header</span><span class="sxs-lookup"><span data-stu-id="329b1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="329b1-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="329b1-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="329b1-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="329b1-127">Library</span></span><br/> | <dl> <span data-ttu-id="329b1-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="329b1-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="329b1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="329b1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="329b1-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="329b1-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
