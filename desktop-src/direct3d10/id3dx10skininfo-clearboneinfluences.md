---
description: Löschen Sie die Liste der Scheitel Punkte, auf die sich die Schnittstelle auswirkt.
ms.assetid: 1ba6f43a-1f85-4057-b0ed-247cc38d4932
title: 'ID3DX10SkinInfo:: clearboneingefluences-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.ClearBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6f161ba400b684b12d6b0a091abb1fa452d476b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961612"
---
# <a name="id3dx10skininfoclearboneinfluences-method"></a><span data-ttu-id="95646-103">ID3DX10SkinInfo:: clearboneingefluences-Methode</span><span class="sxs-lookup"><span data-stu-id="95646-103">ID3DX10SkinInfo::ClearBoneInfluences method</span></span>

<span data-ttu-id="95646-104">Löschen Sie die Liste der Scheitel Punkte, auf die sich die Schnittstelle auswirkt.</span><span class="sxs-lookup"><span data-stu-id="95646-104">Clear a bone's list of vertices that it influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="95646-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95646-105">Syntax</span></span>


```C++
HRESULT ClearBoneInfluences(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a><span data-ttu-id="95646-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95646-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95646-107">*Boneingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95646-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95646-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95646-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95646-109">Ein Index, der einen vorhandenen Knochen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="95646-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="95646-110">Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.</span><span class="sxs-lookup"><span data-stu-id="95646-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95646-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95646-111">Return value</span></span>

<span data-ttu-id="95646-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95646-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95646-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95646-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="95646-114">Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg.</span><span class="sxs-lookup"><span data-stu-id="95646-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="95646-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95646-115">Requirements</span></span>



| <span data-ttu-id="95646-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95646-116">Requirement</span></span> | <span data-ttu-id="95646-117">Wert</span><span class="sxs-lookup"><span data-stu-id="95646-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95646-118">Header</span><span class="sxs-lookup"><span data-stu-id="95646-118">Header</span></span><br/>  | <dl> <span data-ttu-id="95646-119"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="95646-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="95646-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95646-120">Library</span></span><br/> | <dl> <span data-ttu-id="95646-121"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95646-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95646-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95646-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95646-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="95646-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="95646-124">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="95646-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
