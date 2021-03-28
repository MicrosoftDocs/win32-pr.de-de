---
title: ID3DX11EffectType getmembership typebyname-Methode (D3dx11effect. h)
description: Einen Elementtyp nach Name erhalten.
ms.assetid: 0c5a732b-7c3a-41da-b7de-dc464eed814a
keywords:
- Getmembership typebyname-Methode Direct3D 11
- Getmembership typebyname-Methode Direct3D 11, ID3DX11EffectType-Schnittstelle
- ID3DX11EffectType Interface Direct3D 11, getmembership typebyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e573bcdc2dc4470e87539a307cdc38b71a6320ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995853"
---
# <a name="id3dx11effecttypegetmembertypebyname-method"></a><span data-ttu-id="4c9c0-106">ID3DX11EffectType:: getmembership typebyname-Methode</span><span class="sxs-lookup"><span data-stu-id="4c9c0-106">ID3DX11EffectType::GetMemberTypeByName method</span></span>

<span data-ttu-id="4c9c0-107">Einen Elementtyp nach Name erhalten.</span><span class="sxs-lookup"><span data-stu-id="4c9c0-107">Get an member type by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c9c0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c9c0-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="4c9c0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c9c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c9c0-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="4c9c0-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="4c9c0-111">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4c9c0-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4c9c0-112">Der Name eines Members.</span><span class="sxs-lookup"><span data-stu-id="4c9c0-112">A member's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c9c0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c9c0-113">Return value</span></span>

<span data-ttu-id="4c9c0-114">Typ: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c9c0-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="4c9c0-115">Ein Zeiger auf eine [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="4c9c0-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c9c0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c9c0-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c9c0-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="4c9c0-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4c9c0-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4c9c0-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4c9c0-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4c9c0-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c9c0-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4c9c0-120">Requirements</span></span>



| <span data-ttu-id="4c9c0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c9c0-121">Requirement</span></span> | <span data-ttu-id="4c9c0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4c9c0-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c9c0-123">Header</span><span class="sxs-lookup"><span data-stu-id="4c9c0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4c9c0-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c9c0-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4c9c0-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4c9c0-125">Library</span></span><br/> | <dl> <span data-ttu-id="4c9c0-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="4c9c0-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c9c0-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4c9c0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c9c0-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="4c9c0-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

