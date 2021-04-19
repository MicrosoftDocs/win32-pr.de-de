---
description: Erstellen Sie ein Vertex-Shader-Versionsnummern Token.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: D3DVS_VERSION-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373528"
---
# <a name="d3dvs_version-macro"></a><span data-ttu-id="98be2-103">D3DVS- \_ Versions Makro</span><span class="sxs-lookup"><span data-stu-id="98be2-103">D3DVS\_VERSION macro</span></span>

<span data-ttu-id="98be2-104">Erstellen Sie ein Vertex-Shader-Versionsnummern Token.</span><span class="sxs-lookup"><span data-stu-id="98be2-104">Create a vertex shader version number token.</span></span>

## <a name="syntax"></a><span data-ttu-id="98be2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98be2-105">Syntax</span></span>


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="98be2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98be2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98be2-107">*\_Wichtige*</span><span class="sxs-lookup"><span data-stu-id="98be2-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="98be2-108">Die Hauptversion des Vertex-Shaders.</span><span class="sxs-lookup"><span data-stu-id="98be2-108">The major vertex shader version.</span></span> <span data-ttu-id="98be2-109">Entsprechende Werte finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="98be2-109">See remarks for appropriate values.</span></span>

</dd> <dt>

<span data-ttu-id="98be2-110">*\_Nebenversion*</span><span class="sxs-lookup"><span data-stu-id="98be2-110">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="98be2-111">Die kleinere Scheitelpunkt-Shader-Version.</span><span class="sxs-lookup"><span data-stu-id="98be2-111">The minor vertex shader version.</span></span> <span data-ttu-id="98be2-112">Entsprechende Werte finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="98be2-112">See remarks for appropriate values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98be2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98be2-113">Return value</span></span>

<span data-ttu-id="98be2-114">Gibt einen DWORD-Wert zurück, der eine Scheitelpunkt-Shader-Version ist.</span><span class="sxs-lookup"><span data-stu-id="98be2-114">Returns a DWORD value that is a vertex shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="98be2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98be2-115">Remarks</span></span>

<span data-ttu-id="98be2-116">Versionsnummern</span><span class="sxs-lookup"><span data-stu-id="98be2-116">Version Numbers</span></span>

<span data-ttu-id="98be2-117">Die Versionsnummer ist eine Kombination aus der Hauptversion und den kleineren Scheitelpunkt-Shader-Versionsnummern.</span><span class="sxs-lookup"><span data-stu-id="98be2-117">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="98be2-118">In der Tabelle werden gültige Zahlen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98be2-118">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="98be2-119">Hauptversion</span><span class="sxs-lookup"><span data-stu-id="98be2-119">Major</span></span> | <span data-ttu-id="98be2-120">Nebenversion</span><span class="sxs-lookup"><span data-stu-id="98be2-120">Minor</span></span> | <span data-ttu-id="98be2-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="98be2-121">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="98be2-122">1</span><span class="sxs-lookup"><span data-stu-id="98be2-122">1</span></span>     | <span data-ttu-id="98be2-123">1</span><span class="sxs-lookup"><span data-stu-id="98be2-123">1</span></span>     | <span data-ttu-id="98be2-124">D3DVS- \_ Version (1, 1)</span><span class="sxs-lookup"><span data-stu-id="98be2-124">D3DVS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="98be2-125">2</span><span class="sxs-lookup"><span data-stu-id="98be2-125">2</span></span>     | <span data-ttu-id="98be2-126">0</span><span class="sxs-lookup"><span data-stu-id="98be2-126">0</span></span>     | <span data-ttu-id="98be2-127">D3DVS- \_ Version (2, 0)</span><span class="sxs-lookup"><span data-stu-id="98be2-127">D3DVS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="98be2-128">3</span><span class="sxs-lookup"><span data-stu-id="98be2-128">3</span></span>     | <span data-ttu-id="98be2-129">0</span><span class="sxs-lookup"><span data-stu-id="98be2-129">0</span></span>     | <span data-ttu-id="98be2-130">D3DVS- \_ Version (3, 0)</span><span class="sxs-lookup"><span data-stu-id="98be2-130">D3DVS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="98be2-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98be2-131">Requirements</span></span>



| <span data-ttu-id="98be2-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98be2-132">Requirement</span></span> | <span data-ttu-id="98be2-133">Wert</span><span class="sxs-lookup"><span data-stu-id="98be2-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98be2-134">Header</span><span class="sxs-lookup"><span data-stu-id="98be2-134">Header</span></span><br/> | <dl> <span data-ttu-id="98be2-135"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="98be2-135"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98be2-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98be2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98be2-137">Makros</span><span class="sxs-lookup"><span data-stu-id="98be2-137">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




