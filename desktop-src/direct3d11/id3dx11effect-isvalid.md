---
title: ID3DX11Effect IsValid-Methode (D3dx11effect. h)
description: Testen Sie einen Effekt, um festzustellen, ob er eine gültige Syntax enthält. | ID3DX11Effect IsValid-Methode (D3dx11effect. h)
ms.assetid: 42bf0069-1828-4f55-99f5-d0f81eb04336
keywords:
- IsValid-Methode Direct3D 11
- IsValid-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11, IsValid-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88aef9e3864fc77380b3459860178c8537a6a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996093"
---
# <a name="id3dx11effectisvalid-method"></a><span data-ttu-id="70ff0-107">ID3DX11Effect:: IsValid-Methode</span><span class="sxs-lookup"><span data-stu-id="70ff0-107">ID3DX11Effect::IsValid method</span></span>

<span data-ttu-id="70ff0-108">Testen Sie einen Effekt, um festzustellen, ob er eine gültige Syntax enthält.</span><span class="sxs-lookup"><span data-stu-id="70ff0-108">Test an effect to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="70ff0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="70ff0-109">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="70ff0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="70ff0-110">Parameters</span></span>

<span data-ttu-id="70ff0-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="70ff0-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="70ff0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70ff0-112">Return value</span></span>

<span data-ttu-id="70ff0-113">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="70ff0-113">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="70ff0-114">**True** , wenn die Code Syntax gültig ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="70ff0-114">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="70ff0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70ff0-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="70ff0-116">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="70ff0-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="70ff0-117">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="70ff0-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="70ff0-118">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="70ff0-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70ff0-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="70ff0-119">Requirements</span></span>



| <span data-ttu-id="70ff0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70ff0-120">Requirement</span></span> | <span data-ttu-id="70ff0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="70ff0-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70ff0-122">Header</span><span class="sxs-lookup"><span data-stu-id="70ff0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="70ff0-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="70ff0-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="70ff0-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="70ff0-124">Library</span></span><br/> | <dl> <span data-ttu-id="70ff0-125"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="70ff0-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70ff0-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="70ff0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70ff0-127">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="70ff0-127">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

