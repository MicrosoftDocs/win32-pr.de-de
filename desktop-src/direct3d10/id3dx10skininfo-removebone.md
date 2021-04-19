---
description: Entfernt einen Knochen.
ms.assetid: efb88108-5c76-47c8-b8ce-1ba29cb18ba4
title: 'ID3DX10SkinInfo:: removebone-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemoveBone
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 49fd24c5661bbedb7fb839171fa4a835f07e446a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367370"
---
# <a name="id3dx10skininforemovebone-method"></a><span data-ttu-id="a4668-103">ID3DX10SkinInfo:: removebone-Methode</span><span class="sxs-lookup"><span data-stu-id="a4668-103">ID3DX10SkinInfo::RemoveBone method</span></span>

<span data-ttu-id="a4668-104">Entfernt einen Knochen.</span><span class="sxs-lookup"><span data-stu-id="a4668-104">Remove a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4668-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4668-105">Syntax</span></span>


```C++
HRESULT RemoveBone(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="a4668-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4668-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4668-107">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4668-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4668-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4668-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a4668-109">Ein Index, der angibt, welcher zu entfernende Knochen</span><span class="sxs-lookup"><span data-stu-id="a4668-109">An index that specifies which bone to remove.</span></span> <span data-ttu-id="a4668-110">Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.</span><span class="sxs-lookup"><span data-stu-id="a4668-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4668-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4668-111">Return value</span></span>

<span data-ttu-id="a4668-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a4668-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a4668-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a4668-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a4668-114">Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg.</span><span class="sxs-lookup"><span data-stu-id="a4668-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4668-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4668-115">Requirements</span></span>



| <span data-ttu-id="a4668-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4668-116">Requirement</span></span> | <span data-ttu-id="a4668-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a4668-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4668-118">Header</span><span class="sxs-lookup"><span data-stu-id="a4668-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a4668-119"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4668-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4668-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a4668-120">Library</span></span><br/> | <dl> <span data-ttu-id="a4668-121"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4668-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4668-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4668-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4668-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="a4668-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="a4668-124">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a4668-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
