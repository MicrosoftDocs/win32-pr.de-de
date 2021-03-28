---
title: printf-Funktion
description: Übermittelt eine benutzerdefinierte shadernachricht an die Informations Warteschlange.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- printf-Funktion HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74492cc613e22f335eace684300f0380e5751a95
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948254"
---
# <a name="printf-function"></a><span data-ttu-id="b70ae-104">printf-Funktion</span><span class="sxs-lookup"><span data-stu-id="b70ae-104">printf function</span></span>

<span data-ttu-id="b70ae-105">Übermittelt eine benutzerdefinierte shadernachricht an die Informations Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="b70ae-105">Submits a custom shader message to the information queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="b70ae-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b70ae-106">Syntax</span></span>

``` syntax
void printf(
   string format,
    argument ...
);
```

## <a name="parameters"></a><span data-ttu-id="b70ae-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b70ae-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b70ae-108">*format*</span><span class="sxs-lookup"><span data-stu-id="b70ae-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="b70ae-109">Die Formatzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b70ae-109">The format string.</span></span>

</dd> <dt>

<span data-ttu-id="b70ae-110">*Argument...*</span><span class="sxs-lookup"><span data-stu-id="b70ae-110">*argument ...*</span></span> 
</dt> <dd>

<span data-ttu-id="b70ae-111">Optionale Argumente.</span><span class="sxs-lookup"><span data-stu-id="b70ae-111">Optional arguments.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b70ae-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b70ae-112">Return value</span></span>

<span data-ttu-id="b70ae-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b70ae-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b70ae-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b70ae-114">Remarks</span></span>

<span data-ttu-id="b70ae-115">Bei Geräten, die den Vorgang nicht unterstützen, wird dieser Vorgang nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b70ae-115">This operation does nothing on devices that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="b70ae-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="b70ae-116">Minimum Shader Model</span></span>

<span data-ttu-id="b70ae-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b70ae-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b70ae-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b70ae-118">Shader Model</span></span>                                                        | <span data-ttu-id="b70ae-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b70ae-119">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="b70ae-120">Shader Model 4 (DirectX HLSL) oder höher.</span><span class="sxs-lookup"><span data-stu-id="b70ae-120">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b70ae-121">ja</span><span class="sxs-lookup"><span data-stu-id="b70ae-121">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b70ae-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b70ae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b70ae-123">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="b70ae-123">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




