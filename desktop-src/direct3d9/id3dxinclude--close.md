---
description: Eine vom Benutzer implementierte Methode zum Schließen einer Shader- \# Includedatei.
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'ID3DXInclude:: Close-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b60d01d59a4e54fa0d50c16a3fc845ea4e316792
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355838"
---
# <a name="id3dxincludeclose-method"></a><span data-ttu-id="eb9ba-103">ID3DXInclude:: Close-Methode</span><span class="sxs-lookup"><span data-stu-id="eb9ba-103">ID3DXInclude::Close method</span></span>

<span data-ttu-id="eb9ba-104">Eine vom Benutzer implementierte Methode zum Schließen einer Shader- \# Includedatei.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-104">A user-implemented method for closing a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb9ba-105">Syntax</span></span>


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a><span data-ttu-id="eb9ba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb9ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb9ba-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb9ba-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9ba-108">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb9ba-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb9ba-109">Ein Zeiger auf den zurückgegebenen Puffer, der die include-Direktiven enthält.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-109">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="eb9ba-110">Dies ist der Zeiger, der vom entsprechenden [**ID3DXInclude:: Open**](id3dxinclude--open.md) -Befehl zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-110">This is the pointer that was returned by the corresponding [**ID3DXInclude::Open**](id3dxinclude--open.md) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb9ba-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb9ba-111">Return value</span></span>

<span data-ttu-id="eb9ba-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb9ba-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb9ba-113">Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="eb9ba-114">Wenn beim Lesen der Includedatei der Rückruf fehlschlägt \# , schlägt die API fehl, die den Aufruf des Rückrufs bewirkt hat.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-114">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="eb9ba-115">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="eb9ba-115">This is one of the following:</span></span>

-   <span data-ttu-id="eb9ba-116">Der HLSL-Shader erzeugt eine der D3DXCompileShader- \* \* \* Funktionen nicht.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-116">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="eb9ba-117">Der assemblyshader führt einen der D3DXAssembleShader- \* \* \* Funktionen aus.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-117">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="eb9ba-118">Der Effekt führt nicht zu einer der D3DXCreateEffect- \* \* \* oder D3DXCreateEffectCompiler- \* \* \* Funktionen.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-118">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb9ba-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb9ba-119">Remarks</span></span>

<span data-ttu-id="eb9ba-120">Wenn [**ID3DXInclude:: Open**](id3dxinclude--open.md) erfolgreich war, wird **ID3DXInclude:: Close** garantiert aufgerufen, bevor die API, die diese Schnittstelle verwendet, zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="eb9ba-120">If [**ID3DXInclude::Open**](id3dxinclude--open.md) was successful, **ID3DXInclude::Close** is guaranteed to be called before the API using this interface returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb9ba-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb9ba-121">Requirements</span></span>



| <span data-ttu-id="eb9ba-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb9ba-122">Requirement</span></span> | <span data-ttu-id="eb9ba-123">Wert</span><span class="sxs-lookup"><span data-stu-id="eb9ba-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9ba-124">Header</span><span class="sxs-lookup"><span data-stu-id="eb9ba-124">Header</span></span><br/>  | <dl> <span data-ttu-id="eb9ba-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb9ba-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="eb9ba-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eb9ba-126">Library</span></span><br/> | <dl> <span data-ttu-id="eb9ba-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb9ba-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="eb9ba-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb9ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9ba-129">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="eb9ba-129">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="eb9ba-130">**ID3DXInclude:: Open**</span><span class="sxs-lookup"><span data-stu-id="eb9ba-130">**ID3DXInclude::Open**</span></span>](id3dxinclude--open.md)
</dt> </dl>

 

 
