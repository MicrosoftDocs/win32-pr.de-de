---
title: ID3DX11EffectPass IsValid-Methode (D3dx11effect. h)
description: Testen Sie einen Durchlauf, um festzustellen, ob er eine gültige Syntax enthält.
ms.assetid: 3c6ddcef-1303-4161-889c-c3ca271b6ad0
keywords:
- IsValid-Methode Direct3D 11
- IsValid-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11, IsValid-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50db900d3cea82197fb56ce3a57a5a548220ca1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982245"
---
# <a name="id3dx11effectpassisvalid-method"></a><span data-ttu-id="3aadc-106">ID3DX11EffectPass:: IsValid-Methode</span><span class="sxs-lookup"><span data-stu-id="3aadc-106">ID3DX11EffectPass::IsValid method</span></span>

<span data-ttu-id="3aadc-107">Testen Sie einen Durchlauf, um festzustellen, ob er eine gültige Syntax enthält.</span><span class="sxs-lookup"><span data-stu-id="3aadc-107">Test a pass to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aadc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3aadc-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="3aadc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3aadc-109">Parameters</span></span>

<span data-ttu-id="3aadc-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3aadc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3aadc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3aadc-111">Return value</span></span>

<span data-ttu-id="3aadc-112">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3aadc-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3aadc-113">**True** , wenn die Code Syntax gültig ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="3aadc-113">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aadc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3aadc-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3aadc-115">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="3aadc-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3aadc-116">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3aadc-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3aadc-117">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3aadc-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3aadc-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3aadc-118">Requirements</span></span>



| <span data-ttu-id="3aadc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3aadc-119">Requirement</span></span> | <span data-ttu-id="3aadc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3aadc-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aadc-121">Header</span><span class="sxs-lookup"><span data-stu-id="3aadc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3aadc-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3aadc-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3aadc-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3aadc-123">Library</span></span><br/> | <dl> <span data-ttu-id="3aadc-124"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="3aadc-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aadc-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3aadc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aadc-126">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="3aadc-126">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

