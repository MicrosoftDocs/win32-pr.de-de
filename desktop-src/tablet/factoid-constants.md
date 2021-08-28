---
description: Definiert konstante Zeichenfolgenwerte, die verwendet werden, um die Erkennungsgenauigkeit zu erhöhen, indem kontextbezogene Informationen für die Erkennung angegeben werden.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Factoid-Konstanten (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa748c84f8bd39f18f83e1ec72474bcfbe3017f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883673"
---
# <a name="factoid-constants"></a>Factoid-Konstanten

Definiert konstante Zeichenfolgenwerte, die verwendet werden, um die Erkennungsgenauigkeit zu erhöhen, indem kontextbezogene Informationen für die Erkennung angegeben werden.




| Name | Beschreibung | 
|------|-------------|
| <span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl><dt><strong>FACTOID_NONE</strong></dt></dl> | Deaktiviert alle anderen Factoide und Wörterbücher.<br /> | 
| <span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl><dt><strong>FACTOID_DEFAULT</strong></dt></dl> | Die Standardeinstellung für Factoids für westestische Sprachen umfasst das Systemwörterbuch, das Benutzerwörterbuch, verschiedene Interpunktionen sowie das Web- und Zahlenfaktoid. Die Standardeinstellung für Factoids für ostasiatische Sprachen enthält alle Zeichen, die von der -Erkannte unterstützt werden. <br /> | 
| <span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl><dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt></dl> | Gibt an, dass eine Erkennende nur das Systemwörterbuch verwenden soll.<br /> | 
| <span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl><dt><strong>FACTOID_WORDLIST</strong></dt></dl> | Gibt an, dass eine Erkennende eine programmgesteuert definierte Liste von Wörtern verwenden soll. Die Liste der Wörter wird durch die <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList-Eigenschaft</strong></a> eines <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext-Objekts</strong></a> definiert. <br /><blockquote>[!Note]<br />Wenn einer Wortliste eine Zeichenfolge hinzugefügt wird, werden auch die in Groß-//Unter-Zeichenfolgen konvertierten Versionen implizit hinzugefügt. Wenn Sie z. B. "hello" hinzufügen, werden implizit "Hello" und "HELLO" hinzugefügt.</blockquote><br /> | 
| <span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl><dt><strong>FACTOID_EMAIL</strong></dt></dl> | Gibt an, dass eine Erkennende nach einer E-Mail-Adresse sucht.<br /><blockquote>[!Note]<br />Für dieses Faktenoid muss eine vollqualifizierte E-Mail-Adresse wie "" someone@example.com verwendet werden. Ein einsamer Alias, z. B. "jemand", wird nicht erkannt.</blockquote><br /><pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre> | 
| <span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl><dt><strong>FACTOID_WEB</strong></dt></dl> | Gibt an, dass eine Erkennende nach einer Webadresse suchen soll.<br /><pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre> | 
| <span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl><dt><strong>FACTOID_ONECHAR</strong></dt></dl> | Gibt an, dass eine Erkennende nach einem einzelnen Zeichen suchen soll.<br /><blockquote>[!Note]<br />Dieses Factoid sucht nach einem isolierten ANSI-Zeichen.</blockquote><br /> | 
| <span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl><dt><strong>FACTOID_NUMBER</strong></dt></dl> | Gibt an, dass eine Erkennende nach einer Zahl suchen soll.<br /><blockquote>[!Note]<br />Numerische Werte umfassen Trennzeichen, Dezimalstellen, Ordinalzahlen und andere häufig verwendete numerische Symbole.</blockquote><br /> | 
| <span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl><dt><strong>FACTOID_DIGIT</strong></dt></dl> | Gibt an, dass eine Erkennende nach einer einzelnen Ziffer von 0 bis 9 sucht.<br /><pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre> | 
| <span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl><dt><strong>FACTOID_NUMBERSIMPLE</strong></dt></dl> | Stellt einen einfachen numerischen Kontext für eine -Erkennende zur<br /><blockquote>[!Note]<br />Dieses Factoid wird in dieser Version des Tablet PC SDK nicht unterstützt.</blockquote><br /> | 
| <span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl><dt><strong>FACTOID_CURRENCY</strong></dt></dl> | Gibt an, dass eine Erkennende nach Zeichen sucht, die einen Währungswert bezeichnen.<br /><pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre> | 
| <span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl><dt><strong>FACTOID_POSTALCODE</strong></dt></dl> | Gibt an, dass eine Erkennende nach Postleitzahlen sucht.<br /><pre class="syntax" data-space="preserve"><code>98112</code></pre> | 
| <span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl><dt><strong>FACTOID_PERCENT</strong></dt></dl> | Gibt an, dass eine Erkennende nach Prozentsätzen sucht.<br /><pre class="syntax" data-space="preserve"><code>87%</code></pre> | 
| <span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl><dt><strong>FACTOID_DATE</strong></dt></dl> | Gibt an, dass eine Erkennende nach Zeichen sucht, die ein Datum bezeichnen.<br /><pre class="syntax" data-space="preserve"><code>10/30/2001, '01, 31/12, 12/99, 1999-2000</code></pre> | 
| <span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl><dt><strong>FACTOID_TIME</strong></dt></dl> | Gibt an, dass eine Recognizer nach Zeichen sucht, die eine Uhrzeit bezeichnen.<br /><pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre> | 
| <span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl><dt><strong>FACTOID_TELEPHONE</strong></dt></dl> | Gibt an, dass eine Erkennende nach Zeichen sucht, die eine Telefonnummer bezeichnen.<br /><pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre> | 
| <span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl><dt><strong>FACTOID_FILENAME</strong></dt></dl> | Gibt an, dass eine Recognizer nach Zeichen sucht, die einen Dateinamen angeben.<br /><pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre> | 
| <span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl><dt><strong>FACTOID_UPPERCHAR</strong></dt></dl> | Gibt an, dass eine Erkennende nach einem einzelnen Großbuchstaben suchen soll: A bis Z.<br /> | 
| <span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl><dt><strong>FACTOID_LOWERCHAR</strong></dt></dl> | Gibt an, dass eine Erkennende nach einem einzelnen Kleinbuchstaben suchen soll: A bis Z.<br /><blockquote>[!Note]<br />Dieses Factoid wird in dieser Version des Tablet PC SDK nicht unterstützt.</blockquote><br /> | 
| <span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl><dt><strong>FACTOID_PUNCCHAR</strong></dt></dl> | Gibt an, dass eine Erkennende nach Interpunktionszeichen sucht.<br /><blockquote>[!Note]<br />Dieses Factoid wird in dieser Version des Tablet PC SDK nicht unterstützt.</blockquote><br /> | 
| <span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl><dt><strong>FACTOID_JAPANESECOMMON</strong></dt></dl> | Gibt an, dass eine Erkennende nach häufig verwendeten Kanji-, Katakana- und Hiragana-Zeichen sucht.<br /> | 
| <span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt></dl> | Gibt an, dass eine Erkennende nach häufig verwendeten vereinfachten chinesischen Zeichen sucht.<br /> | 
| <span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt></dl> | Gibt an, dass eine Erkennende nach häufig verwendeten traditionellen chinesischen Zeichen sucht.<br /> | 
| <span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl><dt><strong>FACTOID_KOREANCOMMON</strong></dt></dl> | Gibt an, dass eine Erkennende nach häufig verwendeten koreanischen Zeichen sucht.<br /> | 
| <span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl><dt><strong>FACTOID_HIRAGANA</strong></dt></dl> | Gibt an, dass eine Erkennende nur nach Hiragana-Zeichen sucht.<br /> | 
| <span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl><dt><strong>FACTOID_KATAKANA</strong></dt></dl> | Gibt an, dass eine Erkennende nur nach Katakana-Zeichen sucht.<br /> | 
| <span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl><dt><strong>FACTOID_KANJICOMMON</strong></dt></dl> | Gibt an, dass eine Erkennende nach häufig verwendeten Kanjizeichen sucht.<br /> | 
| <span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl><dt><strong>FACTOID_KANJIRARE</strong></dt></dl> | Gibt an, dass eine Erkennende nach selten verwendeten Kanjizeichen sucht.<br /><blockquote>[!Note]<br />Dieses Factoid wird in dieser Version des Tablet PC SDK nicht unterstützt.</blockquote><br /> | 
| <span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl><dt><strong>FACTOID_BOPOMOFO</strong></dt></dl> | Gibt an, dass eine Erkennende nach Bopomofo-Zeichen sucht.<br /> | 
| <span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl><dt><strong>FACTOID_JAMO</strong></dt></dl> | Gibt an, dass eine Erkennende nach Hangul-Kompatibilitäts-Jamo-Zeichen sucht.<br /> | 
| <span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl><dt><strong>FACTOID_HANGULCOMMON</strong></dt></dl> | Gibt an, dass eine Erkennende nach häufig verwendeten Hangulzeichen sucht.<br /> | 
| <span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl><dt><strong>FACTOID_HANGULRARE</strong></dt></dl> | Gibt an, dass eine Erkennende nach selten verwendeten Hangulzeichen sucht.<br /><blockquote>[!Note]<br />Dieses Factoid wird in dieser Version des Tablet PC SDK nicht unterstützt.</blockquote><br /> | 




## <a name="remarks"></a>Hinweise

In C++ können Sie auf diese Konstanten in der Headerdatei "Msinkaut.h" zugreifen, die sich im Verzeichnis systemdrive : Programme Microsoft Tablet PC Platform SDK Include befindet, wenn Sie das SDK am Standardspeicherort installiert &lt; &gt; \\ \\ \\ haben.

> [!Note]  
> Bei diesen Konstanten handelt es sich um WCHARs, nicht um BSTRs. Sie müssen in BSTRs konvertiert werden, bevor sie als Parameter für Objektmethoden verwendet werden. Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).

 

