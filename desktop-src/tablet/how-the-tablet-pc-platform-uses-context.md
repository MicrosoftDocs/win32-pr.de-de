---
description: Entwickler, die Anwendungen für den Tablet PC erstellen, können den Eingabebereich und Kontextinformationen nutzen.
ms.assetid: 74e4e4b2-6ceb-4044-84df-2fff0788267a
title: Verwendung des Kontexts durch die Tablet PC-Plattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd991a2ad8e76bb0a96ea5e41977b158cc30f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347783"
---
# <a name="how-the-tablet-pc-platform-uses-context"></a>Verwendung des Kontexts durch die Tablet PC-Plattform

Entwickler, die Anwendungen für den Tablet PC erstellen, können den Eingabebereich und Kontextinformationen nutzen. Die bestmöglichen Lösungen zum Festlegen von Kontextinformationen für Steuerelemente in Anwendungen hängen davon ab, ob für das Steuerelement frei Hand Eingaben aktiviert sind und ob die Anwendung auf dem Markt freigegeben wurde. Ein frei Hand fähiges Steuerelement ist ein Element, das speziell für die Eingabe von Hand Eingaben entwickelt wurde und in dem die frei Hand Daten primär gesammelt und als freigegeben werden. Beispiele für frei Hand fähige Anwendungen sind Microsoft Windows Journal oder ein verzerringprogramm. In einem Steuerelement, bei dem keine frei Hand Eingabe aktiviert ist, werden Eingabedaten gesammelt und als Text gespeichert. Dies geschieht in der Regel über den Tablet PC-Eingabebereich, wenn die Anwendung auf einem Tablet PC ausgeführt wird. Die Lösungen zum Aktivieren von Kontextinformationen in Steuerelementen sind:

-   Die [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) -APIs: eine programmgesteuerte Lösung auf niedriger Ebene für nicht frei Hand fähige Anwendungen und Steuerelemente. Die Binärdateien für die Anwendung sind betroffen und müssen neu verteilt werden.
-   Die Eigenschaften " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " und " [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) " des [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts: eine programmgesteuerte Lösung für Anwendungen mit aktivierten Steuerelementen. Die Binärdateien für die Anwendung sind betroffen und müssen neu verteilt werden.

Der Tablet PC-Eingabebereich wurde ab Windows Vista aktualisiert, um die von Ihnen bereitgestellten Kontextinformationen zu nutzen, die Sie bei der Verwendung der-APIs für das- [ctinputscope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) angeben. In der folgenden Tabelle finden Sie Details dazu, welche Eingabe Bereiche von Microsoft-Erkennungs-Engines unterstützt werden. Ein "X" in der Zeile für einen Eingabebereich gibt an, dass die Erkennung in dieser Spalte den Eingabebereich unterstützt.



| Eigenschaftsname                                     | Englisch (USA) | Walisisch (Großbritannien) | Deutsch       | Französisch       | Japanisch     | Koreanisch       | Chinesisch (vereinfacht) | Chinesisch (traditionell) |
|---------------------------------------------------|-------------------------|--------------------------|--------------|--------------|--------------|--------------|----------------------|-----------------------|
| **ist \_ Address \_ fullpostaladdress**<br/>     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Address \_ PostalCode**<br/>            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Adress \_ Straße**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Adress \_ StateOrProvince**<br/>       | X<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Adress \_ Stadt**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Address \_ CountryName**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Address \_ countryshortname**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist Currency-Wert- \_ \_ Symbol**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Währungs \_ Betrag**<br/>               | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Date \_ fulldate**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist der \_ Datums \_ Monat**<br/>                    | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Date \_ Day**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Datum- \_ Jahr**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Date \_ MonthName**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Date \_ Day Name**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Standard**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_e-Mail- \_ username**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ e-Mail \_ smtpeer Mail Address**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Datei \_ fullfilepath**<br/>             | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ \_ Dateiname**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ LoginName**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Ziffern**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Zahl**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ OneChar**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Kennwort**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Personal Name \_ FullName**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist ein \_ Personal Name- \_ Präfix**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Personal Name \_ givenName**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Personal Name \_ MiddleName**<br/>       | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Personal Name \_ Nachname**<br/>          | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist " \_ Personal Name"- \_ Suffix**<br/>           | X<br/>            | -<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ \_ telefonfulltelefonienumber**<br/> | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_Telefon \_ CountryCode**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist " \_ Telefon \_ areaCode"**<br/>            | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Telefon \_ localnumber**<br/>         | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Zeit \_ voll Zeit**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Zeit \_ Stunde**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Zeit- \_ minorsec**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ URL**<br/>                            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist die \_ Zahl \_ Fullwidth**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ alphanumerisch \_ Halfwidth**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ alphanumerisch \_ Fullwidth**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Currency \_ Chinese**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Bopomofo**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Hiragana**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Katakana \_ Halfwidth**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Katakana \_ Fullwidth**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ist \_ Hanja**<br/>                          | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |



 

Bei der Verwendung der [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) -APIs oder der Eigenschaft " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " des [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts zum Festlegen des Kontexts wird beim Versuch, einen Eingabebereich für eine Sprache festzulegen, die nicht von der Erkennung dieser Sprache unterstützt wird, das Standard Sprachmodell als Kontext für das Steuerelement verwendet. Beispielsweise wird der Adressbereich von " **\_ Address \_ StateOrProvince** " nicht von der französischen Erkennung unterstützt. Wenn Sie Kontext für ein Feld als

`(!IS_ADDRESS_STATEORPROVINCE)|(!IS_ADDRESS_POSTALCODE)`

Wenn Sie die französische Erkennung verwenden, ist der resultierende Kontext das Standard Sprachmodell. Um dieses Problem zu vermeiden, sollten Sie die Sprache der verwendeten Erkennung erkennen und Eingabe Bereiche entsprechend festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[InputScope-Enumeration](/windows/win32/api/inputscope/ne-inputscope-inputscope)
</dt> </dl>

 

