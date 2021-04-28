---
description: 'ID3DXMATRIXStack::LoadIdentity-Methode (D3DX10.h): Lädt die Identität in der aktuellen Matrix.'
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: ID3DXMATRIXStack::LoadIdentity-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f056a911b19c0ea18f5f728a6ce8c4403dd14587
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107988"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a><span data-ttu-id="55071-103">ID3DXMATRIXStack::LoadIdentity-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="55071-103">ID3DXMATRIXStack::LoadIdentity method (D3DX10.h)</span></span>

<span data-ttu-id="55071-104">Lädt die Identität in der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="55071-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="55071-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="55071-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="55071-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55071-106">Parameters</span></span>

<span data-ttu-id="55071-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="55071-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55071-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55071-108">Return value</span></span>

<span data-ttu-id="55071-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="55071-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="55071-110">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="55071-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="55071-111">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="55071-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="55071-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55071-112">Remarks</span></span>

<span data-ttu-id="55071-113">Die Identitätsmatrix ist eine Matrix, in der alle Koeffizienten 0,0 sind, mit Ausnahme der \[ 1,1 \] \[ 2,2 \] \[ 3,3 \] \[ 4,4-Koeffizienten, die auf \] 1,0 festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="55071-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="55071-114">Die Identitätsmatrix ist besonders, da sie unverändert bleibt, wenn sie auf Scheitelzeichen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="55071-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="55071-115">Die Identitätsmatrix wird als Ausgangspunkt für Matrizen verwendet, die Scheitelpunktwerte ändern, um Drehungen, Übersetzungen und alle anderen Transformationen zu erstellen, die durch eine 4x4-Matrix dargestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="55071-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="55071-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55071-116">Requirements</span></span>



| <span data-ttu-id="55071-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55071-117">Requirement</span></span> | <span data-ttu-id="55071-118">Wert</span><span class="sxs-lookup"><span data-stu-id="55071-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55071-119">Header</span><span class="sxs-lookup"><span data-stu-id="55071-119">Header</span></span><br/>  | <dl> <span data-ttu-id="55071-120"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="55071-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="55071-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="55071-121">Library</span></span><br/> | <dl> <span data-ttu-id="55071-122"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="55071-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55071-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="55071-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55071-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="55071-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="55071-125">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="55071-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




