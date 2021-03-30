---
title: DEF-pragma-Direktive
description: Pragma-Direktive, die manuell ein Gleit Komma-Shader-Register zugeordnet.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- DEF-pragma-Direktive HLSL
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992911"
---
# <a name="def-pragma-directive"></a><span data-ttu-id="1acf8-104">DEF-pragma-Direktive</span><span class="sxs-lookup"><span data-stu-id="1acf8-104">def pragma Directive</span></span>

<span data-ttu-id="1acf8-105">Pragma-Direktive, die manuell ein Gleit Komma-Shader-Register zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1acf8-105">Pragma directive that manually allocates a floating-point shader register.</span></span>



| <span data-ttu-id="1acf8-106">\#pragma DEF ( *target*, *Register*, *Wert1*, *Wert2*,*val3*, *val4* )</span><span class="sxs-lookup"><span data-stu-id="1acf8-106">\#pragma def( *target*, *register*, *val1*, *val2*,*val3*, *val4* )</span></span> |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="1acf8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1acf8-107">Parameters</span></span>



| <span data-ttu-id="1acf8-108">Element</span><span class="sxs-lookup"><span data-stu-id="1acf8-108">Item</span></span>                                                                        | <span data-ttu-id="1acf8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1acf8-109">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="1acf8-110"><span id="target"></span><span id="TARGET"></span>*Spar*</span><span class="sxs-lookup"><span data-stu-id="1acf8-110"><span id="target"></span><span id="TARGET"></span>*target*</span></span><br/>       | <span data-ttu-id="1acf8-111">Das Ziel, das das zuzuordnende Register enthält.</span><span class="sxs-lookup"><span data-stu-id="1acf8-111">Target that contains the register to allocate.</span></span> <br/>                  |
| <span data-ttu-id="1acf8-112"><span id="register"></span><span id="REGISTER"></span>*sich*</span><span class="sxs-lookup"><span data-stu-id="1acf8-112"><span id="register"></span><span id="REGISTER"></span>*register*</span></span><br/> | <span data-ttu-id="1acf8-113">Die zuzuordnende Gleit Komma-Shader-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="1acf8-113">Floating-point shader register to allocate.</span></span> <br/>                     |
| <span data-ttu-id="1acf8-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span><span class="sxs-lookup"><span data-stu-id="1acf8-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span></span><br/>             | <span data-ttu-id="1acf8-115">Das erste Byte des Werts, der dem angegebenen Register zuzuordnen ist.</span><span class="sxs-lookup"><span data-stu-id="1acf8-115">First byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="1acf8-116"><span id="val1"></span><span id="VAL1"></span>*Wert1*</span><span class="sxs-lookup"><span data-stu-id="1acf8-116"><span id="val1"></span><span id="VAL1"></span>*val1*</span></span><br/>             | <span data-ttu-id="1acf8-117">Zweites Byte des Werts, der dem angegebenen Register zuzuordnen ist.</span><span class="sxs-lookup"><span data-stu-id="1acf8-117">Second byte of the value to allocate to the specified register.</span></span> <br/> |
| <span data-ttu-id="1acf8-118"><span id="val2"></span><span id="VAL2"></span>*Wert2*</span><span class="sxs-lookup"><span data-stu-id="1acf8-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span></span><br/>             | <span data-ttu-id="1acf8-119">Drittes Byte des Werts, der dem angegebenen Register zuzuordnen ist.</span><span class="sxs-lookup"><span data-stu-id="1acf8-119">Third byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="1acf8-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span><span class="sxs-lookup"><span data-stu-id="1acf8-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span></span><br/>             | <span data-ttu-id="1acf8-121">Viertes Byte des Werts, der dem angegebenen Register zuzuordnen ist.</span><span class="sxs-lookup"><span data-stu-id="1acf8-121">Fourth byte of the value to allocate to the specified register.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="1acf8-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1acf8-122">Remarks</span></span>

<span data-ttu-id="1acf8-123">Mithilfe des DEF-Pragmas kann ein Entwickler ein Gleit Komma-Shader-Register mit dem angegebenen Wert vorab ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="1acf8-123">The def pragma allows a developer to prefill a floating-point shader register with the specified value.</span></span> <span data-ttu-id="1acf8-124">Dieses Pragma wird nur selten verwendet.</span><span class="sxs-lookup"><span data-stu-id="1acf8-124">This pragma is infrequently used.</span></span>

## <a name="see-also"></a><span data-ttu-id="1acf8-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1acf8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1acf8-126">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1acf8-126">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="1acf8-127">\#pragma-Direktive (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1acf8-127">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





