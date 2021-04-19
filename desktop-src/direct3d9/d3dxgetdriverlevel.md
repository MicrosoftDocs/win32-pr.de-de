---
description: Gibt die Treiber Ebene zurück.
ms.assetid: e8c85201-7850-4c8d-a124-ceb76d4e24d5
title: D3DXGetDriverLevel-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDriverLevel
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83f756f6b6ab5864f14e797879be243f871fb9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355187"
---
# <a name="d3dxgetdriverlevel-function"></a><span data-ttu-id="0642f-103">D3DXGetDriverLevel-Funktion</span><span class="sxs-lookup"><span data-stu-id="0642f-103">D3DXGetDriverLevel function</span></span>

<span data-ttu-id="0642f-104">Gibt die Treiber Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="0642f-104">Returns the driver level.</span></span>

## <a name="syntax"></a><span data-ttu-id="0642f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0642f-105">Syntax</span></span>


```C++
UINT D3DXGetDriverLevel(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="0642f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0642f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0642f-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0642f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0642f-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0642f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0642f-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="0642f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0642f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0642f-110">Return value</span></span>

<span data-ttu-id="0642f-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0642f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0642f-112">Die Treiber Ebene.</span><span class="sxs-lookup"><span data-stu-id="0642f-112">The driver level.</span></span> <span data-ttu-id="0642f-113">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="0642f-113">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="0642f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0642f-114">Remarks</span></span>

<span data-ttu-id="0642f-115">Diese Methode gibt die Treiber Version zurück, die eines der folgenden ist:</span><span class="sxs-lookup"><span data-stu-id="0642f-115">This method returns the driver version, which is one of the following:</span></span>

-   <span data-ttu-id="0642f-116">700-Direct3D 7-Ebenen-Treiber</span><span class="sxs-lookup"><span data-stu-id="0642f-116">700 - Direct3D 7 level driver</span></span>
-   <span data-ttu-id="0642f-117">800-Direct3D 8-Ebenen-Treiber</span><span class="sxs-lookup"><span data-stu-id="0642f-117">800 - Direct3D 8 level driver</span></span>
-   <span data-ttu-id="0642f-118">900-Direct3D 9-sestreiber</span><span class="sxs-lookup"><span data-stu-id="0642f-118">900 - Direct3D 9 level driver</span></span>

## <a name="requirements"></a><span data-ttu-id="0642f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0642f-119">Requirements</span></span>



| <span data-ttu-id="0642f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0642f-120">Requirement</span></span> | <span data-ttu-id="0642f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0642f-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0642f-122">Header</span><span class="sxs-lookup"><span data-stu-id="0642f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0642f-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0642f-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0642f-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0642f-124">Library</span></span><br/> | <dl> <span data-ttu-id="0642f-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0642f-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0642f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0642f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0642f-127">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="0642f-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
