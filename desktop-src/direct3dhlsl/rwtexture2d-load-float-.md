---
title: 'RWTexture2D:: Load (int)-Funktion'
description: 'Liest Textur Daten. | RWTexture2D:: Load (int)-Funktion'
ms.assetid: AEBB9C78-BE4B-4121-93CC-EE03B9925CF0
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
ms.openlocfilehash: ab5f8d755ad4af3127a0c238defc9f1c422061bc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995566"
---
# <a name="rwtexture2dloadint-function"></a><span data-ttu-id="868e9-105">RWTexture2D:: Load (int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="868e9-105">RWTexture2D::Load(int) function</span></span>

<span data-ttu-id="868e9-106">Liest Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="868e9-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="868e9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="868e9-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="868e9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="868e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="868e9-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="868e9-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868e9-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="868e9-110">Type: **int**</span></span>

<span data-ttu-id="868e9-111">Der Speicherort der Textur.</span><span class="sxs-lookup"><span data-stu-id="868e9-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="868e9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="868e9-112">Return value</span></span>

<span data-ttu-id="868e9-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="868e9-113">Type:</span></span>

<span data-ttu-id="868e9-114">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**RWTexture2D**](sm5-object-rwtexture2d.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="868e9-114">The return type matches the type in the declaration for the [**RWTexture2D**](sm5-object-rwtexture2d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="868e9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="868e9-115">Remarks</span></span>

<span data-ttu-id="868e9-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="868e9-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="868e9-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="868e9-117">Vertex</span></span> | <span data-ttu-id="868e9-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="868e9-118">Hull</span></span> | <span data-ttu-id="868e9-119">Domain</span><span class="sxs-lookup"><span data-stu-id="868e9-119">Domain</span></span> | <span data-ttu-id="868e9-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="868e9-120">Geometry</span></span> | <span data-ttu-id="868e9-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="868e9-121">Pixel</span></span> | <span data-ttu-id="868e9-122">Compute</span><span class="sxs-lookup"><span data-stu-id="868e9-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="868e9-123">x</span><span class="sxs-lookup"><span data-stu-id="868e9-123">x</span></span>     | <span data-ttu-id="868e9-124">x</span><span class="sxs-lookup"><span data-stu-id="868e9-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="868e9-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="868e9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868e9-126">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="868e9-126">Load methods</span></span>](rwtexture2d-load.md)
</dt> </dl>

 

 




