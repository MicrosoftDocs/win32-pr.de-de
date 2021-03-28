---
title: 'Structuredbuffer:: Load (int)-Funktion'
description: 'Liest Puffer Daten. | Structuredbuffer:: Load (int)-Funktion'
ms.assetid: ef08d360-0494-49f7-9481-cb802e14aeee
keywords:
- Ladefunktion HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 883d483044a27e35848457e70e22888dd5ad6320
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981897"
---
# <a name="structuredbufferloadint-function"></a><span data-ttu-id="36e17-105">Structuredbuffer:: Load (int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="36e17-105">StructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="36e17-106">Liest Puffer Daten.</span><span class="sxs-lookup"><span data-stu-id="36e17-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="36e17-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="36e17-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="36e17-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="36e17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36e17-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36e17-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36e17-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="36e17-110">Type: **int**</span></span>

<span data-ttu-id="36e17-111">Der Speicherort des Puffers.</span><span class="sxs-lookup"><span data-stu-id="36e17-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36e17-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36e17-112">Return value</span></span>

<span data-ttu-id="36e17-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="36e17-113">Type:</span></span>

<span data-ttu-id="36e17-114">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**structuredbuffer**](sm5-object-structuredbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="36e17-114">The return type matches the type in the declaration for the [**StructuredBuffer**](sm5-object-structuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="36e17-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36e17-115">Remarks</span></span>

<span data-ttu-id="36e17-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="36e17-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="36e17-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="36e17-117">Vertex</span></span> | <span data-ttu-id="36e17-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="36e17-118">Hull</span></span> | <span data-ttu-id="36e17-119">Domain</span><span class="sxs-lookup"><span data-stu-id="36e17-119">Domain</span></span> | <span data-ttu-id="36e17-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="36e17-120">Geometry</span></span> | <span data-ttu-id="36e17-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="36e17-121">Pixel</span></span> | <span data-ttu-id="36e17-122">Compute</span><span class="sxs-lookup"><span data-stu-id="36e17-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="36e17-123">x</span><span class="sxs-lookup"><span data-stu-id="36e17-123">x</span></span>     | <span data-ttu-id="36e17-124">x</span><span class="sxs-lookup"><span data-stu-id="36e17-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="36e17-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="36e17-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36e17-126">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="36e17-126">Load methods</span></span>](structuredbuffer-load.md)
</dt> </dl>

 

 




