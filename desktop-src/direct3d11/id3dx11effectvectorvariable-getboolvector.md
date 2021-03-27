---
title: ID3DX11EffectVectorVariable getboolvector-Methode (D3dx11effect. h)
description: Einen Vektor mit vier Komponenten, der boolesche Daten enthält, erhalten.
ms.assetid: ecaf5705-d13b-4d61-9766-d2ff183af789
keywords:
- Getboolvector-Methode Direct3D 11
- Getboolvector-Methode Direct3D 11, ID3DX11EffectVectorVariable-Schnittstelle
- ID3DX11EffectVectorVariable-Schnittstelle Direct3D 11, getboolvector-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetBoolVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a24563bd7c685579115e3b10309fb0a1c158c2e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982402"
---
# <a name="id3dx11effectvectorvariablegetboolvector-method"></a><span data-ttu-id="52f98-106">ID3DX11EffectVectorVariable:: getboolvector-Methode</span><span class="sxs-lookup"><span data-stu-id="52f98-106">ID3DX11EffectVectorVariable::GetBoolVector method</span></span>

<span data-ttu-id="52f98-107">Einen Vektor mit vier Komponenten, der boolesche Daten enthält, erhalten.</span><span class="sxs-lookup"><span data-stu-id="52f98-107">Get a four-component vector that contains boolean data.</span></span>

## <a name="syntax"></a><span data-ttu-id="52f98-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="52f98-108">Syntax</span></span>


```C++
HRESULT GetBoolVector(
   BOOL *pData
);
```



## <a name="parameters"></a><span data-ttu-id="52f98-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="52f98-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52f98-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="52f98-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="52f98-111">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="52f98-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="52f98-112">Ein Zeiger auf die erste Komponente.</span><span class="sxs-lookup"><span data-stu-id="52f98-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52f98-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52f98-113">Return value</span></span>

<span data-ttu-id="52f98-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52f98-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52f98-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="52f98-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="52f98-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52f98-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="52f98-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="52f98-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="52f98-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="52f98-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="52f98-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="52f98-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52f98-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="52f98-120">Requirements</span></span>



| <span data-ttu-id="52f98-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52f98-121">Requirement</span></span> | <span data-ttu-id="52f98-122">Wert</span><span class="sxs-lookup"><span data-stu-id="52f98-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52f98-123">Header</span><span class="sxs-lookup"><span data-stu-id="52f98-123">Header</span></span><br/>  | <dl> <span data-ttu-id="52f98-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="52f98-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="52f98-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="52f98-125">Library</span></span><br/> | <dl> <span data-ttu-id="52f98-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="52f98-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52f98-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="52f98-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f98-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="52f98-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

