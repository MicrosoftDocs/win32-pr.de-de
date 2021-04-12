---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Sampler festzulegen.
ms.assetid: 1e19e8cd-341d-4372-9182-8b3c82155407
title: 'ID3DXEffectStateManager:: setsamplerstate-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetSamplerState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bba12db8dbc1902adc5c64b4cc1726e081dfea70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355177"
---
# <a name="id3dxeffectstatemanagersetsamplerstate-method"></a><span data-ttu-id="66194-103">ID3DXEffectStateManager:: setsamplerstate-Methode</span><span class="sxs-lookup"><span data-stu-id="66194-103">ID3DXEffectStateManager::SetSamplerState method</span></span>

<span data-ttu-id="66194-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Sampler festzulegen.</span><span class="sxs-lookup"><span data-stu-id="66194-104">A callback function that must be implemented by a user to set a sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="66194-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="66194-105">Syntax</span></span>


```C++
HRESULT SetSamplerState(
  [in] DWORD               Sampler,
  [in] D3DSAMPLERSTATETYPE Type,
  [in] DWORD               Value
);
```



## <a name="parameters"></a><span data-ttu-id="66194-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="66194-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66194-107">*Sampler* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66194-107">*Sampler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66194-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66194-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66194-109">Die null basierte samplernummer.</span><span class="sxs-lookup"><span data-stu-id="66194-109">The zero-based sampler number.</span></span>

</dd> <dt>

<span data-ttu-id="66194-110">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66194-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66194-111">Typ: **[ **D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="66194-111">Type: **[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span></span>

<span data-ttu-id="66194-112">Identifiziert den samplerstatus, der die Filterung, Adressierung oder die Rahmenfarbe angeben kann.</span><span class="sxs-lookup"><span data-stu-id="66194-112">Identifies sampler state, which can specify the filtering, addressing, or the border color.</span></span> <span data-ttu-id="66194-113">Siehe [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="66194-113">See [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="66194-114">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66194-114">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66194-115">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66194-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66194-116">Ein Wert von einem der samplerstatustypen im-Typ.</span><span class="sxs-lookup"><span data-stu-id="66194-116">A value from one of the sampler state types in Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66194-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66194-117">Return value</span></span>

<span data-ttu-id="66194-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66194-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66194-119">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="66194-119">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="66194-120">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="66194-120">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="66194-121">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="66194-121">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="66194-122">Der Status des dynamischen Effekts (z. b. [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="66194-122">The dynamic effect state call (such as [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="66194-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66194-123">Requirements</span></span>



| <span data-ttu-id="66194-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66194-124">Requirement</span></span> | <span data-ttu-id="66194-125">Wert</span><span class="sxs-lookup"><span data-stu-id="66194-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66194-126">Header</span><span class="sxs-lookup"><span data-stu-id="66194-126">Header</span></span><br/>  | <dl> <span data-ttu-id="66194-127"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="66194-127"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="66194-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="66194-128">Library</span></span><br/> | <dl> <span data-ttu-id="66194-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66194-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="66194-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66194-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66194-131">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="66194-131">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
