---
title: Message-pragma-Direktive
description: Pragma-Direktive, die compilerzeitnachrichten erzeugt.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- Message-pragma-Direktive HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f342f4a139320e4beb821f32662da72785ab751c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718924"
---
# <a name="message-pragma-directive"></a><span data-ttu-id="f8108-104">Message-pragma-Direktive</span><span class="sxs-lookup"><span data-stu-id="f8108-104">message pragma Directive</span></span>

<span data-ttu-id="f8108-105">Pragma-Direktive, die compilerzeitnachrichten erzeugt.</span><span class="sxs-lookup"><span data-stu-id="f8108-105">Pragma directive that produces compiler-time messages.</span></span>



| <span data-ttu-id="f8108-106">\#pragma-Meldung "*Token-String*"</span><span class="sxs-lookup"><span data-stu-id="f8108-106">\#pragma message "*token-string*"</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="f8108-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8108-107">Parameters</span></span>



| <span data-ttu-id="f8108-108">Element</span><span class="sxs-lookup"><span data-stu-id="f8108-108">Item</span></span>                                                                                    | <span data-ttu-id="f8108-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8108-109">Description</span></span>                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="f8108-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*Tokenzeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="f8108-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="f8108-111">Compilernachricht.</span><span class="sxs-lookup"><span data-stu-id="f8108-111">Compiler message.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="f8108-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8108-112">Examples</span></span>

<span data-ttu-id="f8108-113">Im folgenden Beispiel wird die Nachrichtenverarbeitung während der Vorverarbeitung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f8108-113">The following example demonstrates message processing during preprocessing.</span></span>


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a><span data-ttu-id="f8108-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f8108-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8108-115">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8108-115">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="f8108-116">\#pragma-Direktive (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8108-116">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





