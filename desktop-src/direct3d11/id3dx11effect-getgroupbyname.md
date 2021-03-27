---
title: ID3DX11Effect getgroupbyname-Methode (D3dx11effect. h)
description: Ruft eine Effekt Gruppe nach dem Namen ab.
ms.assetid: 14b4b484-848a-409c-9a99-207ab25b7566
keywords:
- Getgroupbyname-Methode Direct3D 11
- Getgroupbyname-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, getgroupbyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1c2132dedb34fe71db30bf82b1c6d336f110a8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996115"
---
# <a name="id3dx11effectgetgroupbyname-method"></a><span data-ttu-id="3c69a-106">ID3DX11Effect:: getgroupbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="3c69a-106">ID3DX11Effect::GetGroupByName method</span></span>

<span data-ttu-id="3c69a-107">Ruft eine Effekt Gruppe nach dem Namen ab.</span><span class="sxs-lookup"><span data-stu-id="3c69a-107">Gets an effect group by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c69a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c69a-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="3c69a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c69a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c69a-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="3c69a-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="3c69a-111">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c69a-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c69a-112">Der Name der Effekt Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3c69a-112">Name of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c69a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c69a-113">Return value</span></span>

<span data-ttu-id="3c69a-114">Typ: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c69a-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="3c69a-115">Ein Zeiger auf eine [**ID3DX11EffectGroup**](id3dx11effectgroup.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3c69a-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c69a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c69a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3c69a-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="3c69a-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3c69a-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3c69a-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3c69a-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3c69a-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c69a-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3c69a-120">Requirements</span></span>



| <span data-ttu-id="3c69a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c69a-121">Requirement</span></span> | <span data-ttu-id="3c69a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3c69a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c69a-123">Header</span><span class="sxs-lookup"><span data-stu-id="3c69a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3c69a-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c69a-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3c69a-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3c69a-125">Library</span></span><br/> | <dl> <span data-ttu-id="3c69a-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="3c69a-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c69a-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3c69a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c69a-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="3c69a-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

