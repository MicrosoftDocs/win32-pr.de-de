---
title: ID3DX11Effect getdevice-Methode (D3dx11effect. h)
description: Holen Sie sich das Gerät, das den Effekt erzeugt hat.
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- Getdevice-Methode Direct3D 11
- Getdevice-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, getdevice-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25317740cade8a937aeeeac29f5a608bb4a43931
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219646"
---
# <a name="id3dx11effectgetdevice-method"></a><span data-ttu-id="9f58c-106">ID3DX11Effect:: getdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="9f58c-106">ID3DX11Effect::GetDevice method</span></span>

<span data-ttu-id="9f58c-107">Holen Sie sich das Gerät, das den Effekt erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="9f58c-107">Get the device that created the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f58c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f58c-108">Syntax</span></span>


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="9f58c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f58c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f58c-110">*ppdevice*</span><span class="sxs-lookup"><span data-stu-id="9f58c-110">*ppDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="9f58c-111">Typ: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span><span class="sxs-lookup"><span data-stu-id="9f58c-111">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span></span>

<span data-ttu-id="9f58c-112">Ein Zeiger auf eine [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span><span class="sxs-lookup"><span data-stu-id="9f58c-112">A pointer to an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f58c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f58c-113">Return value</span></span>

<span data-ttu-id="9f58c-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9f58c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9f58c-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="9f58c-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f58c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f58c-116">Remarks</span></span>

<span data-ttu-id="9f58c-117">Für ein bestimmtes Gerät wird ein Effekt erstellt, indem eine Funktion wie [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9f58c-117">An effect is created for a specific device, by calling a function such as [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

> [!Note]  
> <span data-ttu-id="9f58c-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="9f58c-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9f58c-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9f58c-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9f58c-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9f58c-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9f58c-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9f58c-121">Requirements</span></span>



| <span data-ttu-id="9f58c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f58c-122">Requirement</span></span> | <span data-ttu-id="9f58c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9f58c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f58c-124">Header</span><span class="sxs-lookup"><span data-stu-id="9f58c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9f58c-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f58c-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9f58c-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9f58c-126">Library</span></span><br/> | <dl> <span data-ttu-id="9f58c-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="9f58c-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f58c-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9f58c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f58c-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="9f58c-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





