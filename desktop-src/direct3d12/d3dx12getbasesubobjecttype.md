---
title: D3DX12GetBaseSubobjectType-Funktion (D3dx12. h)
description: Gibt den untergeordneten Objekttyp zurück, der der Basisklasse des übergeordneten untergeordneten Objekts entspricht.
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- D3DX12GetBaseSubobjectType-Funktion
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350661"
---
# <a name="d3dx12getbasesubobjecttype-function"></a><span data-ttu-id="9bcc7-104">D3DX12GetBaseSubobjectType-Funktion</span><span class="sxs-lookup"><span data-stu-id="9bcc7-104">D3DX12GetBaseSubobjectType function</span></span>

<span data-ttu-id="9bcc7-105">Gibt den untergeordneten Objekttyp zurück, der der Basisklasse des übergeordneten untergeordneten Objekts entspricht.</span><span class="sxs-lookup"><span data-stu-id="9bcc7-105">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bcc7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bcc7-106">Syntax</span></span>


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a><span data-ttu-id="9bcc7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bcc7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bcc7-108">*Subobjecttype*</span><span class="sxs-lookup"><span data-stu-id="9bcc7-108">*SubobjectType*</span></span> 
</dt> <dd>

<span data-ttu-id="9bcc7-109">Type: **D3D12 \_ Pipeline \_ State \_ SubObject \_ Type**</span><span class="sxs-lookup"><span data-stu-id="9bcc7-109">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="9bcc7-110">Ein-Enumerationswert, der den Typ des untergeordneten Objekts angibt, an dem Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="9bcc7-110">An enumeration value that specifies the subobject type that you're interested in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bcc7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9bcc7-111">Return value</span></span>

<span data-ttu-id="9bcc7-112">Type: **D3D12 \_ Pipeline \_ State \_ SubObject \_ Type**</span><span class="sxs-lookup"><span data-stu-id="9bcc7-112">Type: **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>

<span data-ttu-id="9bcc7-113">Wenn *subobjecttype* einem untergeordneten Datentyp entspricht, der von einem anderen untergeordneten Datentyp abgeleitet ist, wird der untergeordnete Typ des Basis-unter-Datentyps zurückgegeben. Andernfalls wird der bestandene untergeordnete Typ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9bcc7-113">If *SubobjectType* corresponds to a subobject data type that is derived from another subobject data type, the subobject type of the base subobject data type is returned; otherwise, the passed-in subobject type is returned.</span></span> <span data-ttu-id="9bcc7-114">Wenn z. b. die **\_ \_ \_ \_ \_ Tiefe \_ STENCIL1 des D3D12 Pipeline State** -untergeordneten Typs überschritten wird, wird die **\_ \_ \_ \_ \_ tiefen \_ Schablone des D3D12-Pipeline Zustands** untergeordneten Typs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9bcc7-114">For example, if **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL1** is passed in, then **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_DEPTH\_STENCIL** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bcc7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bcc7-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9bcc7-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9bcc7-116">Requirements</span></span>



| <span data-ttu-id="9bcc7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bcc7-117">Requirement</span></span> | <span data-ttu-id="9bcc7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9bcc7-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcc7-119">Header</span><span class="sxs-lookup"><span data-stu-id="9bcc7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9bcc7-120"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bcc7-120"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="9bcc7-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9bcc7-121">Library</span></span><br/> | <dl> <span data-ttu-id="9bcc7-122"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bcc7-122"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="9bcc7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9bcc7-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="9bcc7-124"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bcc7-124"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bcc7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bcc7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bcc7-126">Funktionen des Hilfsprogramms für D3D12</span><span class="sxs-lookup"><span data-stu-id="9bcc7-126">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





