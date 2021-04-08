---
description: In diesem Thema wird beschrieben, wie Windows Search mehrere Sprachen unterstützt.
ms.assetid: a800d2ac-3aee-4e74-a29a-a70355138ebc
title: Von Windows Search unterstützte Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350a8861a5817a8ac5710214ccd35c780f2c9dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750433"
---
# <a name="languages-supported-by-windows-search"></a>Von Windows Search unterstützte Sprachen

In diesem Thema wird beschrieben, wie Windows Search mehrere Sprachen unterstützt.

## <a name="tokenization-wordbreakers-and-language-resources"></a>Tokenisierung, wordtrennungen und Sprachressourcen

Windows Search ist sprachunabhängig, aber die Genauigkeit der Suche über Sprachen hinweg kann aufgrund der Art und Weise, wie Wörter Trennungen den Text mit Token versehen, variieren. Wordtrennungen implementieren verschiedene tokenisierungsregeln für Sprachen und unterbrechen Text in einzelne Token oder Wörter, die indiziert oder durchsucht werden sollen.

Sowohl die Sprache des indizierten Texts als auch die Abfrage Zeichenfolge werden in Token unterteilt. Da tokenisierungsregeln je nach Sprache unterschiedlich sind, gibt es für jede Sprache oder Sprachen Familie separate Wörter Trennungen. Wenn die Abfragesprache und die indizierte Sprache nicht übereinstimmen, kann dies zu unvorhersehbaren Ergebnissen führen.

Windows Search ist mit einem klar definierten Satz von wordtrennungen ausgeliefert. Klassische Wörter Trennung-und Wort Stamm Erkennung-Komponenten werden in Windows Vista und höher unterstützt. Wenn die Sprache eines Dokuments nicht bestimmt werden kann, versucht Windows Search, die Sprache zu erkennen, um die geeignetste Wörter Trennung zu ermitteln. Windows Search versucht, die Sprache zu erkennen, indem die [**GetSystemPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getsystempreferreduilanguages) -Funktion aufgerufen wird, um die erste MUI-Sprache (Multiple User Interface) zu ermitteln (in der Regel die Benutzeroberflächen Sprache des Systems, es sei denn, MUI Language Packs sind installiert). Wenn der Befehl erfolgreich ausgeführt wird, wird die Wörter Trennung für die erste MUI-Sprache verwendet. Wenn der Aufruf von **GetSystemPreferredUILanguages** fehlschlägt, ruft Windows Search das System Gebiets Schema durch Aufrufen der [**GetSystemDefaultLCID**](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlcid) -Funktion ab und verwendet die Wörter Trennung, die diesem Gebiets Schema zugeordnet ist.

Wenn für eine Sprache keine Wörter Trennung installiert ist, wird die Windows-Suche in Leerraum mithilfe des **neutralen** Wörter Trennung unterbrochen.

Sie können eine Sprache durch die Registrierung entfernen, wie im folgenden Beispiel veranschaulicht.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            ContentIndex
               Language
                  Dutch_Dutch
                     (Default)
                     Locale
                     NoiseFile
                     StemmerClass = CLSID
                     WBreakerClass = CLSID
