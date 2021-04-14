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
# <a name="factoid-constants"></a>Faktoid-Konstanten

Definiert konstante Zeichen folgen Werte, die verwendet werden, um die Erkennungsgenauigkeit durch Bereitstellen von Kontextinformationen für die Erkennung zu erhöhen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Name</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl> <dt><strong>FACTOID_NONE</strong></dt> </dl></td>
<td style="text-align: left;">Deaktiviert alle anderen Faktoide und Wörterbücher.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl> <dt><strong>FACTOID_DEFAULT</strong></dt> </dl></td>
<td style="text-align: left;">Die Standardeinstellung für Faktoide für westliche Sprachen umfasst das System Wörterbuch, das Benutzerwörterbuch, verschiedene interpuneration und das Web-und Zahlen-Faktoid. Die Standardeinstellung für Faktoide für ostasiatische Sprachen enthält alle Zeichen, die von der Erkennung unterstützt werden. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl> <dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, dass nur das System Wörterbuch verwendet werden soll.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl> <dt><strong>FACTOID_WORDLIST</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, dass eine Programm gesteuert definierte Liste von Wörtern verwendet werden soll. Die Liste der Wörter wird durch die <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList</strong></a> -Eigenschaft eines <a href="inkrecognizercontext-class.md"><strong>inkrecognizercontext</strong></a> -Objekts definiert. <br/>
<blockquote>
[!Note]<br />
Wenn eine Zeichenfolge zu einer Word-Liste hinzugefügt wird, werden auch die Groß-und Kleinbuchstaben implizit hinzugefügt. Das Hinzufügen von &quot; Hello &quot; fügt beispielsweise implizit &quot; Hello &quot; und &quot; Hello hinzu &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl> <dt><strong>FACTOID_EMAIL</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach einer e-Mail-Adresse zu suchen.<br/>
<blockquote>
[!Note]<br />
&quot; someone@example.com Für dieses Faktoid muss eine voll qualifizierte e-Mail-Adresse wie z &quot; . b. verwendet werden. Ein einzelner Alias, z &quot; . b. "Person" &quot; , wird nicht erkannt.
</blockquote>
<br/>
<pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl> <dt><strong>FACTOID_WEB</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach einer Webadresse zu suchen.<br/>
<pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl> <dt><strong>FACTOID_ONECHAR</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, dass ein einzelnes Zeichen gesucht werden soll.<br/>
<blockquote>
[!Note]<br />
Diese Faktoid sucht nach einem beliebigen isolierten ANSI-Zeichen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl> <dt><strong>FACTOID_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach einer Zahl zu suchen.<br/>
<blockquote>
[!Note]<br />
Numerische Werte sind Trennzeichen, Dezimalstellen, ordinale und andere häufig verwendete numerische Symbole.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl> <dt><strong>FACTOID_DIGIT</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, dass eine einzelne Ziffer, 0 bis 9, gesucht werden soll.<br/>
<pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl> <dt><strong>FACTOID_NUMBERSIMPLE</strong></dt> </dl></td>
<td style="text-align: left;">Stellt einen einfachen numerischen Kontext für eine Erkennung bereit.<br/>
<blockquote>
[!Note]<br />
Diese Faktoid wird in dieser Version des Tablet PC SDK nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl> <dt><strong>FACTOID_CURRENCY</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach Zeichen zu suchen, die einen Währungswert kennzeichnen.<br/>
<pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl> <dt><strong>FACTOID_POSTALCODE</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass eine Erkennung nach Postleitzahlen suchen soll.<br/>
<pre class="syntax" data-space="preserve"><code>98112</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl> <dt><strong>FACTOID_PERCENT</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach Prozentsätzen zu suchen.<br/>
<pre class="syntax" data-space="preserve"><code>87%</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl> <dt><strong>FACTOID_DATE</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach Zeichen zu suchen, die ein Datum kennzeichnen.<br/>
<pre class="syntax" data-space="preserve"><code>10/30/2001, &#39;01, 31/12, 12/99, 1999-2000</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl> <dt><strong>FACTOID_TIME</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach Zeichen zu suchen, die eine Uhrzeit angeben.<br/>
<pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl> <dt><strong>FACTOID_TELEPHONE</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach Zeichen zu suchen, die eine Telefonnummer kennzeichnen.<br/>
<pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl> <dt><strong>FACTOID_FILENAME</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach Zeichen zu suchen, die einen Dateinamen angeben.<br/>
<pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl> <dt><strong>FACTOID_UPPERCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass eine Erkennung nach einem einzelnen Großbuchstaben suchen soll: a bis Z.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl> <dt><strong>FACTOID_LOWERCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass eine Erkennung nach einem einzelnen Kleinbuchstaben suchen soll: a bis Z.<br/>
<blockquote>
[!Note]<br />
Diese Faktoid wird in dieser Version des Tablet PC SDK nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl> <dt><strong>FACTOID_PUNCCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, dass Interpunktions Zeichen gesucht werden sollen.<br/>
<blockquote>
[!Note]<br />
Diese Faktoid wird in dieser Version des Tablet PC SDK nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl> <dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach häufig verwendeten Kanji-, Katakana-und Hiragana-Zeichen zu suchen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl> <dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass eine Erkennung nach häufig verwendeten, vereinfachten chinesischen Zeichen suchen soll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl> <dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach häufig verwendeten herkömmlichen chinesischen Zeichen zu suchen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl> <dt><strong>FACTOID_KOREANCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach häufig verwendeten koreanischen Zeichen zu suchen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl> <dt><strong>FACTOID_HIRAGANA</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, dass nur nach Hiragana-Zeichen gesucht werden soll.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl> <dt><strong>FACTOID_KATAKANA</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nur nach Katakana-Zeichen zu suchen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl> <dt><strong>FACTOID_KANJICOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach häufig verwendeten Kanji-Zeichen zu suchen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl> <dt><strong>FACTOID_KANJIRARE</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach selten verwendeten Kanji-Zeichen zu suchen.<br/>
<blockquote>
[!Note]<br />
Diese Faktoid wird in dieser Version des Tablet PC SDK nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl> <dt><strong>FACTOID_BOPOMOFO</strong></dt> </dl></td>
<td style="text-align: left;">Gibt an, dass eine Erkennung nach Bopomofo-Zeichen suchen soll.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl> <dt><strong>FACTOID_JAMO</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach Hangul Compatibility Jamo-Zeichen zu suchen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl> <dt><strong>FACTOID_HANGULCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach häufig verwendeten Hangul-Zeichen zu suchen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl> <dt><strong>FACTOID_HANGULRARE</strong></dt> </dl></td>
<td style="text-align: left;">Gibt einem Erkennungs Modul an, nach selten verwendeten Hangul-Zeichen zu suchen.<br/>
<blockquote>
[!Note]<br />
Diese Faktoid wird in dieser Version des Tablet PC SDK nicht unterstützt.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