> [!Note]  
> Bei der Suche nach lateinischen Skripts werden die in dieser Klasse definierten Factoids nur aus Gründen der Abwärtskompatibilität bereitgestellt. Bei neuen Entwicklungen wird empfohlen, die in der [SetInputScope-Funktion](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) definierten Werte zu verwenden. Weitere Informationen finden Sie unter [Verwenden von Kontext zur Verbesserung der Genauigkeit.](using-context-to-improve-accuracy.md)

 

Verwenden Sie diese Bezeichner, um anzugeben, welches Factoid während der Erkennung verwendet werden soll.

Die folgenden Kombinationen von Factoiden werden nur für Westsprachen unterstützt. Diese verfügen nicht über separate Definitionen, sind jedoch akzeptable Zeichenfolgenliteraleingaben für die [**Factoid-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) von Objekten, die Factoids verwenden. Mit diesen faktenförmigen Zeichenfolgenkonst constants kann die Eingabe mit einem der Factoids im Ausdruck übereinstimmen.



| Kombination               | Definition                                                |
|---------------------------|-----------------------------------------------------------|
| "WEB \| WORDLIST"           | Das Webf factoid oder die Wortliste.                         |
| "EMAIL \| WORDLIST"         | Das E-Mail-Factoid oder die Wortliste.                       |
| "FILENAME \| WEB \| WORDLIST" | Das Filename-Factoid, das Web-Factoid oder die Wortliste. |



 

