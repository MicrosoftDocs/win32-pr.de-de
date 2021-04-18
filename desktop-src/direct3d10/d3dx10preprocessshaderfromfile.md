---
description: Beachten Sie, dass Sie die D3DPreprocess-API verwenden, anstatt diese Legacy Funktion zu verwenden. Erstellen Sie einen Shader aus einer Datei, ohne ihn zu kompilieren.
ms.assetid: 9f609aa5-5ee7-45fb-9693-69de130b6cc0
title: D3DX10PreprocessShaderFromFile-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e6222febd378b262d9fb9e87a6224968c2d04038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371930"
---
# <a name="d3dx10preprocessshaderfromfile-function"></a><span data-ttu-id="be8eb-104">D3DX10PreprocessShaderFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="be8eb-104">D3DX10PreprocessShaderFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="be8eb-105">Anstatt diese Legacy Funktion zu verwenden, empfiehlt es sich, die [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="be8eb-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="be8eb-106">Erstellen Sie einen Shader aus einer Datei, ohne ihn zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="be8eb-106">Create a shader from a file without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="be8eb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="be8eb-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="be8eb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="be8eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be8eb-109">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be8eb-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be8eb-110">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be8eb-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be8eb-111">Der Name der Shader-Datei.</span><span class="sxs-lookup"><span data-stu-id="be8eb-111">Name of the shader file.</span></span>

</dd> <dt>

<span data-ttu-id="be8eb-112">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be8eb-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be8eb-113">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="be8eb-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="be8eb-114">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="be8eb-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="be8eb-115">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be8eb-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be8eb-116">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="be8eb-116">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="be8eb-117">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Legen Sie dies auf **null** fest, um anzugeben, dass keine Includedatei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="be8eb-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="be8eb-118">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be8eb-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be8eb-119">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="be8eb-119">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="be8eb-120">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="be8eb-120">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="be8eb-121">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="be8eb-121">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="be8eb-122">*ppshadertext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="be8eb-122">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be8eb-123">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="be8eb-123">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="be8eb-124">Ein Zeiger auf den Arbeitsspeicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), der den nicht kompilierten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="be8eb-124">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="be8eb-125">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="be8eb-125">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be8eb-126">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="be8eb-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="be8eb-127">Die Adresse eines Zeigers auf den Speicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), der Fehler bei der Fehler Erstellung enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="be8eb-127">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be8eb-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be8eb-128">Return value</span></span>

<span data-ttu-id="be8eb-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be8eb-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be8eb-130">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="be8eb-130">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be8eb-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be8eb-131">Requirements</span></span>



| <span data-ttu-id="be8eb-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be8eb-132">Requirement</span></span> | <span data-ttu-id="be8eb-133">Wert</span><span class="sxs-lookup"><span data-stu-id="be8eb-133">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="be8eb-134">Header</span><span class="sxs-lookup"><span data-stu-id="be8eb-134">Header</span></span><br/> | <dl> <span data-ttu-id="be8eb-135"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="be8eb-135"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be8eb-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be8eb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be8eb-137">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="be8eb-137">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
