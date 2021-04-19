---
description: Arabisch und viele andere Sprachen verfügen über klassische Formen für Zahlen, die sich von den herkömmlichen westlichen Ziffern unterscheiden, die am häufigsten auf Computern verwendet werden.
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: Ziffern Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e6581b8b0eb87ae09b387c038c1ceba43125ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360784"
---
# <a name="digit-shapes"></a><span data-ttu-id="39dcc-103">Ziffern Formen</span><span class="sxs-lookup"><span data-stu-id="39dcc-103">Digit Shapes</span></span>

<span data-ttu-id="39dcc-104">Arabisch und viele andere Sprachen verfügen über klassische Formen für Zahlen, die sich von den herkömmlichen westlichen Ziffern unterscheiden, die am häufigsten auf Computern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39dcc-104">Arabic and many other languages have classical shapes for numbers that are different from the conventional western digits most often used on computers.</span></span> <span data-ttu-id="39dcc-105">Um Mehrdeutigkeit beim Benennen dieser Formen zu vermeiden, verwendet dieses Dokument die folgenden Namen aus dem Unicode-Standard.</span><span class="sxs-lookup"><span data-stu-id="39dcc-105">To avoid ambiguity in naming these shapes, this document uses the following names from the Unicode standard.</span></span>



| <span data-ttu-id="39dcc-106">Unicode-Name der Ziffern</span><span class="sxs-lookup"><span data-stu-id="39dcc-106">Unicode name of the digits</span></span>                                     | <span data-ttu-id="39dcc-107">Verwendetes Land/Region</span><span class="sxs-lookup"><span data-stu-id="39dcc-107">Country/region where used</span></span>                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="39dcc-108">Europäische Ziffern</span><span class="sxs-lookup"><span data-stu-id="39dcc-108">European digits</span></span>                                                | <span data-ttu-id="39dcc-109">Europa, Nordamerika und viele weitere Länder/Regionen</span><span class="sxs-lookup"><span data-stu-id="39dcc-109">Europe, the Americas, and many other countries/regions</span></span>       |
| <span data-ttu-id="39dcc-110">Arabic-Indic Ziffern</span><span class="sxs-lookup"><span data-stu-id="39dcc-110">Arabic-Indic digits</span></span>                                            | <span data-ttu-id="39dcc-111">Arabische Länder/Regionen (obwohl viele europäische Ziffern verwenden)</span><span class="sxs-lookup"><span data-stu-id="39dcc-111">Arabic countries/regions (although many use European digits)</span></span> |
| <span data-ttu-id="39dcc-112">Weitere nationale Ziffern: indic-Ziffern, thailändische Ziffern und ähnliches</span><span class="sxs-lookup"><span data-stu-id="39dcc-112">Other national digits: Indic digits, Thai digits, and the like</span></span> | <span data-ttu-id="39dcc-113">Verschiedene Länder/Regionen</span><span class="sxs-lookup"><span data-stu-id="39dcc-113">Various countries/regions</span></span>                                    |



 

<span data-ttu-id="39dcc-114">Unicode bietet separate Code Punkte für jede Ziffern Form.</span><span class="sxs-lookup"><span data-stu-id="39dcc-114">Unicode provides separate code points for each digit shape.</span></span> <span data-ttu-id="39dcc-115">Daher kann die Anwendung für den Zugriff auf spezielle sprach Ziffern Formen die relevanten Unicode-Zeichen Codes für die Ziffern oberhalb, u + 0030 bis U + 0039 verwenden.</span><span class="sxs-lookup"><span data-stu-id="39dcc-115">Thus, to access special language digit shapes, your application can use the relevant Unicode character codes for the digits above, U+0030 through U+0039.</span></span> <span data-ttu-id="39dcc-116">Diese Codes werden immer mit der entsprechenden Form angezeigt, die der Schriftart Verfügbarkeit unterliegen.</span><span class="sxs-lookup"><span data-stu-id="39dcc-116">These codes are always displayed with the appropriate shape, subject to font availability.</span></span>

