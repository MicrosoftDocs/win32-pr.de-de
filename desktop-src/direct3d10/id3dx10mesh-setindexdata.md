---
description: Legen Sie die Indexdaten des Netzes fest.
ms.assetid: f3e7e166-94b5-45f6-9d43-8d7e32b7b523
title: 'ID3DX10Mesh:: setindexdata-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetIndexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f561a4109fbab2163b2ec51e95b45a618da5b6d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355821"
---
# <a name="id3dx10meshsetindexdata-method"></a><span data-ttu-id="8b730-103">ID3DX10Mesh:: setindexdata-Methode</span><span class="sxs-lookup"><span data-stu-id="8b730-103">ID3DX10Mesh::SetIndexData method</span></span>

<span data-ttu-id="8b730-104">Legen Sie die Indexdaten des Netzes fest.</span><span class="sxs-lookup"><span data-stu-id="8b730-104">Set the mesh's index data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b730-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b730-105">Syntax</span></span>


```C++
HRESULT SetIndexData(
  [in] const void *pData,
  [in]       UINT cIndices
);
```



## <a name="parameters"></a><span data-ttu-id="8b730-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b730-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b730-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b730-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b730-108">Typ: Konstante **void \***</span><span class="sxs-lookup"><span data-stu-id="8b730-108">Type: **const void\***</span></span>

<span data-ttu-id="8b730-109">Die Indexdaten.</span><span class="sxs-lookup"><span data-stu-id="8b730-109">The index data.</span></span>

</dd> <dt>

<span data-ttu-id="8b730-110">*cindizes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b730-110">*cIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b730-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b730-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b730-112">Die Anzahl der Indizes in pData.</span><span class="sxs-lookup"><span data-stu-id="8b730-112">The number of indices in pData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b730-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b730-113">Return value</span></span>

<span data-ttu-id="8b730-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b730-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b730-115">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="8b730-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b730-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b730-116">Requirements</span></span>



| <span data-ttu-id="8b730-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b730-117">Requirement</span></span> | <span data-ttu-id="8b730-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8b730-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b730-119">Header</span><span class="sxs-lookup"><span data-stu-id="8b730-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8b730-120"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b730-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b730-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8b730-121">Library</span></span><br/> | <dl> <span data-ttu-id="8b730-122"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b730-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b730-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b730-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b730-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="8b730-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="8b730-125">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8b730-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
