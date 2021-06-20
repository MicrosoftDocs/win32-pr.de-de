---
description: Überprüfen Sie die Liste der ImE-Konvertierungsmoduswerte (Input Method Editor). Diese Werte werden mit den Funktionen ImmGetConversionStatus und ImmSetConversionStatus verwendet.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Werte des IME-Konvertierungsmodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c52bc2f8f6f9fc87df48a15c66ce24b33e51742
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406753"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="71091-104">Werte des IME-Konvertierungsmodus</span><span class="sxs-lookup"><span data-stu-id="71091-104">IME Conversion Mode Values</span></span>

<span data-ttu-id="71091-105">Diese Werte werden mit den [**Funktionen ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) und [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) verwendet.</span><span class="sxs-lookup"><span data-stu-id="71091-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="71091-106">bit</span><span class="sxs-lookup"><span data-stu-id="71091-106">Bit</span></span>                      | <span data-ttu-id="71091-107">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="71091-107">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="71091-108">IME \_ CMODE \_ ALPHANUMERIC</span><span class="sxs-lookup"><span data-stu-id="71091-108">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="71091-109">Alphanumerischer Eingabemodus.</span><span class="sxs-lookup"><span data-stu-id="71091-109">Alphanumeric input mode.</span></span> <span data-ttu-id="71091-110">Dies ist die Standardeinstellung, die als 0x0000.</span><span class="sxs-lookup"><span data-stu-id="71091-110">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="71091-111">IME \_ CMODE \_ CHARCODE</span><span class="sxs-lookup"><span data-stu-id="71091-111">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="71091-112">Legen Sie auf 1 fest, wenn der Zeichencodeeingabemodus ist. 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="71091-112">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="71091-113">IME \_ CMODE \_ EUDC</span><span class="sxs-lookup"><span data-stu-id="71091-113">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="71091-114">Legen Sie auf 1 fest, wenn der EUDC-Konvertierungsmodus ist. 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="71091-114">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="71091-115">IME \_ CMODE \_ FIXED</span><span class="sxs-lookup"><span data-stu-id="71091-115">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="71091-116">**Windows Me/98, Windows 2000, Windows XP:** Legen Sie auf 1 fest, wenn der Konvertierungsmodus fest ist. 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="71091-116">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="71091-117">IME \_ CMODE \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="71091-117">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="71091-118">Legen Sie auf 1 fest, wenn der Vollformmodus aktiviert ist. 0, wenn halber Formmodus.</span><span class="sxs-lookup"><span data-stu-id="71091-118">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="71091-119">IME \_ CMODE \_ HANJACONVERT</span><span class="sxs-lookup"><span data-stu-id="71091-119">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="71091-120">Legen Sie auf 1 fest, wenn der HANJA-Konvertierungsmodus aktiviert ist. 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="71091-120">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="71091-121">IME \_ CMODE \_ KATAKANA</span><span class="sxs-lookup"><span data-stu-id="71091-121">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="71091-122">Legen Sie auf 1 fest, wenn der KATAKANA-Modus ist. 0, wenn HIRAGANA-Modus.</span><span class="sxs-lookup"><span data-stu-id="71091-122">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="71091-123">IME \_ CMODE \_ NATIVE</span><span class="sxs-lookup"><span data-stu-id="71091-123">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="71091-124">Legen Sie auf 1 fest, wenn der MODUS NATIV ist. 0, wenn der ALPHANUMERIC-Modus.</span><span class="sxs-lookup"><span data-stu-id="71091-124">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="71091-125">IME \_ CMODE \_ NOCONVERSION</span><span class="sxs-lookup"><span data-stu-id="71091-125">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="71091-126">Legen Sie auf 1 fest, um die Verarbeitung von Konvertierungen durch IME zu verhindern. 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="71091-126">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="71091-127">IME \_ CMODE \_ ROMAN</span><span class="sxs-lookup"><span data-stu-id="71091-127">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="71091-128">Legen Sie auf 1 fest, wenn der EINGABEMODUS FÜR ROMAN festgelegt ist. 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="71091-128">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="71091-129">IME \_ CMODE \_ SOFTKBD</span><span class="sxs-lookup"><span data-stu-id="71091-129">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="71091-130">Legen Sie auf 1 fest, wenn der Softtastaturmodus aktiviert ist. 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="71091-130">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="71091-131">\_IME-CMODE-SYMBOL \_</span><span class="sxs-lookup"><span data-stu-id="71091-131">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="71091-132">Legen Sie auf 1 fest, wenn der SYMBOL-Konvertierungsmodus aktiviert ist. 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="71091-132">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="71091-133">Alle anderen Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="71091-133">All other bits are reserved.</span></span>

 

 



