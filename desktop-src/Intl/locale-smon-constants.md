---
description: Gebiets Schema- \_ smon- \* Konstanten
ms.assetid: df7f026b-2f2d-420f-8a14-656734409835
title: LOCALE_SMON *-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932888360cc81e08a1cff1f45082b5fc1b91ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343776"
---
# <a name="locale_smon-constants"></a><span data-ttu-id="4bf82-103">Gebiets Schema- \_ smon- \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="4bf82-103">LOCALE\_SMON\* Constants</span></span>

<span data-ttu-id="4bf82-104">In diesem Thema werden die \_ von NLS verwendeten Gebiets Schema-smon- \* Konstanten zum Darstellen von Währungswerten definiert.</span><span class="sxs-lookup"><span data-stu-id="4bf82-104">This topic defines the LOCALE\_SMON\* constants used by NLS in representing monetary values.</span></span>



| <span data-ttu-id="4bf82-105">Wert</span><span class="sxs-lookup"><span data-stu-id="4bf82-105">Value</span></span>                   | <span data-ttu-id="4bf82-106">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4bf82-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf82-107">\_Gebiets Schema smondecimalsep</span><span class="sxs-lookup"><span data-stu-id="4bf82-107">LOCALE\_SMONDECIMALSEP</span></span>  | <span data-ttu-id="4bf82-108">Als zimales Dezimaltrennzeichen verwendete Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4bf82-108">Character(s) used as the monetary decimal separator.</span></span> <span data-ttu-id="4bf82-109">Die maximal zulässige Anzahl von Zeichen für diese Zeichenfolge ist vier, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="4bf82-109">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="4bf82-110">Wenn z. b. ein Währungsbetrag als "$3,40" angezeigt wird, so wie "drei Dollar und 40 Cent" im USA angezeigt wird, ist das Dezimaltrennzeichen ".".</span><span class="sxs-lookup"><span data-stu-id="4bf82-110">For example, if a monetary amount is displayed as "$3.40", just as "three dollars and forty cents" is displayed in the United States, then the monetary decimal separator is ".".</span></span>                                                                                                                                             |
| <span data-ttu-id="4bf82-111">Gebiets Schema- \_ smongruppierung</span><span class="sxs-lookup"><span data-stu-id="4bf82-111">LOCALE\_SMONGROUPING</span></span>    | <span data-ttu-id="4bf82-112">Größen für jede Gruppe von monetären Ziffern links vom Dezimaltrennzeichen.</span><span class="sxs-lookup"><span data-stu-id="4bf82-112">Sizes for each group of monetary digits to the left of the decimal.</span></span> <span data-ttu-id="4bf82-113">Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist zehn, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="4bf82-113">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="4bf82-114">Für jede Gruppe ist eine explizite Größe erforderlich, und die Größen werden durch Semikolons getrennt.</span><span class="sxs-lookup"><span data-stu-id="4bf82-114">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="4bf82-115">Wenn der letzte Wert 0 ist, wird der vorangehende Wert wiederholt.</span><span class="sxs-lookup"><span data-stu-id="4bf82-115">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="4bf82-116">Wenn Sie z. b. Tausende gruppieren möchten, geben Sie 3; 0 an.</span><span class="sxs-lookup"><span data-stu-id="4bf82-116">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="4bf82-117">Indic-Sprachen gruppieren die ersten tausend und Gruppieren dann nach Hunderten.</span><span class="sxs-lookup"><span data-stu-id="4bf82-117">Indic languages group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="4bf82-118">Beispielsweise ist der Wert 12, 34, 56789 durch 3; 2; 0 (null) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4bf82-118">For example 12,34,56,789 is represented by 3;2;0.</span></span> |
| <span data-ttu-id="4bf82-119">\_Gebiets Schema smontausendandsep</span><span class="sxs-lookup"><span data-stu-id="4bf82-119">LOCALE\_SMONTHOUSANDSEP</span></span> | <span data-ttu-id="4bf82-120">Zeichen, die als Währungs Trennzeichen zwischen Ziffern Gruppen Links vom Dezimaltrennzeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bf82-120">Character(s) used as the monetary separator between groups of digits to the left of the decimal.</span></span> <span data-ttu-id="4bf82-121">Die maximal zulässige Anzahl von Zeichen für diese Zeichenfolge ist vier, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="4bf82-121">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="4bf82-122">In der Regel stellen die Gruppen Tausende dar.</span><span class="sxs-lookup"><span data-stu-id="4bf82-122">Typically, the groups represent thousands.</span></span> <span data-ttu-id="4bf82-123">Abhängig von dem für locale \_ smongruppierung angegebenen Wert können Sie jedoch etwas anderes darstellen.</span><span class="sxs-lookup"><span data-stu-id="4bf82-123">However, depending on the value specified for LOCALE\_SMONGROUPING, they can represent something else.</span></span>                                                                                                                                 |



 

 

 



