---
description: Gibt die Stärke der Linie an.
ms.assetid: cedf9217-2b47-40c3-a64c-9872c1083d71
title: ID3DXLine::-Methode (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetWidth
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d357d7516233caf6ef9206aa2aecc2a98a435cde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050922"
---
# <a name="id3dxlinesetwidth-method"></a><span data-ttu-id="5891b-103">ID3DXLine:: stwidth-Methode</span><span class="sxs-lookup"><span data-stu-id="5891b-103">ID3DXLine::SetWidth method</span></span>

<span data-ttu-id="5891b-104">Gibt die Stärke der Linie an.</span><span class="sxs-lookup"><span data-stu-id="5891b-104">Specifies the thickness of the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="5891b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5891b-105">Syntax</span></span>


```C++
HRESULT SetWidth(
  [in] FLOAT fWidth
);
```



## <a name="parameters"></a><span data-ttu-id="5891b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5891b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5891b-107">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5891b-107">*fWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891b-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5891b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5891b-109">Beschreibt die Linienstärke.</span><span class="sxs-lookup"><span data-stu-id="5891b-109">Describes the line width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5891b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5891b-110">Return value</span></span>

<span data-ttu-id="5891b-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5891b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5891b-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5891b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5891b-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="5891b-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="5891b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5891b-114">Requirements</span></span>



| <span data-ttu-id="5891b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5891b-115">Requirement</span></span> | <span data-ttu-id="5891b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5891b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5891b-117">Header</span><span class="sxs-lookup"><span data-stu-id="5891b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5891b-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="5891b-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="5891b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5891b-119">Library</span></span><br/> | <dl> <span data-ttu-id="5891b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5891b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5891b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5891b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5891b-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="5891b-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
