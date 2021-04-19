---
description: ID3DXInclude ist eine vom Benutzer implementierte Schnittstelle, um Rückrufe für \# Includedirektiven während der shaderkompilierung bereitzustellen.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: ID3DXInclude-Schnittstelle (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369331"
---
# <a name="id3dxinclude-interface"></a><span data-ttu-id="40fc4-103">ID3DXInclude-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="40fc4-103">ID3DXInclude interface</span></span>

<span data-ttu-id="40fc4-104">ID3DXInclude ist eine vom Benutzer implementierte Schnittstelle, um Rückrufe für \# Includedirektiven während der shaderkompilierung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="40fc4-104">ID3DXInclude is a user-implemented interface to provide callbacks for \#include directives during shader compilation.</span></span> <span data-ttu-id="40fc4-105">Jede der Methoden in dieser Schnittstelle muss vom Benutzer implementiert werden, der dann als Rückrufe für die Anwendung verwendet wird, wenn einer der folgenden Punkte zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40fc4-105">Each of the methods in this interface must be implemented by the user which will then be used as callbacks to the application when one of the following occurs:</span></span>

-   <span data-ttu-id="40fc4-106">Ein HLSL-Shader, der eine include-Datei enthält, \# wird durch Aufrufen einer der D3DXCompileShader- \* \* \* Funktionen kompiliert.</span><span class="sxs-lookup"><span data-stu-id="40fc4-106">An HLSL shader that contains a \#include is compiled by calling one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="40fc4-107">Ein assemblyshader \# wird durch Aufrufen einer der D3DXAssembleShader-Funktionen zusammengestellt \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="40fc4-107">An assembly shader \#include is assembled by calling any of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="40fc4-108">Ein Effekt, der einen Include-Wert enthält, \# wird durch den Aufruf einer der D3DXCreateEffect- \* \* \* oder D3DXCreateEffectCompiler- \* \* \* Funktionen kompiliert.</span><span class="sxs-lookup"><span data-stu-id="40fc4-108">An effect that contains a \#include is compiled by by calling any of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="members"></a><span data-ttu-id="40fc4-109">Member</span><span class="sxs-lookup"><span data-stu-id="40fc4-109">Members</span></span>

<span data-ttu-id="40fc4-110">Die **ID3DXInclude** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="40fc4-110">The **ID3DXInclude** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="40fc4-111">**ID3DXInclude** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="40fc4-111">**ID3DXInclude** also has these types of members:</span></span>

-   [<span data-ttu-id="40fc4-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="40fc4-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="40fc4-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="40fc4-113">Methods</span></span>

<span data-ttu-id="40fc4-114">Die **ID3DXInclude** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="40fc4-114">The **ID3DXInclude** interface has these methods.</span></span>



| <span data-ttu-id="40fc4-115">Methode</span><span class="sxs-lookup"><span data-stu-id="40fc4-115">Method</span></span>                               | <span data-ttu-id="40fc4-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40fc4-116">Description</span></span>                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40fc4-117">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="40fc4-117">**Close**</span></span>](id3dxinclude--close.md) | <span data-ttu-id="40fc4-118">Eine vom Benutzer implementierte Methode zum Schließen einer Shader- \# Includedatei.</span><span class="sxs-lookup"><span data-stu-id="40fc4-118">A user-implemented method for closing a shader \#include file.</span></span><br/>                             |
| [<span data-ttu-id="40fc4-119">**Eren**</span><span class="sxs-lookup"><span data-stu-id="40fc4-119">**Open**</span></span>](id3dxinclude--open.md)   | <span data-ttu-id="40fc4-120">Eine vom Benutzer implementierte Methode zum Öffnen und Lesen des Inhalts einer-Shader- \# Includedatei.</span><span class="sxs-lookup"><span data-stu-id="40fc4-120">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="40fc4-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40fc4-121">Remarks</span></span>

<span data-ttu-id="40fc4-122">Ein Benutzer erstellt eine ID3DXInclude-Schnittstelle, indem er eine Klasse implementiert, die von dieser Schnittstelle abgeleitet wird, und alle Schnittstellen Methoden implementiert.</span><span class="sxs-lookup"><span data-stu-id="40fc4-122">A user creates an ID3DXInclude interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span>

<span data-ttu-id="40fc4-123">Der LPD3DXINCLUDE-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="40fc4-123">The LPD3DXINCLUDE type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a><span data-ttu-id="40fc4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40fc4-124">Requirements</span></span>



| <span data-ttu-id="40fc4-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40fc4-125">Requirement</span></span> | <span data-ttu-id="40fc4-126">Wert</span><span class="sxs-lookup"><span data-stu-id="40fc4-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="40fc4-127">Header</span><span class="sxs-lookup"><span data-stu-id="40fc4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="40fc4-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="40fc4-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="40fc4-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="40fc4-129">Library</span></span><br/> | <dl> <span data-ttu-id="40fc4-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40fc4-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="40fc4-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40fc4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40fc4-132">Effekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="40fc4-132">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
