---
title: ID3DX11EffectVariable getannotationbyindex-Methode (D3dx11effect. h)
description: Eine Anmerkung nach Index erhalten. | ID3DX11EffectVariable getannotationbyindex-Methode (D3dx11effect. h)
ms.assetid: fc130098-0269-4c78-bc45-284aa0b77865
keywords:
- Getannotationbyindex-Methode Direct3D 11
- Getannotationbyindex-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable Interface Direct3D 11, getannotationbyindex-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e13cfcb27e94c64af132e5eec600941d0b41cd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132293"
---
# <a name="id3dx11effectvariablegetannotationbyindex-method"></a><span data-ttu-id="93af2-107">ID3DX11EffectVariable:: getannotationbyindex-Methode</span><span class="sxs-lookup"><span data-stu-id="93af2-107">ID3DX11EffectVariable::GetAnnotationByIndex method</span></span>

<span data-ttu-id="93af2-108">Eine Anmerkung nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="93af2-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="93af2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="93af2-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="93af2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="93af2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93af2-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="93af2-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="93af2-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="93af2-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="93af2-113">Ein NULL basierter Index.</span><span class="sxs-lookup"><span data-stu-id="93af2-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93af2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93af2-114">Return value</span></span>

<span data-ttu-id="93af2-115">Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="93af2-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="93af2-116">Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="93af2-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="93af2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93af2-117">Remarks</span></span>

<span data-ttu-id="93af2-118">Anmerkungen können an eine Technik, einen Durchlauf oder eine globale Variable angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="93af2-118">Annonations can be attached to a technique, a pass, or a global variable.</span></span>

> [!Note]  
> <span data-ttu-id="93af2-119">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="93af2-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="93af2-120">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="93af2-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="93af2-121">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="93af2-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="93af2-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="93af2-122">Requirements</span></span>



| <span data-ttu-id="93af2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93af2-123">Requirement</span></span> | <span data-ttu-id="93af2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="93af2-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93af2-125">Header</span><span class="sxs-lookup"><span data-stu-id="93af2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="93af2-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="93af2-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="93af2-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="93af2-127">Library</span></span><br/> | <dl> <span data-ttu-id="93af2-128"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="93af2-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93af2-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="93af2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93af2-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="93af2-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

