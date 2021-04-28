---
description: 'D3DXMatrixDecompose-Funktion (D3dx9math.h): Unterbricht eine allgemeine 3D-Transformationsmatrix in ihre skalaren, rotierten und übersetzungsbasierten Komponenten.'
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: D3DXMatrixDecompose-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aaaa1059c4ffeafa453694d9c348656c856decaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098188"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a><span data-ttu-id="f0327-103">D3DXMatrixDecompose-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="f0327-103">D3DXMatrixDecompose function (D3dx9math.h)</span></span>

<span data-ttu-id="f0327-104">Unterteilen einer allgemeinen 3D-Transformationsmatrix in ihre skalaren, drehlichen und übersetzungsübergreifenden Komponenten.</span><span class="sxs-lookup"><span data-stu-id="f0327-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0327-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0327-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="f0327-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0327-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0327-107">*pOutScale* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0327-107">*pOutScale* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0327-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0327-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f0327-109">Zeiger auf die Ausgabe [**D3DXVECTOR3,**](d3dxvector3.md) die Skalierungsfaktoren enthält, die entlang der x-, y- und z-Achsen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0327-109">Pointer to the output [**D3DXVECTOR3**](d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="f0327-110">*pOutRotation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0327-110">*pOutRotation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0327-111">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0327-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f0327-112">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die die Drehung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f0327-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="f0327-113">*pOutTranslation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0327-113">*pOutTranslation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0327-114">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0327-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f0327-115">Zeiger auf den [**D3DXVECTOR3-Vektor,**](d3dxvector3.md) der die Übersetzung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f0327-115">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="f0327-116">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f0327-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0327-117">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f0327-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f0327-118">Zeiger auf eine [**D3DXMATRIX-Eingabematrix,**](d3dxmatrix.md) die zersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0327-118">Pointer to an input [**D3DXMATRIX**](d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0327-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0327-119">Return value</span></span>

<span data-ttu-id="f0327-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f0327-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f0327-121">Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f0327-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f0327-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f0327-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0327-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0327-123">Requirements</span></span>



| <span data-ttu-id="f0327-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0327-124">Requirement</span></span> | <span data-ttu-id="f0327-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f0327-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0327-126">Header</span><span class="sxs-lookup"><span data-stu-id="f0327-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f0327-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f0327-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f0327-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0327-128">Library</span></span><br/> | <dl> <span data-ttu-id="f0327-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0327-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f0327-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f0327-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0327-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f0327-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




