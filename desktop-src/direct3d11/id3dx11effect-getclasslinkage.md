---
title: ID3DX11Effect getclasslink-Methode (D3dx11effect. h)
description: Ruft eine Schnittstelle für die Klassen Verknüpfung ab.
ms.assetid: 006c900d-3464-4666-9fe9-d62ba8cb2b7f
keywords:
- Getclasslink-Methode Direct3D 11
- Getclasslink-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, getclasslink-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetClassLinkage
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b19f14794186f85d0a51f21bc6b2759e512998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961571"
---
# <a name="id3dx11effectgetclasslinkage-method"></a><span data-ttu-id="2e7ab-106">ID3DX11Effect:: getclasslink-Methode</span><span class="sxs-lookup"><span data-stu-id="2e7ab-106">ID3DX11Effect::GetClassLinkage method</span></span>

<span data-ttu-id="2e7ab-107">Ruft eine Schnittstelle für die Klassen Verknüpfung ab.</span><span class="sxs-lookup"><span data-stu-id="2e7ab-107">Gets a class linkage interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e7ab-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e7ab-108">Syntax</span></span>


```C++
ID3D11ClassLinkage* GetClassLinkage();
```



## <a name="parameters"></a><span data-ttu-id="2e7ab-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e7ab-109">Parameters</span></span>

<span data-ttu-id="2e7ab-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2e7ab-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e7ab-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e7ab-111">Return value</span></span>

<span data-ttu-id="2e7ab-112">Typ: **[ **ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***</span><span class="sxs-lookup"><span data-stu-id="2e7ab-112">Type: **[**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***</span></span>

<span data-ttu-id="2e7ab-113">Gibt einen Zeiger auf eine [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="2e7ab-113">Returns a pointer to an [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e7ab-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e7ab-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2e7ab-115">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="2e7ab-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2e7ab-116">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2e7ab-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2e7ab-117">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2e7ab-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e7ab-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2e7ab-118">Requirements</span></span>



| <span data-ttu-id="2e7ab-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e7ab-119">Requirement</span></span> | <span data-ttu-id="2e7ab-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2e7ab-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e7ab-121">Header</span><span class="sxs-lookup"><span data-stu-id="2e7ab-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2e7ab-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e7ab-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2e7ab-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e7ab-123">Library</span></span><br/> | <dl> <span data-ttu-id="2e7ab-124"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="2e7ab-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e7ab-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2e7ab-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e7ab-126">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="2e7ab-126">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





