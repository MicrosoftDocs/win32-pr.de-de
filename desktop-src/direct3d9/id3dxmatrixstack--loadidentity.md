---
description: Lädt die Identität in der aktuellen Matrix.
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: 'ID3DXMATRIXStack:: loadidentity-Methode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e7ebc7b61679dc3938c2a57aa2346a45b136e5a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367354"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a><span data-ttu-id="52eb9-103">ID3DXMATRIXStack:: loadidentity-Methode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="52eb9-103">ID3DXMATRIXStack::LoadIdentity method (D3dx9math.h)</span></span>

<span data-ttu-id="52eb9-104">Lädt die Identität in der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="52eb9-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="52eb9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52eb9-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="52eb9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52eb9-106">Parameters</span></span>

<span data-ttu-id="52eb9-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="52eb9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="52eb9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52eb9-108">Return value</span></span>

<span data-ttu-id="52eb9-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52eb9-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52eb9-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52eb9-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="52eb9-111">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="52eb9-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="52eb9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52eb9-112">Remarks</span></span>

<span data-ttu-id="52eb9-113">Die Identitätsmatrix ist eine Matrix, in der alle Koeffizienten 0,0 sind, mit Ausnahme der \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, 4 Koeffizienten \] , die auf 1,0 festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="52eb9-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="52eb9-114">Die Identitätsmatrix ist ein besonderes, da Sie bei der Anwendung auf Vertices nicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="52eb9-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="52eb9-115">Die Identitätsmatrix dient als Ausgangspunkt für Matrizen, die Scheitelpunkt Werte ändern, um Drehungen, Übersetzungen und andere Transformationen zu erstellen, die durch eine 4 x 4-Matrix dargestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="52eb9-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="52eb9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52eb9-116">Requirements</span></span>



| <span data-ttu-id="52eb9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52eb9-117">Requirement</span></span> | <span data-ttu-id="52eb9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="52eb9-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52eb9-119">Header</span><span class="sxs-lookup"><span data-stu-id="52eb9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="52eb9-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="52eb9-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="52eb9-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="52eb9-121">Library</span></span><br/> | <dl> <span data-ttu-id="52eb9-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52eb9-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52eb9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52eb9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52eb9-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="52eb9-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="52eb9-125">**ID3DXMATRIXStack:: loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="52eb9-125">**ID3DXMATRIXStack::LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




