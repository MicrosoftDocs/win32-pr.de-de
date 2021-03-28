---
title: ID3DX11EffectVectorVariable getintvector-Methode (D3dx11effect. h)
description: Sie erhalten einen Vektor mit vier Komponenten, der ganzzahlige Daten enthält.
ms.assetid: 27c75cfb-7c6f-43f4-9489-186006a60203
keywords:
- Getintvector-Methode Direct3D 11
- Getintvector-Methode Direct3D 11, ID3DX11EffectVectorVariable-Schnittstelle
- ID3DX11EffectVectorVariable-Schnittstelle Direct3D 11, getintvector-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetIntVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e661ecce642cae4cf94a1bc35f92dc1afad16a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531010"
---
# <a name="id3dx11effectvectorvariablegetintvector-method"></a><span data-ttu-id="f2703-106">ID3DX11EffectVectorVariable:: getintvector-Methode</span><span class="sxs-lookup"><span data-stu-id="f2703-106">ID3DX11EffectVectorVariable::GetIntVector method</span></span>

<span data-ttu-id="f2703-107">Sie erhalten einen Vektor mit vier Komponenten, der ganzzahlige Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="f2703-107">Get a four-component vector that contains integer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2703-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2703-108">Syntax</span></span>


```C++
HRESULT GetIntVector(
   int *pData
);
```



## <a name="parameters"></a><span data-ttu-id="f2703-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2703-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2703-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="f2703-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="f2703-111">Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="f2703-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="f2703-112">Ein Zeiger auf die erste Komponente.</span><span class="sxs-lookup"><span data-stu-id="f2703-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2703-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2703-113">Return value</span></span>

<span data-ttu-id="f2703-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2703-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2703-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="f2703-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2703-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2703-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f2703-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="f2703-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f2703-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f2703-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f2703-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f2703-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f2703-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f2703-120">Requirements</span></span>



| <span data-ttu-id="f2703-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2703-121">Requirement</span></span> | <span data-ttu-id="f2703-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f2703-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2703-123">Header</span><span class="sxs-lookup"><span data-stu-id="f2703-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f2703-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2703-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f2703-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2703-125">Library</span></span><br/> | <dl> <span data-ttu-id="f2703-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="f2703-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2703-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f2703-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2703-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="f2703-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

