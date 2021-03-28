---
title: " pragma-Direktive"
description: Eine Präprozessordirektive, die Computer spezifische oder betriebssystemspezifische Features bereitstellt und gleichzeitig die Gesamt Kompatibilität mit den Programmiersprachen C und C++ beibehält.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- pragma-Direktive HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037986"
---
# <a name="pragma-directive"></a><span data-ttu-id="3486f-104">\#pragma-Direktive</span><span class="sxs-lookup"><span data-stu-id="3486f-104">\#pragma Directive</span></span>

<span data-ttu-id="3486f-105">Eine Präprozessordirektive, die Computer spezifische oder betriebssystemspezifische Features bereitstellt und gleichzeitig die Gesamt Kompatibilität mit den Programmiersprachen C und C++ beibehält.</span><span class="sxs-lookup"><span data-stu-id="3486f-105">Preprocessor directive that provides machine-specific or operating system-specific features while retaining overall compatibility with the C and C++ languages.</span></span>



| <span data-ttu-id="3486f-106">\#Pragma *-Token-Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="3486f-106">\#pragma *token-string*</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="3486f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3486f-107">Parameters</span></span>



| <span data-ttu-id="3486f-108">Element</span><span class="sxs-lookup"><span data-stu-id="3486f-108">Item</span></span>                                                                                    | <span data-ttu-id="3486f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3486f-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3486f-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*Tokenzeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="3486f-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="3486f-111">Eine Reihe von Zeichen, die eine bestimmte Compileranweisung und Argumente enthält.</span><span class="sxs-lookup"><span data-stu-id="3486f-111">Series of characters that gives a specific compiler instruction and arguments.</span></span> <span data-ttu-id="3486f-112">Dieser Parameter unterliegt der Makro Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="3486f-112">This parameter is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3486f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3486f-113">Remarks</span></span>

<span data-ttu-id="3486f-114">Wenn der Compiler ein Pragma findet, das er nicht erkennt, gibt er eine Warnung aus, die Kompilierung wird jedoch fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="3486f-114">If the compiler finds a pragma it does not recognize, it issues a warning, but compilation continues.</span></span>

<span data-ttu-id="3486f-115">Der HLSL-Compiler erkennt die folgenden Pragmas:</span><span class="sxs-lookup"><span data-stu-id="3486f-115">The HLSL compiler recognizes the following pragmas:</span></span>

-   [<span data-ttu-id="3486f-116">auflösenden</span><span class="sxs-lookup"><span data-stu-id="3486f-116">def</span></span>](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [<span data-ttu-id="3486f-117">Nachricht</span><span class="sxs-lookup"><span data-stu-id="3486f-117">message</span></span>](message-pragma-directive--directx-hlsl-.md)
-   [<span data-ttu-id="3486f-118">Paket \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="3486f-118">pack\_matrix</span></span>](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [<span data-ttu-id="3486f-119">warning</span><span class="sxs-lookup"><span data-stu-id="3486f-119">warning</span></span>](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a><span data-ttu-id="3486f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3486f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3486f-121">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3486f-121">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





