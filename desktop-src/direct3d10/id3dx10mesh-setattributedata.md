---
description: Legen Sie die Attributdaten des Mesh fest.
ms.assetid: bcf7b1b3-b923-400a-8d12-5094f3844d8f
title: 'ID3DX10Mesh:: stattributedata-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 19d69f8747196d7b25c85cb04fb173adef193098
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219610"
---
# <a name="id3dx10meshsetattributedata-method"></a><span data-ttu-id="7d523-103">ID3DX10Mesh:: stattributedata-Methode</span><span class="sxs-lookup"><span data-stu-id="7d523-103">ID3DX10Mesh::SetAttributeData method</span></span>

<span data-ttu-id="7d523-104">Legen Sie die Attributdaten des Mesh fest.</span><span class="sxs-lookup"><span data-stu-id="7d523-104">Set the mesh's attribute data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d523-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d523-105">Syntax</span></span>


```C++
HRESULT SetAttributeData(
  [in] const UINT *pData
);
```



## <a name="parameters"></a><span data-ttu-id="7d523-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d523-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d523-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d523-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d523-108">Typ: Konstante **[**uint**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7d523-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7d523-109">Die festzulegenden Attributdaten.</span><span class="sxs-lookup"><span data-stu-id="7d523-109">The attribute data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d523-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d523-110">Return value</span></span>

<span data-ttu-id="7d523-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7d523-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7d523-112">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="7d523-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d523-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d523-113">Requirements</span></span>



| <span data-ttu-id="7d523-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d523-114">Requirement</span></span> | <span data-ttu-id="7d523-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7d523-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d523-116">Header</span><span class="sxs-lookup"><span data-stu-id="7d523-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7d523-117"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d523-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7d523-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7d523-118">Library</span></span><br/> | <dl> <span data-ttu-id="7d523-119"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d523-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d523-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d523-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d523-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="7d523-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="7d523-122">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7d523-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
