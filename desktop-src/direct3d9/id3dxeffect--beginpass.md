---
description: Startet einen Durchlauf innerhalb der aktiven Technik.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'ID3DXEffect:: beginpass-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 56a2648f65c3747f8a98fc0cdbd3ed06cea560b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353367"
---
# <a name="id3dxeffectbeginpass-method"></a><span data-ttu-id="91da7-103">ID3DXEffect:: beginpass-Methode</span><span class="sxs-lookup"><span data-stu-id="91da7-103">ID3DXEffect::BeginPass method</span></span>

<span data-ttu-id="91da7-104">Startet einen Durchlauf innerhalb der aktiven Technik.</span><span class="sxs-lookup"><span data-stu-id="91da7-104">Begins a pass, within the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="91da7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="91da7-105">Syntax</span></span>


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a><span data-ttu-id="91da7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="91da7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91da7-107">*Durchlauf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91da7-107">*Pass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91da7-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91da7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91da7-109">Ein NULL basierter ganzzahliger Index in der Technik.</span><span class="sxs-lookup"><span data-stu-id="91da7-109">A zero-based integer index into the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91da7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91da7-110">Return value</span></span>

<span data-ttu-id="91da7-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91da7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91da7-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="91da7-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="91da7-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="91da7-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="91da7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91da7-114">Remarks</span></span>

<span data-ttu-id="91da7-115">Eine Anwendung legt einen aktiven Durchlauf (innerhalb eines aktiven Verfahrens) im Effektsystem fest, indem **ID3DXEffect:: beginpass** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="91da7-115">An application sets one active pass (within one active technique) in the effect system by calling **ID3DXEffect::BeginPass**.</span></span> <span data-ttu-id="91da7-116">Eine Anwendung signalisiert das Ende des aktiven Pass durch Aufrufen von [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md).</span><span class="sxs-lookup"><span data-stu-id="91da7-116">An application signals the end of the active pass by calling [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="91da7-117">**ID3DXEffect:: beginpass** und **ID3DXEffect:: endpass** müssen in einem übereinstimmenden Paar innerhalb eines übereinstimmenden Paares von [**ID3DXEffect:: begin**](id3dxeffect--begin.md) -und [**ID3DXEffect:: End**](id3dxeffect--end.md) -aufrufen auftreten.</span><span class="sxs-lookup"><span data-stu-id="91da7-117">**ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** must occur in a matching pair, within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="91da7-118">Wenn die Anwendung in einem [](id3dxeffect.md) **ID3DXEffect:: beginpass** / [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) -übereinstimmenden paar den Effekt Zustand ändert, muss Sie [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) aufrufen, um das Update des Geräts mit den Statusänderungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="91da7-118">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a **ID3DXEffect::BeginPass**/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) to set the update the device with the state changes.</span></span> <span data-ttu-id="91da7-119">Wenn keine Zustandsänderungen innerhalb eines **ID3DXEffect:: beginpass** -und **ID3DXEffect:: endpass** -übereinstimmenden Paars auftreten, ist es nicht erforderlich, **ID3DXEffect:: CommitChanges** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="91da7-119">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="91da7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91da7-120">Requirements</span></span>



| <span data-ttu-id="91da7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91da7-121">Requirement</span></span> | <span data-ttu-id="91da7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="91da7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="91da7-123">Header</span><span class="sxs-lookup"><span data-stu-id="91da7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="91da7-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="91da7-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="91da7-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="91da7-125">Library</span></span><br/> | <dl> <span data-ttu-id="91da7-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91da7-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="91da7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91da7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91da7-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="91da7-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
