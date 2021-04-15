---
description: Legen Sie den Effekt Zustands-Manager fest.
ms.assetid: 87409687-03f1-4593-ae58-3a8ba08e592b
title: 'ID3DXEffect:: setstatuemanager-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bb32e3f668884a6f51bd5c5058a4f27e141f0aa3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394074"
---
# <a name="id3dxeffectsetstatemanager-method"></a><span data-ttu-id="8d3f9-103">ID3DXEffect:: setstatuemanager-Methode</span><span class="sxs-lookup"><span data-stu-id="8d3f9-103">ID3DXEffect::SetStateManager method</span></span>

<span data-ttu-id="8d3f9-104">Legen Sie den Effekt Zustands-Manager fest.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-104">Set the effect state manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d3f9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d3f9-105">Syntax</span></span>


```C++
HRESULT SetStateManager(
  [in] LPD3DXEFFECTSTATEMANAGER pManager
);
```



## <a name="parameters"></a><span data-ttu-id="8d3f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d3f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d3f9-107">*pManager* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d3f9-107">*pManager* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d3f9-108">Typ: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**</span><span class="sxs-lookup"><span data-stu-id="8d3f9-108">Type: **[**LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**</span></span>

<span data-ttu-id="8d3f9-109">Ein Zeiger auf den Zustands-Manager.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-109">A pointer to the state manager.</span></span> <span data-ttu-id="8d3f9-110">Siehe [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="8d3f9-110">See [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d3f9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d3f9-111">Return value</span></span>

<span data-ttu-id="8d3f9-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8d3f9-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8d3f9-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8d3f9-114">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d3f9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d3f9-115">Remarks</span></span>

<span data-ttu-id="8d3f9-116">[**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) ist eine vom Benutzer implementierte Schnittstelle, die Rückrufe in eine Anwendung eingibt, um den Gerätezustand von einem Effekt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8d3f9-116">The [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) is a user-implemented interface that furnishes callbacks into an application for setting device state from an effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d3f9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d3f9-117">Requirements</span></span>



| <span data-ttu-id="8d3f9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d3f9-118">Requirement</span></span> | <span data-ttu-id="8d3f9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8d3f9-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d3f9-120">Header</span><span class="sxs-lookup"><span data-stu-id="8d3f9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8d3f9-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d3f9-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8d3f9-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8d3f9-122">Library</span></span><br/> | <dl> <span data-ttu-id="8d3f9-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d3f9-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8d3f9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d3f9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d3f9-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="8d3f9-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="8d3f9-126">**ID3DXEffect:: GetStatus Manager**</span><span class="sxs-lookup"><span data-stu-id="8d3f9-126">**ID3DXEffect::GetStateManager**</span></span>](id3dxeffect--getstatemanager.md)
</dt> </dl>

 

 




