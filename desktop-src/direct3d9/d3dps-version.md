---
description: Erstellen Sie ein Pixel-Shader-Versions Token.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: D3DPS_VERSION-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355047"
---
# <a name="d3dps_version-macro"></a><span data-ttu-id="cad69-103">D3DPS- \_ Versions Makro</span><span class="sxs-lookup"><span data-stu-id="cad69-103">D3DPS\_VERSION macro</span></span>

<span data-ttu-id="cad69-104">Erstellen Sie ein Pixel-Shader-Versions Token.</span><span class="sxs-lookup"><span data-stu-id="cad69-104">Create a pixel shader version token.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad69-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cad69-105">Syntax</span></span>


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="cad69-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cad69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cad69-107">*\_Wichtige*</span><span class="sxs-lookup"><span data-stu-id="cad69-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="cad69-108">Die Haupt-Pixel-Shader-Version.</span><span class="sxs-lookup"><span data-stu-id="cad69-108">The major pixel shader version.</span></span>

</dd> <dt>

<span data-ttu-id="cad69-109">*\_Nebenversion*</span><span class="sxs-lookup"><span data-stu-id="cad69-109">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="cad69-110">Die neben Version des Pixelshaders.</span><span class="sxs-lookup"><span data-stu-id="cad69-110">The minor pixel shader version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cad69-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cad69-111">Return value</span></span>

<span data-ttu-id="cad69-112">Gibt einen DWORD-Wert zurück, der eine Pixel-Shader-Version ist.</span><span class="sxs-lookup"><span data-stu-id="cad69-112">Returns a DWORD value that is a pixel shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="cad69-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cad69-113">Remarks</span></span>

<span data-ttu-id="cad69-114">Versionsnummern</span><span class="sxs-lookup"><span data-stu-id="cad69-114">Version Numbers</span></span>

<span data-ttu-id="cad69-115">Die Versionsnummer ist eine Kombination aus der Hauptversion und den kleineren Scheitelpunkt-Shader-Versionsnummern.</span><span class="sxs-lookup"><span data-stu-id="cad69-115">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="cad69-116">In der Tabelle werden gültige Zahlen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cad69-116">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="cad69-117">Hauptversion</span><span class="sxs-lookup"><span data-stu-id="cad69-117">Major</span></span> | <span data-ttu-id="cad69-118">Nebenversion</span><span class="sxs-lookup"><span data-stu-id="cad69-118">Minor</span></span> | <span data-ttu-id="cad69-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cad69-119">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="cad69-120">1</span><span class="sxs-lookup"><span data-stu-id="cad69-120">1</span></span>     | <span data-ttu-id="cad69-121">1</span><span class="sxs-lookup"><span data-stu-id="cad69-121">1</span></span>     | <span data-ttu-id="cad69-122">D3DPS- \_ Version (1, 1)</span><span class="sxs-lookup"><span data-stu-id="cad69-122">D3DPS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="cad69-123">1</span><span class="sxs-lookup"><span data-stu-id="cad69-123">1</span></span>     | <span data-ttu-id="cad69-124">2</span><span class="sxs-lookup"><span data-stu-id="cad69-124">2</span></span>     | <span data-ttu-id="cad69-125">D3DPS- \_ Version (1, 2)</span><span class="sxs-lookup"><span data-stu-id="cad69-125">D3DPS\_VERSION(1,2)</span></span> |
| <span data-ttu-id="cad69-126">1</span><span class="sxs-lookup"><span data-stu-id="cad69-126">1</span></span>     | <span data-ttu-id="cad69-127">3</span><span class="sxs-lookup"><span data-stu-id="cad69-127">3</span></span>     | <span data-ttu-id="cad69-128">D3DPS- \_ Version (1, 3)</span><span class="sxs-lookup"><span data-stu-id="cad69-128">D3DPS\_VERSION(1,3)</span></span> |
| <span data-ttu-id="cad69-129">1</span><span class="sxs-lookup"><span data-stu-id="cad69-129">1</span></span>     | <span data-ttu-id="cad69-130">4</span><span class="sxs-lookup"><span data-stu-id="cad69-130">4</span></span>     | <span data-ttu-id="cad69-131">D3DPS- \_ Version (1, 4)</span><span class="sxs-lookup"><span data-stu-id="cad69-131">D3DPS\_VERSION(1,4)</span></span> |
| <span data-ttu-id="cad69-132">2</span><span class="sxs-lookup"><span data-stu-id="cad69-132">2</span></span>     | <span data-ttu-id="cad69-133">0</span><span class="sxs-lookup"><span data-stu-id="cad69-133">0</span></span>     | <span data-ttu-id="cad69-134">D3DPS- \_ Version (2, 0)</span><span class="sxs-lookup"><span data-stu-id="cad69-134">D3DPS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="cad69-135">3</span><span class="sxs-lookup"><span data-stu-id="cad69-135">3</span></span>     | <span data-ttu-id="cad69-136">0</span><span class="sxs-lookup"><span data-stu-id="cad69-136">0</span></span>     | <span data-ttu-id="cad69-137">D3DPS- \_ Version (3, 0)</span><span class="sxs-lookup"><span data-stu-id="cad69-137">D3DPS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="cad69-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cad69-138">Requirements</span></span>



| <span data-ttu-id="cad69-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cad69-139">Requirement</span></span> | <span data-ttu-id="cad69-140">Wert</span><span class="sxs-lookup"><span data-stu-id="cad69-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cad69-141">Header</span><span class="sxs-lookup"><span data-stu-id="cad69-141">Header</span></span><br/> | <dl> <span data-ttu-id="cad69-142"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="cad69-142"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cad69-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cad69-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cad69-144">Makros</span><span class="sxs-lookup"><span data-stu-id="cad69-144">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="cad69-145">D3DCAPS9</span><span class="sxs-lookup"><span data-stu-id="cad69-145">D3DCAPS9</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




