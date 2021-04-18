---
description: Beachten Sie, dass Sie die D3DDisassemble-API verwenden, anstatt diese Legacy Funktion zu verwenden. Diese Funktion, die einen kompilierten Shader in eine Text Zeichenfolge disassembliert, die Assemblyanweisungen und Register Zuweisungen enthält, ist nicht mehr vorhanden.
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: D3DX10DisassembleShader-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 13716fd5d25e2e8602379ea3864c516fa5388475
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354979"
---
# <a name="d3dx10disassembleshader-function"></a><span data-ttu-id="e7171-104">D3DX10DisassembleShader-Funktion</span><span class="sxs-lookup"><span data-stu-id="e7171-104">D3DX10DisassembleShader function</span></span>

> [!Note]  
> <span data-ttu-id="e7171-105">Anstatt diese Legacy Funktion zu verwenden, empfiehlt es sich, die [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7171-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="e7171-106">Diese Funktion, die einen kompilierten Shader in eine Text Zeichenfolge disassembliert, die Assemblyanweisungen und Register Zuweisungen enthält, ist nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e7171-106">This function -- which disassembles a compiled shader into a text string that contains assembly instructions and register assignments -- no longer exists.</span></span> <span data-ttu-id="e7171-107">Verwenden Sie stattdessen [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span><span class="sxs-lookup"><span data-stu-id="e7171-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7171-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7171-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="e7171-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7171-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7171-110">*pshader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7171-110">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7171-111">Typ: Konstante **void \***</span><span class="sxs-lookup"><span data-stu-id="e7171-111">Type: **const void\***</span></span>

<span data-ttu-id="e7171-112">Ein Zeiger auf den [**kompilierten Shader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="e7171-112">A pointer to the [**compiled shader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="e7171-113">*Bytecodelta ength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7171-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7171-114">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7171-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7171-115">Die Größe des pshader.</span><span class="sxs-lookup"><span data-stu-id="e7171-115">The size of pShader.</span></span>

</dd> <dt>

<span data-ttu-id="e7171-116">*Enablecolorcode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7171-116">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7171-117">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7171-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7171-118">Fügen Sie HTML-Tags in die Ausgabe ein, um das Ergebnis farblich zu färben.</span><span class="sxs-lookup"><span data-stu-id="e7171-118">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="e7171-119">*pcomments* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7171-119">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7171-120">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7171-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7171-121">Die Kommentar Zeichenfolge am Anfang des Shader, die die shaderkonstanten und Variablen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e7171-121">The comment string at the top of the shader that identifies the shader constants and variables.</span></span>

</dd> <dt>

<span data-ttu-id="e7171-122">*ppdisassembly* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e7171-122">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7171-123">Typ: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="e7171-123">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="e7171-124">Adresse eines Puffers (siehe [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)), der den disassemblierten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="e7171-124">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7171-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7171-125">Return value</span></span>

<span data-ttu-id="e7171-126">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7171-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7171-127">Gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="e7171-127">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7171-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7171-128">Remarks</span></span>

<span data-ttu-id="e7171-129">Dieser zurückgegebene Text enthält einen Header mit der Version des HLSL-Compilers, der zum Generieren dieses Objekts verwendet wurde, Kommentare, die das Speicher Layout der vom Shader verwendeten Konstanten Puffer, Eingabe-und Ausgabe Signaturen und Ressourcen Bindungs Punkte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e7171-129">This returned text includes a header with the version of the HLSL compiler used to generate this object, comments describing the memory layout of the constant buffers used by the shader, input and output signatures, and resource binding points.</span></span>

<span data-ttu-id="e7171-130">Im folgenden finden Sie ein Beispiel für die Disassemblierung eines kompilierten Shaders.</span><span class="sxs-lookup"><span data-stu-id="e7171-130">Here is an example of disassembling a compiled shader.</span></span> <span data-ttu-id="e7171-131">Im Beispiel wird davon ausgegangen, dass Sie mit einem kompilierten Shader beginnen (als *pvsbuf* angezeigt, den Sie in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)sehen können).</span><span class="sxs-lookup"><span data-stu-id="e7171-131">The example assumes you start with a compiled shader (shown as *pVSBuf* which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


```
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleShader( (UINT*) pVSBuf->GetBufferPointer(), 
        pVSBuf->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "shader.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="e7171-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7171-132">Requirements</span></span>



| <span data-ttu-id="e7171-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7171-133">Requirement</span></span> | <span data-ttu-id="e7171-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e7171-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7171-135">Header</span><span class="sxs-lookup"><span data-stu-id="e7171-135">Header</span></span><br/> | <dl> <span data-ttu-id="e7171-136"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7171-136"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7171-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7171-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7171-138">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="e7171-138">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
