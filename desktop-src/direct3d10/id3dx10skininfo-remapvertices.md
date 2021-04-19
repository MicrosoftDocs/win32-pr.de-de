---
description: Ändern der zu ändernden Scheitel Punkte
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'ID3DX10SkinInfo:: remapvertices-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc51c912794135b456542bb9a8a779601681f393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355190"
---
# <a name="id3dx10skininforemapvertices-method"></a><span data-ttu-id="6fa31-103">ID3DX10SkinInfo:: remapvertices-Methode</span><span class="sxs-lookup"><span data-stu-id="6fa31-103">ID3DX10SkinInfo::RemapVertices method</span></span>

<span data-ttu-id="6fa31-104">Ändern der zu ändernden Scheitel Punkte</span><span class="sxs-lookup"><span data-stu-id="6fa31-104">Change which vertices are influenced by which bones.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa31-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fa31-105">Syntax</span></span>


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="6fa31-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fa31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fa31-107">*Newvertexcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6fa31-107">*NewVertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fa31-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6fa31-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6fa31-109">Die neue Anzahl von Vertices.</span><span class="sxs-lookup"><span data-stu-id="6fa31-109">The new number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="6fa31-110">*pvertexremap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6fa31-110">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fa31-111">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6fa31-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6fa31-112">Ein Zeiger auf ein Array von Scheitelpunkt Indizes, die die Neuzuordnung beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6fa31-112">A pointer to an array of vertex indices, which describe the remapping.</span></span> <span data-ttu-id="6fa31-113">Beispiel: "skininfo" enthält einige Scheitel Punkte, z. b. "bone0", "v0", "bone1 to v1" und "bone2" zu "V2" und "Array mit 2, 1, 0" für "pboneremap".</span><span class="sxs-lookup"><span data-stu-id="6fa31-113">For example, say SkinInfo contains some vertices such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="6fa31-114">Dies bewirkt, dass bone0 v2, bone1 zu v1 und bone2 zu v0 zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="6fa31-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fa31-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6fa31-115">Return value</span></span>

<span data-ttu-id="6fa31-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6fa31-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6fa31-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6fa31-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6fa31-118">Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: e \_ outo-Memory oder e \_ invalidArg.</span><span class="sxs-lookup"><span data-stu-id="6fa31-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fa31-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fa31-119">Requirements</span></span>



| <span data-ttu-id="6fa31-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fa31-120">Requirement</span></span> | <span data-ttu-id="6fa31-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6fa31-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa31-122">Header</span><span class="sxs-lookup"><span data-stu-id="6fa31-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6fa31-123"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fa31-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6fa31-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6fa31-124">Library</span></span><br/> | <dl> <span data-ttu-id="6fa31-125"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fa31-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fa31-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fa31-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa31-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="6fa31-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="6fa31-128">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6fa31-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
