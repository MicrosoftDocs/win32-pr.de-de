---
description: Ruft den Skalierungs Wert Stippel-Pattern ab.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'ID3DXLine:: getpatternscale-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14a9919ede81eb64b844e1882725e37359ad6738
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394262"
---
# <a name="id3dxlinegetpatternscale-method"></a><span data-ttu-id="7b2b5-103">ID3DXLine:: getpatternscale-Methode</span><span class="sxs-lookup"><span data-stu-id="7b2b5-103">ID3DXLine::GetPatternScale method</span></span>

<span data-ttu-id="7b2b5-104">Ruft den Skalierungs Wert Stippel-Pattern ab.</span><span class="sxs-lookup"><span data-stu-id="7b2b5-104">Gets the stipple-pattern scale value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b2b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b2b5-105">Syntax</span></span>


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a><span data-ttu-id="7b2b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b2b5-106">Parameters</span></span>

<span data-ttu-id="7b2b5-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7b2b5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b2b5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b2b5-108">Return value</span></span>

<span data-ttu-id="7b2b5-109">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b2b5-109">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b2b5-110">Gibt den Wert zurück, mit dem das Stippel Muster skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="7b2b5-110">Returns the value used to scale the stipple-pattern.</span></span> <span data-ttu-id="7b2b5-111">1.0 f ist der Standardwert und stellt keine Skalierung dar.</span><span class="sxs-lookup"><span data-stu-id="7b2b5-111">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="7b2b5-112">Ein Wert kleiner als 1,0 f verkleinert das Muster, und ein Wert größer als 1,0 dehnt das Muster aus.</span><span class="sxs-lookup"><span data-stu-id="7b2b5-112">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b2b5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b2b5-113">Requirements</span></span>



| <span data-ttu-id="7b2b5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b2b5-114">Requirement</span></span> | <span data-ttu-id="7b2b5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7b2b5-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b2b5-116">Header</span><span class="sxs-lookup"><span data-stu-id="7b2b5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7b2b5-117"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b2b5-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7b2b5-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7b2b5-118">Library</span></span><br/> | <dl> <span data-ttu-id="7b2b5-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b2b5-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7b2b5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b2b5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b2b5-121">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="7b2b5-121">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="7b2b5-122">**ID3DXLine:: setpatternscale**</span><span class="sxs-lookup"><span data-stu-id="7b2b5-122">**ID3DXLine::SetPatternScale**</span></span>](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