```

> [!TIP]
> Wenn Sie Änderungen an der Registrierung vornehmen, starten Sie Windows Search neu.

 

Wenn für Windows Search eine neue Wörter Trennung-Klausel erforderlich ist, wird der Klassen Bezeichner (CLSID) gelesen, und die instanziierte Wörter Trennung wird zwischengespeichert.

Sie können eine benutzerdefinierte Wörter Trennung für eine Sprache erstellen, indem Sie die [**iwordbreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) -Schnittstelle implementieren. Windows Search ruft dann die **iwordbreaker** -Methoden auf, wenn Inhalts Indizes erstellt und Abfragen ausgeführt werden.

Gebiets Schema Informationen für indizierten Inhalt werden aus der Quelle des Inhalts abgerufen. Wenn der quellimplementierer das Gebiets Schema des indizierten Inhalts nicht kennt, sollte das Gebiets Schema auf Gebiets Schema [**\_ neutral**](../intl/locale-neutral.md)festgelegt werden.

Wenn Sie z. b. einen Filter Handler (eine Implementierung der [**IFilter**](https://www.bing.com/search?q=**IFilter**) -Schnittstelle), einen Eigenschafts Handler oder einen Protokollhandler implementieren, sollten Sie das Gebiets Schema für indizierten Inhalt auf Gebiets Schema [**\_ neutral**](../intl/locale-neutral.md) festlegen, es sei denn, Sie haben bestimmte Gebiets Schema Informationen und sind sicher von seiner Genauigkeit.

> [!TIP]
> Wenn eine Index Abfrage auf Benutzereingaben basiert, sollte das Gebiets Schema der Sprache entsprechen, in der der Benutzer die Eingabe durchläuft. Sie können dieses Gebiets Schema ermitteln, indem Sie die [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) -Funktion aufrufen.

 

## <a name="languages-supported-by-wordbreakers"></a>Von wordtrennungen unterstützte Sprachen

Windows Search umfasst wordtrennungen zur Unterstützung der folgenden Sprachen.



| Registrierungsschlüssel             | Sprache (unter Sprache)                            | LCID   |
|--------------------------|---------------------------------------------------|--------|
| **Arabisch ( \_ Saudiarabien)**  | Arabisch (neutral)                                  | 0x0001 |
| **Bengalischer \_ Standardwert**     | Bangla (neutral)                                  | 0x0045 |
| **Bulgarischer \_ Standard**   | Bulgarisch (Bulgarien)                              | 0x0402 |
| **Katalanisch \_ Standard**     | Katalanisch (Katalanisch)                                 | 0x0403 |
| **Chinesisch ( \_ Hongkong)**    | Chinesisch (Hongkong SAR, VR China)                      | 0x0c04 |
| **Chinesisch ( \_ vereinfacht)**  | Chinesisch (vereinfacht)                              | 0x0804 |
| **Chinesisch ( \_ traditionell)** | Chinesisch (traditionell)                             | 0x0404 |
| **Kroatisch \_ Standard**    | Kroatisch (Kroatien)                                | 0x041a |
| **Tschechische \_ Standardeinstellung**       | Tschechisch (Tschechische Republik)                            | 0x0405 |
| **Dänisch ( \_ Standard)**      | Dänisch (Dänemark)                                  | 0x0406 |
| **Niederländisch \_ Niederländisch**         | Niederländisch (Niederlande)                               | 0x0413 |
| **English \_ UK**          | Walisisch (Großbritannien)                          | 0x0809 |
| **Englisch ( \_ USA)**          | Englisch (USA)                           | 0x0409 |
| **Finnischer \_ Standard**     | Finnisch (Finnland)                                 | 0x040b |
| **Französisch \_ Französisch**       | Französisch (Frankreich)                                   | 0x040c |
| **Deutsch \_ Deutsch**       | Deutsch (Deutschland)                                  | 0x0407 |
| **Griechisch ( \_ Standard)**       | Griechisch (Griechenland)                                    | 0x0408 |
| **Standardwert von Gujarati \_**    | Gujarati (Indien)                                  | 0x0447 |
| **Hebräisch ( \_ Standard)**      | Hebräisch (neutral)                                  | 0x000D |
| **Hindi- \_ Standard**       | Hindi (Indien)                                     | 0x0439 |
| **Ungarischer \_ Standard**   | Ungarisch (Ungarn)                               | 0x040e |
| **Isländisch \_ Standard**   | Isländisch (Island)                               | 0x040f |
| **Indonesischer \_ Standardwert**  | Indonesisch (Indonesien)                            | 0x0421 |
| **Italienisch \_ Italienisch**     | Italienisch (Italien)                                   | 0x0410 |
| **Japanischer \_ Standard**    | Japanisch (Japan)                                  | 0x0411 |
| **Kannada- \_ Standard**     | Kannada (Indien)                                   | 0x044B |
| **Koreanisch \_ Standard**      | Koreanisch (Korea)                                    | 0x0412 |
| **Lettischer \_ Standardwert**     | Lettisch (Lettland)                                  | 0x0426 |
| **Litauischer \_ Standardwert**  | Litauisch (Litauisch)                           | 0x0427 |
| **Malaiisch, \_ Malaysia**      | Malaiisch (Malaysia)                                  | 0x043e |
| **Malayalam ( \_ Standard)**   | Malayalam (neutral)                               | 0x004c |
| **Marathi- \_ Standard**     | Marathi (Indien)                                   | 0x044e |
| **Norwegisch \_ Bokmal**    | Norwegisch, Bokmål (Norwegen)                        | 0x0414 |
| **Polnisch ( \_ Standard)**      | Polnisch (Polen)                                   | 0x0415 |
| **Portugiesisch ( \_ Portugal)** | Portugiesisch (Portugal)                             | 0x0816 |
| **Portugiesisch ( \_ Brasilien)**   | Portugiesisch (Brasilien)                               | 0x0416 |
| **Punjabi- \_ Standard**     | Punjabi (Indien)                                   | 0x0446 |
| **Rumänischer \_ Standard**    | Rumänisch (Rumänien)                                | 0x0418 |
| **Russischer \_ Standard**     | Russisch (neutral)                                 | 0x0019 |
| **Serbisch \_ Kyrillisch**    | Serbisch (Serbien und Montenegro, ehemals, Kyrillisch) | 0x0c1a |
| **Serbisch \_ lateinisch**       | Serbisch (Serbien und Montenegro, ehemals, lateinisch)    | 0x081a |
| **Slowakisch \_ Standard**      | Slowakisch (Slowakei)                                 | 0x041b |
| **Slowenisch \_ Standard**   | Slowenisch (Slowenien)                              | 0x0424 |
| **Spanisch \_ modern**      | Spanisch (Spanien, modern Sort)                      | 0x0C0A |
| **Schwedischer \_ Standard**     | Schwedisch (Schweden)                                  | 0x041d |
| **Tamil- \_ Standard**       | Tamil (Indien)                                     | 0x0449 |
| **Telugu- \_ Standard**      | Telugu (Indien)                                    | 0x044a |
| **Thailändischer \_ Standard**        | Thai (Thailand)                                   | 0x041E |
| **Türkisch ( \_ Standard)**     | Türkisch (Türkei)                                  | 0x041f |
| **Ukrainischer \_ Standard**   | Ukrainisch (Ukraine)                               | 0x0422 |
| **Urdu- \_ Standard**        | Urdu (Pakistan)                                   | 0x0420 |
| **Vietnamesisch \_ Standard**  | Vietnamesisch (Vietnam)                              | 0x042a |



 

> [!Note]  
> LCIDs für einige Sprachen in der Tabelle werden mithilfe der Sprachen-ID, der unter Sprachen-ID und des Sortier Bezeichners generiert.

 

Weitere Informationen zu Sprachen und zugeordneten Bezeichnern finden Sie unter [sprach Bezeichner-Konstanten und-](../intl/language-identifier-constants-and-strings.md)Zeichen folgen.

> [!Note]  
> Es gibt keine Garantie dafür, dass alle diese sprach Registrierungsschlüssel auf einem beliebigen Computer vorhanden sind. Die Wörter Trennung für eine bestimmte Sprache kann abhängig von den Benutzereinstellungen auf dem Computer installiert werden.

 

**Ab Windows 8.1** ist die bevorzugte Methode für die Verwendung von wordtrennungen die WinRT-API [**wordssegmenter-Klasse**](/uwp/api/Windows.Data.Text.WordsSegmenter?view=winrt-19041).

## <a name="additional-resources"></a>Weitere Ressourcen

-   Informationen zum Implementieren und Verwenden von benutzerdefinierten Wörter Trennungen und Wort Stamm Erkennungen für weitere Sprachen und Gebiets Schemas finden Sie unter [Erweitern von Sprachressourcen in Windows Search](extending-language-resources-in-windows-search.md).
-   Wenn Sie die Sprache eines Texts identifizieren müssen, können Sie die automatische Erkennung von Sprachen (LAD) verwenden, die in Windows 7 und höher verfügbar ist. Weitere Informationen finden Sie unter [Erweiterte linguistische Dienste](../intl/extended-linguistic-services.md) (STS).
-   Informationen zum Verwalten, Abfragen und Erweitern des Indexes finden Sie im [Entwicklerhandbuch für Windows-Suche](-search-developers-guide-entry-page.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Search als Entwicklungsplattform](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Verwenden von verwaltetem Code mit Shelldaten und Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
