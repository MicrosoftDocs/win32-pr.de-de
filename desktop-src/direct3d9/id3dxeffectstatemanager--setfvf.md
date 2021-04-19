---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen FVF-Code festzulegen.
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: 'ID3DXEffectStateManager:: setf VF-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetFVF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a68ab07e4f486a8df80ecde5844739a6a010c2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355210"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a><span data-ttu-id="e2683-103">ID3DXEffectStateManager:: setf VF-Methode</span><span class="sxs-lookup"><span data-stu-id="e2683-103">ID3DXEffectStateManager::SetFVF method</span></span>

<span data-ttu-id="e2683-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen FVF-Code festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e2683-104">A callback function that must be implemented by a user to set a FVF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2683-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2683-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="e2683-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2683-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2683-107">*F-VF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2683-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2683-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2683-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2683-109">Die FVF-Konstante, die bestimmt, wie Scheitelpunkt Daten interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="e2683-109">The FVF constant, that determines how to interpret vertex data.</span></span> <span data-ttu-id="e2683-110">Siehe [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="e2683-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2683-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2683-111">Return value</span></span>

<span data-ttu-id="e2683-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2683-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2683-113">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e2683-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="e2683-114">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="e2683-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="e2683-115">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="e2683-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="e2683-116">Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: setfvf**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="e2683-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2683-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2683-117">Requirements</span></span>



| <span data-ttu-id="e2683-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2683-118">Requirement</span></span> | <span data-ttu-id="e2683-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e2683-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2683-120">Header</span><span class="sxs-lookup"><span data-stu-id="e2683-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e2683-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2683-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e2683-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2683-122">Library</span></span><br/> | <dl> <span data-ttu-id="e2683-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2683-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e2683-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2683-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2683-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="e2683-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
