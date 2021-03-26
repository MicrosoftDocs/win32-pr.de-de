---
title: ID3DX11EffectStringVariable GetString-Methode (D3dx11effect. h)
description: Die Zeichenfolge zu erhalten.
ms.assetid: ce96ae18-d316-41ba-9b2a-eac084b86098
keywords:
- GetString-Methode Direct3D 11
- GetString-Methode Direct3D 11, ID3DX11EffectStringVariable-Schnittstelle
- ID3DX11EffectStringVariable-Schnittstelle Direct3D 11, GetString-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d15666bd70bf00395b7052b7820981dd8d0dcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982143"
---
# <a name="id3dx11effectstringvariablegetstring-method"></a><span data-ttu-id="3152c-106">ID3DX11EffectStringVariable:: GetString-Methode</span><span class="sxs-lookup"><span data-stu-id="3152c-106">ID3DX11EffectStringVariable::GetString method</span></span>

<span data-ttu-id="3152c-107">Die Zeichenfolge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3152c-107">Get the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3152c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3152c-108">Syntax</span></span>


```C++
HRESULT GetString(
   LPCSTR *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="3152c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3152c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3152c-110">*ppString*</span><span class="sxs-lookup"><span data-stu-id="3152c-110">*ppString*</span></span> 
</dt> <dd>

<span data-ttu-id="3152c-111">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="3152c-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="3152c-112">Ein Zeiger auf die Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3152c-112">A pointer to the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3152c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3152c-113">Return value</span></span>

<span data-ttu-id="3152c-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3152c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3152c-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="3152c-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3152c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3152c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3152c-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="3152c-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3152c-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3152c-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3152c-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3152c-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3152c-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3152c-120">Requirements</span></span>



| <span data-ttu-id="3152c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3152c-121">Requirement</span></span> | <span data-ttu-id="3152c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3152c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3152c-123">Header</span><span class="sxs-lookup"><span data-stu-id="3152c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3152c-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3152c-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3152c-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3152c-125">Library</span></span><br/> | <dl> <span data-ttu-id="3152c-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="3152c-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3152c-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3152c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3152c-128">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="3152c-128">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

