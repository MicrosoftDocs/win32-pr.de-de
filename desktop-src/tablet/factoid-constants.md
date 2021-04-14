---
description: Definiert konstante Zeichen folgen Werte, die verwendet werden, um die Erkennungsgenauigkeit durch Bereitstellen von Kontextinformationen für die Erkennung zu erhöhen.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Faktoid-Konstanten (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1353a4989ddfb5af3865788c0fa7fdc2d377f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526594"
---
# <a name="factoid-constants"></a><span data-ttu-id="00622-103">Faktoid-Konstanten</span><span class="sxs-lookup"><span data-stu-id="00622-103">Factoid Constants</span></span>

<span data-ttu-id="00622-104">Definiert konstante Zeichen folgen Werte, die verwendet werden, um die Erkennungsgenauigkeit durch Bereitstellen von Kontextinformationen für die Erkennung zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="00622-104">Defines constant string values that are used to increase recognition accuracy by providing contextual information to the recognizer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="00622-105">Name</span><span class="sxs-lookup"><span data-stu-id="00622-105">Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="00622-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00622-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl> <span data-ttu-id="00622-107"><dt><strong>FACTOID_NONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-107"><dt><strong>FACTOID_NONE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-108">Deaktiviert alle anderen Faktoide und Wörterbücher.</span><span class="sxs-lookup"><span data-stu-id="00622-108">Disables all other factoids and dictionaries.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl> <span data-ttu-id="00622-109"><dt><strong>FACTOID_DEFAULT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-109"><dt> <strong>FACTOID_DEFAULT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-110">Die Standardeinstellung für Faktoide für westliche Sprachen umfasst das System Wörterbuch, das Benutzerwörterbuch, verschiedene interpuneration und das Web-und Zahlen-Faktoid.</span><span class="sxs-lookup"><span data-stu-id="00622-110">The Default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the Web and Number factoid.</span></span> <span data-ttu-id="00622-111">Die Standardeinstellung für Faktoide für ostasiatische Sprachen enthält alle Zeichen, die von der Erkennung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="00622-111">The Default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl> <span data-ttu-id="00622-112"><dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-112"><dt> <strong>FACTOID_SYSTEMDICTIONARY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-113">Gibt einem Erkennungs Modul an, dass nur das System Wörterbuch verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00622-113">Indicates to a recognizer to use the system dictionary only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl> <span data-ttu-id="00622-114"><dt><strong>FACTOID_WORDLIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-114"><dt> <strong>FACTOID_WORDLIST</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-115">Gibt einem Erkennungs Modul an, dass eine Programm gesteuert definierte Liste von Wörtern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00622-115">Indicates to a recognizer to use a programmatically-defined list of words.</span></span> <span data-ttu-id="00622-116">Die Liste der Wörter wird durch die <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList</strong></a> -Eigenschaft eines <a href="inkrecognizercontext-class.md"><strong>inkrecognizercontext</strong></a> -Objekts definiert.</span><span class="sxs-lookup"><span data-stu-id="00622-116">The list of words is defined by the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList</strong></a> property of a <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="00622-117">Wenn eine Zeichenfolge zu einer Word-Liste hinzugefügt wird, werden auch die Groß-und Kleinbuchstaben implizit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="00622-117">If a string is added to a word list, its capitalized versions are also implicitly added.</span></span> <span data-ttu-id="00622-118">Das Hinzufügen von &quot; Hello &quot; fügt beispielsweise implizit &quot; Hello &quot; und &quot; Hello hinzu &quot; .</span><span class="sxs-lookup"><span data-stu-id="00622-118">For instance, adding &quot;hello&quot; implicitly adds &quot;Hello&quot; and &quot;HELLO&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl> <span data-ttu-id="00622-119"><dt><strong>FACTOID_EMAIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-119"><dt> <strong>FACTOID_EMAIL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-120">Gibt einem Erkennungs Modul an, nach einer e-Mail-Adresse zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-120">Indicates to a recognizer to look for an email address.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="00622-121">&quot; someone@example.com Für dieses Faktoid muss eine voll qualifizierte e-Mail-Adresse wie z &quot; . b. verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00622-121">A fully qualified email address, such as &quot;someone@example.com&quot;, must be used for this factoid.</span></span> <span data-ttu-id="00622-122">Ein einzelner Alias, z &quot; . b. "Person" &quot; , wird nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="00622-122">A lone alias, such as &quot;someone&quot;, is not recognized.</span></span>
</blockquote>
<br/>
<pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl> <span data-ttu-id="00622-123"><dt><strong>FACTOID_WEB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-123"><dt><strong>FACTOID_WEB</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-124">Gibt einem Erkennungs Modul an, nach einer Webadresse zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-124">Indicates to a recognizer to look for a Web address.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl> <span data-ttu-id="00622-125"><dt><strong>FACTOID_ONECHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-125"><dt> <strong>FACTOID_ONECHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-126">Gibt einem Erkennungs Modul an, dass ein einzelnes Zeichen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="00622-126">Indicates to a recognizer to look for a single character.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="00622-127">Diese Faktoid sucht nach einem beliebigen isolierten ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="00622-127">This factoid looks for any isolated ANSI character.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl> <span data-ttu-id="00622-128"><dt><strong>FACTOID_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-128"><dt> <strong>FACTOID_NUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-129">Gibt einem Erkennungs Modul an, nach einer Zahl zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-129">Indicates to a recognizer to look for a number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="00622-130">Numerische Werte sind Trennzeichen, Dezimalstellen, ordinale und andere häufig verwendete numerische Symbole.</span><span class="sxs-lookup"><span data-stu-id="00622-130">Numeric values include separators, decimals, ordinals and other commonly used numeric symbols.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl> <span data-ttu-id="00622-131"><dt><strong>FACTOID_DIGIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-131"><dt> <strong>FACTOID_DIGIT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-132">Gibt einem Erkennungs Modul an, dass eine einzelne Ziffer, 0 bis 9, gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="00622-132">Indicates to a recognizer to look for a single digit, 0 through 9.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl> <span data-ttu-id="00622-133"><dt><strong>FACTOID_NUMBERSIMPLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-133"><dt> <strong>FACTOID_NUMBERSIMPLE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-134">Stellt einen einfachen numerischen Kontext für eine Erkennung bereit.</span><span class="sxs-lookup"><span data-stu-id="00622-134">Provides a simple numeric context to a recognizer.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="00622-135">Diese Faktoid wird in dieser Version des Tablet PC SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00622-135">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl> <span data-ttu-id="00622-136"><dt><strong>FACTOID_CURRENCY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-136"><dt> <strong>FACTOID_CURRENCY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-137">Gibt einem Erkennungs Modul an, nach Zeichen zu suchen, die einen Währungswert kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="00622-137">Indicates to a recognizer to look for characters that denote a currency value.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl> <span data-ttu-id="00622-138"><dt><strong>FACTOID_POSTALCODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-138"><dt> <strong>FACTOID_POSTALCODE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-139">Gibt an, dass eine Erkennung nach Postleitzahlen suchen soll.</span><span class="sxs-lookup"><span data-stu-id="00622-139">Indicates to a recognizer to look for postal codes.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>98112</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl> <span data-ttu-id="00622-140"><dt><strong>FACTOID_PERCENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-140"><dt> <strong>FACTOID_PERCENT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-141">Gibt einem Erkennungs Modul an, nach Prozentsätzen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-141">Indicates to a recognizer to look for percentages.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>87%</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl> <span data-ttu-id="00622-142"><dt><strong>FACTOID_DATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-142"><dt> <strong>FACTOID_DATE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-143">Gibt einem Erkennungs Modul an, nach Zeichen zu suchen, die ein Datum kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="00622-143">Indicates to a recognizer to look for characters that denote a date.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>10/30/2001, &#39;01, 31/12, 12/99, 1999-2000</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl> <span data-ttu-id="00622-144"><dt><strong>FACTOID_TIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-144"><dt> <strong>FACTOID_TIME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-145">Gibt einem Erkennungs Modul an, nach Zeichen zu suchen, die eine Uhrzeit angeben.</span><span class="sxs-lookup"><span data-stu-id="00622-145">Indicates to a recognizer to look for characters that denote a time.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl> <span data-ttu-id="00622-146"><dt><strong>FACTOID_TELEPHONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-146"><dt> <strong>FACTOID_TELEPHONE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-147">Gibt einem Erkennungs Modul an, nach Zeichen zu suchen, die eine Telefonnummer kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="00622-147">Indicates to a recognizer to look for characters that denote a telephone number.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl> <span data-ttu-id="00622-148"><dt><strong>FACTOID_FILENAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-148"><dt> <strong>FACTOID_FILENAME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-149">Gibt einem Erkennungs Modul an, nach Zeichen zu suchen, die einen Dateinamen angeben.</span><span class="sxs-lookup"><span data-stu-id="00622-149">Indicates to a recognizer to look for characters that denote a file name.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl> <span data-ttu-id="00622-150"><dt><strong>FACTOID_UPPERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-150"><dt> <strong>FACTOID_UPPERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-151">Gibt an, dass eine Erkennung nach einem einzelnen Großbuchstaben suchen soll: a bis Z.</span><span class="sxs-lookup"><span data-stu-id="00622-151">Indicates to a recognizer to look for a single uppercase character: A through Z.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl> <span data-ttu-id="00622-152"><dt><strong>FACTOID_LOWERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-152"><dt> <strong>FACTOID_LOWERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-153">Gibt an, dass eine Erkennung nach einem einzelnen Kleinbuchstaben suchen soll: a bis Z.</span><span class="sxs-lookup"><span data-stu-id="00622-153">Indicates to a recognizer to look for a single lowercase character: A through Z.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="00622-154">Diese Faktoid wird in dieser Version des Tablet PC SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00622-154">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl> <span data-ttu-id="00622-155"><dt><strong>FACTOID_PUNCCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-155"><dt> <strong>FACTOID_PUNCCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-156">Gibt einem Erkennungs Modul an, dass Interpunktions Zeichen gesucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="00622-156">Indicates to a recognizer to look for punctuation characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="00622-157">Diese Faktoid wird in dieser Version des Tablet PC SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00622-157">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl> <span data-ttu-id="00622-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-159">Gibt einem Erkennungs Modul an, nach häufig verwendeten Kanji-, Katakana-und Hiragana-Zeichen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-159">Indicates to a recognizer to look for commonly used Kanji, Katakana, and Hiragana characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl> <span data-ttu-id="00622-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-161">Gibt an, dass eine Erkennung nach häufig verwendeten, vereinfachten chinesischen Zeichen suchen soll.</span><span class="sxs-lookup"><span data-stu-id="00622-161">Indicates to a recognizer to look for commonly used Simplified Chinese characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl> <span data-ttu-id="00622-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-163">Gibt einem Erkennungs Modul an, nach häufig verwendeten herkömmlichen chinesischen Zeichen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-163">Indicates to a recognizer to look for commonly used Traditional Chinese characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl> <span data-ttu-id="00622-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-165">Gibt einem Erkennungs Modul an, nach häufig verwendeten koreanischen Zeichen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-165">Indicates to a recognizer to look for commonly used Korean characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl> <span data-ttu-id="00622-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-167">Gibt einem Erkennungs Modul an, dass nur nach Hiragana-Zeichen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="00622-167">Indicates to a recognizer to look for Hiragana characters only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl> <span data-ttu-id="00622-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-169">Gibt einem Erkennungs Modul an, nur nach Katakana-Zeichen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-169">Indicates to a recognizer to look for Katakana characters only.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl> <span data-ttu-id="00622-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-171">Gibt einem Erkennungs Modul an, nach häufig verwendeten Kanji-Zeichen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-171">Indicates to a recognizer to look for commonly used kanji characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl> <span data-ttu-id="00622-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-173">Gibt einem Erkennungs Modul an, nach selten verwendeten Kanji-Zeichen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-173">Indicates to a recognizer to look for rarely used kanji characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="00622-174">Diese Faktoid wird in dieser Version des Tablet PC SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00622-174">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl> <span data-ttu-id="00622-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-176">Gibt an, dass eine Erkennung nach Bopomofo-Zeichen suchen soll.</span><span class="sxs-lookup"><span data-stu-id="00622-176">Indicates to a recognizer to look for Bopomofo characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl> <span data-ttu-id="00622-177"><dt><strong>FACTOID_JAMO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-177"><dt><strong>FACTOID_JAMO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-178">Gibt einem Erkennungs Modul an, nach Hangul Compatibility Jamo-Zeichen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-178">Indicates to a recognizer to look for Hangul compatibility Jamo characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl> <span data-ttu-id="00622-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-180">Gibt einem Erkennungs Modul an, nach häufig verwendeten Hangul-Zeichen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-180">Indicates to a recognizer to look for commonly used Hangul characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl> <span data-ttu-id="00622-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="00622-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="00622-182">Gibt einem Erkennungs Modul an, nach selten verwendeten Hangul-Zeichen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00622-182">Indicates to a recognizer to look for rarely used Hangul characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="00622-183">Diese Faktoid wird in dieser Version des Tablet PC SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00622-183">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="00622-184">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00622-184">Remarks</span></span>

<span data-ttu-id="00622-185">In C++ können Sie in der Header Datei "msink AUT. h" auf diese Konstanten zugreifen, die sich im <systemdrive> Verzeichnis "Programme" des \\ \\ Microsoft Tablet PC Platform SDK include befinden, \\ Wenn Sie das SDK am Standard Speicherort installiert haben.</span><span class="sxs-lookup"><span data-stu-id="00622-185">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="00622-186">Diese Konstanten sind WCHARs, nicht bstrins.</span><span class="sxs-lookup"><span data-stu-id="00622-186">These constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="00622-187">Sie müssen in bstrans konvertiert werden, bevor Sie als Parameter für Objektmethoden verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="00622-187">They must be converted into BSTRs before use as parameters to object methods.</span></span> <span data-ttu-id="00622-188">Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="00622-188">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="00622-189">Für Erkennungs Modul von lateinischen Skripts werden die in dieser Klasse definierten factoide nur aus Gründen der Abwärtskompatibilität bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="00622-189">For recognizers of Latin script, the factoids defined in this class are provided for backward compatibility only.</span></span> <span data-ttu-id="00622-190">Bei der neuen Entwicklung wird empfohlen, die in [der Funktion "](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) " von "" in der Funktion "" festgelegten Werte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="00622-190">For new development, you are encouraged to use the values defined in the [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) function.</span></span> <span data-ttu-id="00622-191">Weitere Informationen finden [Sie unter Verwenden von Kontext zur Verbesserung der Genauigkeit](using-context-to-improve-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="00622-191">For details, see [Using Context to Improve Accuracy](using-context-to-improve-accuracy.md).</span></span>

 

<span data-ttu-id="00622-192">Verwenden Sie diese Bezeichner, um anzugeben, welches Faktoid während der Erkennung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00622-192">Use these identifiers to specify which factoid should be used during recognition.</span></span>

<span data-ttu-id="00622-193">Die folgenden Kombinationen von Faktoiden werden nur für westliche Sprachen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00622-193">The following combinations of factoids are supported for western languages only.</span></span> <span data-ttu-id="00622-194">Diese weisen keine separaten Definitionen auf, sind jedoch akzeptable zeichenfolgenliteraleingaben für die [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) -Eigenschaft von Objekten, die Faktoide verwenden.</span><span class="sxs-lookup"><span data-stu-id="00622-194">These do not have separate definitions, but are acceptable string literal inputs to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of objects that use factoids.</span></span> <span data-ttu-id="00622-195">Diese Faktoid-Zeichen folgen Konstanten ermöglichen, dass die Eingabe mit einer der Faktoide im Ausdruck identisch ist.</span><span class="sxs-lookup"><span data-stu-id="00622-195">These factoid string constants allow the input to match any of the factoids in the expression.</span></span>



| <span data-ttu-id="00622-196">Kombination</span><span class="sxs-lookup"><span data-stu-id="00622-196">Combination</span></span>               | <span data-ttu-id="00622-197">Definition</span><span class="sxs-lookup"><span data-stu-id="00622-197">Definition</span></span>                                                |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="00622-198">"Web \| WordList"</span><span class="sxs-lookup"><span data-stu-id="00622-198">"WEB\|WORDLIST"</span></span>           | <span data-ttu-id="00622-199">Webfaktoid oder Wort Liste.</span><span class="sxs-lookup"><span data-stu-id="00622-199">The Web factoid or the word list.</span></span>                         |
| <span data-ttu-id="00622-200">"e-Mail- \| WordList"</span><span class="sxs-lookup"><span data-stu-id="00622-200">"EMAIL\|WORDLIST"</span></span>         | <span data-ttu-id="00622-201">Die e-Mail-Faktoid oder die Wortliste.</span><span class="sxs-lookup"><span data-stu-id="00622-201">The Email factoid or the word list.</span></span>                       |
| <span data-ttu-id="00622-202">"Dateiname \| Web \| WordList"</span><span class="sxs-lookup"><span data-stu-id="00622-202">"FILENAME\|WEB\|WORDLIST"</span></span> | <span data-ttu-id="00622-203">Der Dateiname (Faktoid) oder das webfaktoid oder die Wort Liste.</span><span class="sxs-lookup"><span data-stu-id="00622-203">The Filename factoid or the Web factoid or the word list.</span></span> |



 

<span data-ttu-id="00622-204">Wenn Sie das [InkEdit](inkedit-control-reference.md) -Steuerelement verwenden, kann die Faktoid als Eigenschaft des Steuer Elements festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="00622-204">If you are using the [InkEdit](inkedit-control-reference.md) control, the factoid can be set as a property of the control.</span></span>

<span data-ttu-id="00622-205">Wenn Sie die Tablet PC Platform-APIs verwenden, können Sie die Eigenschaft " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " für ein " [**inkrecognizercontext**](inkrecognizercontext-class.md) "-Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="00622-205">If you are using the Tablet PC Platform APIs, you can set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on an [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

<span data-ttu-id="00622-206">Alternativ können Sie diese Eigenschaft mit der eigentlichen Faktoid-Zeichen folgen Konstante festlegen.</span><span class="sxs-lookup"><span data-stu-id="00622-206">Alternatively, you can set this property with the actual factoid string constant.</span></span>

> [!Note]  
> <span data-ttu-id="00622-207">Bei Faktoid-Zeichen folgen Konstanten wird Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="00622-207">Factoid string constants are case sensitive.</span></span> <span data-ttu-id="00622-208">Weitere Informationen zu Faktoiden und deren Verwendung finden Sie unter Verwenden von Kontext zur [Verbesserung der Genauigkeit](using-context-to-improve-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="00622-208">For more information about factoids and how to use them, see Using Context to [Improve Accuracy](using-context-to-improve-accuracy.md).</span></span> <span data-ttu-id="00622-209">Informationen zum bestimmen, ob ein Faktoid in einer bestimmten Sprache verfügbar ist, finden Sie [unter Unterstützte Faktoide aus Version 1](supported-factoids-from-version-1.md).</span><span class="sxs-lookup"><span data-stu-id="00622-209">To determine whether a factoid is available in a specific language, see [Supported Factoids from Version 1](supported-factoids-from-version-1.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="00622-210">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00622-210">Requirements</span></span>



| <span data-ttu-id="00622-211">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00622-211">Requirement</span></span> | <span data-ttu-id="00622-212">Wert</span><span class="sxs-lookup"><span data-stu-id="00622-212">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00622-213">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00622-213">Minimum supported client</span></span><br/> | <span data-ttu-id="00622-214">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00622-214">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="00622-215">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00622-215">Minimum supported server</span></span><br/> | <span data-ttu-id="00622-216">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="00622-216">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="00622-217">Header</span><span class="sxs-lookup"><span data-stu-id="00622-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="00622-218"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="00622-218"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00622-219">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00622-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="00622-220">[**Factoid-Eigenschaft " \[ inkrecognizecontext"-Klasse\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="00622-220">[**Factoid Property \[InkRecognizeContext Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="00622-221">[**Eigenschaft "paninputpanel" der Factoid-Eigenschaft \[\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="00622-221">[**Factoid Property \[PenInputPanel Class\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="00622-222">[**Faktoid-Eigenschaft, \[ InkEdit-Steuerelement\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="00622-222">[**Factoid Property \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span></span>
</dt> <dt>

[<span data-ttu-id="00622-223">Verwenden des Kontexts zur Verbesserung der Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="00622-223">Using Context to Improve Accuracy</span></span>](using-context-to-improve-accuracy.md)
</dt> <dt>

[<span data-ttu-id="00622-224">Unterstützte Faktoide aus Version 1</span><span class="sxs-lookup"><span data-stu-id="00622-224">Supported Factoids from Version 1</span></span>](supported-factoids-from-version-1.md)
</dt> </dl>

 

