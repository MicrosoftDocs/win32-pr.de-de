---
title: ID3DX11EffectVariable-Methode für das-Methode (D3dx11effect. h)
description: Legen Sie Daten fest.
ms.assetid: c5d53aa6-6cd8-4a93-9851-2a93bc6a728a
keywords:
- -Methode von "strawvalue" Direct3D 11
- Methode "-Methode" Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable Interface Direct3D 11, Methode "-Methode"
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.SetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5186e55b8b1d3472cb25ea6fa067988d4fb1f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219444"
---
# <a name="id3dx11effectvariablesetrawvalue-method"></a><span data-ttu-id="f31dc-106">ID3DX11EffectVariable:: strawvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="f31dc-106">ID3DX11EffectVariable::SetRawValue method</span></span>

<span data-ttu-id="f31dc-107">Legen Sie Daten fest.</span><span class="sxs-lookup"><span data-stu-id="f31dc-107">Set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f31dc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f31dc-108">Syntax</span></span>


```C++
HRESULT SetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="f31dc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f31dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f31dc-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="f31dc-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="f31dc-111">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="f31dc-111">Type: **void\***</span></span>

<span data-ttu-id="f31dc-112">Ein Zeiger auf die Variable.</span><span class="sxs-lookup"><span data-stu-id="f31dc-112">A pointer to the variable.</span></span>

</dd> <dt>

<span data-ttu-id="f31dc-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="f31dc-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="f31dc-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f31dc-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f31dc-115">Der Offset (in Bytes) vom Anfang des Zeigers auf die Daten.</span><span class="sxs-lookup"><span data-stu-id="f31dc-115">The offset (in bytes) from the beginning of the pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="f31dc-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="f31dc-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="f31dc-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f31dc-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f31dc-118">Die Anzahl der festzulegenden bytes.</span><span class="sxs-lookup"><span data-stu-id="f31dc-118">The number of bytes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f31dc-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f31dc-119">Return value</span></span>

<span data-ttu-id="f31dc-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f31dc-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f31dc-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="f31dc-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f31dc-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f31dc-122">Remarks</span></span>

<span data-ttu-id="f31dc-123">Diese Methode führt keine Konvertierung oder Typüberprüfung durch. Es ist daher eine sehr schnelle Möglichkeit für den Zugriff auf Array Elemente.</span><span class="sxs-lookup"><span data-stu-id="f31dc-123">This method does no conversion or type checking; it is therefore a very quick way to access array items.</span></span>

> [!Note]  
> <span data-ttu-id="f31dc-124">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="f31dc-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f31dc-125">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f31dc-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f31dc-126">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f31dc-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f31dc-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f31dc-127">Requirements</span></span>



| <span data-ttu-id="f31dc-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f31dc-128">Requirement</span></span> | <span data-ttu-id="f31dc-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f31dc-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f31dc-130">Header</span><span class="sxs-lookup"><span data-stu-id="f31dc-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f31dc-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f31dc-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f31dc-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f31dc-132">Library</span></span><br/> | <dl> <span data-ttu-id="f31dc-133"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="f31dc-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f31dc-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f31dc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31dc-135">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="f31dc-135">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

