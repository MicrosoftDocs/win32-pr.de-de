---
description: Gibt die Anzahl der Scheitel Punkte an, die von einem bestimmten Knochen beeinflusst werden.
ms.assetid: e92361ea-4269-4d63-a8d1-560a486b6563
title: 'ID3DX10SkinInfo:: getboneinfludencecount-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluenceCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ad6ddc6ebc80c51e07b7ff0c887371fd45fd42b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366468"
---
# <a name="id3dx10skininfogetboneinfluencecount-method"></a><span data-ttu-id="8f9d4-103">ID3DX10SkinInfo:: getboneinfluscecount-Methode</span><span class="sxs-lookup"><span data-stu-id="8f9d4-103">ID3DX10SkinInfo::GetBoneInfluenceCount method</span></span>

<span data-ttu-id="8f9d4-104">Gibt die Anzahl der Scheitel Punkte an, die von einem bestimmten Knochen beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="8f9d4-104">Get the number of vertices that a given bone influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f9d4-105">Syntax</span></span>


```C++
UINT GetBoneInfluenceCount(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a><span data-ttu-id="8f9d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f9d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f9d4-107">*Boneingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f9d4-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9d4-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f9d4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f9d4-109">Ein Index, der einen vorhandenen Knochen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="8f9d4-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="8f9d4-110">Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.</span><span class="sxs-lookup"><span data-stu-id="8f9d4-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f9d4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f9d4-111">Return value</span></span>

<span data-ttu-id="8f9d4-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f9d4-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f9d4-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8f9d4-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8f9d4-114">Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg.</span><span class="sxs-lookup"><span data-stu-id="8f9d4-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f9d4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f9d4-115">Requirements</span></span>



| <span data-ttu-id="8f9d4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f9d4-116">Requirement</span></span> | <span data-ttu-id="8f9d4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8f9d4-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9d4-118">Header</span><span class="sxs-lookup"><span data-stu-id="8f9d4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8f9d4-119"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f9d4-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f9d4-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8f9d4-120">Library</span></span><br/> | <dl> <span data-ttu-id="8f9d4-121"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f9d4-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f9d4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f9d4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9d4-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="8f9d4-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="8f9d4-124">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8f9d4-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
