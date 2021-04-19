---
description: Fügt dem Animations Controller eine Animations Ausgabe hinzu und registriert Zeiger für die Transformation für Skalierung, Drehung und Übersetzung (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: 'ID3DXAnimationController:: registeranimationoutput-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670f8b311532d096b9957ebbefcf1f6fb15d952
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350716"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a><span data-ttu-id="45d2a-103">ID3DXAnimationController:: registeranimationoutput-Methode</span><span class="sxs-lookup"><span data-stu-id="45d2a-103">ID3DXAnimationController::RegisterAnimationOutput method</span></span>

<span data-ttu-id="45d2a-104">Fügt dem Animations Controller eine Animations Ausgabe hinzu und registriert Zeiger für die Transformation für Skalierung, Drehung und Übersetzung (SRT).</span><span class="sxs-lookup"><span data-stu-id="45d2a-104">Adds an animation output to the animation controller and registers pointers for scale, rotate, and translate (SRT) transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="45d2a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="45d2a-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="45d2a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="45d2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45d2a-107">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45d2a-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d2a-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45d2a-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45d2a-109">Der Name der Animations Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="45d2a-109">Name of the animation output.</span></span>

</dd> <dt>

<span data-ttu-id="45d2a-110">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45d2a-110">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d2a-111">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="45d2a-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="45d2a-112">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die Daten der SRT-Transformation enthält.</span><span class="sxs-lookup"><span data-stu-id="45d2a-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure containing SRT transformation data.</span></span> <span data-ttu-id="45d2a-113">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="45d2a-113">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="45d2a-114">*pscale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45d2a-114">*pScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d2a-115">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="45d2a-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="45d2a-116">Zeiger auf einen [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Skala des Animations Satzes beschreibt.</span><span class="sxs-lookup"><span data-stu-id="45d2a-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span> <span data-ttu-id="45d2a-117">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="45d2a-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="45d2a-118">*protation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45d2a-118">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d2a-119">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="45d2a-119">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="45d2a-120">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) Quaternion, die die Drehung des Animations Satzes beschreibt.</span><span class="sxs-lookup"><span data-stu-id="45d2a-120">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span> <span data-ttu-id="45d2a-121">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="45d2a-121">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="45d2a-122">*ptranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45d2a-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d2a-123">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="45d2a-123">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="45d2a-124">Zeiger auf einen [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Übersetzung des Animations Satzes beschreibt.</span><span class="sxs-lookup"><span data-stu-id="45d2a-124">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span> <span data-ttu-id="45d2a-125">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="45d2a-125">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45d2a-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45d2a-126">Return value</span></span>

<span data-ttu-id="45d2a-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="45d2a-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="45d2a-128">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="45d2a-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="45d2a-129">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="45d2a-129">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="45d2a-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45d2a-130">Remarks</span></span>

<span data-ttu-id="45d2a-131">Wenn die Ausgabe der Animation bereits registriert ist, wird pmatrix mit den Eingabe Transformations Daten aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="45d2a-131">If the animation output is already registered, pMatrix will be filled with the input transformation data.</span></span>

<span data-ttu-id="45d2a-132">Mit [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) erstellte Animations Sätze registrieren automatisch alle geladenen Animations Sätze.</span><span class="sxs-lookup"><span data-stu-id="45d2a-132">Animation sets created with [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) automatically register all loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="45d2a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45d2a-133">Requirements</span></span>



| <span data-ttu-id="45d2a-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45d2a-134">Requirement</span></span> | <span data-ttu-id="45d2a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="45d2a-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45d2a-136">Header</span><span class="sxs-lookup"><span data-stu-id="45d2a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="45d2a-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="45d2a-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="45d2a-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="45d2a-138">Library</span></span><br/> | <dl> <span data-ttu-id="45d2a-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45d2a-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45d2a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45d2a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d2a-141">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="45d2a-141">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
