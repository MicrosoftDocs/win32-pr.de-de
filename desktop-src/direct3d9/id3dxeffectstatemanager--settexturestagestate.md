---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Status der Textur Stufe festzulegen.
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: 'ID3DXEffectStateManager:: settexturestagestate-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTextureStageState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 937fd3f2b89dc093d9dceb9441f53d6be2cb06b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357252"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a><span data-ttu-id="71470-103">ID3DXEffectStateManager:: settexturestagestate-Methode</span><span class="sxs-lookup"><span data-stu-id="71470-103">ID3DXEffectStateManager::SetTextureStageState method</span></span>

<span data-ttu-id="71470-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Status der Textur Stufe festzulegen.</span><span class="sxs-lookup"><span data-stu-id="71470-104">A callback function that must be implemented by a user to set the texture stage state.</span></span>

## <a name="syntax"></a><span data-ttu-id="71470-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="71470-105">Syntax</span></span>


```C++
HRESULT SetTextureStageState(
  [in] DWORD                    Stage,
  [in] D3DTEXTURESTAGESTATETYPE Type,
  [in] DWORD                    Value
);
```



## <a name="parameters"></a><span data-ttu-id="71470-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="71470-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71470-107">*Stage* \[in\]</span><span class="sxs-lookup"><span data-stu-id="71470-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71470-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71470-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71470-109">Die Stufe, der die Textur zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="71470-109">The stage that the texture is assigned to.</span></span> <span data-ttu-id="71470-110">Dies ist der Indexwert in [**IDirect3DDevice9:: SetTexture**](/windows/desktop/api) oder [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="71470-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/desktop/api) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="71470-111">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71470-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71470-112">Typ: **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="71470-112">Type: **[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span></span>

<span data-ttu-id="71470-113">Definiert den Typ des Vorgangs, der von einer Textur Phase durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71470-113">Defines the type of operation that a texture stage will perform.</span></span> <span data-ttu-id="71470-114">Siehe [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span><span class="sxs-lookup"><span data-stu-id="71470-114">See [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="71470-115">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71470-115">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71470-116">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71470-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71470-117">Kann entweder ein Vorgang ([**D3DTEXTUREOP**](./d3dtextureop.md)) oder ein Argument Wert ([D3DTA](d3dta.md)) sein, je nachdem, was für den Typ ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="71470-117">Can be either an operation ([**D3DTEXTUREOP**](./d3dtextureop.md)) or an argument value ([D3DTA](d3dta.md)), depending on what is chosen for Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71470-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71470-118">Return value</span></span>

<span data-ttu-id="71470-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71470-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71470-120">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="71470-120">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="71470-121">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="71470-121">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="71470-122">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="71470-122">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="71470-123">Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="71470-123">The dynamic effect state call (such as [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="71470-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71470-124">Requirements</span></span>



| <span data-ttu-id="71470-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71470-125">Requirement</span></span> | <span data-ttu-id="71470-126">Wert</span><span class="sxs-lookup"><span data-stu-id="71470-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="71470-127">Header</span><span class="sxs-lookup"><span data-stu-id="71470-127">Header</span></span><br/>  | <dl> <span data-ttu-id="71470-128"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="71470-128"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="71470-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71470-129">Library</span></span><br/> | <dl> <span data-ttu-id="71470-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71470-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="71470-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71470-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71470-132">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="71470-132">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
