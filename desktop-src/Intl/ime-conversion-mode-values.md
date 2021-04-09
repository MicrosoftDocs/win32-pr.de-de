---
description: Diese Werte werden mit den Funktionen "immgetdeversionstatus" und "immsetconfiguration" verwendet.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Werte des IME-Konvertierungsmodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59b9f1a8d5015e78a5249d3499fc55e1a94d941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129740"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="200e2-103">Werte des IME-Konvertierungsmodus</span><span class="sxs-lookup"><span data-stu-id="200e2-103">IME Conversion Mode Values</span></span>

<span data-ttu-id="200e2-104">Diese Werte werden mit den Funktionen " [**immgetdeversionstatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) " und " [**immsetconfiguration**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="200e2-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="200e2-105">bit</span><span class="sxs-lookup"><span data-stu-id="200e2-105">Bit</span></span>                      | <span data-ttu-id="200e2-106">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="200e2-106">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="200e2-107">\_alphanumerischer IME-cmode-Wert \_</span><span class="sxs-lookup"><span data-stu-id="200e2-107">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="200e2-108">Alphanumerischer Eingabemodus.</span><span class="sxs-lookup"><span data-stu-id="200e2-108">Alphanumeric input mode.</span></span> <span data-ttu-id="200e2-109">Dies ist die Standardeinstellung, die als 0x0000 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="200e2-109">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="200e2-110">IME- \_ cmode- \_ CharCode</span><span class="sxs-lookup"><span data-stu-id="200e2-110">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="200e2-111">Auf 1 festgelegt, wenn Zeichencode Eingabemodus; 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="200e2-111">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="200e2-112">IME- \_ cmode- \_ EUDC</span><span class="sxs-lookup"><span data-stu-id="200e2-112">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="200e2-113">Auf 1 festgelegt, wenn EUDC-Konvertierungsmodus; 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="200e2-113">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="200e2-114">IME- \_ cmode- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="200e2-114">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="200e2-115">**Windows Me/98, Windows 2000, Windows XP:** Auf 1 festgelegt, wenn fester Konvertierungsmodus; 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="200e2-115">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="200e2-116">IME \_ cmode \_ fullshape</span><span class="sxs-lookup"><span data-stu-id="200e2-116">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="200e2-117">Auf 1 festgelegt, wenn vollständiger Shape-Modus; 0 (null), wenn Halbform Modus.</span><span class="sxs-lookup"><span data-stu-id="200e2-117">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="200e2-118">IME- \_ cmode- \_ hanjaconvert</span><span class="sxs-lookup"><span data-stu-id="200e2-118">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="200e2-119">Auf 1 festgelegt, wenn der Hanja-Konvertierungsmodus. 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="200e2-119">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="200e2-120">IME- \_ cmode- \_ Katakana</span><span class="sxs-lookup"><span data-stu-id="200e2-120">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="200e2-121">Auf 1 festgelegt, wenn Katakana-Modus; 0, wenn der Hiragana-Modus ist.</span><span class="sxs-lookup"><span data-stu-id="200e2-121">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="200e2-122">IME \_ cmode \_ Native</span><span class="sxs-lookup"><span data-stu-id="200e2-122">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="200e2-123">Auf 1 festgelegt, wenn der einheitliche Modus ist; 0 (null), wenn der alphanumerische Modus ist.</span><span class="sxs-lookup"><span data-stu-id="200e2-123">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="200e2-124">IME \_ cmode- \_ noconversion</span><span class="sxs-lookup"><span data-stu-id="200e2-124">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="200e2-125">Auf 1 festgelegt, um die Verarbeitung von Konvertierungen durch IME zu verhindern. 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="200e2-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="200e2-126">IME \_ cmode- \_ Roman</span><span class="sxs-lookup"><span data-stu-id="200e2-126">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="200e2-127">Auf 1 festgelegt, wenn der römische Eingabemodus; 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="200e2-127">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="200e2-128">IME \_ cmode- \_ Software</span><span class="sxs-lookup"><span data-stu-id="200e2-128">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="200e2-129">Auf 1 festgelegt, wenn weicher Tastaturmodus 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="200e2-129">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="200e2-130">IME- \_ cmode- \_ Symbol</span><span class="sxs-lookup"><span data-stu-id="200e2-130">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="200e2-131">Auf 1 festgelegt, wenn der Modus für die Symbol Konvertierung 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="200e2-131">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="200e2-132">Alle anderen Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="200e2-132">All other bits are reserved.</span></span>

 

 



