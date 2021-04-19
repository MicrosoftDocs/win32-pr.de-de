---
description: Ruft das Handle einer Anmerkung ab.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: 'ID3DXBaseEffect:: GetAnnotation-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aad446e436478c8c7673a1919879983437fd9602
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364008"
---
# <a name="id3dxbaseeffectgetannotation-method"></a><span data-ttu-id="0dc99-103">ID3DXBaseEffect:: GetAnnotation-Methode</span><span class="sxs-lookup"><span data-stu-id="0dc99-103">ID3DXBaseEffect::GetAnnotation method</span></span>

<span data-ttu-id="0dc99-104">Ruft das Handle einer Anmerkung ab.</span><span class="sxs-lookup"><span data-stu-id="0dc99-104">Gets the handle of an annotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc99-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dc99-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="0dc99-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0dc99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc99-107">*hobject* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0dc99-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc99-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0dc99-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0dc99-109">Handle eines Verfahrens, eines bestanden oder eines Parameters der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="0dc99-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="0dc99-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0dc99-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0dc99-111">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0dc99-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc99-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dc99-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0dc99-113">Annotation-Index.</span><span class="sxs-lookup"><span data-stu-id="0dc99-113">Annotation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dc99-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0dc99-114">Return value</span></span>

<span data-ttu-id="0dc99-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0dc99-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0dc99-116">Gibt das Handle der angegebenen Anmerkung zurück, oder **null** , wenn der Index ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="0dc99-116">Returns the handle of the specified annotation, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="0dc99-117">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0dc99-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc99-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0dc99-118">Remarks</span></span>

<span data-ttu-id="0dc99-119">Anmerkungen sind benutzerspezifische Daten, die an beliebige Techniken, Pass oder Parameter angefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="0dc99-119">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="0dc99-120">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0dc99-120">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc99-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dc99-121">Requirements</span></span>



| <span data-ttu-id="0dc99-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0dc99-122">Requirement</span></span> | <span data-ttu-id="0dc99-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0dc99-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc99-124">Header</span><span class="sxs-lookup"><span data-stu-id="0dc99-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0dc99-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dc99-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0dc99-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0dc99-126">Library</span></span><br/> | <dl> <span data-ttu-id="0dc99-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0dc99-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0dc99-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dc99-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc99-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0dc99-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
