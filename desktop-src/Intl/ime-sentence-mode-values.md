---
description: Diese Werte werden mit den Funktionen "immgetdeversionstatus" und "immsetconfiguration" verwendet.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Werte für den IME-Satzmodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2fb9d25b2c3b1828e8c36aca554468f6447af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216237"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="7f86b-103">Werte für den IME-Satzmodus</span><span class="sxs-lookup"><span data-stu-id="7f86b-103">IME Sentence Mode Values</span></span>

<span data-ttu-id="7f86b-104">Diese Werte werden mit den Funktionen " [**immgetdeversionstatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) " und " [**immsetconfiguration**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f86b-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="7f86b-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="7f86b-105">Constant</span></span>                  | <span data-ttu-id="7f86b-106">Definition</span><span class="sxs-lookup"><span data-stu-id="7f86b-106">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="7f86b-107">IME- \_ smode \_ automatisch</span><span class="sxs-lookup"><span data-stu-id="7f86b-107">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="7f86b-108">Der IME führt die Konvertierungs Verarbeitung im automatischen Modus aus.</span><span class="sxs-lookup"><span data-stu-id="7f86b-108">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="7f86b-109">IME \_ smode \_ None</span><span class="sxs-lookup"><span data-stu-id="7f86b-109">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="7f86b-110">Keine Informationen für einen Satz.</span><span class="sxs-lookup"><span data-stu-id="7f86b-110">No information for sentence.</span></span>                                               |
| <span data-ttu-id="7f86b-111">IME \_ smode \_ phravervorhersage</span><span class="sxs-lookup"><span data-stu-id="7f86b-111">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="7f86b-112">Der IME verwendet Ausdrucks Informationen, um das nächste Zeichen vorherzusagen.</span><span class="sxs-lookup"><span data-stu-id="7f86b-112">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="7f86b-113">IME \_ smode \_ pluralclause</span><span class="sxs-lookup"><span data-stu-id="7f86b-113">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="7f86b-114">Der IME verwendet die Plural-klauselinformationen, um die Konvertierungs Verarbeitung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7f86b-114">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="7f86b-115">IME \_ smode \_ singleconvert</span><span class="sxs-lookup"><span data-stu-id="7f86b-115">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="7f86b-116">Der IME führt die Konvertierungs Verarbeitung im Einzelzeichen Modus aus.</span><span class="sxs-lookup"><span data-stu-id="7f86b-116">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="7f86b-117">IME- \_ smode- \_ Konversation</span><span class="sxs-lookup"><span data-stu-id="7f86b-117">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="7f86b-118">Der IME verwendet den Konversationsmodus.</span><span class="sxs-lookup"><span data-stu-id="7f86b-118">The IME uses conversation mode.</span></span> <span data-ttu-id="7f86b-119">Dies ist nützlich für Chat Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="7f86b-119">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="7f86b-120">Bits 16 bis 31 sind für die IME-Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="7f86b-120">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