<span data-ttu-id="39dcc-117">Die Unicode-Zeichen Codes U + 0030 bis u + 0039 stellen nominell die europäischen Ziffern 0 bis 9 dar, ihre Ziffern Form kann jedoch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="39dcc-117">The Unicode character codes U+0030 through U+0039 nominally represent the European digits 0 through 9, but their digit shape can be altered.</span></span> <span data-ttu-id="39dcc-118">GDI-und DirectWrite-Text-APIs stellen Mechanismen bereit, mit denen Anwendungen dieses Verhalten steuern können.</span><span class="sxs-lookup"><span data-stu-id="39dcc-118">GDI and DirectWrite text APIs provide mechanisms for applications to control this behavior.</span></span> <span data-ttu-id="39dcc-119">(Siehe beispielsweise [**scriptapplydigitsubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) oder [**idwrite tetextanalysissink:: setnumersubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) Das Verhalten in einigen Shellsteuerelementen und Benutzeroberflächen-Frameworks kann auf Benutzer Gebiets Schema Einstellungen für die Ziffern Ersetzung reagieren. Das Gebiets Schema [ \_ idigitsubstitution](locale-idigitsubstitution.md) LCTYPE kann verwendet werden, um Standardeinstellungen für die Ersetzungs Ersetzung für verschiedene Gebiets Schemas oder die Desktop Einstellungen des aktuellen Benutzers für die Ziffern Ersetzung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="39dcc-119">(See, for instance, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) or [**IDWriteTextAnalysisSink::SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) The behavior in some shell controls and user interface frameworks may respond to user locale settings for digit substitution; the [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE can be used to obtain default digit substitution settings for different locales or the current user's desktop settings for digit substitution.</span></span>

## <a name="native-digits"></a><span data-ttu-id="39dcc-120">Native Ziffern</span><span class="sxs-lookup"><span data-stu-id="39dcc-120">Native Digits</span></span>

<span data-ttu-id="39dcc-121">Native Ziffern sind die vom Benutzer ausgewählten Ziffern Formen im Eigenschaften Blatt " **Zahl** " im Bereich "Regions-und Sprachoptionen" der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="39dcc-121">Native digits are the digit shapes chosen by the user in the **Number** property sheet in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="39dcc-122">Um die vom Benutzer bevorzugte Ziffern Präsentation zu finden, verwendet Ihre Anwendung die [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) -Funktion oder die [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) -Funktion mit der " [locale- \_ snativedigits](locale-snative-constants.md) "-Konstante, die die Gebiets Schema Informationen darstellt.</span><span class="sxs-lookup"><span data-stu-id="39dcc-122">To find the digit presentation preferred by the user, your application uses the [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) function with the [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) constant representing the locale information.</span></span>

> [!Note]  
> <span data-ttu-id="39dcc-123">In der Regel werden Unicode-Ziffern Codes in Lauf Zeit Betriebssystemroutinen generiert.</span><span class="sxs-lookup"><span data-stu-id="39dcc-123">Typically, Unicode digit codes are generated in runtime operating system routines.</span></span> <span data-ttu-id="39dcc-124">Daher müssen allgemeine Lauf Zeit Betriebssysteme aktualisiert werden, damit die Anwendung die [Gebiets \_ Schema-snativedigits](locale-snative-constants.md) entsprechend überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="39dcc-124">Therefore, common runtime operating systems must be upgraded for the application to inspect [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) appropriately.</span></span>

 

## <a name="digit-substitution"></a><span data-ttu-id="39dcc-125">Ziffern Ersetzung</span><span class="sxs-lookup"><span data-stu-id="39dcc-125">Digit Substitution</span></span>

<span data-ttu-id="39dcc-126">Die Anwendung kann die Ziffern Ersetzung verwenden, um dem Betriebssystem mitzuteilen, wie Ziffern u + 0030 bis u + 0039 gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39dcc-126">The application can use digit substitution to tell the operating system how to print digits U+0030 through U+0039.</span></span> <span data-ttu-id="39dcc-127">Dieser Vorgang wird von der [ \_ idigitsubstitution](locale-idigitsubstitution.md) -Schema-Konstante gesteuert.</span><span class="sxs-lookup"><span data-stu-id="39dcc-127">The [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) constant controls this operation.</span></span>

## <a name="digit-shaping-for-a-single-function"></a><span data-ttu-id="39dcc-128">Ziffern Strukturierung für eine einzelne Funktion</span><span class="sxs-lookup"><span data-stu-id="39dcc-128">Digit Shaping for a Single Function</span></span>

<span data-ttu-id="39dcc-129">Die [resulttextout](/windows/win32/api/wingdi/nf-wingdi-exttextouta)-, [getcharakteriplacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)-und [GCP- \_ Ergebnis](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) Funktionen verfügen über Flags, die die Ersetzung von Unicode-Codes U + 0030 bis u + 0039 für die Dauer des Funktions Aufrufes steuern.</span><span class="sxs-lookup"><span data-stu-id="39dcc-129">The [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa), and [GCP\_RESULTS](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) functions have flags that govern the substitution of Unicode codes U+0030 through U+0039 for the duration of the function call.</span></span> <span data-ttu-id="39dcc-130">Diese Flags überschreiben regionale Einstellungen in der Systemsteuerung, setzen jedoch nicht die Einstellungen zurück.</span><span class="sxs-lookup"><span data-stu-id="39dcc-130">These flags override regional settings in the Control Panel, but do not reset the settings.</span></span> <span data-ttu-id="39dcc-131">Außerdem überschreiben Sie nicht die Unicode-Codes NADS und Nods.</span><span class="sxs-lookup"><span data-stu-id="39dcc-131">Also, they do not override the Unicode codes NADS and NODS.</span></span> <span data-ttu-id="39dcc-132">Die folgenden Flags sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="39dcc-132">The following flags are available.</span></span>



| <span data-ttu-id="39dcc-133">Flags</span><span class="sxs-lookup"><span data-stu-id="39dcc-133">Flags</span></span>                 | <span data-ttu-id="39dcc-134">Verwendete Ziffern</span><span class="sxs-lookup"><span data-stu-id="39dcc-134">Digits used</span></span>                      | <span data-ttu-id="39dcc-135">Verwendung in</span><span class="sxs-lookup"><span data-stu-id="39dcc-135">Used in</span></span>                   |
|-----------------------|----------------------------------|---------------------------|
| <span data-ttu-id="39dcc-136">Eto- \_ numericslatin</span><span class="sxs-lookup"><span data-stu-id="39dcc-136">ETO\_NUMERICSLATIN</span></span>    | <span data-ttu-id="39dcc-137">Europäische Ziffern</span><span class="sxs-lookup"><span data-stu-id="39dcc-137">European digits</span></span>                  | <span data-ttu-id="39dcc-138">**Exttextout**</span><span class="sxs-lookup"><span data-stu-id="39dcc-138">**ExtTextOut**</span></span>            |
| <span data-ttu-id="39dcc-139">Eto \_ numericslocal</span><span class="sxs-lookup"><span data-stu-id="39dcc-139">ETO\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="39dcc-140">Für das Gebiets Schema geeignete Ziffern</span><span class="sxs-lookup"><span data-stu-id="39dcc-140">Digits appropriate to the locale</span></span> | <span data-ttu-id="39dcc-141">**Exttextout**</span><span class="sxs-lookup"><span data-stu-id="39dcc-141">**ExtTextOut**</span></span>            |
| <span data-ttu-id="39dcc-142">GCP- \_ numericslatin</span><span class="sxs-lookup"><span data-stu-id="39dcc-142">GCP\_NUMERICSLATIN</span></span>    | <span data-ttu-id="39dcc-143">Europäische Ziffern</span><span class="sxs-lookup"><span data-stu-id="39dcc-143">European digits</span></span>                  | <span data-ttu-id="39dcc-144">**GetCharacterPlacement**</span><span class="sxs-lookup"><span data-stu-id="39dcc-144">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="39dcc-145">GCP \_ numericslocal</span><span class="sxs-lookup"><span data-stu-id="39dcc-145">GCP\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="39dcc-146">Für das Gebiets Schema geeignete Ziffern</span><span class="sxs-lookup"><span data-stu-id="39dcc-146">Digits appropriate to the locale</span></span> | <span data-ttu-id="39dcc-147">**GetCharacterPlacement**</span><span class="sxs-lookup"><span data-stu-id="39dcc-147">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="39dcc-148">gcpclass- \_ latinnumber</span><span class="sxs-lookup"><span data-stu-id="39dcc-148">GCPCLASS\_LATINNUMBER</span></span> | <span data-ttu-id="39dcc-149">Europäische Ziffern</span><span class="sxs-lookup"><span data-stu-id="39dcc-149">European digits</span></span>                  | <span data-ttu-id="39dcc-150">**GCP- \_ Ergebnisse**</span><span class="sxs-lookup"><span data-stu-id="39dcc-150">**GCP\_RESULTS**</span></span>          |
| <span data-ttu-id="39dcc-151">gcpclass \_ localnumber</span><span class="sxs-lookup"><span data-stu-id="39dcc-151">GCPCLASS\_LOCALNUMBER</span></span> | <span data-ttu-id="39dcc-152">Für das Gebiets Schema geeignete Ziffern</span><span class="sxs-lookup"><span data-stu-id="39dcc-152">Digits appropriate to the locale</span></span> | <span data-ttu-id="39dcc-153">**GCP- \_ Ergebnisse**</span><span class="sxs-lookup"><span data-stu-id="39dcc-153">**GCP\_RESULTS**</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="39dcc-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39dcc-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39dcc-155">Informationen zur Unterstützung der Landessprache</span><span class="sxs-lookup"><span data-stu-id="39dcc-155">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="39dcc-156">**Getlocaleingefo**</span><span class="sxs-lookup"><span data-stu-id="39dcc-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[<span data-ttu-id="39dcc-157">**GetLocaleInfoEx**</span><span class="sxs-lookup"><span data-stu-id="39dcc-157">**GetLocaleInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
