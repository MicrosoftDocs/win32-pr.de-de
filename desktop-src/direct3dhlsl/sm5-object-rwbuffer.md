---
title: Rwbuffer
description: Ein Lese-/Schreibpuffer.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- Rwbuffer HLSL
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 765634da85fb74f2d3a3591bfe4767ccee1a80c8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312558"
---
# <a name="rwbuffer"></a><span data-ttu-id="9707c-104">Rwbuffer</span><span class="sxs-lookup"><span data-stu-id="9707c-104">RWBuffer</span></span>

<span data-ttu-id="9707c-105">Ein Lese-/Schreibpuffer.</span><span class="sxs-lookup"><span data-stu-id="9707c-105">A read/write buffer.</span></span>



| <span data-ttu-id="9707c-106">Methode</span><span class="sxs-lookup"><span data-stu-id="9707c-106">Method</span></span>                                                     | <span data-ttu-id="9707c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9707c-107">Description</span></span>                            |
|------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="9707c-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="9707c-108">**GetDimensions**</span></span>](sm5-object-rwbuffer-getdimensions.md) | <span data-ttu-id="9707c-109">Ruft die Ressourcen Dimensionen ab.</span><span class="sxs-lookup"><span data-stu-id="9707c-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="9707c-110">**Laden**</span><span class="sxs-lookup"><span data-stu-id="9707c-110">**Load**</span></span>](rwbuffer-load.md)                              | <span data-ttu-id="9707c-111">Ruft einen Wert in einem Puffer mit Lese-/Schreibzugriff ab.</span><span class="sxs-lookup"><span data-stu-id="9707c-111">Gets one value in a read-write buffer.</span></span> |
| <span data-ttu-id="9707c-112">[**KOM\[\]**](sm5-object-rwbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="9707c-112">[**Operator\[\]**](sm5-object-rwbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="9707c-113">Gibt eine Ressourcen Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="9707c-113">Returns a resource variable.</span></span>           |



 

<span data-ttu-id="9707c-114">Eine Ressourcen Variable kann auch an einen ungeordneten oder Interlocked-Vorgang übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9707c-114">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="9707c-115">**Rwbuffer** -Objekten kann die Speicher Klasse **globallycoherent** vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9707c-115">**RWBuffer** objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="9707c-116">Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können.</span><span class="sxs-lookup"><span data-stu-id="9707c-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="9707c-117">Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung eine UAV nur innerhalb der aktuellen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9707c-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="9707c-118">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="9707c-118">Minimum Shader Model</span></span>

<span data-ttu-id="9707c-119">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9707c-119">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="9707c-120">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="9707c-120">Shader Model</span></span>                                                                | <span data-ttu-id="9707c-121">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="9707c-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9707c-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="9707c-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="9707c-123">ja</span><span class="sxs-lookup"><span data-stu-id="9707c-123">yes</span></span>       |



 

<span data-ttu-id="9707c-124">Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9707c-124">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9707c-125">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="9707c-125">Vertex</span></span> | <span data-ttu-id="9707c-126">Hülle</span><span class="sxs-lookup"><span data-stu-id="9707c-126">Hull</span></span> | <span data-ttu-id="9707c-127">Domain</span><span class="sxs-lookup"><span data-stu-id="9707c-127">Domain</span></span> | <span data-ttu-id="9707c-128">Geometrie</span><span class="sxs-lookup"><span data-stu-id="9707c-128">Geometry</span></span> | <span data-ttu-id="9707c-129">Pixel</span><span class="sxs-lookup"><span data-stu-id="9707c-129">Pixel</span></span> | <span data-ttu-id="9707c-130">Compute</span><span class="sxs-lookup"><span data-stu-id="9707c-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9707c-131">x</span><span class="sxs-lookup"><span data-stu-id="9707c-131">x</span></span>     | <span data-ttu-id="9707c-132">x</span><span class="sxs-lookup"><span data-stu-id="9707c-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9707c-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9707c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9707c-134">Shader Model 5-Objekte</span><span class="sxs-lookup"><span data-stu-id="9707c-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




