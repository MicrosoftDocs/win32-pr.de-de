---
description: Ruft das Handle einer Funktion ab, indem der zugehörige Name gesucht wird.
ms.assetid: 1e2e2dae-5084-47f3-9812-3dbf609bd70b
title: 'ID3DXBaseEffect:: getfunctionbyname-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1cd9ec56ff5df3bff293ade0669b4cd7c8dad5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355907"
---
# <a name="id3dxbaseeffectgetfunctionbyname-method"></a><span data-ttu-id="01c7b-103">ID3DXBaseEffect:: getfunctionbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="01c7b-103">ID3DXBaseEffect::GetFunctionByName method</span></span>

<span data-ttu-id="01c7b-104">Ruft das Handle einer Funktion ab, indem der zugehörige Name gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="01c7b-104">Gets the handle of a function by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="01c7b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="01c7b-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunctionByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="01c7b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="01c7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01c7b-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01c7b-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01c7b-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01c7b-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01c7b-109">Zeichenfolge, die den Funktionsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="01c7b-109">String containing the function name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01c7b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01c7b-110">Return value</span></span>

<span data-ttu-id="01c7b-111">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="01c7b-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="01c7b-112">Gibt das Handle der angegebenen Funktion zurück, oder **null** , wenn der Name nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="01c7b-112">Returns the handle of the specified function, or **NULL** if the name was not found.</span></span> <span data-ttu-id="01c7b-113">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="01c7b-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01c7b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01c7b-114">Requirements</span></span>



| <span data-ttu-id="01c7b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01c7b-115">Requirement</span></span> | <span data-ttu-id="01c7b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="01c7b-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c7b-117">Header</span><span class="sxs-lookup"><span data-stu-id="01c7b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="01c7b-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="01c7b-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="01c7b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="01c7b-119">Library</span></span><br/> | <dl> <span data-ttu-id="01c7b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01c7b-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="01c7b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01c7b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c7b-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="01c7b-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
