---
title: " Error-Direktive"
description: Eine Präprozessordirektive, die compilerzeitfehlermeldungen erzeugt.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- Fehler-Direktive HLSL
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389153"
---
# <a name="error-directive"></a><span data-ttu-id="1abc5-104">\#Error-Direktive</span><span class="sxs-lookup"><span data-stu-id="1abc5-104">\#error Directive</span></span>

<span data-ttu-id="1abc5-105">Eine Präprozessordirektive, die compilerzeitfehlermeldungen erzeugt.</span><span class="sxs-lookup"><span data-stu-id="1abc5-105">Preprocessor directive that produces compiler-time error messages.</span></span>



| <span data-ttu-id="1abc5-106">\#Fehler *Token-Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="1abc5-106">\#error *token-string*</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="1abc5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1abc5-107">Parameters</span></span>



| <span data-ttu-id="1abc5-108">Element</span><span class="sxs-lookup"><span data-stu-id="1abc5-108">Item</span></span>                                                                                    | <span data-ttu-id="1abc5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1abc5-109">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1abc5-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*Tokenzeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="1abc5-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="1abc5-111">Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="1abc5-111">Error message.</span></span> <span data-ttu-id="1abc5-112">Dieser Parameter besteht aus einer Reihe von Token, wie z. b. Schlüsselwörtern, Konstanten oder Complete-Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="1abc5-112">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="1abc5-113">Die Tokenzeichenfolge unterliegt der Makro Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="1abc5-113">The token string is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="1abc5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1abc5-114">Remarks</span></span>

<span data-ttu-id="1abc5-115">\#Fehler Anweisungen sind besonders nützlich, wenn Sie Programmierer-Inkonsistenzen erkennen und Einschränkungen während der Vorverarbeitung verletzen.</span><span class="sxs-lookup"><span data-stu-id="1abc5-115">\#error directives are most useful for detecting programmer inconsistencies and violation of constraints during preprocessing.</span></span> <span data-ttu-id="1abc5-116">Wenn eine \# Fehler Anweisung auftritt, wird die Kompilierung beendet.</span><span class="sxs-lookup"><span data-stu-id="1abc5-116">When an \#error directive is encountered, compilation terminates.</span></span>

## <a name="examples"></a><span data-ttu-id="1abc5-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1abc5-117">Examples</span></span>

<span data-ttu-id="1abc5-118">Im folgenden Beispiel wird die Fehler Verarbeitung während der Vorverarbeitung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1abc5-118">The following example demonstrates error processing during preprocessing.</span></span>


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a><span data-ttu-id="1abc5-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1abc5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1abc5-120">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1abc5-120">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





