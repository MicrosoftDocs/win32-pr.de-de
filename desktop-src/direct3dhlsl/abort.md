---
title: Abbruch-Funktion (corecrt \_ beenden. h)
description: Sendet eine Fehlermeldung an die Informations Warteschlange und beendet den aktuellen Draw-oder Dispatch-Befehl, der ausgeführt wird.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- Abbruch-Funktion HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982636"
---
# <a name="abort-function"></a><span data-ttu-id="a31a7-104">abort-Funktion</span><span class="sxs-lookup"><span data-stu-id="a31a7-104">abort function</span></span>

<span data-ttu-id="a31a7-105">Sendet eine Fehlermeldung an die Informations Warteschlange und beendet den aktuellen Draw-oder Dispatch-Befehl, der ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a31a7-105">Submits an error message to the information queue and terminates the current draw or dispatch call being executed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a31a7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a31a7-106">Syntax</span></span>

``` syntax
void abort(
    
);
```

## <a name="parameters"></a><span data-ttu-id="a31a7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a31a7-107">Parameters</span></span>

<dl> <dt>

 
</dt> <dd>

<span data-ttu-id="a31a7-108">Keine</span><span class="sxs-lookup"><span data-stu-id="a31a7-108">None</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a31a7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a31a7-109">Return value</span></span>

<span data-ttu-id="a31a7-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a31a7-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a31a7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a31a7-111">Remarks</span></span>

<span data-ttu-id="a31a7-112">Bei diesem Vorgang werden keine Rasterizer unterstützt, die dies nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a31a7-112">This operation does nothing on rasterizers that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="a31a7-113">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="a31a7-113">Minimum Shader Model</span></span>

<span data-ttu-id="a31a7-114">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a31a7-114">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a31a7-115">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="a31a7-115">Shader Model</span></span>                                                        | <span data-ttu-id="a31a7-116">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="a31a7-116">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="a31a7-117">Shader Model 4 (DirectX HLSL) oder höher.</span><span class="sxs-lookup"><span data-stu-id="a31a7-117">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a31a7-118">ja</span><span class="sxs-lookup"><span data-stu-id="a31a7-118">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="a31a7-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a31a7-119">Requirements</span></span>



| <span data-ttu-id="a31a7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a31a7-120">Requirement</span></span> | <span data-ttu-id="a31a7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a31a7-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31a7-122">Header</span><span class="sxs-lookup"><span data-stu-id="a31a7-122">Header</span></span><br/> | <dl> <span data-ttu-id="a31a7-123"><dt>Corecrt \_ beenden. h</dt></span><span class="sxs-lookup"><span data-stu-id="a31a7-123"><dt>Corecrt\_terminate.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a31a7-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a31a7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a31a7-125">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a31a7-125">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





