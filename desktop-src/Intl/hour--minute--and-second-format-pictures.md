---
description: Dieses Thema beschreibt die Format Typen für Zeichen folgen, die zum Verfassen des Format Bilds für eine Zeit Zeichenfolge verwendet werden. Jedes Format Bild besteht aus einer Kombination aus einer Zeichenfolge der einzelnen Format Typen.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Bilder im Format "Stunde, Minute und Sekunde"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589c04fea0d6ce2f522436c30c39c873e3a7165e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050608"
---
# <a name="hour-minute-and-second-format-pictures"></a><span data-ttu-id="b3c90-104">Bilder im Format "Stunde, Minute und Sekunde"</span><span class="sxs-lookup"><span data-stu-id="b3c90-104">Hour, Minute, and Second Format Pictures</span></span>

<span data-ttu-id="b3c90-105">Dieses Thema beschreibt die Format Typen für Zeichen folgen, die zum Verfassen des Format Bilds für eine Zeit Zeichenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3c90-105">This topic describes the format types for strings used to compose the format picture for a time string.</span></span> <span data-ttu-id="b3c90-106">Jedes Format Bild besteht aus einer Kombination aus einer Zeichenfolge der einzelnen Format Typen.</span><span class="sxs-lookup"><span data-stu-id="b3c90-106">Each format picture consists of a combination of one string of each of the format types.</span></span>

> [!Note]  
> <span data-ttu-id="b3c90-107">In den Format Typen müssen die Buchstaben "m", "s" und "t" in Kleinbuchstaben eingegeben werden, und der Buchstabe "h" muss klein geschrieben sein, um die 12-Stunden-Uhr oder den Großbuchstaben ("h") anzugeben, um den 24-Stunden-Takt anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b3c90-107">In the format types, the letters "m", "s", and "t" must be lowercase, and the letter "h" must be lowercase to denote the 12-hour clock or uppercase ("H") to denote the 24-hour clock.</span></span>

<span data-ttu-id="b3c90-108">Einfache Anführungszeichen können verwendet werden, um Zeichen zu markieren, die genau wie angegeben angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b3c90-108">Single quotation marks can be used to mark characters that should be displayed exactly as specified.</span></span> <span data-ttu-id="b3c90-109">Wenn die Anwendung ein einzelnes Anführungszeichen anzeigen muss, sollte Sie zwei einfache Anführungszeichen in einer Zeile platzieren.</span><span class="sxs-lookup"><span data-stu-id="b3c90-109">If the application must display a single quotation mark, it should place two single quotation marks in a row.</span></span> <span data-ttu-id="b3c90-110">Beispielsweise wird ' abc ' ' Bar ' als ' ABl-Leiste ' angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b3c90-110">For example, 'abc''bar', is displayed as "abc'bar".</span></span>

<span data-ttu-id="b3c90-111">In der folgenden Tabelle sind die Format Typen definiert, die zur Darstellung von Stunden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3c90-111">The following table defines the format types used to represent hours.</span></span>

| <span data-ttu-id="b3c90-112">String</span><span class="sxs-lookup"><span data-stu-id="b3c90-112">String</span></span> | <span data-ttu-id="b3c90-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b3c90-113">Meaning</span></span>                                                             |
|--------|---------------------------------------------------------------------|
| <span data-ttu-id="b3c90-114">h.</span><span class="sxs-lookup"><span data-stu-id="b3c90-114">h</span></span>      | <span data-ttu-id="b3c90-115">Stunden ohne führende Nullen für Einstellige Stunden (12-Stunden-Takt).</span><span class="sxs-lookup"><span data-stu-id="b3c90-115">Hours without leading zeros for single-digit hours (12-hour clock).</span></span> |
| <span data-ttu-id="b3c90-116">hh</span><span class="sxs-lookup"><span data-stu-id="b3c90-116">hh</span></span>     | <span data-ttu-id="b3c90-117">Stunden mit führenden Nullen für Einstellige Stunden (12-Stunden-Takt).</span><span class="sxs-lookup"><span data-stu-id="b3c90-117">Hours with leading zeros for single-digit hours (12-hour clock).</span></span>    |
| <span data-ttu-id="b3c90-118">H</span><span class="sxs-lookup"><span data-stu-id="b3c90-118">H</span></span>      | <span data-ttu-id="b3c90-119">Stunden ohne führende Nullen für Einstellige Stunden (24-Stunden-Takt).</span><span class="sxs-lookup"><span data-stu-id="b3c90-119">Hours without leading zeros for single-digit hours (24-hour clock).</span></span> |
| <span data-ttu-id="b3c90-120">HH</span><span class="sxs-lookup"><span data-stu-id="b3c90-120">HH</span></span>     | <span data-ttu-id="b3c90-121">Stunden mit führenden Nullen für Einstellige Stunden (24-Stunden-Takt).</span><span class="sxs-lookup"><span data-stu-id="b3c90-121">Hours with leading zeros for single-digit hours (24-hour clock).</span></span>    |

