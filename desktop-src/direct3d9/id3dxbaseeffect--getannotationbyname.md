---
description: Ruft das Handle einer Anmerkung ab, indem der zugehörige Name gesucht wird.
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: 'ID3DXBaseEffect:: getannotationbyname-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00698030488b8f4ae788367f87b8d569476292ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371950"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a><span data-ttu-id="d34cf-103">ID3DXBaseEffect:: getannotationbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="d34cf-103">ID3DXBaseEffect::GetAnnotationByName method</span></span>

<span data-ttu-id="d34cf-104">Ruft das Handle einer Anmerkung ab, indem der zugehörige Name gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="d34cf-104">Gets the handle of an annotation by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="d34cf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d34cf-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="d34cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d34cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d34cf-107">*hobject* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d34cf-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34cf-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d34cf-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d34cf-109">Handle eines Verfahrens, eines bestanden oder eines Parameters der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="d34cf-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="d34cf-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="d34cf-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="d34cf-111">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d34cf-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34cf-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d34cf-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d34cf-113">Zeichenfolge, die den Namen der Anmerkung enthält.</span><span class="sxs-lookup"><span data-stu-id="d34cf-113">String containing the annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d34cf-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d34cf-114">Return value</span></span>

<span data-ttu-id="d34cf-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d34cf-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d34cf-116">Gibt das Handle der angegebenen Anmerkung zurück, oder **null** , wenn der Name nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="d34cf-116">Returns the handle of the specified annotation, or **NULL** if the name was not found.</span></span> <span data-ttu-id="d34cf-117">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="d34cf-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d34cf-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d34cf-118">Requirements</span></span>



| <span data-ttu-id="d34cf-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d34cf-119">Requirement</span></span> | <span data-ttu-id="d34cf-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d34cf-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d34cf-121">Header</span><span class="sxs-lookup"><span data-stu-id="d34cf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d34cf-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d34cf-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d34cf-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d34cf-123">Library</span></span><br/> | <dl> <span data-ttu-id="d34cf-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d34cf-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d34cf-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d34cf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34cf-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="d34cf-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
