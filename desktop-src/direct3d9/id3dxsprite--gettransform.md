---
description: Ruft die Sprite-Transformation ab.
ms.assetid: d91f2776-ee87-42b3-998b-fccea178cee2
title: 'ID3DXSprite:: GetTransform-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 646fa3574c3b9be788ad32ef402a7ca2051d04de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050876"
---
# <a name="id3dxspritegettransform-method"></a><span data-ttu-id="5625e-103">ID3DXSprite:: GetTransform-Methode</span><span class="sxs-lookup"><span data-stu-id="5625e-103">ID3DXSprite::GetTransform method</span></span>

<span data-ttu-id="5625e-104">Ruft die Sprite-Transformation ab.</span><span class="sxs-lookup"><span data-stu-id="5625e-104">Gets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="5625e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5625e-105">Syntax</span></span>


```C++
HRESULT GetTransform(
  [in] D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="5625e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5625e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5625e-107">*ptransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5625e-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5625e-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5625e-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5625e-109">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) , die eine Transformation des Sprite aus dem ursprünglichen Raum enthält.</span><span class="sxs-lookup"><span data-stu-id="5625e-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5625e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5625e-110">Return value</span></span>

<span data-ttu-id="5625e-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5625e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5625e-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5625e-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5625e-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="5625e-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="5625e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5625e-114">Requirements</span></span>



| <span data-ttu-id="5625e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5625e-115">Requirement</span></span> | <span data-ttu-id="5625e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5625e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5625e-117">Header</span><span class="sxs-lookup"><span data-stu-id="5625e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5625e-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="5625e-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="5625e-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5625e-119">Library</span></span><br/> | <dl> <span data-ttu-id="5625e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5625e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5625e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5625e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5625e-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="5625e-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




