---
title: ID3DX11EffectPass Apply-Methode (D3dx11effect. h)
description: Legen Sie den in einem Pass enthaltenen Status auf das Gerät fest.
ms.assetid: d67fe968-bfb2-4f3a-b393-3f72f680211f
keywords:
- Apply-Methode Direct3D 11
- Apply-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11, Apply-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.Apply
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a061609953e164524e16722222a5ecea81f275b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982251"
---
# <a name="id3dx11effectpassapply-method"></a><span data-ttu-id="0a11a-106">ID3DX11EffectPass:: Apply-Methode</span><span class="sxs-lookup"><span data-stu-id="0a11a-106">ID3DX11EffectPass::Apply method</span></span>

<span data-ttu-id="0a11a-107">Legen Sie den in einem Pass enthaltenen Status auf das Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="0a11a-107">Set the state contained in a pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a11a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a11a-108">Syntax</span></span>


```C++
HRESULT Apply(
   UINT                Flags,
   ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="0a11a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a11a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a11a-110">*Flags*</span><span class="sxs-lookup"><span data-stu-id="0a11a-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="0a11a-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0a11a-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0a11a-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a11a-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="0a11a-113">*pContext*</span><span class="sxs-lookup"><span data-stu-id="0a11a-113">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="0a11a-114">Typ: **[ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="0a11a-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="0a11a-115">Der [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) , auf den die Übergabe angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a11a-115">The [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) to apply the pass to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a11a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a11a-116">Return value</span></span>

<span data-ttu-id="0a11a-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a11a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a11a-118">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="0a11a-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a11a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a11a-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0a11a-120">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="0a11a-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0a11a-121">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a11a-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0a11a-122">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0a11a-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a11a-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0a11a-123">Requirements</span></span>



| <span data-ttu-id="0a11a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a11a-124">Requirement</span></span> | <span data-ttu-id="0a11a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0a11a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a11a-126">Header</span><span class="sxs-lookup"><span data-stu-id="0a11a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0a11a-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a11a-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0a11a-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0a11a-128">Library</span></span><br/> | <dl> <span data-ttu-id="0a11a-129"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="0a11a-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a11a-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0a11a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a11a-131">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="0a11a-131">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

