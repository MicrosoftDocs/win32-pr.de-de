---
description: Gibt an, dass die Transformationsmatrix als World Transformation Matrix festgelegt wird.
ms.assetid: 2bf7ac8a-43d8-460e-a400-3b33e96441db
title: D3DTS_WORLD-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLD
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3c8f0ac30230a747fba34d9962791b4b331d647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363126"
---
# <a name="d3dts_world-macro"></a><span data-ttu-id="1aa10-103">D3DTS \_ World-Makro</span><span class="sxs-lookup"><span data-stu-id="1aa10-103">D3DTS\_WORLD macro</span></span>

<span data-ttu-id="1aa10-104">Gibt an, dass die Transformationsmatrix als World Transformation Matrix festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1aa10-104">Identifies the transformation matrix being set as the world transformation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa10-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1aa10-105">Syntax</span></span>


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLD(void);
```



## <a name="parameters"></a><span data-ttu-id="1aa10-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1aa10-106">Parameters</span></span>

<span data-ttu-id="1aa10-107">Dieses Makro weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="1aa10-107">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1aa10-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1aa10-108">Return value</span></span>

<span data-ttu-id="1aa10-109">Ein [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) Äquivalent zu [**D3DTS \_ worldmatrix (0)**](./d3dts-worldmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="1aa10-109">A [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) equivalent to [**D3DTS\_WORLDMATRIX(0)**](./d3dts-worldmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1aa10-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aa10-110">Remarks</span></span>

<span data-ttu-id="1aa10-111">Dieses Makro wird bereitgestellt, um das Portieren vorhandener Anwendungen auf Direct3D 9 zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="1aa10-111">This macro is provided to facilitate porting existing applications to Direct3D 9.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa10-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1aa10-112">Requirements</span></span>



| <span data-ttu-id="1aa10-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1aa10-113">Requirement</span></span> | <span data-ttu-id="1aa10-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1aa10-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa10-115">Header</span><span class="sxs-lookup"><span data-stu-id="1aa10-115">Header</span></span><br/> | <dl> <span data-ttu-id="1aa10-116"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aa10-116"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aa10-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1aa10-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa10-118">Makros</span><span class="sxs-lookup"><span data-stu-id="1aa10-118">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="1aa10-119">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="1aa10-119">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="1aa10-120">**D3DTS \_ worldmatrix**</span><span class="sxs-lookup"><span data-stu-id="1aa10-120">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
