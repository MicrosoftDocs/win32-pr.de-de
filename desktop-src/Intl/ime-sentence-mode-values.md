---
description: Überprüfen Sie die Liste der Ime-Satzmoduswerte (Input Method Editor). Diese Werte werden mit den Funktionen ImmGetConversionStatus und ImmSetConversionStatus verwendet.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: IME-Satzmoduswerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 285636ab097bd536e5bd0e4e1869f12c648c3cbb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406763"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="a53b9-104">IME-Satzmoduswerte</span><span class="sxs-lookup"><span data-stu-id="a53b9-104">IME Sentence Mode Values</span></span>

<span data-ttu-id="a53b9-105">Diese Werte werden mit den Funktionen [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) und [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a53b9-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="a53b9-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="a53b9-106">Constant</span></span>                  | <span data-ttu-id="a53b9-107">Definition</span><span class="sxs-lookup"><span data-stu-id="a53b9-107">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="a53b9-108">IME \_ SMODE \_ AUTOMATIC</span><span class="sxs-lookup"><span data-stu-id="a53b9-108">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="a53b9-109">Die IME führt die Konvertierungsverarbeitung im automatischen Modus durch.</span><span class="sxs-lookup"><span data-stu-id="a53b9-109">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="a53b9-110">IME \_ SMODE \_ NONE</span><span class="sxs-lookup"><span data-stu-id="a53b9-110">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="a53b9-111">Keine Informationen für Satz.</span><span class="sxs-lookup"><span data-stu-id="a53b9-111">No information for sentence.</span></span>                                               |
| <span data-ttu-id="a53b9-112">IME \_ SMODE \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="a53b9-112">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="a53b9-113">Die IME verwendet Ausdrucksinformationen, um das nächste Zeichen vorherzusagen.</span><span class="sxs-lookup"><span data-stu-id="a53b9-113">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="a53b9-114">IME \_ SMODE \_ PLURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="a53b9-114">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="a53b9-115">Die IME verwendet Pluralklauselinformationen, um die Konvertierungsverarbeitung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="a53b9-115">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="a53b9-116">IME \_ SMODE \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="a53b9-116">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="a53b9-117">Die IME führt die Konvertierungsverarbeitung im Einzelzeichenmodus durch.</span><span class="sxs-lookup"><span data-stu-id="a53b9-117">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="a53b9-118">IME \_ SMODE \_ CONVERSATION</span><span class="sxs-lookup"><span data-stu-id="a53b9-118">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="a53b9-119">Die IME verwendet den Konversationsmodus.</span><span class="sxs-lookup"><span data-stu-id="a53b9-119">The IME uses conversation mode.</span></span> <span data-ttu-id="a53b9-120">Dies ist nützlich für Chatanwendungen.</span><span class="sxs-lookup"><span data-stu-id="a53b9-120">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="a53b9-121">Die Bits 16 bis 31 sind für die Ime-Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="a53b9-121">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



