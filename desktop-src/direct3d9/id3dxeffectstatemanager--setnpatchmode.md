---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um die Anzahl der unter Divisions Segmente für N-Patches festzulegen.
ms.assetid: f94910ee-3385-44d3-b4f1-a0e88c7afa39
title: 'ID3DXEffectStateManager:: setnpatchmode-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetNPatchMode
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9b8725a0482b6945b04013df43d34a502f25b7b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961752"
---
# <a name="id3dxeffectstatemanagersetnpatchmode-method"></a><span data-ttu-id="08e30-103">ID3DXEffectStateManager:: setnpatchmode-Methode</span><span class="sxs-lookup"><span data-stu-id="08e30-103">ID3DXEffectStateManager::SetNPatchMode method</span></span>

<span data-ttu-id="08e30-104">Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um die Anzahl der unter Divisions Segmente für N-Patches festzulegen.</span><span class="sxs-lookup"><span data-stu-id="08e30-104">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e30-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="08e30-105">Syntax</span></span>


```C++
HRESULT SetNPatchMode(
  [in] FLOAT nSegments
);
```



## <a name="parameters"></a><span data-ttu-id="08e30-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08e30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08e30-107">*nsegmente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08e30-107">*nSegments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08e30-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08e30-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08e30-109">Unterteilen Sie die Oberfläche in diese Anzahl von Unterteilungen.</span><span class="sxs-lookup"><span data-stu-id="08e30-109">Break the surface into this number of subdivisions.</span></span> <span data-ttu-id="08e30-110">Dies entspricht der Anzahl, die von [**IDirect3DDevice9:: setnpatchmode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08e30-110">This is the same as the number used by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08e30-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08e30-111">Return value</span></span>

<span data-ttu-id="08e30-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="08e30-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="08e30-113">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="08e30-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="08e30-114">Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="08e30-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="08e30-115">Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="08e30-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="08e30-116">Der dynamische Effekt Status-aufrufen (z. b. [**IDirect3DDevice9:: setnpatchmode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="08e30-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="08e30-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08e30-117">Requirements</span></span>



| <span data-ttu-id="08e30-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08e30-118">Requirement</span></span> | <span data-ttu-id="08e30-119">Wert</span><span class="sxs-lookup"><span data-stu-id="08e30-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08e30-120">Header</span><span class="sxs-lookup"><span data-stu-id="08e30-120">Header</span></span><br/>  | <dl> <span data-ttu-id="08e30-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="08e30-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="08e30-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="08e30-122">Library</span></span><br/> | <dl> <span data-ttu-id="08e30-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08e30-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="08e30-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08e30-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08e30-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="08e30-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
