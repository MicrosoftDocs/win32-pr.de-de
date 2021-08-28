---
description: Entwickler, die Anwendungen für den Tablet-PC erstellen, können eingabeumfangs- und kontextinformationen nutzen.
ms.assetid: 74e4e4b2-6ceb-4044-84df-2fff0788267a
title: Verwendung des Kontexts durch die Tablet PC-Plattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c586bf3ffcff8fc92b02bc0b4f5aff79c6bd0bbd66e6f048eab35a78d3be9676
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709280"
---
# <a name="how-the-tablet-pc-platform-uses-context"></a>Verwendung des Kontexts durch die Tablet PC-Plattform

Entwickler, die Anwendungen für den Tablet-PC erstellen, können eingabeumfangs- und kontextinformationen nutzen. Die bestmöglichen Lösungen zum Festlegen von Kontextinformationen für Steuerelemente in Anwendungen hängen davon ab, ob das Steuerelement freigeschaltet ist und ob die Anwendung auf den Markt gebracht wurde. Ein Steuerelement mit aktivierter Ink-Funktion ist ein Steuerelement, das speziell für die Eingabe von Ink entwickelt wurde und bei dem die Ink-Daten in erster Linie gesammelt und als Ink gespeichert werden. Beispiele für Ink-fähige Anwendungen sind Microsoft Windows Journal oder ein Sketching-Programm. In einem Steuerelement, für das keine Ink-Funktion aktiviert ist, werden Eingabedaten gesammelt und als Text beibehalten, in der Regel über den Tablet PC-Eingabebereich, wenn die Anwendung auf einem Tablet PC ausgeführt wird. Die Lösungen zum Aktivieren von Kontextinformationen in Steuerelementen sind:

-   Die [SetInputScope-APIs:](/windows/win32/api/inputscope/nf-inputscope-setinputscope) Eine programmgesteuerte Lösung auf niedriger Ebene für Nicht-Ink-fähige Anwendungen und Steuerelemente. Die Binärdateien für die Anwendung sind von der Verteilung der Binärdateien und müssen weiterverteilt werden.
-   Eigenschaften [**"Factoid"**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) und [**"WordList"**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) des [**RecognizerContext-Objekts:**](inkrecognizercontext-class.md) Eine programmgesteuerte Lösung für Anwendungen mit aktivierten Steuerelementen. Die Binärdateien für die Anwendung sind von der Verteilung der Binärdateien und müssen weiterverteilt werden.

Der Tablet PC-Eingabebereich wurde ab Windows Vista aktualisiert, um die Kontextinformationen zu nutzen, die Sie bei verwendung der [SetInputScope-APIs](/windows/win32/api/inputscope/nf-inputscope-setinputscope) bereitstellen. Die folgende Tabelle enthält Details dazu, welche Microsoft-Erkennungs-Engines welche Eingabebereich unterstützen. Ein "X" in der Zeile für einen Eingabebereich gibt an, dass die Erkannte in dieser Spalte den Eingabebereich unterstützt.



| Eigenschaftsname                                     | Englisch (USA) | Walisisch (Großbritannien) | Deutsch       | Französisch       | Japanisch     | Koreanisch       | Chinesisch (vereinfacht) | Chinesisch (traditionell) |
|---------------------------------------------------|-------------------------|--------------------------|--------------|--------------|--------------|--------------|----------------------|-----------------------|
| **IS \_ ADDRESS \_ FULLPOSTALADDRESS**<br/>     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ POSTALCODE**<br/>            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ STREET**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ STATEORPROVINCE**<br/>       | X<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ CITY**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ COUNTRYNAME**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ COUNTRYSHORTNAME**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ CURRENCY \_ AMOUNTANDSYMBOL**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ CURRENCY \_ AMOUNT**<br/>               | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IST \_ DATE \_ FULLDATE**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ MONTH**<br/>                    | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ DAY**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ YEAR**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ MONTHNAME**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ DAYNAME**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DEFAULT**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IST \_ \_ E-MAIL-BENUTZERNAME**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ EMAIL \_ SMTPEMAILADDRESS**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ FILE \_ FULLFILEPATH**<br/>             | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ FILE \_ FILENAME**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ LOGINNAME**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DIGITS**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ NUMBER**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ONECHAR**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ PASSWORD**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IST \_ PERSONALNAME \_ FULLNAME**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IST \_ PERSONALNAME \_ PREFIX**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IST \_ PERSONALNAME \_ GIVENNAME**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IST \_ PERSONALNAME \_ MIDDLENAME**<br/>       | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ PERSONALNAME \_ SURNAME**<br/>          | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ PERSONALNAME \_ SUFFIX**<br/>           | X<br/>            | -<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IST \_ TELEFON \_ FULLTELEPHONENUMBER**<br/> | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TELEPHONE \_ COUNTRYCODE**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TELEPHONE \_ AREACODE**<br/>            | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TELEPHONE \_ LOCALNUMBER**<br/>         | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TIME \_ FULLTIME**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TIME \_ HOUR**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TIME \_ MINORSEC**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_IS-URL**<br/>                            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ NUMBER \_ FULLWIDTH**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IST \_ ALPHANUMERIC \_ HALFWIDTH**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IST \_ ALPHANUMERISCH \_ FULLWIDTH**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ CURRENCY \_ CHINESE**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IST \_ BOPOMOFO**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ HIRAGANA**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ KATAKANA \_ HALFWIDTH**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ KATAKANA \_ FULLWIDTH**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ HANJA**<br/>                          | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |



 

Wenn Sie die [SetInputScope-APIs](/windows/win32/api/inputscope/nf-inputscope-setinputscope) oder die [**Factoid-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) des [**RecognizerContext-Objekts**](inkrecognizercontext-class.md) zum Festlegen des Kontexts verwenden, führt der Versuch, einen Eingabebereich für eine Sprache festzulegen, die von der Erkennung dieser Sprache nicht unterstützt wird, dazu, dass der Tablet PC-Eingabebereich das Standardsprachmodell als Kontext für das Steuerelement verwendet. Beispielsweise wird der **Eingabebereich IS \_ ADDRESS \_ STATEORPROVINCE** von der französischen Erkennung nicht unterstützt. Wenn Sie den Kontext für ein Feld als festlegen

`(!IS_ADDRESS_STATEORPROVINCE)|(!IS_ADDRESS_POSTALCODE)`

Bei Verwendung der französischen Erkennung ist der resultierende Kontext das Standardsprachmodell. Um dieses Problem zu vermeiden, erkennen Sie die Sprache der verwendeten Erkennung und legen die Eingabebereiche entsprechend fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[InputScope-Enumeration](/windows/win32/api/inputscope/ne-inputscope-inputscope)
</dt> </dl>

 

