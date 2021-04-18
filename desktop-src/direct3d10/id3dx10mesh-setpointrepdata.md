---
description: Legen Sie die Punkt-Rep-Daten für das Mesh fest.
ms.assetid: 451a1ff0-68fa-48c4-b3f1-d41d7583cb3f
title: 'ID3DX10Mesh:: setpointrepdata-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetPointRepData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65114c5411de7932e9cb71166fcf8554fa0bf7b6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365326"
---
# <a name="id3dx10meshsetpointrepdata-method"></a><span data-ttu-id="7e051-103">ID3DX10Mesh:: setpointrepdata-Methode</span><span class="sxs-lookup"><span data-stu-id="7e051-103">ID3DX10Mesh::SetPointRepData method</span></span>

<span data-ttu-id="7e051-104">Legen Sie die Punkt-Rep-Daten für das Mesh fest.</span><span class="sxs-lookup"><span data-stu-id="7e051-104">Set the point rep data for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e051-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e051-105">Syntax</span></span>


```C++
HRESULT SetPointRepData(
  [in] const UINT *pPointReps
);
```



## <a name="parameters"></a><span data-ttu-id="7e051-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e051-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e051-107">*ppointreps* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e051-107">*pPointReps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e051-108">Typ: Konstante **[**uint**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e051-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7e051-109">Die festzulegenden Punkt-Rep-Daten.</span><span class="sxs-lookup"><span data-stu-id="7e051-109">The point rep data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e051-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e051-110">Return value</span></span>

<span data-ttu-id="7e051-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e051-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e051-112">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="7e051-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e051-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e051-113">Requirements</span></span>



| <span data-ttu-id="7e051-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e051-114">Requirement</span></span> | <span data-ttu-id="7e051-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7e051-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e051-116">Header</span><span class="sxs-lookup"><span data-stu-id="7e051-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7e051-117"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e051-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e051-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7e051-118">Library</span></span><br/> | <dl> <span data-ttu-id="7e051-119"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e051-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e051-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e051-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e051-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="7e051-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="7e051-122">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7e051-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
