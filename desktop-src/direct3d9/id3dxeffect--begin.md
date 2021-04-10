---
description: Startet ein aktives Verfahren.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'ID3DXEffect:: Begin-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1912698fbb6d6ac13f119161c4d05926f05d245b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219547"
---
# <a name="id3dxeffectbegin-method"></a><span data-ttu-id="08f16-103">ID3DXEffect:: Begin-Methode</span><span class="sxs-lookup"><span data-stu-id="08f16-103">ID3DXEffect::Begin method</span></span>

<span data-ttu-id="08f16-104">Startet ein aktives Verfahren.</span><span class="sxs-lookup"><span data-stu-id="08f16-104">Starts an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="08f16-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="08f16-105">Syntax</span></span>


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="08f16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08f16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08f16-107">*ppasses* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="08f16-107">*pPasses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08f16-108">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="08f16-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="08f16-109">Ein Zeiger auf einen zurückgegebenen Wert, der die Anzahl der zum renderingder aktuellen Technik benötigten Pass-ins angibt.</span><span class="sxs-lookup"><span data-stu-id="08f16-109">Pointer to a value returned that indicates the number of passes needed to render the current technique.</span></span>

</dd> <dt>

<span data-ttu-id="08f16-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="08f16-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08f16-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08f16-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08f16-112">DWORD, das bestimmt, ob der durch einen Effekt geänderte Zustand gespeichert und wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="08f16-112">DWORD that determines if state modified by an effect is saved and restored.</span></span> <span data-ttu-id="08f16-113">Der Standardwert 0 gibt an, dass **ID3DXEffect:: begin** und [**ID3DXEffect:: End**](id3dxeffect--end.md) alle durch den Effekt geänderten Status (einschließlich Pixel-und Vertexshader-Konstanten) speichern und wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="08f16-113">The default value 0 specifies that **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) will save and restore all state modified by the effect (including pixel and vertex shader constants).</span></span> <span data-ttu-id="08f16-114">Gültige Flags können als [Speicher-und Wiederherstellungs Flags des Effekts](d3dxfx.md)erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="08f16-114">Valid flags can be seen at [Effect State Save and Restore Flags](d3dxfx.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08f16-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08f16-115">Return value</span></span>

<span data-ttu-id="08f16-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="08f16-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="08f16-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="08f16-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="08f16-118">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="08f16-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="08f16-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08f16-119">Remarks</span></span>

<span data-ttu-id="08f16-120">Eine Anwendung legt eine aktive Technik im Effektsystem fest, indem **ID3DXEffect:: begin** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="08f16-120">An application sets one active technique in the effect system by calling **ID3DXEffect::Begin**.</span></span> <span data-ttu-id="08f16-121">Das Effektsystem antwortet, indem er den gesamten Pipeline Status erfasst, der durch die Technik in einem Zustands Block geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="08f16-121">The effect system responds by capturing all the pipeline state that can be changed by the technique in a state block.</span></span> <span data-ttu-id="08f16-122">Eine Anwendung signalisiert das Ende einer Technik durch Aufrufen von [**ID3DXEffect:: End**](id3dxeffect--end.md), bei der der State-Block verwendet wird, um den ursprünglichen Zustand wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="08f16-122">An application signals the end of a technique by calling [**ID3DXEffect::End**](id3dxeffect--end.md), which uses the state block to restore the original state.</span></span> <span data-ttu-id="08f16-123">Folglich übernimmt das Effektsystem das Speichern des Zustands, wenn eine Technik aktiv wird und der Zustand wieder hergestellt wird, wenn eine Technik endet.</span><span class="sxs-lookup"><span data-stu-id="08f16-123">The effect system, therefore, takes care of saving state when a technique becomes active and restoring state when a technique ends.</span></span> <span data-ttu-id="08f16-124">Wenn Sie diese Speicher-und Wiederherstellungs Funktion deaktivieren möchten, finden Sie weitere Informationen unter [D3DXFX \_ donotsavesamplerstate](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="08f16-124">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

<span data-ttu-id="08f16-125">Innerhalb des **ID3DXEffect:: begin** -und [**ID3DXEffect:: End**](id3dxeffect--end.md) -Paars verwendet eine Anwendung [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) , um den aktiven Durchlauf festzulegen, [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) , wenn nach dem Aktivieren des Pass Zustandsänderungen aufgetreten sind, und [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) , um den aktiven Durchlauf zu beenden.</span><span class="sxs-lookup"><span data-stu-id="08f16-125">Within the **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) pair, an application uses [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) to set the active pass, [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) if any state changes occurred after the pass was activated, and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) to end the active pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="08f16-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08f16-126">Requirements</span></span>



| <span data-ttu-id="08f16-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08f16-127">Requirement</span></span> | <span data-ttu-id="08f16-128">Wert</span><span class="sxs-lookup"><span data-stu-id="08f16-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08f16-129">Header</span><span class="sxs-lookup"><span data-stu-id="08f16-129">Header</span></span><br/>  | <dl> <span data-ttu-id="08f16-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="08f16-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="08f16-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="08f16-131">Library</span></span><br/> | <dl> <span data-ttu-id="08f16-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08f16-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="08f16-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08f16-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f16-134">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="08f16-134">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
