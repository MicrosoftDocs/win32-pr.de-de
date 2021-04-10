---
description: Beachten Sie, dass Sie die D3DDisassemble-API verwenden, anstatt diese Legacy Funktion zu verwenden. Diese Funktion, die einen kompilierten Effekt in eine Text Zeichenfolge disassembliert, die Assemblyanweisungen und Register Zuweisungen enthält, ist veraltet.
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: D3DX10DisassembleEffect-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 67fe19365616e779bd17ab689550b34737288317
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961674"
---
# <a name="d3dx10disassembleeffect-function"></a><span data-ttu-id="6da56-104">D3DX10DisassembleEffect-Funktion</span><span class="sxs-lookup"><span data-stu-id="6da56-104">D3DX10DisassembleEffect function</span></span>

> [!Note]  
> <span data-ttu-id="6da56-105">Anstatt diese Legacy Funktion zu verwenden, empfiehlt es sich, die [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6da56-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="6da56-106">Diese Funktion, die einen kompilierten Effekt in eine Text Zeichenfolge disassembliert, die Assemblyanweisungen und Register Zuweisungen enthält, ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="6da56-106">This function -- which disassembles a compiled effect into a text string that contains assembly instructions and register assignments -- has been deprecated.</span></span> <span data-ttu-id="6da56-107">Verwenden Sie stattdessen [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span><span class="sxs-lookup"><span data-stu-id="6da56-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="6da56-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6da56-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="6da56-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6da56-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6da56-110">*Peer-ect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6da56-110">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da56-111">Typ: **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span><span class="sxs-lookup"><span data-stu-id="6da56-111">Type: **[**ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span></span>

<span data-ttu-id="6da56-112">Ein Zeiger auf die Effekt Schnittstelle (siehe [**ID3D10Effect-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span><span class="sxs-lookup"><span data-stu-id="6da56-112">A pointer to the effect interface (see [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span></span>

</dd> <dt>

<span data-ttu-id="6da56-113">*Enablecolorcode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6da56-113">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da56-114">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6da56-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6da56-115">Fügen Sie HTML-Tags in die Ausgabe ein, um das Ergebnis farblich zu färben.</span><span class="sxs-lookup"><span data-stu-id="6da56-115">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="6da56-116">*ppdisassembly* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6da56-116">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6da56-117">Typ: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="6da56-117">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="6da56-118">Die Adresse eines Puffers (siehe [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)), die den disassemblierten Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="6da56-118">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6da56-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6da56-119">Return value</span></span>

<span data-ttu-id="6da56-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6da56-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6da56-121">Gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="6da56-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6da56-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6da56-122">Requirements</span></span>



| <span data-ttu-id="6da56-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6da56-123">Requirement</span></span> | <span data-ttu-id="6da56-124">Wert</span><span class="sxs-lookup"><span data-stu-id="6da56-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6da56-125">Header</span><span class="sxs-lookup"><span data-stu-id="6da56-125">Header</span></span><br/> | <dl> <span data-ttu-id="6da56-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6da56-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6da56-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6da56-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da56-128">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="6da56-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