<span data-ttu-id="b3c90-122">In der folgenden Tabelle sind die Format Typen definiert, die zur Darstellung von Minuten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3c90-122">The following table defines the format types used to represent minutes.</span></span>

| <span data-ttu-id="b3c90-123">String</span><span class="sxs-lookup"><span data-stu-id="b3c90-123">String</span></span> | <span data-ttu-id="b3c90-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b3c90-124">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="b3c90-125">m</span><span class="sxs-lookup"><span data-stu-id="b3c90-125">m</span></span>      | <span data-ttu-id="b3c90-126">Minuten ohne führende Nullen für Einstellige Minuten.</span><span class="sxs-lookup"><span data-stu-id="b3c90-126">Minutes without leading zeros for single-digit minutes.</span></span> |
| <span data-ttu-id="b3c90-127">MM</span><span class="sxs-lookup"><span data-stu-id="b3c90-127">mm</span></span>     | <span data-ttu-id="b3c90-128">Minuten mit führenden Nullen für Einstellige Minuten.</span><span class="sxs-lookup"><span data-stu-id="b3c90-128">Minutes with leading zeros for single-digit minutes.</span></span>    |

<span data-ttu-id="b3c90-129">In der folgenden Tabelle sind die Format Typen definiert, die zur Darstellung von Sekunden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3c90-129">The following table defines the format types used to represent seconds.</span></span>

| <span data-ttu-id="b3c90-130">String</span><span class="sxs-lookup"><span data-stu-id="b3c90-130">String</span></span> | <span data-ttu-id="b3c90-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b3c90-131">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="b3c90-132">s</span><span class="sxs-lookup"><span data-stu-id="b3c90-132">s</span></span>      | <span data-ttu-id="b3c90-133">Sekunden ohne führende Nullen für Einstellige Sekunden.</span><span class="sxs-lookup"><span data-stu-id="b3c90-133">Seconds without leading zeros for single-digit seconds.</span></span> |
| <span data-ttu-id="b3c90-134">ss</span><span class="sxs-lookup"><span data-stu-id="b3c90-134">ss</span></span>     | <span data-ttu-id="b3c90-135">Sekunden mit führenden Nullen für Einstellige Sekunden.</span><span class="sxs-lookup"><span data-stu-id="b3c90-135">Seconds with leading zeros for single-digit seconds.</span></span>    |

<span data-ttu-id="b3c90-136">In der folgenden Tabelle sind die Format Typen definiert, die zur Darstellung eines Zeit Markers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3c90-136">The following table defines the format types used to represent a time marker.</span></span>

| <span data-ttu-id="b3c90-137">String</span><span class="sxs-lookup"><span data-stu-id="b3c90-137">String</span></span> | <span data-ttu-id="b3c90-138">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b3c90-138">Meaning</span></span>|
| ---    | ---    |
| <span data-ttu-id="b3c90-139">t</span><span class="sxs-lookup"><span data-stu-id="b3c90-139">t</span></span>      | <span data-ttu-id="b3c90-140">Zeichenfolge mit einem Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3c90-140">One-character time marker string.</span></span><br /><span data-ttu-id="b3c90-141">**Hinweis:** Dieses Format wird nicht für die Verwendung mit bestimmten Sprachen, wie z. b. Japanisch (Japan), empfohlen.</span><span class="sxs-lookup"><span data-stu-id="b3c90-141">**Note:** This format is not recommended for use with certain languages, such as Japanese (Japan).</span></span> <span data-ttu-id="b3c90-142">Bei diesem Format übernimmt eine Anwendung immer das erste Zeichen aus der Zeit Marker-Zeichenfolge, die durch [LOCALE_S1159](locale-s1159.md) (am) und [LOCALE_S2359](locale-s2359.md) (PM) definiert wird.</span><span class="sxs-lookup"><span data-stu-id="b3c90-142">With this format, an application always takes the first character from the time marker string, defined by [LOCALE_S1159](locale-s1159.md) (AM) and [LOCALE_S2359](locale-s2359.md) (PM).</span></span> <span data-ttu-id="b3c90-143">Aus diesem Grund kann die Anwendung eine falsche Formatierung mit derselben Zeichenfolge erstellen, die sowohl für am als auch für PM verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3c90-143">Because of this, the application can create incorrect formatting with the same string used for both AM and PM.</span></span>|
| <span data-ttu-id="b3c90-144">tt</span><span class="sxs-lookup"><span data-stu-id="b3c90-144">tt</span></span>     | <span data-ttu-id="b3c90-145">Zeichenfolge für Zeichen folgen mit mehreren Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b3c90-145">Multi-character time marker string.</span></span> |
