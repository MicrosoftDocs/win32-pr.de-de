---
description: Beendet eine aktive Technik.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'ID3DXEffect:: End-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: baaccd7710845296497dcc7f16d3d71c7ceeb9bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355016"
---
# <a name="id3dxeffectend-method"></a><span data-ttu-id="c802b-103">ID3DXEffect:: End-Methode</span><span class="sxs-lookup"><span data-stu-id="c802b-103">ID3DXEffect::End method</span></span>

<span data-ttu-id="c802b-104">Beendet eine aktive Technik.</span><span class="sxs-lookup"><span data-stu-id="c802b-104">Ends an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="c802b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c802b-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="c802b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c802b-106">Parameters</span></span>

<span data-ttu-id="c802b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c802b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c802b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c802b-108">Return value</span></span>

<span data-ttu-id="c802b-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c802b-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c802b-110">Diese Methode gibt immer den Wert S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="c802b-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c802b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c802b-111">Remarks</span></span>

<span data-ttu-id="c802b-112">Alle Rendering in einem Effekt erfolgt in einem passenden Paar aus [**ID3DXEffect:: begin**](id3dxeffect--begin.md) -und **ID3DXEffect:: End** -aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c802b-112">All rendering in an effect is done within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and **ID3DXEffect::End** calls.</span></span> <span data-ttu-id="c802b-113">Nachdem alle Durchgänge gerendert wurden, muss **ID3DXEffect:: End** aufgerufen werden, um die aktive Technik zu beenden.</span><span class="sxs-lookup"><span data-stu-id="c802b-113">After all passes are rendered, **ID3DXEffect::End** must be called to end the active technique.</span></span> <span data-ttu-id="c802b-114">Das Effektsystem antwortet mithilfe des Zustands Blocks, der erstellt wurde, als **ID3DXEffect:: begin** aufgerufen wurde, um den Pipeline Zustand vor **ID3DXEffect:: begin** automatisch wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c802b-114">The effect system responds by using the state block created when **ID3DXEffect::Begin** was called, to automatically restore the pipeline state before **ID3DXEffect::Begin**.</span></span>

<span data-ttu-id="c802b-115">Standardmäßig übernimmt das Effektsystem das Speichern des Zustands vor einer Technik und das Wiederherstellen des Zustands nach einer Technik.</span><span class="sxs-lookup"><span data-stu-id="c802b-115">By default, the effect system takes care of saving state prior to a technique, and restoring state after a technique.</span></span> <span data-ttu-id="c802b-116">Wenn Sie diese Speicher-und Wiederherstellungs Funktion deaktivieren möchten, finden Sie weitere Informationen unter [D3DXFX \_ donotsavesamplerstate](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="c802b-116">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c802b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c802b-117">Requirements</span></span>



| <span data-ttu-id="c802b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c802b-118">Requirement</span></span> | <span data-ttu-id="c802b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c802b-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c802b-120">Header</span><span class="sxs-lookup"><span data-stu-id="c802b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c802b-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c802b-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c802b-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c802b-122">Library</span></span><br/> | <dl> <span data-ttu-id="c802b-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c802b-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c802b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c802b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c802b-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="c802b-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