Wenn Sie das [InkEdit-Steuerelement](inkedit-control-reference.md) verwenden, kann das Factoid als Eigenschaft des Steuerelements festgelegt werden.

Wenn Sie die Tablet PC Platform-APIs verwenden, können Sie die [**Factoid-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) für ein [**InkRecognizerContext-Objekt**](inkrecognizercontext-class.md) festlegen.

Alternativ können Sie diese Eigenschaft mit der tatsächlichen Factoidzeichenfolgenkonstante festlegen.

> [!Note]  
> Bei Factoid-Zeichenfolgenkonstanten wird die Groß-/Kleinschreibung beachtet. Weitere Informationen zu Factoiden und deren Verwendung finden Sie unter Verwenden von Kontext zur [Verbesserung der Genauigkeit.](using-context-to-improve-accuracy.md) Informationen dazu, ob ein Factoid in einer bestimmten Sprache verfügbar ist, finden Sie unter [Unterstützte Factoids aus Version 1.](supported-factoids-from-version-1.md)

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Factoid Property \[ InkRecognizeContext-Klasse\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)
</dt> <dt>

[**Factoid Property \[ PenInputPanel-Klasse\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)
</dt> <dt>

[**Factoid Property \[ InkEdit-Steuerelement\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)
</dt> <dt>

[Verwenden von Kontext zur Verbesserung der Genauigkeit](using-context-to-improve-accuracy.md)
</dt> <dt>

[Unterstützte Factoids aus Version 1](supported-factoids-from-version-1.md)
</dt> </dl>

 

