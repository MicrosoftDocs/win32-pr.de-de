---
title: D3D12IsLayoutOpaque-Funktion (D3dx12. h)
description: Gibt an, ob das Layout nicht transparent ist.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- D3D12IsLayoutOpaque-Funktion
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351925"
---
# <a name="d3d12islayoutopaque-function"></a><span data-ttu-id="fe469-104">D3D12IsLayoutOpaque-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe469-104">D3D12IsLayoutOpaque function</span></span>

<span data-ttu-id="fe469-105">Gibt an, ob das Layout nicht transparent ist.</span><span class="sxs-lookup"><span data-stu-id="fe469-105">Indicates whether the layout is opaque.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe469-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe469-106">Syntax</span></span>


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a><span data-ttu-id="fe469-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe469-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe469-108">*Layout*</span><span class="sxs-lookup"><span data-stu-id="fe469-108">*Layout*</span></span> 
</dt> <dd>

<span data-ttu-id="fe469-109">Type: **[ **D3D12 \_ Texture \_ Layout**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span><span class="sxs-lookup"><span data-stu-id="fe469-109">Type: **[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span></span>

<span data-ttu-id="fe469-110">Das zu überprüfen Layout als [**D3D12 \_ Textur \_ Layout**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span><span class="sxs-lookup"><span data-stu-id="fe469-110">The layout to check, as a [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe469-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe469-111">Return value</span></span>

<span data-ttu-id="fe469-112">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="fe469-112">Type: **bool**</span></span>

<span data-ttu-id="fe469-113">Ein **boolescher** Wert, der angibt, ob das Layout nicht transparent ist.</span><span class="sxs-lookup"><span data-stu-id="fe469-113">A **bool** that indicates whether the layout is opaque.</span></span> <span data-ttu-id="fe469-114">Ein Layout ist nicht transparent, wenn es D3D12 \_ Texture \_ Layout \_ unknown oder D3D12 \_ Texture \_ Layout \_ 64 KB \_ undefiniertes \_ Swizzle ist.</span><span class="sxs-lookup"><span data-stu-id="fe469-114">A layout is opaque if it is D3D12\_TEXTURE\_LAYOUT\_UNKNOWN or D3D12\_TEXTURE\_LAYOUT\_64KB\_UNDEFINED\_SWIZZLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe469-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe469-115">Requirements</span></span>



| <span data-ttu-id="fe469-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe469-116">Requirement</span></span> | <span data-ttu-id="fe469-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fe469-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fe469-118">Header</span><span class="sxs-lookup"><span data-stu-id="fe469-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fe469-119"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe469-119"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="fe469-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe469-120">Library</span></span><br/> | <dl> <span data-ttu-id="fe469-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe469-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="fe469-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fe469-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="fe469-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe469-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe469-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe469-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe469-125">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="fe469-125">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





