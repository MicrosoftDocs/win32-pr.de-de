---
title: ID3DX11Effect cloneeffect-Methode (D3dx11effect. h)
description: Erstellt eine Kopie einer Effect-Schnittstelle.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- Cloneeffect-Methode Direct3D 11
- Cloneeffect-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, cloneeffect-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dc7e47d1c50d0e41c29c90102afaaebdce8dda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982604"
---
# <a name="id3dx11effectcloneeffect-method"></a><span data-ttu-id="1d5ae-106">ID3DX11Effect:: cloneeffect-Methode</span><span class="sxs-lookup"><span data-stu-id="1d5ae-106">ID3DX11Effect::CloneEffect method</span></span>

<span data-ttu-id="1d5ae-107">Erstellt eine Kopie einer Effect-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-107">Creates a copy of an effect interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d5ae-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d5ae-108">Syntax</span></span>


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a><span data-ttu-id="1d5ae-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d5ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d5ae-110">*Flags*</span><span class="sxs-lookup"><span data-stu-id="1d5ae-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="1d5ae-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1d5ae-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1d5ae-112">Flags, die sich auf die Erstellung des geklonten Effekts auswirken.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-112">Flags affecting the creation of the cloned effect.</span></span> <span data-ttu-id="1d5ae-113">Kann 0 oder einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-113">Can be 0 or one of the following values.</span></span>



| <span data-ttu-id="1d5ae-114">Flag</span><span class="sxs-lookup"><span data-stu-id="1d5ae-114">Flag</span></span>                                    | <span data-ttu-id="1d5ae-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d5ae-115">Description</span></span>                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5ae-116">Bibliothek d3dx11 \_ Effect \_ Klon \_ Force \_ nonsingle</span><span class="sxs-lookup"><span data-stu-id="1d5ae-116">D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE</span></span> | <span data-ttu-id="1d5ae-117">Ignorieren Sie alle "einzelnen" Qualifizierer für cbuffers.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-117">Ignore all "single" qualifiers on cbuffers.</span></span> <span data-ttu-id="1d5ae-118">Alle cBuffer verfügen über eigene [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s, die im geklonten Effekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-118">All cbuffers will have their own [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)s created in the cloned effect.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1d5ae-119">*ppclonedebug*</span><span class="sxs-lookup"><span data-stu-id="1d5ae-119">*ppClonedEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="1d5ae-120">Typ: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1d5ae-120">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="1d5ae-121">Zeiger auf einen [**ID3DX11Effect**](id3dx11effect.md) -Zeiger, der auf die Kopie des Effekts festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-121">Pointer to an [**ID3DX11Effect**](id3dx11effect.md) pointer that will be set to the copy of the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d5ae-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d5ae-122">Return value</span></span>

<span data-ttu-id="1d5ae-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d5ae-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d5ae-124">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-124">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1d5ae-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d5ae-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1d5ae-126">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-126">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1d5ae-127">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d5ae-127">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1d5ae-128">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1d5ae-128">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d5ae-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1d5ae-129">Requirements</span></span>



| <span data-ttu-id="1d5ae-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d5ae-130">Requirement</span></span> | <span data-ttu-id="1d5ae-131">Wert</span><span class="sxs-lookup"><span data-stu-id="1d5ae-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d5ae-132">Header</span><span class="sxs-lookup"><span data-stu-id="1d5ae-132">Header</span></span><br/>  | <dl> <span data-ttu-id="1d5ae-133"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d5ae-133"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1d5ae-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1d5ae-134">Library</span></span><br/> | <dl> <span data-ttu-id="1d5ae-135"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="1d5ae-135"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d5ae-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1d5ae-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d5ae-137">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="1d5ae-137">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

