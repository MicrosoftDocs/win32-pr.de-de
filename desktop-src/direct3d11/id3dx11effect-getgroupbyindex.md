---
title: ID3DX11Effect getgroupbyindex-Methode (D3dx11effect. h)
description: Ruft eine Effekt Gruppe nach Index ab.
ms.assetid: b38ecdbf-0920-48ff-a599-9629a3581d75
keywords:
- Getgroupbyindex-Methode Direct3D 11
- Getgroupbyindex-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, getgroupbyindex-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd0f629a60255ed28aa5cc426b99198867e0b23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961707"
---
# <a name="id3dx11effectgetgroupbyindex-method"></a><span data-ttu-id="6b1ce-106">ID3DX11Effect:: getgroupbyindex-Methode</span><span class="sxs-lookup"><span data-stu-id="6b1ce-106">ID3DX11Effect::GetGroupByIndex method</span></span>

<span data-ttu-id="6b1ce-107">Ruft eine Effekt Gruppe nach Index ab.</span><span class="sxs-lookup"><span data-stu-id="6b1ce-107">Gets an effect group by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b1ce-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b1ce-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="6b1ce-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b1ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b1ce-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="6b1ce-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="6b1ce-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6b1ce-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6b1ce-112">Der Index der Effekt Gruppe.</span><span class="sxs-lookup"><span data-stu-id="6b1ce-112">Index of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b1ce-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b1ce-113">Return value</span></span>

<span data-ttu-id="6b1ce-114">Typ: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b1ce-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="6b1ce-115">Ein Zeiger auf eine [**ID3DX11EffectGroup**](id3dx11effectgroup.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6b1ce-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b1ce-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b1ce-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6b1ce-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="6b1ce-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6b1ce-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b1ce-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6b1ce-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6b1ce-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6b1ce-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6b1ce-120">Requirements</span></span>



| <span data-ttu-id="6b1ce-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b1ce-121">Requirement</span></span> | <span data-ttu-id="6b1ce-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6b1ce-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b1ce-123">Header</span><span class="sxs-lookup"><span data-stu-id="6b1ce-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6b1ce-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b1ce-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6b1ce-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b1ce-125">Library</span></span><br/> | <dl> <span data-ttu-id="6b1ce-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="6b1ce-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b1ce-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6b1ce-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b1ce-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="6b1ce-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

