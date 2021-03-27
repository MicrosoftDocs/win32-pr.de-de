---
title: ID3DX11EffectVectorVariable-Methode für das-Objekt (D3dx11effect. h)
description: Legen Sie einen Vektor mit vier Komponenten fest, der ganzzahlige Daten enthält.
ms.assetid: d0546da4-c3b4-4e97-9aa9-d3b7022e22c5
keywords:
- Methode "Direct3D 11"
- Methode "Direct3D 11", ID3DX11EffectVectorVariable-Schnittstelle
- ID3DX11EffectVectorVariable-Schnittstelle Direct3D 11, Methode "-Methode"
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetIntVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea6141185459dbe7aad494312210b4517fe4f4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219527"
---
# <a name="id3dx11effectvectorvariablesetintvector-method"></a><span data-ttu-id="0ba47-106">ID3DX11EffectVectorVariable:: abtintvector-Methode</span><span class="sxs-lookup"><span data-stu-id="0ba47-106">ID3DX11EffectVectorVariable::SetIntVector method</span></span>

<span data-ttu-id="0ba47-107">Legen Sie einen Vektor mit vier Komponenten fest, der ganzzahlige Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="0ba47-107">Set a four-component vector that contains integer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba47-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ba47-108">Syntax</span></span>


```C++
HRESULT SetIntVector(
   int *pData
);
```



## <a name="parameters"></a><span data-ttu-id="0ba47-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ba47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ba47-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="0ba47-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="0ba47-111">Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="0ba47-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="0ba47-112">Ein Zeiger auf die erste Komponente.</span><span class="sxs-lookup"><span data-stu-id="0ba47-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ba47-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ba47-113">Return value</span></span>

<span data-ttu-id="0ba47-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ba47-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ba47-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="0ba47-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ba47-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ba47-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0ba47-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="0ba47-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0ba47-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ba47-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0ba47-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0ba47-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0ba47-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0ba47-120">Requirements</span></span>



| <span data-ttu-id="0ba47-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ba47-121">Requirement</span></span> | <span data-ttu-id="0ba47-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0ba47-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba47-123">Header</span><span class="sxs-lookup"><span data-stu-id="0ba47-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0ba47-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ba47-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0ba47-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ba47-125">Library</span></span><br/> | <dl> <span data-ttu-id="0ba47-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba47-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ba47-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0ba47-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba47-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="0ba47-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

