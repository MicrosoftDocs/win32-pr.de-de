---
title: "\"errorf\"-Funktion"
description: Sendet eine Fehlermeldung an die Informations Warteschlange.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- "\"errorf\"-Funktion HLSL"
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76c8fbcd9b6cb15dbbb735296a3aada8f5e568cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037850"
---
# <a name="errorf-function"></a><span data-ttu-id="73864-104">"errorf"-Funktion</span><span class="sxs-lookup"><span data-stu-id="73864-104">errorf function</span></span>

<span data-ttu-id="73864-105">Sendet eine Fehlermeldung an die Informations Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="73864-105">Submits an error message to the information queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="73864-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="73864-106">Syntax</span></span>

``` syntax
void errorf(
   string format,
    argument ...
);
```

## <a name="parameters"></a><span data-ttu-id="73864-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="73864-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73864-108">*format*</span><span class="sxs-lookup"><span data-stu-id="73864-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="73864-109">Die Formatzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="73864-109">The format string.</span></span>

</dd> <dt>

<span data-ttu-id="73864-110">*Argument...*</span><span class="sxs-lookup"><span data-stu-id="73864-110">*argument ...*</span></span> 
</dt> <dd>

<span data-ttu-id="73864-111">Optionale Argumente.</span><span class="sxs-lookup"><span data-stu-id="73864-111">Optional arguments.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73864-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73864-112">Return value</span></span>

<span data-ttu-id="73864-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="73864-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73864-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73864-114">Remarks</span></span>

<span data-ttu-id="73864-115">Bei Geräten, die den Vorgang nicht unterstützen, wird dieser Vorgang nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="73864-115">This operation does nothing on devices that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="73864-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="73864-116">Minimum Shader Model</span></span>

<span data-ttu-id="73864-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="73864-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="73864-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="73864-118">Shader Model</span></span>                                                        | <span data-ttu-id="73864-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="73864-119">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="73864-120">Shader Model 4 (DirectX HLSL) oder höher.</span><span class="sxs-lookup"><span data-stu-id="73864-120">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="73864-121">ja</span><span class="sxs-lookup"><span data-stu-id="73864-121">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="73864-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="73864-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73864-123">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="73864-123">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




