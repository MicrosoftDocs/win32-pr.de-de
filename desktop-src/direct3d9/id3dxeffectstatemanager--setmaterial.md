---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Materialzustand festzulegen.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: 'ID3DXEffectStateManager:: setmaterial-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b503bd195468fb323e7e655c0bdd201e25dfdce2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363153"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a><span data-ttu-id="aeffa-103">ID3DXEffectStateManager:: setmaterial-Methode</span><span class="sxs-lookup"><span data-stu-id="aeffa-103">ID3DXEffectStateManager::SetMaterial method</span></span>

<span data-ttu-id="aeffa-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Materialzustand festzulegen.</span><span class="sxs-lookup"><span data-stu-id="aeffa-104">A callback function that must be implemented by a user to set material state.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeffa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aeffa-105">Syntax</span></span>


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a><span data-ttu-id="aeffa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aeffa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeffa-107">*pmaterial* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aeffa-107">*pMaterial* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeffa-108">Typ: **Konstanten [**D3DMATERIAL9**](d3dmaterial9.md) \***</span><span class="sxs-lookup"><span data-stu-id="aeffa-108">Type: **const [**D3DMATERIAL9**](d3dmaterial9.md)\***</span></span>

<span data-ttu-id="aeffa-109">Ein Zeiger auf den Materialzustand.</span><span class="sxs-lookup"><span data-stu-id="aeffa-109">A pointer to the material state.</span></span> <span data-ttu-id="aeffa-110">Siehe [**D3DMATERIAL9**](d3dmaterial9.md).</span><span class="sxs-lookup"><span data-stu-id="aeffa-110">See [**D3DMATERIAL9**](d3dmaterial9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeffa-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aeffa-111">Return value</span></span>

<span data-ttu-id="aeffa-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aeffa-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aeffa-113">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="aeffa-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="aeffa-114">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="aeffa-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="aeffa-115">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="aeffa-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="aeffa-116">Der Status des dynamischen Effekts (z. b. [**IDirect3DDevice9:: setmaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="aeffa-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeffa-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aeffa-117">Requirements</span></span>



| <span data-ttu-id="aeffa-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aeffa-118">Requirement</span></span> | <span data-ttu-id="aeffa-119">Wert</span><span class="sxs-lookup"><span data-stu-id="aeffa-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeffa-120">Header</span><span class="sxs-lookup"><span data-stu-id="aeffa-120">Header</span></span><br/>  | <dl> <span data-ttu-id="aeffa-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeffa-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="aeffa-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aeffa-122">Library</span></span><br/> | <dl> <span data-ttu-id="aeffa-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aeffa-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="aeffa-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aeffa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeffa-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="aeffa-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