In C++ können Sie in der Header Datei "msink AUT. h" auf diese Konstanten zugreifen, die sich im <systemdrive> Verzeichnis "Programme" des \\ \\ Microsoft Tablet PC Platform SDK include befinden, \\ Wenn Sie das SDK am Standard Speicherort installiert haben.

> [!Note]  
> Diese Konstanten sind WCHARs, nicht bstrins. Sie müssen in bstrans konvertiert werden, bevor Sie als Parameter für Objektmethoden verwendet werden können. Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

 

> [!Note]  
> Für Erkennungs Modul von lateinischen Skripts werden die in dieser Klasse definierten factoide nur aus Gründen der Abwärtskompatibilität bereitgestellt. Bei der neuen Entwicklung wird empfohlen, die in [der Funktion "](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) " von "" in der Funktion "" festgelegten Werte zu verwenden. Weitere Informationen finden [Sie unter Verwenden von Kontext zur Verbesserung der Genauigkeit](using-context-to-improve-accuracy.md).

 

Verwenden Sie diese Bezeichner, um anzugeben, welches Faktoid während der Erkennung verwendet werden soll.

Die folgenden Kombinationen von Faktoiden werden nur für westliche Sprachen unterstützt. Diese weisen keine separaten Definitionen auf, sind jedoch akzeptable zeichenfolgenliteraleingaben für die [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) -Eigenschaft von Objekten, die Faktoide verwenden. Diese Faktoid-Zeichen folgen Konstanten ermöglichen, dass die Eingabe mit einer der Faktoide im Ausdruck identisch ist.



| Kombination               | Definition                                                |
|---------------------------|-----------------------------------------------------------|
| "Web \| WordList"           | Webfaktoid oder Wort Liste.                         |
| "e-Mail- \| WordList"         | Die e-Mail-Faktoid oder die Wortliste.                       |
| "Dateiname \| Web \| WordList" | Der Dateiname (Faktoid) oder das webfaktoid oder die Wort Liste. |



 

Wenn Sie das [InkEdit](inkedit-control-reference.md) -Steuerelement verwenden, kann die Faktoid als Eigenschaft des Steuer Elements festgelegt werden.

Wenn Sie die Tablet PC Platform-APIs verwenden, können Sie die Eigenschaft " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " für ein " [**inkrecognizercontext**](inkrecognizercontext-class.md) "-Objekt festlegen.

Alternativ können Sie diese Eigenschaft mit der eigentlichen Faktoid-Zeichen folgen Konstante festlegen.

> [!Note]  
> Bei Faktoid-Zeichen folgen Konstanten wird Groß-/Kleinschreibung Weitere Informationen zu Faktoiden und deren Verwendung finden Sie unter Verwenden von Kontext zur [Verbesserung der Genauigkeit](using-context-to-improve-accuracy.md). Informationen zum bestimmen, ob ein Faktoid in einer bestimmten Sprache verfügbar ist, finden Sie [unter Unterstützte Faktoide aus Version 1](supported-factoids-from-version-1.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Factoid-Eigenschaft " \[ inkrecognizecontext"-Klasse\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)
</dt> <dt>

[**Eigenschaft "paninputpanel" der Factoid-Eigenschaft \[\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)
</dt> <dt>

[**Faktoid-Eigenschaft, \[ InkEdit-Steuerelement\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)
</dt> <dt>

[Verwenden des Kontexts zur Verbesserung der Genauigkeit](using-context-to-improve-accuracy.md)
</dt> <dt>

[Unterstützte Faktoide aus Version 1](supported-factoids-from-version-1.md)
</dt> </dl>

 

